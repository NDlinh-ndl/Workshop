---
title: "Worklog Tuần 9"
date: 2024-01-01
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:

* Lên ý tưởng và thiết kế kiến trúc cho project thực tế: ITCoach.
* Xác định tech stack, phân tích yêu cầu hệ thống và lập kế hoạch triển khai.
* Thiết kế data model và phân chia công việc cho các tuần tiếp theo.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Brainstorm ý tưởng project <br> - Xác định vấn đề cần giải quyết: nền tảng luyện phỏng vấn IT <br> - Phân tích đối tượng người dùng mục tiêu | 15/06/2026 | 15/06/2026 | |
| 3 | - Xác định tech stack: ReactJS + Lambda + DynamoDB + Cognito + Polly + OpenAI <br> - Thiết kế kiến trúc Serverless tổng thể <br> - Vẽ sơ đồ kiến trúc AWS: CloudFront, API Gateway, Lambda, DynamoDB, S3, SQS, Cognito | 16/06/2026 | 16/06/2026 | |
| 4 | - Thiết kế data model cho 8 bảng DynamoDB: <br>&emsp; + itcoach-users, itcoach-questions, itcoach-sessions <br>&emsp; + itcoach-answers, itcoach-history, itcoach-topics <br>&emsp; + itcoach-quiz-attempts (Spaced Repetition SM-2) <br>&emsp; + itcoach-gamification (XP, level, streak, badge) <br> - Xác định Partition Key, Sort Key, GSI cho từng bảng | 17/06/2026 | 17/06/2026 | |
| 5 | - Thiết kế 8 API endpoint: `/auth`, `/questions`, `/topics`, `/sessions`, `/answers`, `/results`, `/quiz`, `/leaderboard` <br> - Phân tích luồng xử lý bất đồng bộ: Answer -> SQS -> Lambda AI Processor -> OpenAI -> Polly -> DynamoDB <br> - Lên kế hoạch bảo mật: Cognito JWT, WAF, Rate Limiting | 18/06/2026 | 19/06/2026 | |
| 6 | - Lập kế hoạch triển khai chi tiết cho tuần 10, 11, 12 <br> - Phân chia module: IAM, S3, DynamoDB, Cognito, SQS (tuần 10) <br> - Lambda, API Gateway, CloudFront, WAF (tuần 11) <br> - Route 53, ACM, Monitoring, Deploy code (tuần 12) | 19/06/2026 | 19/06/2026 | |

### Kết quả đạt được tuần 9:

* Xác định được bài toán cốt lõi: xây dựng nền tảng luyện phỏng vấn IT sử dụng AI, bao gồm Mock Interview (tự luận + giọng nói), Quiz trắc nghiệm với Spaced Repetition, và hệ thống gamification.

* Thiết kế kiến trúc Serverless hoàn chỉnh trên AWS:
  * Frontend: ReactJS host trên S3, phân phối qua CloudFront
  * Backend: 8 Lambda functions, gọi qua API Gateway (Regional)
  * Xử lý bất đồng bộ: SQS -> Lambda AI Processor -> OpenAI STT/GPT -> Polly TTS
  * Auth: Amazon Cognito User Pool với JWT
  * Domain: itcoach24h.xyz, SSL qua ACM, DNS qua Route 53

* Thiết kế data model DynamoDB cho 8 bảng, xác định rõ:
  * Partition Key và Sort Key phù hợp với access pattern thực tế
  * GSI cần thiết: category-index, userId-index, sessionId-index, xp-index
  * Bảng itcoach-quiz-attempts lưu trạng thái SM-2 (interval, easeFactor, nextReviewDate)

* Lên kế hoạch bảo mật 2 lớp WAF:
  * WAF Global (us-east-1) gắn vào CloudFront
  * WAF Regional (ap-southeast-1) gắn vào API Gateway, có rule riêng bảo vệ endpoint `/auth` khỏi brute-force

* Hoàn thành kế hoạch triển khai 3 tuần tiếp theo, phân chia rõ từng phần theo tài liệu ITCoach Console ClickGuide v14.
