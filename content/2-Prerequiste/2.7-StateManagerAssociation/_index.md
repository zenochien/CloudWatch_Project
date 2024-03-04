---
title : "State Manager Association"
date : "`r Sys.Date()`"
weight : 7
chapter : false
pre : " <b> 2.5 </b> "
---


### State Manager Association

1. In the **State Manager Association** interface:
    - Select **State Manager**
    - Select **Create a association**

    ![SMA](/images/5/0001.png?featherlight=false&width=90pc)

2. Configure the **State Manager Association**:
    - Name - optional as `LinuxColletdSetup`
    - Document, search as `AWS-RunShellScript`
    - Choose **AWS-RunShellScript**

    ![SMA](/images/5/0002.png?featherlight=false&width=90pc)

3. Command paraments:
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

5. Check Output options and finish **Run**
    - No **Enable an S3 bucket**

    ![SMA](/images/5/0005.png?featherlight=false&width=90pc)

6. Next step, Create Association
    - Name - optional `LinuxCloudWatchInstall`
    - Document, search as `AWS-ConfigureAWSPackage`
    - Choose **AWS-ConfigureAWSPackage**

    ![SMA](/images/5/0006.png?featherlight=false&width=90pc)

7. Command paramenters
    - Action as **Install**
    - Name as **AmazonCloudWatch**

    ![SMA](/images/5/0007.png?featherlight=false&width=90pc)

8. Check Output options 
    - No **Enable an S3 bucket**
    - Finish **Run**

    ![SMA](/images/5/0008.png?featherlight=false&width=90pc)

9. Next step, Create Association
    - Name - optional `LinuxCloudWacthConfig`
    - Document, search as `AmazonCloudWatch-ManageAgent`
    - Choose **AmazonCloudWatch-ManageAgent**

    ![SMA](/images/5/0009.png?featherlight=false&width=90pc)

10. Command paramenters 
    - Action as **configure**
    - Mode as **EC2**
    - Optional Configuration Source as **SSM**
    - Optional Configuration Location as **cloudwatch-config-forcollectd**
    - Optional Restart as **yes**

    ![SMA](/images/5/00010.png?featherlight=false&width=90pc)

11. Check Output options
    - No **Enable an S3 bucket**
    - Finish **Run**

    ![SMA](/images/5/00012.png?featherlight=false&width=90pc)

12. Review the **State Manager Association** created
    
    ![SMA](/images/5/00013.png?featherlight=false&width=90pc)

 