---
title : "State Manager Association"
date : "`r Sys.Date()`"
weight : 7
chapter : false
pre : " <b> 2.5 </b> "
---


### State Manager Association

1. Trong giao diện **State Manager Association**:
    - Chọn **State Manager**
    - Chọn **Create a association**

    ![SMA](/images/5/0001.png?featherlight=false&width=90pc)

2. Thiết lập cấu hình **State Manager Association**:
    - Name - optional: `LinuxColletdSetup`
    - Document, search: `AWS-RunShellScript`
    - Chọn **AWS-RunShellScript**

    ![SMA](/images/5/0002.png?featherlight=false&width=90pc)

3. Dòng lệnh command paraments:
    - Commands
    ```
    sudo amazon-linux-extras install collectd
    sudo systemctl stop collectd.service
    sudo echo '{{ssm:collectd-config}}' > /etc/collectd.conf
    sudo systemctl start collectd.service
    ```

    ![SMA](/images/5/0003.png?featherlight=false&width=90pc)

4. Target selection
    - **Choose instances manually** 
    - Choose instances **CloudWatch-Service** 

    ![SMA](/images/5/0004.png?featherlight=false&width=90pc)

5. Kiểm tra Output options và hoàn thành **Run**
    - Tắt **Enable an S3 bucket**

    ![SMA](/images/5/0005.png?featherlight=false&width=90pc)

6. Tiếp theo, tạo Association
    - Name - optional: `LinuxCloudWatchInstall`
    - Document, search: `AWS-ConfigureAWSPackage`
    - Chọn **AWS-ConfigureAWSPackage**

    ![SMA](/images/5/0006.png?featherlight=false&width=90pc)

7. Dòng lệnh command paramenters
    - Action: **Install**
    - Name: **AmazonCloudWatch**

    ![SMA](/images/5/0007.png?featherlight=false&width=90pc)

8. Kiểm tra Output options và hoàn thành **Run**
    - Tắt **Enable an S3 bucket**

    ![SMA](/images/5/0008.png?featherlight=false&width=90pc)

9. Tiếp theo, tạo Association
    - Name - optional `LinuxCloudWacthConfig`
    - Document, search: `AmazonCloudWatch-ManageAgent`
    - Chọn **AmazonCloudWatch-ManageAgent**

    ![SMA](/images/5/0009.png?featherlight=false&width=90pc)

10. Dòng lệnh Command paramenters 
    - Action: **configure**
    - Mode: **EC2**
    - Optional Configuration Source: **SSM**
    - Optional Configuration Location: **cloudwatch-config-forcollectd**
    - Optional Restart: **yes**

    ![SMA](/images/5/00010.png?featherlight=false&width=90pc)

11. Kiểm tra Output options và kiểm tra **Run**
    - Tắt **Enable an S3 bucket**

    ![SMA](/images/5/00012.png?featherlight=false&width=90pc)

12. Chi tiết mẫu **State Manager Association** đã tạo
    
    ![SMA](/images/5/00013.png?featherlight=false&width=90pc)

 