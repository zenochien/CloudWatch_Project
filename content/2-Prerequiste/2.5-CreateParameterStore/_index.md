---
title : "Create Parameter Store"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 2.3 </b> "
---

## Create Parameter Store

1. In the **Parameter Store** interface:
   - Select **Parameter Store**
   - Click on **Create Parameter**  
   ![Create PS](/images/3/0001.png?featherlight=false&width=90pc)

2. Configure the Parameter details:
   - Name `conttectd-config`
   - Description - Optional `Setup Collectd Config`
   - Vaule as `collectd-config`
   - Finish create parameter

   ![Create PS](/images/3/0002.png?featherlight=false&width=90pc)

3. Next configure the Parameter details:
   - Name `cloudwatch-config-forcollectd`
   - Description - Optional `Setup Cloud Watch Config`
   - Vaule as `cloudwatch-config-forcollectd`
   - Finish create parameter

   ![Create PS](/images/3/0003.png?featherlight=false&width=90pc)

4. Review the Parameter Store:
   - Click Parameter Store > My paramertrs

   ![Create PS](/images/3/0004.png?featherlight=false&width=90pc)
