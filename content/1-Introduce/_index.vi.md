---
title : "Giới thiệu"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---

![Cloud Watch](/images/3-Prerequiste/cw.png?featherlight=false&width=60pc)

#### Giới thiệu Amazon CloudWatch

**Amazon CloudWatch** là dịch vụ giám sát của AWS cho các tài nguyên đám mây và các application mà bạn chạy trên AWS. Bạn có thể sử dụng Amazon CloudWatch để thu thập và theo dõi số liệu, thu thập và theo dõi alarms. Amazon CloudWatch có thể giám sát các tài nguyên của AWS như các Amazon EC2 instances, Amazon DynamoDB tables và các Amazon RDS DB instances, ngoài số liệu tùy chỉnh được tạo bởi các application và dịch vụ của bạn và bất kỳ tệp nhật ký nào được tạo bởi các application, host on premises, hybrid hoặc cloud khác. Bạn có thể sử dụng Amazon CloudWatch để nắm bắt thông tin trên toàn hệ thống về mức sử dụng tài nguyên, hiệu năng application và tình trạng vận hành. Bạn có thể sử dụng những thông tin này để phản ứng và duy trì application luôn chạy trơn tru.

Để bắt đầu theo dõi, bạn có thể sử dụng Auto Dashboards với các phương pháp tối ưu tích hợp sẵn của AWS, khám phá tài khoản và xem số liệu cũng như cảnh báo dựa trên tài nguyên, đồng thời dễ dàng phân tích sâu để hiểu được nguyên nhân cốt lõi của các sự cố về hiệu năng.

**Amazon CloudWatch hỗ trợ những hệ điều hành nào?**

Amazon CloudWatch nhận và cung cấp số liệu tới tất cả các Amazon EC2 instances và có thể làm việc với bất kỳ hệ điều hành nào hiện đang được dịch vụ Amazon EC2 hỗ trợ.

**Tôi có thể triển khai chính sách quản lý truy cập nào cho CloudWatch?**

Amazon CloudWatch được tích hợp với AWS Identity and Access Management (IAM) để bạn có thể chọn thao tác CloudWatch nào mà người dùng trong AWS Account của bạn có thể thực hiện. Ví dụ: bạn có thể tạo chính sách IAM chỉ cho một số người dùng nhất định quyền tổ chức để sử dụng GetMetricStatistics. Sau đó, họ có thể sử dụng thao tác đó để truy xuất dữ liệu về tài nguyên đám mây của bạn.

Bạn không thể sử dụng IAM để kiểm soát quyền truy cập dữ liệu CloudWatch cho các tài nguyên cụ thể. Ví dụ: bạn không thể trao cho người dùng quyền truy cập dữ liệu CloudWatch cho chỉ một instances nhất định hay LoadBalancer nhất định. Quyền được trao bằng cách sử dụng IAM bao hàm tất cả tài nguyên đám mây bạn sử dụng với CloudWatch. Ngoài ra, bạn không thể sử dụng IAM roles với công cụ dòng lệnh Amazon CloudWatch.

**Trình đại diện Bản ghi CloudWatch có hỗ trợ các IAM roles không?**

Có. Trình đại diện CloudWatch Logs được tích hợp với Identity and Access Management (IAM) và có hỗ trợ cho cả khóa truy cập lẫn roles IAM.

#### Nội dung

- [Agent](1.1-agent)
- [Systems Manager](1.2-sm)

Bây giờ chúng ta sẽ cùng nhau đi qua các khái niệm cơ bản nhất của CloudWatch nhé.
