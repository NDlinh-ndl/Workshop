---
title: "Worklog Tuần 12"
date: 2024-01-01
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12:

* Cấu hình Route 53, mua domain và gắn SSL Certificate qua ACM.
* Thiết lập SNS + CloudWatch Alarms để giám sát hệ thống.
* Build và deploy code thật (ReactJS + 8 Lambda), xác nhận website chạy tại itcoach24h.xyz.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | **Phần 11 - SNS + CloudWatch** <br> - Tạo SNS Topic `itcoach-alerts` (Standard) <br> - Tạo Email subscription, xác nhận qua email <br> - Tạo 3 CloudWatch Alarms: <br>&emsp; + `itcoach-ai-errors`: Lambda itcoach-ai-processor Errors > 5 / 5 phút <br>&emsp; + `itcoach-api-5xx-errors`: API Gateway 5XXError > 10 / 5 phút <br>&emsp; + `itcoach-sqs-backlog`: SQS ApproximateNumberOfMessagesVisible > 50 / 5 phút <br> - Gắn cả 3 alarm vào SNS topic `itcoach-alerts` | 06/07/2026 | 06/07/2026 | |
| 3 | **Phần 12 - Route 53 + ACM** <br> - Mua domain `itcoach24h.xyz` trên Namecheap (bật Free Domain Privacy, tắt Auto-renew) <br> - Tạo Hosted Zone `itcoach24h.xyz` (Public) trên Route 53, copy 4 NS records về Namecheap Custom DNS <br> - Chuyển Region sang us-east-1 (N. Virginia) <br> - Tạo SSL Certificate trên ACM: `itcoach24h.xyz` + `*.itcoach24h.xyz`, DNS validation, tạo record trong Route 53 <br> - Chờ Certificate chuyển sang Issued | 07/07/2026 | 07/07/2026 | |
| 4 | **Phần 12 (tiếp) - Gắn domain vào CloudFront + DNS Records** <br> - Chuyển Region về ap-southeast-1 <br> - Vào CloudFront `itcoach-distribution`: thêm CNAME `itcoach24h.xyz` và `www.itcoach24h.xyz`, gắn SSL certificate vừa tạo <br> - Tạo 2 A record Alias trong Route 53 trỏ về CloudFront distribution: root domain và www <br> - Chờ DNS đồng bộ, truy cập `https://itcoach24h.xyz` kiểm tra | 08/07/2026 | 08/07/2026 | |
| 5 | **Deploy code thật** <br> - Frontend: chạy `npm run build`, upload toàn bộ `/dist` lên S3 bucket `itcoach-static-assets`, tạo CloudFront Invalidation (`/*`) <br> - Backend: đóng gói 8 Lambda functions thành `.zip`, upload lên từng function qua console <br> - Cập nhật Cognito Callback URL từ `localhost:3000` về `https://itcoach24h.xyz` <br> - Test toàn bộ luồng: đăng ký -> đăng nhập -> quiz -> mock interview -> leaderboard | 09/07/2026 | 10/07/2026 | |
| 6 | - Kiểm tra toàn diện hệ thống lần cuối <br> - Xác nhận 12/12 phần hạ tầng hoàn thành <br> - Nhập dữ liệu mẫu vào `itcoach-questions` và `itcoach-topics` <br> - Kiểm tra CloudWatch Alarms và WAF logs <br> - Ghi chép tổng kết project, vẽ lại sơ đồ kiến trúc hoàn chỉnh | 10/07/2026 | 10/07/2026 | |

### Kết quả đạt được tuần 12:

* Thiết lập giám sát hệ thống với SNS + CloudWatch:
  * SNS topic `itcoach-alerts` nhận email cảnh báo khi có sự cố
  * 3 alarms bao phủ 3 điểm quan trọng nhất: Lambda errors, API 5xx, SQS backlog
  * Hiểu trạng thái "Insufficient data" là bình thường khi chưa có traffic thật

* Cấu hình domain và SSL hoàn chỉnh:
  * Mua và trỏ domain `itcoach24h.xyz` từ Namecheap về Route 53 (4 NS records)
  * Tạo SSL Certificate wildcard (`*.itcoach24h.xyz`) trên ACM us-east-1, xác thực DNS
  * Gắn certificate vào CloudFront, tạo 2 A record Alias (root + www) trỏ về CloudFront

* Deploy code thật và xác nhận hệ thống vận hành:
  * ReactJS build thành công, upload lên S3, CloudFront Invalidation để clear cache
  * 8 Lambda functions chạy code thật (xử lý được quiz, mock interview, gamification)
  * Website truy cập được tại `https://itcoach24h.xyz` với HTTPS

* Hoàn thành 12/12 phần hạ tầng AWS:
  * Stack: Serverless - ReactJS + Lambda + DynamoDB + Cognito + Polly + OpenAI + WAF (CloudFront + API Gateway)
  * Region: ap-southeast-1 (Singapore) | Domain: itcoach24h.xyz
  * API Gateway URL: `https://shyhx5tj6k.execute-api.ap-southeast-1.amazonaws.com/prod`
  * 2 Web ACL WAF hoạt động độc lập bảo vệ cả CloudFront lẫn API Gateway
  * Tổng: 8 Lambda, 8 DynamoDB tables, 8 API endpoints, 2 S3 buckets, 1 Cognito User Pool, 2 SQS queues, 2 WAF Web ACLs, 3 CloudWatch Alarms
