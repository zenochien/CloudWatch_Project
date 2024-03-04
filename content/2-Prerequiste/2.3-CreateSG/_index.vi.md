---
title : "Tạo Security Group"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

## Tạo Security Group

1. Giao diện **Security Group**:
   - Chọn **Security Group**
   - Chọn **Create Security Group**

   ![Create SG](/images/2/0005.png?featherlight=false&width=90pc)

2. Các bước cài đặt Security Group:
   - Tên Security Group: `CloudWatch-SG`
   - Chủ đề: `CloudWatch-SG`
   - Chọn VPC **CloudWatch-vpc**
   - Cấu hình nội bộ **Add rule**

   ![Create SG](/images/2/0006.png?featherlight=false&width=90pc)

3. Add rule
   - Chọn Type **SSH**
   - Port range **22**
   - Chọn Source **Anywhere-IPv4**

   ![Create SG](/images/2/0007.png?featherlight=false&width=90pc)

4. Hoàn thành tạo security group
   - Chọn **Create Security Group**

   ![Create SG](/images/2/0008.png?featherlight=false&width=90pc)
