---
title : "Create EC2"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 2.4 </b> "
---

## Create EC2

1. Within the **EC2** interface:
   - Select **EC2 instances**
   - Click **Launch an instance**

   ![Create EC2](/images/2/0009.png?featherlight=false&width=90pc)

2. Follow these steps to create EC2 instances
   - Name as `CloudWatch-Service`

   ![Create EC2](/images/2/00010.png?featherlight=false&width=90pc)

3. These steps is Application and OS Images
   - Amazon Machine Image (AMI), select **Amazon Linux 2 AMI (HVM) - Kenel 5.10, SSD Volume Type**
   - Instance type, select **t2.micro**
   - Key pair name - required, select **cloudwatch**

   ![Create EC2](/images/2/00011.png?featherlight=false&width=90pc)

4. Network settings
   - VPC - required, select **CloudWatch-vpc**
   - Subnet, select **CloudWatch-subnet-public-1a-southeast-1st**
   - Auto-assign public IP, select **Enable**
   - Firewall (security group), select existing security group
   - Common security groups, select **CloudWatch-SG**

   ![Create EC2](/images/2/00012.png?featherlight=false&width=90pc)


5. Finish Launch instance
   Click on **Launch instance**

   ![Create EC2](/images/2/00013.png?featherlight=false&width=90pc)

6. IAM role
   - Select as **Instances** 
   - Select Action > Security > click **Modify IAM role**

   ![Create EC2](/images/2/00014.png?featherlight=false&width=90pc)

7. Follow these steps to Modify IAM role
   - IAM role, select as **CloudWatch**
   - Click **Update IAM role**

   ![Create EC2](/images/2/00015.png?featherlight=false&width=90pc)
