---
title : "Dọn dẹp tài nguyên"
date :  "`r Sys.Date()`" 
weight : 4
chapter : false
pre : " <b> 4. </b> "
---
#### Dọn dẹp tài nguyên

Chúng ta sẽ tiến hành xóa các tài nguyên theo thứ tự sau

### Terminate các EC2 Instance.
1. Terminate EC2 instance.
    - Truy cập Amazon EC2 console tại địa chỉ [EC2](https://console.aws.amazon.com/ec2/).
    - Trên thanh điều hướng bên trái, chọn Intances
    - Chọn tất cả EC2 Instance liên quan tới bài lab.
    - Chọn **Instance state**
    - Chọn **Terminate instance**

    ![Terminate EC2](/images/8/0001.png?featherlight=false&width=90pc)

2. Xác nhận terminate.

    ![Confirm Termination](/images/8/0002.png?featherlight=false&width=90pc)

#### Xóa NAT Gateway, Elastic IP Address 
- Truy cập trang Amazon VPC console tại địa chỉ [VPC](https://console.aws.amazon.com/vpc/)
- Trên thanh điều hướng bên trái , click VPC.
- Chọn YourVPC.
- Click Action.
- Click **Delete VPC**.

   ![Delete VPC](/images/8/0003.png?featherlight=false&width=90pc)

- Gõ `delete`.
- Click **Delete** để xác nhận xóa VPC

   ![Confirm Deletion](/images/8/0004.png?featherlight=false&width=90pc)

#### Xóa CloudWatch
- Truy cập trang Amazon VPC console tại địa chỉ https://console.aws.amazon.com/cloudwatch/
- Trên thanh điều hướng bên trái , click All Alarm.
- Chọn Alarm chúng ta đã tạo.
- Click Action.
- Click **Delete**

   ![Delete CloudWatch](/images/8/0005.png?featherlight=false&width=90pc)

    - Chọn **CloudWatch** để xác nhận xóa Alarm.
   ![Confirm CloudWatch](/images/8/0006.png?featherlight=false&width=90pc)


#### Delete the IAM
- Truy cập trang Amazon VPC console tại địa chỉ [IAM](https://console.aws.amazon.com/iam/).
- rên thanh điều hướng bên trái, click "Roles."
- Chọn **CloudWatch** ta đã tạo.
- Click **Delete**.

   ![Confirm CloudWatch](/images/8/0007.png?featherlight=false&width=90pc)

- Xác nhận terminate.

   ![Confirm Termination](/images/8/0008.png?featherlight=false&width=90pc)