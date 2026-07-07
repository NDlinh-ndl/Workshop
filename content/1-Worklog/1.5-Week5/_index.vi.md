---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:

* Cấu hình Route 53 cho DNS management và routing policies.
* Bảo vệ ứng dụng web với AWS WAF.
* Mã hóa dữ liệu với AWS Key Management Service (KMS).

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Ôn lại kiến thức Storage và Database tuần trước <br> - Đọc tài liệu về DNS cơ bản và các loại record <br> - Tìm hiểu tổng quan về AWS Security best practices | 18/05/2026 | 18/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Lab 10: Hybrid DNS Management with Amazon Route 53** <br> - Tìm hiểu Route 53: Hosted Zones, Record Types <br> - Cấu hình các Routing Policy: Simple, Weighted, Latency, Failover, Geolocation <br> - Tích hợp Route 53 với ALB và CloudFront <br> - Thiết lập Health Checks <br> - Thực hành DNS failover scenario | 19/05/2026 | 19/05/2026 | <https://000010.awsstudygroup.com/> |
| 4 | **Lab 11: Application Protection with AWS WAF** <br> - Tìm hiểu WAF: Web ACL, Rules, Rule Groups <br> - Tạo Web ACL với AWS Managed Rules <br> - Viết custom rule để block/allow traffic <br> - Gắn WAF vào ALB và CloudFront <br> - Phân tích WAF logs trong CloudWatch | 20/05/2026 | 20/05/2026 | <https://000026.awsstudygroup.com/> |
| 5 | **Lab 12: Encryption with AWS Key Management Service (KMS)** <br> - Tìm hiểu KMS: CMK, Data Key, Envelope Encryption <br> - Tạo KMS key và cấu hình key policy <br> - Mã hóa EBS volume và S3 bucket với KMS <br> - Mã hóa RDS database <br> - Sử dụng KMS với AWS CLI | 21/05/2026 | 22/05/2026 | <https://000033.awsstudygroup.com/> |
| 6 | - Ôn tập và tổng hợp kiến thức tuần 5 <br> - Thiết kế kiến trúc bảo mật cho một ứng dụng web hoàn chỉnh <br> - Ghi chép AWS Security best practices | 22/05/2026 | 22/05/2026 | |

### Kết quả đạt được tuần 5:

* Cấu hình Route 53 thành thạo:
  * Tạo hosted zone và quản lý các DNS record
  * Cấu hình được 5+ loại routing policy khác nhau
  * Thiết lập health check và tự động failover
  * Hiểu cách Route 53 tích hợp với các dịch vụ AWS khác

* Bảo vệ ứng dụng với AWS WAF:
  * Tạo Web ACL với các managed rule groups
  * Viết custom rule để xử lý các mối đe dọa cụ thể
  * Phân tích và điều tra WAF logs
  * Hiểu các loại tấn công phổ biến: SQL injection, XSS, DDoS

* Quản lý mã hóa với KMS:
  * Tạo và quản lý Customer Managed Keys
  * Áp dụng mã hóa at-rest cho EBS, S3, RDS
  * Hiểu cơ chế envelope encryption
  * Cấu hình key rotation tự động
