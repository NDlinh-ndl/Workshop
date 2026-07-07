---
title: "Worklog Tuần 4"
date: 2024-01-01
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Hiểu và sử dụng S3 cho object storage và static website hosting.
* Triển khai RDS để quản lý cơ sở dữ liệu quan hệ trên AWS.
* Làm quen với DynamoDB — NoSQL database serverless của AWS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Ôn lại kiến thức EC2 và Auto Scaling tuần trước <br> - Đọc tài liệu về S3: storage classes, versioning, lifecycle <br> - Tìm hiểu sự khác biệt giữa SQL và NoSQL | 11/05/2026 | 11/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Lab 7: Static Website Hosting with Amazon S3** <br> - Tạo S3 bucket và cấu hình quyền truy cập <br> - Kích hoạt versioning và lifecycle policy <br> - Host static website trên S3 <br> - Cấu hình S3 bucket policy và CORS <br> - Sử dụng AWS CLI để upload/download objects | 12/05/2026 | 12/05/2026 | <https://000057.awsstudygroup.com/> |
| 4 | **Lab 8: Database Essentials with Amazon RDS** <br> - Tìm hiểu RDS: supported engines, Multi-AZ, Read Replica <br> - Tạo RDS MySQL instance trong private subnet <br> - Kết nối vào RDS từ EC2 <br> - Tạo Read Replica và thực hiện failover <br> - Cấu hình automated backup và snapshot | 13/05/2026 | 13/05/2026 | <https://000005.awsstudygroup.com/> |
| 5 | **Lab 9: NoSQL Database Essentials with Amazon DynamoDB** <br> - Tìm hiểu DynamoDB: partition key, sort key, GSI, LSI <br> - Tạo DynamoDB table và thực hiện CRUD operations <br> - Tìm hiểu DynamoDB capacity modes (On-demand vs Provisioned) <br> - Sử dụng DynamoDB Streams <br> - Tìm hiểu DAX (DynamoDB Accelerator) | 14/05/2026 | 15/05/2026 | <https://000060.awsstudygroup.com/> |
| 6 | - Ôn tập và tổng hợp kiến thức tuần 4 <br> - So sánh khi nào dùng RDS, khi nào dùng DynamoDB <br> - Thiết kế data model cho một ứng dụng mẫu | 15/05/2026 | 15/05/2026 | |

### Kết quả đạt được tuần 4:

* Sử dụng thành thạo Amazon S3:
  * Quản lý bucket, object permissions, bucket policies
  * Cấu hình versioning để bảo vệ dữ liệu
  * Thiết lập lifecycle rule để tối ưu chi phí lưu trữ
  * Deploy static website lên S3

* Triển khai và quản lý RDS:
  * Tạo RDS instance trong private subnet với đúng security group
  * Cấu hình Multi-AZ để đảm bảo High Availability
  * Tạo Read Replica để scale đọc
  * Thực hành backup và restore từ snapshot

* Làm việc với DynamoDB:
  * Thiết kế data model với partition key và sort key hợp lý
  * Thực hiện các query và scan operations hiệu quả
  * Hiểu sự khác biệt giữa On-demand và Provisioned capacity
  * Cấu hình DynamoDB Streams để xử lý sự kiện
