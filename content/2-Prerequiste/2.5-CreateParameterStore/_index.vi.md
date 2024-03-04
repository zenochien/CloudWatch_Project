---
title : "Tạo Parameter Store"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 2.3 </b> "
---

## Tạo Parameter Store

1. Trong giao diện **Parameter Store**:
   - Chọn **Parameter Store**
   - Chọn **Create Parameter**  

   ![Create PS](/images/3/0001.png?featherlight=false&width=90pc)

2. Thiết lập Parameter details:
   - Name `conttectd-config`
   - Description - Optional `Setup Collectd Config`
   - Vaule as `collectd-config`
   - Hoàn thành chọn create parameter

   ![Create PS](/images/3/0002.png?featherlight=false&width=90pc)

3. Next configure the Parameter details:
   - Name `cloudwatch-config-forcollectd`
   - Description - Optional `Setup Cloud Watch Config`
   - Vaule as `cloudwatch-config-forcollectd`
   - Hoàn thành chọn create parameter

   ![Create PS](/images/3/0003.png?featherlight=false&width=90pc)

4. Xem các chi tiết đã tạo parameter store:
   - Chọn Parameter Store > My paramertrs

   ![Create PS](/images/3/0004.png?featherlight=false&width=90pc)
