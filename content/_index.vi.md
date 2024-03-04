---
title : "Bắt đầu với CloudWatch agent và collectd"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---

# Bắt đầu với CloudWatch agent và collectd

#### Tổng quan

Khả năng quan sát giúp bạn hiểu rõ tình trạng, cách sử dụng, hiệu suất và trải nghiệm khách hàng đối với khối lượng công việc của bạn. Khả năng quan sát có thể hỗ trợ nhiều trường hợp sử dụng, từ phát hiện sự cố và hỗ trợ giải quyết sự cố cho đến hiểu rõ tác động của các tính năng mới đối với người dùng và quy trình làm việc của bạn. Việc thiết lập giải pháp phù hợp phụ thuộc vào khả năng thu thập dữ liệu phù hợp cho tình huống của bạn. Trong bài đăng này, bạn sẽ khám phá cách sử dụng Collectd và tác nhân Amazon CloudWatch để thêm vào các số liệu có thể được thu thập từ các Linux instances.

Bạn sẽ hướng dẫn thiết lập cơ bản về colld và tác nhân CloudWatch trên Linux instances của Amazon Elastic Computing Cloud (Amazon EC2). Tác nhân CloudWatch có thể thu thập số liệu và nhật ký cấp hệ thống từ Amazon EC2 instances, đồng thời hỗ trợ thu thập số liệu bổ sung từ Collectd. Dữ liệu bạn thu thập có thể giúp bạn hiểu hiệu suất và cách sử dụng tài nguyên của mình, đồng thời đưa ra quyết định dựa trên dữ liệu để hỗ trợ khách hàng và khối lượng công việc của bạn.

Để giúp bạn bắt đầu, bạn sẽ sử dụng một ví dụ đơn giản về thu thập dữ liệu về các tệp đang mở, đồng thời xem cách cài đặt và định cấu hình cả tác nhân Collectd và CloudWatch bằng AWS Systems Manager (SSM) để cho phép bạn quản lý quy trình này trên nhiều máy chủ. Sau đó, bạn có thể khám phá các số liệu liên quan đến mình và định cấu hình được thu thập cho phù hợp.


#### Nội dung

1. [Introduction](1-introduce/)
2. [Prerequiste](2-prerequiste/)
3. [Metrics](3-metrics)
4. [cleanup](4-cleanup)
