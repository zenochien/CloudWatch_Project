---
title : "Cài đặt/cấu hình với State Manager"
date : "`r Sys.Date()`"
weight : 6
chapter : false
pre : " <b> 2.4 </b> "
---

## Cài đặt/cấu hình với State Manager

1. Tải về máy [MobaXterm](https://mobaxterm.mobatek.net/download.html)

2. Sao chép địa chỉ IPv4 public
   - Giao diện **EC2 Dashboard**
   - Chọn **CloudWatch-Server**
   - Sao chép địa chỉ Ipv4 public `3.0.55.206`

   ![StateManager](/images/4/0001.png?featherlight=false&width=90pc)


3. Các bước kết nối SSH với **MobaXterm**:
   - Chọn Session
   - Chọn SSH
   - Basic SSH settings, Romote host `3.0.55.206`
   - Chọn Specify username as `ec2-user`
   - Chọn Use private key, chọn đường dẫn của **cloudwatch.pem** được tạo và tải xuống trong quá trình tạo EC2 instances.
   - Click OK
   
   ![StateManager](/images/4/0002.png?featherlight=false&width=90pc)

2. Cài đặt collectd trên aws Linux:

   ```
   sudo amazon-linux-extras install collectd
   ```

   ![StateManager](/images/4/0003.png?featherlight=false&width=90pc)

3. Hoàn thành cài đặt **collectd**.

   ![StateManager](/images/4/0004.png?featherlight=false&width=90pc)

4. Sử dụng cấu hình ở trên và thay thế nội dung của tệp tại **/etc/collectd.conf**

   ```
    sudo vi /etc/collectd.conf
   ```

   ![StateManager](/images/4/0005.png?featherlight=false&width=90pc)

5. Chi tiết mẫu cấu hình **collectd**

   ![StateManager](/images/4/0006.png?featherlight=false&width=90pc)


6. Khởi đầu **collectd**
   ```
   sudo systemctl start collectd.service
   ```

   ![StateManager](/images/4/0007.png?featherlight=false&width=90pc)



