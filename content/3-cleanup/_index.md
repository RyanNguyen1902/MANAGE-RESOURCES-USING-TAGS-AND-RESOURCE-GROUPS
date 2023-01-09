+++
title = "Resource Cleanup"
date = 2021-07-09T14:40:59+07:00
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

You may clean up the resources provisioned during this lab in the following order:
1. Delete EC2 Instance
   - Access the [EC2 Management Console](console.aws.amazon.com/ec2)
   - On the left pane, select **Intances**.
   - Select all EC2 Instances related to the lab (**you can use the card to filter the instances to be deleted or refer to the created Resource Group)
   - Click **Actions**.
   - Click **Manage Instance State**.
   - Click on **Terminate**.
   - Click **Change State**, then click **Terminate**.

![Tag](/images/remove/1de.png?width=90pc)

![Tag](/images/remove/2de.png?width=90pc)

2. Delete Resource Group
   - Access the [AWS Resource Group Console](console.aws.amazon.com/resource-groups/).
   - Click **Saved Resource Group** in the left bar.
   - Click on the Resource Group name related to the lab (**MarketingBu**).
   - Click **Delete**, then click **Delete** again to confirm deletion of Resource Group.

![Tag](/images/remove/2dl.png?width=90pc)
