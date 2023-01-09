+++
title = "Creating an EC2 Instance with a tag"
date = 2021
weight = 1
chapter = false
pre = "<b>1.1.1 </b>"
+++


#### Create EC2 Instance with tag

{{%notice note%}}
In this workshop, we will use the Singapore region (ap-southeast-1). If you want to use another Region, be sure to move the Region back to the Region you want to use when creating workshop-related resources.
{{%/notice%}}

![region](/images/tag/1region.png?width=90pc)

1. Visit [**EC2 Management Console**](https://ap-southeast-1.console.aws.amazon.com/ec2/v2/) and click **Launch Instances**.

![Tag](/images/tag/1ec2.png?width=90pc)

2. On the display **Launch Instances**.
  +	Click **Add additional tags**

![Tag](/images/tag/2ec2.png?width=90pc)

3. On the display **Add tags** according to the instruction picture.
  + Click **Add tags**.

| Key           | Value       |
| ------------- | ----------- |
| Owner         | Yourname    |
| Service`      | Yourservice |
| Environment   | UAT         |

![Tag](/images/tag/3ec2.png?width=90pc)

{{%notice tip%}}
You can download the best-practices guide to implementing an effective AWS resource tagging strategy below.
{{%/notice%}}

{{%attachments style="orange" title="AWS Tagging Best practices" pattern=".*(pdf)" /%}}

4. With **Amazon Machine Image**.
  + You keep the default configuration.

![Tag](/images/tag/4ec2.png?width=90pc)

5. For key pair, select **Create new key pair** .
  + **Key pair name** as **TestTagging**.
  + Select **Create new key pair**
  
![Tag](/images/tag/5ec2.png?width=90pc)


6. **Key pair name** as TestTagging. Then select **Create key pair**.

![Tag](/images/tag/6ec2.png?width=90pc)

7. For the **Networking** section, keep the default and click click as shown.

![Tag](/images/tag/7ec2.png?width=90pc)

8. Check the configuration again and select **Launch instance**.
  + Click **Launch instance**.
  
  ![Tag](/images/tag/8ec2.png?width=90pc)

9. Complete **Launch instance**

   ![Tag](/images/tag/9ec2.png?width=90pc)

10. Return to the **EC2** interface. Select **Instance** to select the instance you just created.
   + Click the **Tags** tab to check the created tags.

   ![Tag](/images/tag/10ec2a.png?width=90pc)

11. Repeat steps 1 - 10 to create more EC2 Instance with Tag as follows:

| Key | Value |
| ------ | ----------- |
| Owner   | Yourname |
| Service   | Yourservice |
| Environment   | Test |

{{%notice tip%}}
We can avoid creating a new key-pair by reusing the key-pair that we just created to initialize the second EC2 instance.\
After clicking **Launch** on the **Review Instance Launch** page:\
\
Select **Choose an existing key pair**. \
Select key pair **Testtagging**. \
Click select **I knowledge that I have access to the corresponding private key file, and that without this file, I won't be able to log into my instance.**\
Click **Launch**. \
Click **View Instance**. \

{{%/notice%}}

![Tag](/images/tag/009.png?width=90pc)

Next, we will modify these tags.

