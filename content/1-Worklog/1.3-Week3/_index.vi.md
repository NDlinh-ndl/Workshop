---
title: "Worklog Tuần 3"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Thành thạo EC2 — dịch vụ compute cốt lõi của AWS.
* Hiểu và cấu hình Auto Scaling để đảm bảo tính sẵn sàng cao.
* Sử dụng CloudWatch để giám sát tài nguyên và thiết lập cảnh báo.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Ôn lại kiến thức VPC tuần trước <br> - Đọc tài liệu về EC2: instance types, pricing model, AMI <br> - Tìm hiểu EBS volume types và use case | 04/05/2026 | 04/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Lab 4: Compute Essentials with Amazon EC2** <br> - Khởi chạy EC2 instance trong VPC đã tạo <br> - Kết nối SSH vào instance <br> - Gắn và mount EBS volume <br> - Tạo AMI từ instance đang chạy <br> - Tìm hiểu Elastic IP | 05/05/2026 | 05/05/2026 | <https://000004.awsstudygroup.com/> |
| 4 | **Lab 5: Scaling Applications with EC2 Auto Scaling** <br> - Tìm hiểu Launch Template <br> - Tạo Auto Scaling Group <br> - Cấu hình Scaling Policy (Target Tracking, Step Scaling) <br> - Tích hợp với Application Load Balancer <br> - Kiểm tra scale-out/scale-in | 06/05/2026 | 06/05/2026 | <https://000006.awsstudygroup.com/> |
| 5 | **Lab 6: Monitoring with Amazon CloudWatch** <br> - Tìm hiểu CloudWatch Metrics, Logs, Alarms, Dashboards <br> - Tạo CloudWatch Alarm cho CPU utilization <br> - Cài đặt CloudWatch Agent trên EC2 <br> - Tạo Dashboard tổng hợp <br> - Tích hợp Alarm với Auto Scaling | 07/05/2026 | 08/05/2026 | <https://000008.awsstudygroup.com/> |
| 6 | - Ôn tập và tổng hợp kiến thức tuần 3 <br> - Thử nghiệm stress test để quan sát Auto Scaling hoạt động <br> - Ghi chép lại các bài học kinh nghiệm | 08/05/2026 | 08/05/2026 | |

### Kết quả đạt được tuần 3:

* Thành thạo Amazon EC2:
  * Khởi chạy instance với đúng instance type cho từng workload
  * Kết nối SSH bằng key pair và Session Manager
  * Quản lý EBS volume: tạo, gắn, mount, resize
  * Tạo và sử dụng AMI làm template

* Cấu hình được Auto Scaling hoàn chỉnh:
  * Tạo Launch Template với user data script
  * Thiết lập scaling policy dựa trên CPU và request count
  * Tích hợp với ALB để phân phối traffic
  * Quan sát scale-out khi tải tăng và scale-in khi tải giảm

* Giám sát hệ thống với CloudWatch:
  * Tạo được custom metric từ CloudWatch Agent
  * Thiết lập alarm tự động trigger scaling action
  * Xây dựng dashboard theo dõi sức khỏe hệ thống
