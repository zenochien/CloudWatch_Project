---
title : "Install Cloudwatch agent"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---

## Install Cloudwatch agent

1. In the **MobaXterm** interface with EC2 connect SSH:

   - Install cloudwatch agent

   ```
   sudo install amazon-cloudwatch-agent
   ```

   ![collectd](/images/6/0001.png?featherlight=false&width=90pc)

2. Run the wizard on the EC2 instance command line

   ```
   sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-config-wizard
   ```

   ![collectd](/images/6/0002.png?featherlight=false&width=90pc)

3. Follow the CloudWatch agent Configura Manager wizard and run default

   ![collectd](/images/6/0003.png?featherlight=false&width=90pc)

4. During the wizard specify additional log file collection

   ```
   /var/log/messages
   ```

   ![collectd](/images/6/0004.png?featherlight=false&width=90pc)

5. Run configura default on the CloudWacth

   ![collectd](/images/6/0005.png?featherlight=false&width=90pc)

6. Run the following commmand

   ![collectd](/images/6/0006.png?featherlight=false&width=90pc)

7. Then make sure the agent is started

   ```
   sudo systemctl start amazon-cloudwatch-agent
   ```

   ![collectd](/images/6/0007.png?featherlight=false&width=90pc)

8. Review the **Metrics** interface: 
   - Select Metrics > All Metrics

   ![collectd](/images/6/0008.png?featherlight=false&width=90pc)

