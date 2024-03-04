---
title : "Create Alarms/Dashboards"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2 </b> "
---

## Create Alarms/Dashboards

> ℹ️ **Note:** Note that the Metric Math queries include a period of 300s, or 5 minutes.

1. In the **In alarm** with create alarm:
   - Select **In alarm** > **create alarm**

   ![alarms](/images/7/0001.png?featherlight=false&width=90pc)

2. Select Metric

   ![alarms](/images/7/0002.png?featherlight=false&width=90pc)

3. Choose **CWAgent** in Custom namespaces

   ![alarms](/images/7/0003.png?featherlight=false&width=90pc)

4. Choose **ImageId, InstanceId, InstanceType, device, fstype, path** in the CWAgent

   ![alarms](/images/7/0004.png?featherlight=false&width=90pc)

5. Choose only instances > Select metric

   ![alarms](/images/7/0005.png?featherlight=false&width=90pc)

6. Review and next step 

   ![alarms](/images/7/0007.png?featherlight=false&width=90pc)
   ![alarms](/images/7/0008.png?featherlight=false&width=90pc)


7. Configure action
   - Choose **in alarm**
   - Send a noctification to **asg-topics** and next step

   ![alarms](/images/7/0009.png?featherlight=false&width=90pc)
   ![alarms](/images/7/00010.png?featherlight=false&width=90pc)

8. Add name and description
   - Alarm name as **Agent**
   - Next step

   ![alarms](/images/7/00011.png?featherlight=false&width=90pc)
   ![alarms](/images/7/00012.png?featherlight=false&width=90pc)

9. Review the **Preview and create**

   ![alarms](/images/7/00012.png?featherlight=false&width=90pc)
   ![alarms](/images/7/00013.png?featherlight=false&width=90pc)

10. Finish create alarm

   ![alarms](/images/7/00014.png?featherlight=false&width=90pc)

11. In the **All Metrics** interface
   - In all of these examples, we are using numbers
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

13. In the **All Metrics** interface
   - All instances of CPU
   - Namespace
   - Metric name
   - Fitter by
   - Click  **Graph query**

   ![alarms](/images/7/00017.png?featherlight=false&width=90pc)

14. Metrics Insights - query editor

   ```
   SELECT MAX(disk_used_percent) FROM SCHEMA(CWAgent, ImageId,InstanceId,InstanceType,device,fstype,path) WHERE ImageId = 'ami-0e75e9888b89c15e1' ORDER BY COUNT() ASC
   ```

   ![alarms](/images/7/00018.png?featherlight=false&width=90pc)
