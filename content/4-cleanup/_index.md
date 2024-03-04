---
title : "Clean up resources"
date : "`r Sys.Date()`"
weight : 4
chapter : false
pre : " <b> 4. </b> "
---
## Clean up resources

We will proceed to delete the resources in the following order:

### Terminate EC2 Instances

1. Terminate EC2 instance:
    - Access the Amazon EC2 console at [EC2](https://console.aws.amazon.com/ec2/).
    - On the left navigation bar, select "Instances."
    - Select all EC2 instances related to the lab.
    - Select **Instance state**.
    - Select **Terminate instance**.

   ![Terminate EC2](/images/8/0001.png?featherlight=false&width=90pc)

2. Confirm termination.

   ![Confirm Termination](/images/8/0002.png?featherlight=false&width=90pc)

### Remove VPC

- Visit the Amazon VPC console page at [VPC](https://console.aws.amazon.com/vpc/).
- On the left navigation bar, click "VPC"
- Select Your VPC.
- Click **Action**.
- Click **Delete VPC**.

   ![Delete VPC](/images/8/0003.png?featherlight=false&width=90pc)

- Type "delete."
- Click **Delete** to confirm the deletion of VPC.

   ![Confirm Deletion](/images/8/0004.png?featherlight=false&width=90pc)

### Delete CloudWatch
- Visit the Amazon VPC console page at [CloudWatch](https://console.aws.amazon.com/cloudwatch/).
- On the left navigation bar, click "CloudWatch."
- Select the All Alarm we created.
- Click **Action**.
- Click **Delete**.

   ![Delete CloudWatch](/images/8/0005.png?featherlight=false&width=90pc)

- Click **CloudWatch** to confirm the deletion of Alarm.

   ![Confirm CloudWatch](/images/8/0006.png?featherlight=false&width=90pc)

#### Delete the IAM
- Visit the Amazon VPC console page at [IAM](https://console.aws.amazon.com/iam/).
- On the left navigation bar, click "Roles."
- Select the **CloudWatch** we created.
- Click **Delete**.

   ![Confirm CloudWatch](/images/8/0007.png?featherlight=false&width=90pc)

- Confirm termination.

   ![Confirm Termination](/images/8/0008.png?featherlight=false&width=90pc)