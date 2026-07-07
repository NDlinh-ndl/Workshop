---
title: "Worklog Tuần 10"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:

* Dựng nền tảng hạ tầng AWS cho project ITCoach: IAM, S3, DynamoDB, Cognito, SQS.
* Tạo đầy đủ 8 bảng DynamoDB với đúng key schema và GSI theo thiết kế.
* Hoàn thành phần base infrastructure sẵn sàng cho Lambda và API Gateway tuần sau.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | **Phần 1 - IAM Role** <br> - Tạo IAM Role `itcoach-lambda-role` <br> - Gắn 6 managed policies: AWSLambdaBasicExecutionRole, AmazonDynamoDBFullAccess, AmazonS3FullAccess, AmazonSQSFullAccess, AmazonPollyFullAccess, CloudWatchFullAccess | 22/06/2026 | 22/06/2026 | |
| 3 | **Phần 2 + 3 - S3 Buckets** <br> - Tạo bucket `itcoach-static-assets` (public, static website hosting: index.html) <br> - Tạo bucket `itcoach-audio-upload` (private, cấu hình CORS cho phép GET/PUT/POST/DELETE) | 23/06/2026 | 23/06/2026 | |
| 4 | **Phần 4 - DynamoDB (8 bảng, On-demand)** <br> - Tạo 8 bảng: users, questions, sessions, answers, history, topics, quiz-attempts, gamification <br> - Tạo GSI: category-index (questions), userId-index (sessions), sessionId-index (answers), xp-index (gamification: type+xp) <br> - Bảng topics: PK=specialty, SK=topicId <br> - Bảng quiz-attempts: PK=userId, SK=questionId <br> - Bảng history: PK=userId, SK=timestamp | 24/06/2026 | 24/06/2026 | |
| 5 | **Phần 5 + 6 - Cognito + SQS** <br> - Tạo Cognito User Pool, App Client `itcoach-web-client` (SPA), sign-in bằng Email, required attribute: name <br> - Lưu User Pool ID và App Client ID <br> - Tạo SQS DLQ `itcoach-dlq` trước <br> - Tạo queue chính `itcoach-processing-queue`: visibility timeout 300s, encryption bật, gắn DLQ (max receives 3) <br> - Lưu Queue URL | 25/06/2026 | 26/06/2026 | |
| 6 | - Kiểm tra lại toàn bộ hạ tầng tuần 10 <br> - Xác nhận tất cả 8 bảng DynamoDB đã có đúng key schema và GSI <br> - Test Cognito sign-up/sign-in thử nghiệm <br> - Chuẩn bị danh sách thông tin cần lưu cho tuần 11 | 26/06/2026 | 26/06/2026 | |

### Kết quả đạt được tuần 10:

* Tạo thành công IAM Role `itcoach-lambda-role` với đủ 6 permissions cần thiết cho toàn bộ Lambda functions.

* Dựng 2 S3 bucket đúng cấu hình:
  * `itcoach-static-assets`: public access, static website hosting enabled, index/error document = index.html
  * `itcoach-audio-upload`: private, CORS policy cho phép upload audio từ browser

* Tạo đầy đủ 8 bảng DynamoDB với capacity mode On-demand:
  * Xác định đúng Partition Key và Sort Key theo access pattern thực tế
  * Tạo 4 GSI: category-index, userId-index, sessionId-index, xp-index (type String + xp Number)
  * Hiểu rõ lý do thiết kế: bảng gamification dùng field `type="USER"` để nhóm tất cả user vào 1 partition, sort theo xp để làm leaderboard

* Cấu hình Cognito User Pool:
  * App type: Single-page application (SPA)
  * Sign-in: Email
  * Required attribute: name
  * Lưu User Pool ID (`ap-southeast-1_Z4aYtoxGr`) và App Client ID

* Tạo SQS queue theo đúng thứ tự (DLQ trước, queue chính sau):
  * DLQ: `itcoach-dlq`
  * Queue chính: `itcoach-processing-queue`, visibility 300s, encryption enabled, gắn DLQ max 3 lần retry
  * Lưu Queue URL để cấu hình Lambda environment variable tuần sau
