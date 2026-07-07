---
title: "Event 2"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Bài thu hoạch: FCAJ Community Day (27/06/2026)

### Thông tin sự kiện

- **Tên sự kiện:** FCAJ Community Day
- **Thời gian:** Thứ Bảy, 27/06/2026 — 9:00 AM đến 12:00 PM (GMT+7)
- **Địa điểm:** Bitexco Financial Tower, TP. Hồ Chí Minh
- **Tổ chức bởi:** Huỳnh Hoàng Long
- **Số lượng tham dự:** 325 người (Sold Out)
- **Link sự kiện:** https://luma.com/s1ymc95q

### Lịch trình sự kiện

| Thời gian | Nội dung |
| --------- | -------- |
| 8:30 – 9:00 | Ổn định chỗ ngồi |
| 9:00 – 9:25 | Deep Response Engine: From Detection to Autonomous Resolution |
| 9:25 – 9:55 | Voice Agents: Building Human-Like AI Conversations at Scale |
| 9:55 – 10:20 | AWS DevOps Agent: Your Always-Available Operations Teammate |
| 10:20 – 10:45 | AI-Powered Productivity: Workforce Planning For Enterprise |
| 10:45 – 11:30 | Building Secure Private MCP Connection with Amazon Q |

### Nội dung nổi bật

#### Deep Response Engine: From Detection to Autonomous Resolution

- Bức tường phức tạp trong vận hành cloud hiện đại
- Chuyển dịch từ hệ thống dựa trên alert sang hệ thống dựa trên action
- Tổng quan kiến trúc Deep Response Engine
- Live demo: autonomous incident response tự động phát hiện và xử lý sự cố
- Business impact: giảm chi phí và đạt zero-downtime operations

#### Voice Agents: Building Human-Like AI Conversations at Scale

- Tiến hóa từ IVR và chatbot đến AI voice agent
- Những thách thức cốt lõi: latency, accuracy và natural interaction
- **Amazon Nova Sonic**: speech-to-speech foundation model mới của AWS
- Kiến trúc: telephony, streaming, Bedrock, MCP tools
- Enterprise use cases, best practices và live demo thực tế

#### AWS DevOps Agent: Your Always-Available Operations Teammate

- Tổng quan về AWS DevOps Agent
- Giảm MTTD (Mean Time to Detect) và MTTR (Mean Time to Resolve) với AI-driven operations
- Hỗ trợ môi trường multi-cloud và hybrid
- **Bedrock AgentCore** và multi-agent reasoning approach
- Real-world use cases và ECS demo walkthrough

#### AI-Powered Productivity: Workforce Planning For Enterprise

- Những thách thức HR transformation trong doanh nghiệp hiện đại
- Tổng quan Amazon Q và các tính năng HR
- Tăng tốc HR operations với automation
- Workforce analytics và data-driven insights
- Lập kế hoạch nhân sự chiến lược cho doanh nghiệp

#### Building Secure Private MCP Connection with Amazon Q

- Giới thiệu Amazon Q như một AI assistant platform
- **MCP (Model Context Protocol)** và vai trò của nó trong khả năng mở rộng
- Các thách thức bảo mật trong tích hợp MCP
- Cấu hình Amazon Q VPC private connectivity
- Demo và implementation insights thực tế

### Những gì học được

**Về Autonomous Operations:**
- Deep Response Engine cho thấy tương lai của cloud operations là hệ thống tự phát hiện và tự xử lý sự cố mà không cần can thiệp thủ công — giảm đáng kể thời gian phản hồi
- Sự khác biệt rõ ràng giữa alert-driven (chỉ thông báo) và action-driven (tự động xử lý) — hướng đi này sẽ thay đổi cách các team DevOps vận hành hệ thống

**Về Voice AI:**
- Amazon Nova Sonic là bước tiến lớn trong voice AI — xử lý speech-to-speech thay vì pipeline STT → LLM → TTS truyền thống, giúp giảm latency đáng kể
- Kiến trúc voice agent với Bedrock và MCP rất liên quan đến tính năng Mock Interview của ITCoach — tôi đang dùng Polly nhưng có thể nâng cấp lên Nova Sonic sau

**Về DevOps Agent:**
- AWS DevOps Agent với Bedrock AgentCore cho thấy multi-agent reasoning là hướng tiếp cận phù hợp cho các bài toán vận hành phức tạp
- Cách giảm MTTD/MTTR bằng AI thực tế, áp dụng được ngay cho hệ thống CloudWatch Alarms mà tôi đã thiết lập cho ITCoach

**Về MCP và Bảo mật:**
- MCP (Model Context Protocol) là chuẩn mở để kết nối AI với các công cụ bên ngoài — hiểu được tại sao nó đang trở thành tiêu chuẩn ngành
- VPC private connectivity cho MCP giải quyết bài toán bảo mật khi AI cần truy cập dữ liệu nội bộ doanh nghiệp mà không đi qua internet công cộng

### Ứng dụng vào project ITCoach

- Lấy cảm hứng từ Deep Response Engine để cải thiện monitoring của ITCoach: thay vì chỉ tạo CloudWatch Alarm thông báo, có thể dùng Lambda để tự động xử lý một số sự cố thường gặp
- Tham khảo kiến trúc Voice Agent với Amazon Nova Sonic để nâng cấp tính năng Mock Interview — thay thế pipeline Polly TTS hiện tại bằng speech-to-speech end-to-end trong phiên bản sau
- Hiểu rõ hơn về MCP protocol giúp thiết kế tốt hơn cách ITCoach Lambda functions giao tiếp với OpenAI và các external services

### Trải nghiệm tại sự kiện

Event lần này diễn ra đúng vào tuần 11 của chương trình thực tập — thời điểm tôi đang deploy Lambda và API Gateway cho ITCoach. Điều đặc biệt là nội dung của cả 5 talk đều rất liên quan trực tiếp đến những gì tôi đang làm: voice AI, DevOps automation, MCP và bảo mật.

Phần demo live của Deep Response Engine rất ấn tượng — xem một hệ thống tự phát hiện lỗi trong ECS và tự rollback mà không cần người can thiệp khiến tôi nghĩ lại về cách thiết kế monitoring cho ITCoach.

Event sold out với 325 người, không gian tuy nhỏ hơn lần trước nhưng chất lượng các talk rất cao và tập trung hơn vào các chủ đề AI trong cloud operations — phù hợp với giai đoạn mà AI đang được tích hợp vào mọi tầng của hạ tầng.

### Hình ảnh sự kiện

![FCAJ Community Day - June 2026](/images/event21.jpg)
