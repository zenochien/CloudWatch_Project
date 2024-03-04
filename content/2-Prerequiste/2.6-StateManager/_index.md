---
title : "Install/configure with State Manager"
date : "`r Sys.Date()`"
weight : 6
chapter : false
pre : " <b> 2.4 </b> "
---

## Install/configure with State Manager

1. Download click link [MobaXterm](https://mobaxterm.mobatek.net/download.html)

2. Copy pubilc addess on EC2 instances
   - In **EC2 Dashboard**
   - Select **CloudWatch-Server**
   - Copy Public IPv4 address as `3.0.55.206`

   ![StateManager](/images/4/0001.png?featherlight=false&width=90pc)


3. Follow step on the **MobaXterm** interface:
   - Click Session
   - Choose on SSH
   - Basic SSH settings, Romote host `3.0.55.206`
   - Select Specify username as `ec2-user`
   - Select Use private key, choose the path of the **cloudwatch.pem** created and downloaded during EC2 instance creation.
   - Click OK
   
   ![StateManager](/images/4/0002.png?featherlight=false&width=90pc)

2. Install collectd on aws Linux:

   ```
   sudo amazon-linux-extras install collectd
   ```

   ![StateManager](/images/4/0003.png?featherlight=false&width=90pc)

3. Complete install the **collectd**.

   ![StateManager](/images/4/0004.png?featherlight=false&width=90pc)

4. Use the configuration above and replace the contents of the file at **/etc/collectd.conf**

   ```
    sudo vi /etc/collectd.conf
   ```

   ![StateManager](/images/4/0005.png?featherlight=false&width=90pc)

5. Review the **collectd** configuration

   ![StateManager](/images/4/0006.png?featherlight=false&width=90pc)


6. Start the **collectd** agent
   ```
   sudo systemctl start collectd.service
   ```

   ![StateManager](/images/4/0007.png?featherlight=false&width=90pc)



