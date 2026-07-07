---
title: "Worklog Tuần 6"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Tự động hóa infrastructure với AWS CloudFormation (Infrastructure as Code).
* Xây dựng CI/CD pipeline với AWS CodePipeline.
* Containerize ứng dụng với Docker và deploy lên Amazon ECS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Ôn lại kiến thức Networking và Security tuần trước <br> - Đọc tài liệu về Infrastructure as Code (IaC) concepts <br> - Tìm hiểu về CI/CD và DevOps practices | 25/05/2026 | 25/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Lab 13: Infrastructure as Code with AWS CloudFormation** <br> - Tìm hiểu CloudFormation: Templates, Stacks, Change Sets <br> - Viết CloudFormation template tạo VPC + EC2 + RDS <br> - Sử dụng Parameters, Mappings, Conditions, Outputs <br> - Cập nhật stack với Change Set <br> - Rollback khi deployment thất bại | 26/05/2026 | 26/05/2026 | <https://000037.awsstudygroup.com/> |
| 4 | **Lab 14: CI/CD Pipeline with AWS CodePipeline** <br> - Tìm hiểu CodeCommit, CodeBuild, CodeDeploy, CodePipeline <br> - Tạo repository trên CodeCommit <br> - Cấu hình CodeBuild để build và test ứng dụng <br> - Tạo pipeline tự động deploy lên EC2 <br> - Trigger pipeline khi có code push | 27/05/2026 | 27/05/2026 | <https://000017.awsstudygroup.com/> |
| 5 | **Lab 15: Containerization with Docker và Amazon ECS** <br> - Cài Docker và build Docker image <br> - Push image lên Amazon ECR <br> - Tạo ECS Cluster (Fargate) <br> - Tạo Task Definition và Service <br> - Cấu hình ALB với ECS service <br> - Cập nhật container image qua rolling deployment | 28/05/2026 | 29/05/2026 | <https://000016.awsstudygroup.com/> |
| 6 | - Ôn tập và tổng hợp kiến thức tuần 6 <br> - Kết hợp CodePipeline với ECS để tạo pipeline hoàn chỉnh <br> - So sánh deploy trên EC2 vs ECS | 29/05/2026 | 29/05/2026 | |

### Kết quả đạt được tuần 6:

* Viết CloudFormation template thành thạo:
  * Tạo được kiến trúc multi-tier (VPC + EC2 + RDS) bằng code
  * Sử dụng Parameters để tạo template tái sử dụng
  * Thực hiện stack update an toàn qua Change Set
  * Hiểu vòng đời của một CloudFormation stack

* Xây dựng CI/CD pipeline với CodePipeline:
  * Thiết lập pipeline 3 giai đoạn: Source → Build → Deploy
  * Cấu hình CodeBuild với buildspec.yml
  * Tự động deploy lên EC2 khi có commit mới
  * Cài đặt manual approval step trước khi deploy production

* Triển khai container lên Amazon ECS:
  * Build và push Docker image lên ECR
  * Tạo ECS service chạy trên Fargate (serverless)
  * Cấu hình health check và auto-recovery
  * Thực hiện rolling deployment không có downtime
