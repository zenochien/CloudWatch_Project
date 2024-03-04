---
title : "Cài đặt Cloudwatch agent"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---

## Cài đặt Cloudwatch agent

1. Trong giao diện **MobaXterm** với EC2 instances kết nối SSH:

   - Cài đật cloudwatch agent

   ```
   sudo install amazon-cloudwatch-agent
   ```

   ![collectd](/images/6/0001.png?featherlight=false&width=90pc)

2. Chạy trình hướng dẫn trên dòng lệnh EC2 instances

   ```
   sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-config-wizard
   ```

   ![collectd](/images/6/0002.png?featherlight=false&width=90pc)

3. Làm theo trình hướng dẫn Trình quản lý cấu hình của tác nhân **CloudWatch** và đặt cấu hình mặc định

   ![collectd](/images/6/0003.png?featherlight=false&width=90pc)

4. Trong trình hướng dẫn chỉ định cấu hình bổ sung nhật kí

   ```
   /var/log/messages
   ```

   ![collectd](/images/6/0004.png?featherlight=false&width=90pc)

5. Chạy cấu hình mặc định trên CloudWacth

   ![collectd](/images/6/0005.png?featherlight=false&width=90pc)

6. Chạy lệnh sau

   ![collectd](/images/6/0006.png?featherlight=false&width=90pc)

7. Sau đó hãy đảm bảo agent được khởi động

   ```
   sudo systemctl start amazon-cloudwatch-agent
   ```

   ![collectd](/images/6/0007.png?featherlight=false&width=90pc)

8. Chi tiết giao diện **Metrics**: 
   - Chọn Metrics > All Metrics

   ![collectd](/images/6/0008.png?featherlight=false&width=90pc)
