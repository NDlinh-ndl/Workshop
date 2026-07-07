---
title: "Worklog Tuần 11"
date: 2024-01-01
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:

* Tạo và deploy 8 Lambda functions với đúng environment variables và SQS trigger.
* Dựng API Gateway với 8 endpoints, Cognito Authorizer và Throttling.
* Tạo CloudFront distribution và cấu hình 2 Web ACL WAF (Global + Regional).

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | **Phần 7 - Lambda (8 functions)** <br> - Tạo 8 Lambda functions (Python 3.12), gắn role `itcoach-lambda-role` <br> - Deploy placeholder code cho từng function <br> - Cài timeout 30s, memory 256MB <br> - Cấu hình environment variables cho 6 functions cần thiết: answer-handler, ai-processor, result-handler, session-handler, quiz-handler, gamification-handler | 29/06/2026 | 29/06/2026 | |
| 3 | **Phần 7 (tiếp) - SQS Trigger + Phần 8 - API Gateway** <br> - Gắn SQS trigger `itcoach-processing-queue` vào Lambda `itcoach-ai-processor` (batch size 1) <br> - Tạo API Gateway REST API `itcoach-api` (Regional) <br> - Tạo Cognito Authorizer `itcoach-cognito-auth` <br> - Tạo 8 resources và methods theo đúng bảng endpoint <br> - Endpoint `/auth`: Authorization = NONE; 7 endpoint còn lại: `itcoach-cognito-auth` <br> - Bật CORS cho tất cả resources | 30/06/2026 | 30/06/2026 | |
| 4 | **Phần 8 (tiếp) + Phần 9 - Deploy API + CloudFront** <br> - Deploy API lên stage `prod`, lưu Invoke URL <br> - Cấu hình Throttling: Rate 100 req/s, Burst 200 <br> - Tạo CloudFront distribution `itcoach-distribution` (Free plan) <br> - Origin: S3 bucket `itcoach-static-assets`, dùng website endpoint <br> - Default root object: `index.html` <br> - Tạo 2 custom error response: 403/404 -> /index.html (200) cho React Router | 01/07/2026 | 01/07/2026 | |
| 5 | **Phần 10.1 - WAF CloudFront (Global)** <br> - Xác nhận CloudFront đã tự sinh Web ACL `CreatedByCloudFront-...` với 3 managed rule mặc định <br> - Bổ sung custom rule `itcoach-rate-limit`: 2000 req / 5 phút / IP, Action = Block <br> - Kiểm tra thứ tự: 3 managed rule chạy trước rate-limit <br> **Phần 10.2 - WAF API Gateway (Regional)** <br> - Tạo Web ACL `itcoach-api-waf` (scope: API Gateway, region ap-southeast-1) <br> - Gắn vào stage `itcoach-api/prod` <br> - Thêm 3 managed rule groups + rule `itcoach-api-rate-limit` (2000/5min) + rule `itcoach-auth-bruteforce-protect` (20 req / 5 phút / IP, scope-down: URI starts with /auth) | 02/07/2026 | 03/07/2026 | |
| 6 | - Kiểm tra toàn bộ hạ tầng tuần 11 <br> - Test gọi thử API endpoint qua Invoke URL <br> - Xác nhận WAF hoạt động: check WAF & Shield console, tab Requests <br> - Kiểm tra CloudFront distribution đã Enabled <br> - Chuẩn bị thông tin cho tuần 12: Route 53, ACM, deploy code thật | 03/07/2026 | 03/07/2026 | |

### Kết quả đạt được tuần 11:

* Tạo và cấu hình đầy đủ 8 Lambda functions:
  * Gắn đúng IAM role `itcoach-lambda-role` cho tất cả functions
  * Cài environment variables cho từng function theo đúng mapping (REGION, S3 bucket, DynamoDB tables, SQS URL, OpenAI key)
  * Gắn SQS trigger vào `itcoach-ai-processor` với batch size 1 để xử lý từng message
  * Hiểu luồng bất đồng bộ: answer-handler nhận request -> đẩy vào SQS -> ai-processor trigger -> gọi OpenAI -> lưu kết quả + tạo audio Polly

* Dựng API Gateway hoàn chỉnh:
  * 8 endpoints đúng method và Lambda integration
  * Cognito Authorizer hoạt động với JWT từ User Pool
  * Endpoint `/auth` public (NONE), 7 endpoint còn lại yêu cầu token
  * CORS enabled trên tất cả resources
  * Deploy lên stage `prod`, throttling Rate 100 / Burst 200

* Tạo CloudFront distribution:
  * Origin trỏ đúng S3 website endpoint
  * Error pages 403/404 redirect về index.html để React Router hoạt động
  * Ghi nhận domain CloudFront: `d19z6xk3gva030.cloudfront.net`

* Cấu hình 2 Web ACL WAF độc lập:
  * WAF Global (us-east-1): gắn vào CloudFront, 3 managed rule + 1 rate-limit tự tạo
  * WAF Regional (ap-southeast-1): gắn vào API Gateway stage prod, 3 managed rule + rate-limit chung + rule riêng cho `/auth` (20 req/5min để chống brute-force login)
  * Hiểu rõ lý do phải tách 2 WAF: app gọi thẳng API Gateway không qua CloudFront nên WAF Global không lọc được traffic API
