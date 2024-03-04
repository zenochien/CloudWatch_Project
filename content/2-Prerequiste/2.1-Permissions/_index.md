---
title : "Create role"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---
## Create role

1. Access the **AWS Management Console** interface:
   - Locate and click on **IAM**
   - Choose **IAM**

![Create role](/images/1/0001.png?featherlight=false&width=90pc)

2. Within the **IAM** interface:
   - Select **Roles**
   - Click on **Create role**

![Create role](/images/1/0002.png?featherlight=false&width=90pc)

3. Follow these steps to create a VPC:
   - Select **AWS Service**
   - Select **Service or Use case** as **`EC2`**
   - Select **Use case** as **`EC2`**

![Create role](/images/1/0003.png?featherlight=false&width=90pc)

4. Click on **Next**

![Create role](/images/1/0003.png?featherlight=false&width=90pc)

5. Add Premission 
   - Search `CloudWatchAgentPollcy`
   - Select **CloudWatchAgentPollcy**
   - Search `AmazonSSMManagedInstanceCore`
   - Select **AmazonSSMManagedInstanceCore**
   - Click on **Next**

![Create role](/images/1/0004.png?featherlight=false&width=90pc)
![Create role](/images/1/0005.png?featherlight=false&width=90pc)

6. Review the details of the newly created role
![Create role](/images/1/0007.png?featherlight=false&width=90pc)

