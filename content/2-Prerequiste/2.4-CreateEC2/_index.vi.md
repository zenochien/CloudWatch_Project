---
title : "Tạo EC2"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 2.5 </b> "
---

## Tạo EC2

1. Giao diện **EC2**:
   - Chọn **EC2 instances**
   - Chọn **Launch an instance**

   ![Create EC2](/images/2/0009.png?featherlight=false&width=90pc)

2. Các bước tạo EC2 instances
   - Name `CloudWatch-Service`

   ![Create EC2](/images/2/00010.png?featherlight=false&width=90pc)

3. Bước là Application and OS Images
   - Amazon Machine Image (AMI), chọn **Amazon Linux 2 AMI (HVM) - Kenel 5.10, SSD Volume Type**
   - Instance type, chọn **t2.micro**
   - Key pair name - required, chọn **cloudwatch**

   ![Create EC2](/images/2/00011.png?featherlight=false&width=90pc)

4. Network settings
   - VPC - required, chọn **CloudWatch-vpc**
   - Subnet, chọn **CloudWatch-subnet-public-1a-southeast-1st**
   - Auto-assign public IP, chọn **Enable**
   - Firewall (security group), *select existing security group*
   - Common security groups, chọn **CloudWatch-SG**

   ![Create EC2](/images/2/00012.png?featherlight=false&width=90pc)

5. Hoàn thành Launch instance
   - Chọn **Launch instance**

   ![Create EC2](/images/2/00013.png?featherlight=false&width=90pc)

6. IAM role
   - Chọn **Instances** 
   - Chọn Action > Security > **Modify IAM role**

   ![Create EC2](/images/2/00014.png?featherlight=false&width=90pc)

7. Các bước Modify IAM role
   - IAM role, Chọn **CloudWatch**
   - Chọn **Update IAM role**

   ![Create EC2](/images/2/00015.png?featherlight=false&width=90pc)
