+++
title = "Using tags via AWS CLI"
date = 2020
weight = 2
chapter = false
pre = "<b>1.2. </b>"
+++
#### Overview

In this step, you'll familiarize yourself with performing tagging operations from the AWS CLI.

{{% notice note%}}
To do this step, you need to have **AWS CLI** installed on your machine. Please refer to this [link](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html) for installation instructions.
{{% /notice%}}


**Content:**
- [Overview](#overview)
- [Adding tags to an existing EC2 resource](#adding-tags-to-an-existing-ec2-resource)
- [Adding a tag to a new resource](#adding-a-tag-to-a-new-resource)
- [Description of tagged resources](#description-of-tagged-resources)

#### Adding tags to an existing EC2 resource
From the CLI, invoke  `ec2 create-tags` with flags `—resources` and `—tags` 

```bash
aws ec2 create-tags —resources <ResourceID> —tags Key=<Key>, value=<Value>
```

For example, if you wanted to create a tag of **"Key=Environment, Value=Test"** for an EC2 instance resource, your parameters will be:
```bash
aws ec2 create-tags —resources i-01234example56789 —tags Key=Environment, Value=Test
```

![1.2_Describe](../../../images/tag2/1cli.png?width=90pc)

#### Adding a tag to a new resource

**Add tag to new virtual machines**

From the CLI, invoke `ec2 run-instances` to create a new virtual machine and use the flag `—tag-specifications` to declare tag information:

```bash
aws ec2 run-instances\
—image-id <image-id> \
—count 1\
—instance-type t2.micro\
—key-name <YourKeyPair> \
—subnet-id <YouSubnetID> \
—tag-specifications resourceType=Instance, Tags= [{Key=Environment, Value=Test}] resourceType=Volume, Tags= [{Key=Environment, Value=Test}] 
#Volume created with the instance will also have the tag "Key=Environment, Value=Test"
```

**Note:** You will have to replace the appropriate parameters for your account.\
The image below illustrates sample output:

![1.2_Describe](../../../images/tag2/2cli.png?width=90pc)

**Add tag to new drive**

From the CLI, invoke `ec2 create-volume` to create a new volume and use the flag `—tag-specifications` to declare the following tag information:

```bash
aws ec2 create-volume\
—availability-zone ap-southeast-1a\
—volume-type gp2\
—size 80\
—tag-specifications resourceType=Volume, Tags= [{Key=Environment, Value=Test}, {key=Cost-Center, value=CC123}]
#Volume will be assigned 2 tags as "Key=Environment, Value=Test" and "Key=Cost-Center, Value=CC123"
```
**Note:** You will have to replace the appropriate parameters for your account.\
The picture below illustrates sample output:

![1.2_Describe](../../../images/tag2/3cli.png?width=90pc)

#### Description of tagged resources
From the CLI, invoke `ec2 derscibe-instances` with the flag  `—filters`:

```bash
aws ec2 descripbe-instances —filters name=tag-key, Values=<SampleTagKey>
```
The picture below illustrates sample output:

![1.2_Describe](../../../images/tag2/4cli.png?width=90pc)

