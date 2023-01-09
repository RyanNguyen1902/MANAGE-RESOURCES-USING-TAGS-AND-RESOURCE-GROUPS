+++
title = "Creating a Resource Group"
date = 2021-07-09T14:42:20+07:00
weight = 2
chapter = false
pre = "<b>2. </b>"
+++


#### Create a Resource Group 
In this step, we will create a Resource Group categorized by tag.
1. Go to the [AWS Resource Groups Console](https://console.aws.amazon.com/resource-groups)
2. In the left pane, click on **Create Resource Group**
3. From the **Create query-based group** page, under **Group type**, select **Tag-based**. 
4. Under **Grouping criteria**, select **Resource types** (*resource type*) is **AWS።EC2።Instance**.

![Tag](/images/2/1gr.png?width=90pc)  

5. Under **Tags**, type tag **"key=BusinessUnit, Value=Marketing"** and then press **Add** to add the tag.
6. Click **Preview group resources** to show **Group Resources** resources with the resource type and tag mentioned above.


![Tag](/images/2/2gr.png?width=90pc)  


7. In the **Group details** section, enter the following parameters:
   - Group name: **MarketingBu**
   - Group description - optional: enter a description for Resource Group (eg: **Servers of Marketing BU**)
   - Verify the above and click **Create group**.

![Tag](/images/2/3gr.png?width=90pc)  

{{%notice tip%}}

We can skip **Group tags - optional**. \
However, if you want the Resource Group being created to be a part of a larger Resource Group, you can add a tag to the Resource Group. (Example: **"Key=Organization, value=AWS"**)
{{%/notice%}}


8. After the Resource Group has been successfully created, click **Saved Resource Groups** in the left pane to see the Resource Group we have just created.

![Tag](/images/2/5gr.png?width=90pc)  

![Tag](/images/2/6gr.png?width=90pc)  

9. Click on Resource Group **MarketingBu**.

10. Scroll down the **Group resources** section, you'll see all the resources that belong to this Resource Group.

![Tag](/images/2/7gr.png?width=90pc)  



