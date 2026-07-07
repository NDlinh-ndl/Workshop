---
title: "Worklog Tuần 8"
date: 2024-01-01
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:

* Triển khai Kubernetes trên AWS với Amazon EKS.
* Xây dựng Data Lake và phân tích dữ liệu với các dịch vụ AWS Analytics.
* Tìm hiểu Machine Learning trên AWS với Amazon SageMaker.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Ôn lại kiến thức Serverless và Operations tuần trước <br> - Đọc tài liệu về Kubernetes concepts: Pod, Deployment, Service, Ingress <br> - Tìm hiểu tổng quan về Data Analytics trên AWS | 08/06/2026 | 08/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Lab 19: Getting Started with Amazon EKS** <br> - Cài đặt eksctl, kubectl và cấu hình <br> - Tạo EKS cluster với managed node group <br> - Deploy ứng dụng lên EKS bằng kubectl <br> - Cấu hình ALB Ingress Controller <br> - Thiết lập Horizontal Pod Autoscaler (HPA) <br> - Quản lý secrets với Kubernetes Secrets và AWS Secrets Manager | 09/06/2026 | 09/06/2026 | <https://000126.awsstudygroup.com/> |
| 4 | **Lab 20: Data Lake Fundamentals on AWS** <br> - Tìm hiểu kiến trúc Data Lake trên AWS <br> - Tạo Data Lake với Amazon S3 làm storage layer <br> - Sử dụng AWS Glue để catalog và ETL data <br> - Query data bằng Amazon Athena (serverless SQL) <br> - Visualize kết quả với Amazon QuickSight <br> - Tìm hiểu AWS Lake Formation | 10/06/2026 | 10/06/2026 | <https://000035.awsstudygroup.com/> |
| 5 | **Lab 21: Machine Learning with Amazon SageMaker** <br> - Tìm hiểu SageMaker: Studio, Notebooks, Training Jobs <br> - Khởi chạy SageMaker Studio <br> - Chuẩn bị và explore dataset với Jupyter Notebook <br> - Train ML model với built-in algorithm (XGBoost) <br> - Deploy model thành real-time endpoint <br> - Gọi endpoint để thực hiện predictions | 11/06/2026 | 12/06/2026 | <https://000200.awsstudygroup.com/> |
| 6 | - Ôn tập và tổng hợp toàn bộ kiến thức 7 tuần học labs <br> - Vẽ kiến trúc AWS hoàn chỉnh cho một ứng dụng production <br> - Chuẩn bị cho giai đoạn 2: thiết kế project ITCoach | 12/06/2026 | 12/06/2026 | |

### Kết quả đạt được tuần 8:

* Triển khai ứng dụng trên Amazon EKS:
  * Tạo EKS cluster và quản lý node groups
  * Deploy, scale và update ứng dụng containerized
  * Cấu hình ALB Ingress để expose ứng dụng ra ngoài
  * Thiết lập HPA để tự động scale pods theo traffic
  * Hiểu sự khác biệt giữa ECS và EKS, khi nào nên dùng gì

* Xây dựng Data Lake và phân tích dữ liệu:
  * Thiết kế kiến trúc Data Lake: Raw → Processed → Curated
  * Tạo Glue Crawler để tự động catalog data
  * Viết Glue ETL job để transform data
  * Query data bằng Athena với cú pháp SQL tiêu chuẩn
  * Tạo QuickSight dashboard để visualize insights

* Bước đầu với Machine Learning trên SageMaker:
  * Làm quen với SageMaker Studio IDE
  * Thực hành full ML workflow: data → train → evaluate → deploy
  * Train model với XGBoost trên SageMaker managed infrastructure
  * Deploy model và gọi inference endpoint từ ứng dụng

* **Tổng kết 7 tuần học labs:**
  * Nắm vững các dịch vụ AWS cốt lõi: EC2, VPC, S3, RDS, IAM
  * Có thể thiết kế kiến trúc 3-tier application trên AWS
  * Thực hành được CI/CD pipeline hoàn chỉnh
  * Hiểu các best practices về security, reliability, performance
  * Hoàn thành 21 hands-on labs từ cơ bản đến nâng cao
