---
title : "Tạo Alarms/Dashboards"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2 </b> "
---

## Tạo Alarms/Dashboards

> ℹ️ **Note:** Lưu ý rằng các truy vấn Metric Math bao gồm khoảng thời gian 300 giây hoặc 5 phút.

1. Trong giao diện **In alarm** với tạo alarm:
   - Chọn **In alarm** > **create alarm**

   ![alarms](/images/7/0001.png?featherlight=false&width=90pc)

2. Chọn Metric

   ![alarms](/images/7/0002.png?featherlight=false&width=90pc)

3. Chọn **CWAgent** trong Custom namespaces

   ![alarms](/images/7/0003.png?featherlight=false&width=90pc)

4. Chọn **ImageId, InstanceId, InstanceType, device, fstype, path** trong the CWAgent

   ![alarms](/images/7/0004.png?featherlight=false&width=90pc)

5. Chọn một duy nhất instances > select metric

   ![alarms](/images/7/0005.png?featherlight=false&width=90pc)

6. Xem chi tiết và tiếp theo

   ![alarms](/images/7/0007.png?featherlight=false&width=90pc)
   ![alarms](/images/7/0008.png?featherlight=false&width=90pc)


7. Cấu hình thiết lập
   - Chọn **in alarm**
   - Gửi một thông báo tới **asg-topics** và tiếp theo

   ![alarms](/images/7/0009.png?featherlight=false&width=90pc)
   ![alarms](/images/7/00010.png?featherlight=false&width=90pc)

8. Thêm tên và chi tiết
   - Alarm name as **Agent**
   - Tiếp theo

   ![alarms](/images/7/00011.png?featherlight=false&width=90pc)
   ![alarms](/images/7/00012.png?featherlight=false&width=90pc)

9. Review the **Preview and create**

   ![alarms](/images/7/00012.png?featherlight=false&width=90pc)
   ![alarms](/images/7/00013.png?featherlight=false&width=90pc)

10. Hoàn thành tạo alarm

   ![alarms](/images/7/00014.png?featherlight=false&width=90pc)

11. In the **All Metrics** interface
   - Trong tất cả các ví dụ này, ta đang sử dụng số liệu
   - Namespace
   - Metric name
   - Fitter by
   - Click  **Graph query**

   ![alarms](/images/7/00015.png?featherlight=false&width=90pc)

12. Metrics Insights - query editor

   ```
   SELECT MAX(cpu_usage_steal) FROM SCHEMA(CWAgent, ImageId,InstanceId,InstanceType,cpu) WHERE cpu = 'cpu0'
   ```

   ![alarms](/images/7/00016.png?featherlight=false&width=90pc)

13. Trong giao diện **All Metrics**
   - Tất cả instance của CPU
   - Namespace
   - Metric name
   - Fitter by
   - Chọn  **Graph query**

   ![alarms](/images/7/00017.png?featherlight=false&width=90pc)

14. Metrics Insights - query editor

   ```
   SELECT MAX(disk_used_percent) FROM SCHEMA(CWAgent, ImageId,InstanceId,InstanceType,device,fstype,path) WHERE ImageId = 'ami-0e75e9888b89c15e1' ORDER BY COUNT() ASC
   ```

   ![alarms](/images/7/00018.png?featherlight=false&width=90pc)