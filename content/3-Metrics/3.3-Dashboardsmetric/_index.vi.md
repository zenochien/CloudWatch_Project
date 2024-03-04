---
title : "Dashboards Metric"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3.3 </b> "
---

## Dashboards Metric

1. Trong giao diện điều khiển **All Metrics**
   - Trong tất cả các ví dụ này, ta đang sử dụng số liệu
   - Namespace
   - Metric name
   - Fitter by
   - Click  **Graph query**

   ![alarms](/images/7/00015.png?featherlight=false&width=90pc)

2. Metrics Insights - query editor

   ```
   SELECT MAX(cpu_usage_steal) FROM SCHEMA(CWAgent, ImageId,InstanceId,InstanceType,cpu) WHERE cpu = 'cpu0'
   ```

   ![alarms](/images/7/00016.png?featherlight=false&width=90pc)

3. Trong giao diện điều khiển **All Metrics**
   - Tất cả instance của CPU
   - Namespace
   - Metric name
   - Fitter by
   - Chọn  **Graph query**

   ![alarms](/images/7/00017.png?featherlight=false&width=90pc)

4. Metrics Insights - query editor

   ```
   SELECT MAX(disk_used_percent) FROM SCHEMA(CWAgent, ImageId,InstanceId,InstanceType,device,fstype,path) WHERE ImageId = 'ami-0e75e9888b89c15e1' ORDER BY COUNT() ASC
   ```

   ![alarms](/images/7/00018.png?featherlight=false&width=90pc)