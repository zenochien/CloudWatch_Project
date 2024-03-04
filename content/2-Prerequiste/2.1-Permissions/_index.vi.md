---
title : "Tạo role"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---
## Tạo Roles

1. Trong giao diện **AWS Management Console**:
   - Chọn ở ví trị **IAM**
   - Chọn **IAM**

![Create role](/images/1/0001.png?featherlight=false&width=90pc)

2. Giao diện **IAM**:
   - Chọn **Roles**
   - Chọn **Create role**

![Create role](/images/1/0002.png?featherlight=false&width=90pc)

3. Các bước tạo role
   - Chọn **AWS Service**
   - Chọn **Service or Use case** ở **`EC2`**
   - Chọn **Use case** ở **`EC2`**

![Create role](/images/1/0003.png?featherlight=false&width=90pc)

4. Chọn **Next**

![Create role](/images/1/0003.png?featherlight=false&width=90pc)

5. Add Premission 
   - Tìm kiếm `CloudWatchAgentPollcy`
   - Chọn **CloudWatchAgentPollcy**
   - Tìm kiếm `AmazonSSMManagedInstanceCore`
   - Chọn **AmazonSSMManagedInstanceCore**
   - Chọn **Next**

![Create role](/images/1/0004.png?featherlight=false&width=90pc)
![Create role](/images/1/0005.png?featherlight=false&width=90pc)

6. Xem các mẫu chi tiết đã được tạo
![Create role](/images/1/0007.png?featherlight=false&width=90pc)

