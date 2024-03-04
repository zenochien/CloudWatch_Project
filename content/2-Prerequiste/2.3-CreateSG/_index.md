---
title : "Create Security Group"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

## Create Security Group

1. Within the **Security Group** interface:
   - Select **Security Group**
   - Click on **Create Security Group**

   ![Create SG](/images/2/0005.png?featherlight=false&width=90pc)


2. Follow these steps to create security group:
   - Security group name: `CloudWatch-SG`
   - Description: `CloudWatch-SG`
   - Select on VPC **CloudWatch-vpc**
   - Inbound rules to **Add rule**

   ![Create SG](/images/2/0006.png?featherlight=false&width=90pc)

3. Add rule
   - Select on Type as **SSH**
   - Port range **22**
   - Select on Source **Anywhere-IPv4**

   ![Create SG](/images/2/0007.png?featherlight=false&width=90pc)

4. Finish create security group
   - Click on **Create Security Group**

   ![Create SG](/images/2/0008.png?featherlight=false&width=90pc)
