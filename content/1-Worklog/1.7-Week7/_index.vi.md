---
title: "Worklog Tuần 7"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:

* Xây dựng serverless backend với AWS Lambda và API Gateway.
* Sử dụng AWS Systems Manager để quản lý và vận hành fleet EC2.
* Tìm hiểu AWS Backup để bảo vệ dữ liệu toàn diện.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Ôn lại kiến thức CI/CD và Container tuần trước <br> - Đọc tài liệu về Serverless architecture <br> - Tìm hiểu event-driven architecture patterns | 01/06/2026 | 01/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Lab 16: Serverless Automation with AWS Lambda** <br> - Tìm hiểu Lambda: triggers, execution model, cold start <br> - Viết Lambda function bằng Python/Node.js <br> - Cấu hình Lambda triggers: API Gateway, S3, DynamoDB Streams <br> - Thiết lập environment variables và layers <br> - Giám sát Lambda với CloudWatch Logs và X-Ray | 02/06/2026 | 02/06/2026 | <https://000022.awsstudygroup.com/> |
| 4 | **Lab 17: Remote Server Access with Systems Manager Session Manager** <br> - Tìm hiểu AWS Systems Manager và các tính năng <br> - Cấu hình Session Manager để SSH không cần key pair <br> - Sử dụng SSM Run Command để chạy lệnh hàng loạt <br> - Quản lý Patch Manager cho fleet EC2 <br> - Lưu trữ cấu hình với Parameter Store | 03/06/2026 | 03/06/2026 | <https://000058.awsstudygroup.com/> |
| 5 | **Lab 18: Data Protection with AWS Backup** <br> - Tìm hiểu AWS Backup: Backup Plans, Vaults, Recovery Points <br> - Tạo Backup Plan tự động cho EC2, RDS, EFS, DynamoDB <br> - Cấu hình backup retention và lifecycle <br> - Thực hành restore từ backup <br> - Thiết lập cross-region backup | 04/06/2026 | 05/06/2026 | <https://000013.awsstudygroup.com/> |
| 6 | - Ôn tập và tổng hợp kiến thức tuần 7 <br> - Xây dựng ứng dụng serverless CRUD nhỏ: Lambda + API Gateway + DynamoDB <br> - Thiết lập backup strategy cho toàn bộ môi trường | 05/06/2026 | 05/06/2026 | |

### Kết quả đạt được tuần 7:

* Phát triển serverless với AWS Lambda:
  * Viết và deploy Lambda function xử lý nhiều loại event
  * Tích hợp Lambda với API Gateway tạo RESTful API
  * Kết nối Lambda với DynamoDB và S3
  * Debug và monitor Lambda bằng CloudWatch Logs Insights
  * Hiểu cách tối ưu cold start và memory allocation

* Quản lý hệ thống với AWS Systems Manager:
  * Truy cập EC2 an toàn qua Session Manager không cần mở port 22
  * Chạy được commands trên nhiều instance cùng lúc
  * Tự động patch OS cho fleet server
  * Lưu trữ secrets và config trong Parameter Store

* Thiết lập backup strategy toàn diện:
  * Tạo backup plan tự động với lịch chạy cụ thể
  * Bảo vệ nhiều loại tài nguyên: EC2, RDS, DynamoDB
  * Restore thành công từ backup point
  * Cấu hình cross-region backup để disaster recovery
