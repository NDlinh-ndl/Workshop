---
title: "Worklog Tuần 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Làm quen với môi trường AWS, tạo tài khoản và thiết lập bảo mật cơ bản.
* Hiểu và thực hành IAM để quản lý quyền truy cập.
* Nắm vững kiến thức nền tảng về VPC và mạng trên AWS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Đọc tài liệu tổng quan về AWS Cloud <br> - Tìm hiểu các mô hình dịch vụ: IaaS, PaaS, SaaS <br> - Tìm hiểu AWS Global Infrastructure (Region, AZ, Edge Location) | 27/04/2026 | 27/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Lab 1: Creating Your First AWS Account** <br> - Tạo tài khoản AWS Free Tier <br> - Thiết lập MFA cho root account <br> - Cài đặt AWS CLI và cấu hình credentials <br> - Khám phá AWS Management Console | 28/04/2026 | 28/04/2026 | <https://000001.awsstudygroup.com/> |
| 4 | **Lab 2: Access Management with AWS IAM** <br> - Tìm hiểu IAM Users, Groups, Roles, Policies <br> - Tạo IAM user với quyền hạn cụ thể <br> - Tạo IAM policy tùy chỉnh <br> - Thực hành principle of least privilege | 29/04/2026 | 29/04/2026 | <https://000002.awsstudygroup.com/> |
| 5 | **Lab 3: Networking Essentials with Amazon VPC** <br> - Tìm hiểu VPC, Subnet (public/private), Route Table <br> - Tìm hiểu Internet Gateway, NAT Gateway <br> - Tìm hiểu Security Group và Network ACL <br> - Tạo VPC với kiến trúc multi-tier | 30/04/2026 | 01/05/2026 | <https://000003.awsstudygroup.com/> |
| 6 | - Ôn tập và tổng hợp kiến thức tuần 2 <br> - Vẽ sơ đồ kiến trúc những gì đã học <br> - Ghi chép các điểm cần lưu ý | 01/05/2026 | 01/05/2026 | |

### Kết quả đạt được tuần 2:

* Tạo thành công tài khoản AWS Free Tier, bật MFA cho root account, cài đặt và cấu hình AWS CLI.

* Hiểu rõ cấu trúc IAM:
  * Phân biệt được User, Group, Role, Policy
  * Tạo được IAM user với quyền hạn giới hạn theo nguyên tắc least privilege
  * Viết được IAM policy JSON tùy chỉnh

* Nắm vững kiến thức VPC:
  * Hiểu sự khác biệt giữa public subnet và private subnet
  * Cấu hình được Route Table, Internet Gateway, NAT Gateway
  * Phân biệt được Security Group (stateful) và Network ACL (stateless)
  * Tạo được VPC từ đầu với kiến trúc 2 tầng (public + private)
