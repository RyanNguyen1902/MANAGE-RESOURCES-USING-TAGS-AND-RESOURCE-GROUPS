+++
title = "Adding or deleting tags"
date = 2020
weight = 2
chapter = false
pre = "<b>1.1.2 </b>"
+++


**Content:**
- [Add or delete tags on a single resource](#add-or-delete-tags-on-a-single-resource)
- [Add or delete tags on groups of resources](#add-or-delete-tags-on-groups-of-resources)

#### Add or delete tags on a single resource

**Adding tags on a single EC2 instance:**
1. Navigate to the resource we want to tag, in this case we will access our **[Amazon EC2 Console](https://console.aws.amazon.com/ec2/)**.
2. In the navigation bar at the top of the screen, ensure that the correct **Region** is selected (In this lab, we are using the Singapore region)
3. Click on the resource to tag from the list of resources, select the **Tags** tab, and then select **Manage tags**

![Tag](/images/tag/11ec2.png?width=90pc)

4. Next, click on **Add tag**. Enter *Key* and *Value* information for the tag as shown below and click **Save**.

![Tag](/images/tag/12ec2.png?width=90pc)

We have just added a new tag to identify the operating system for EC2 Instance.
#### Add or delete tags on groups of resources

**Adding tags on multiple EC2 instances:**
1. Access the **[Amazon EC2 Console](https://console.aws.amazon.com/ec2/)**.
2. In the left pane, select **Tags**
3. Select **Manage Tags**

![Tag](/images/tag/13ec2.png?width=90pc)

4. On the **Manage Tags** page, select the type of resource to filter at **Filter** (for example, **Instances**)
5. To add tags on the resource group:
   - Select the resources you want to tag
   - From the **Add Tag** section, fill in *Key* and *Value* of your desired tag and click **Add Tag**

![Tag](/images/tag/14ec2.png?width=90pc)

6. To delete the tag on the resource group:
   - Select the resources which you want to remove a given tag
   - At **Remove Tag**, fill in *Key* and select **Remove Tag**.



