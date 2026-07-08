---
title: "Event 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Bài thu hoạch: FCAJ Community Day (23/05/2026)

### Thông tin sự kiện

- **Tên sự kiện:** FCAJ Community Day
- **Thời gian:** Thứ Bảy, 23/05/2026 — 9:00 AM đến 12:00 PM (GMT+7)
- **Địa điểm:** Bitexco Financial Tower, Tầng 26, TP. Hồ Chí Minh
- **Tổ chức bởi:** Huỳnh Hoàng Long, Thien Lu, Trần Đại Vĩ
- **Số lượng tham dự:** 399 người
- **Link sự kiện:** https://luma.com/ubaur0y5

### Lịch trình sự kiện

| Thời gian | Nội dung | Diễn giả |
| --------- | -------- | --------- |
| 8:30 – 9:00 | Ổn định chỗ ngồi tại tầng 26 | |
| 9:00 – 9:30 | Context Is Everything: Making AI Actually Work for You | Tinh Truong |
| 9:30 – 9:45 | Friendly AI Assistant with Amazon Q | Anh Pham |
| 9:45 – 10:25 | From Edge To Origin: CloudFront as Your Foundation | Thinh Nguyen |
| 10:25 – 10:55 | 36 hrs with LotusHacks – Building UTMorpho from Idea to Reality | Team VIB |
| 10:55 – 11:00 | Break | |
| 11:00 – 11:30 | Non-Determinism of "Deterministic" LLM Settings | Duc Dao |
| 11:30 – 12:00 | Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring | Vy Lam |

### Nội dung nổi bật

#### Context Is Everything: Making AI Actually Work for You — Tinh Truong

- Lý do AI thất bại khi thiếu context và "context" thực sự có nghĩa là gì
- Từ prompts đến memory: AI đang tiến hóa như thế nào (khái niệm Second AI Brain)
- Context tốt hơn dẫn đến kết quả tốt hơn — tư duy thực hành và mẹo hay
- Career insights và cách sinh viên có thể bắt đầu xây dựng với AI

#### Friendly AI Assistant with Amazon Q — Anh Pham

- **Quick Chat Agent**: AI assistant giúp khám phá dữ liệu và phân tích insights
- **Quick Flows**: Tạo intelligent workflows bằng ngôn ngữ tự nhiên, không cần code
- **Quick Spaces**: Không gian cộng tác biến insights cá nhân thành kiến thức nhóm
- **Quick Sight**: Xây dựng dashboard và báo cáo từ raw data bằng ngôn ngữ tự nhiên

#### From Edge To Origin: CloudFront as Your Foundation — Thinh Nguyen

- Amazon CloudFront cho mọi loại workload
- Tối ưu chi phí với Amazon CloudFront
- Các khả năng bảo mật của CloudFront
- Tăng cường độ tin cậy và hiệu suất với Amazon CloudFront

#### 36 hrs with LotusHacks – Building UTMorpho — Team VIB

- Hành trình từ zero đến ý tưởng trong 36 giờ hackathon
- Xác định vấn đề và định hình sản phẩm UTMorpho
- Xây dựng dưới áp lực — những thách thức, thất bại và điểm bước ngoặt
- Demo sản phẩm UTMorpho và bài học rút ra

#### Non-Determinism of "Deterministic" LLM Settings — Duc Dao

- Cách LLM chọn token tiếp theo
- Giả định: Temperature=0 đảm bảo tính xác định
- Thực tế: Inference optimizations phá vỡ giả định này
- Tác động thực tế và chiến lược giảm thiểu

#### Enterprise-Grade Multi-Agent System: Startup Credit Scoring — Vy Lam

- Sự không tương thích cấu trúc giữa hệ thống ngân hàng và dữ liệu startup
- Single Agent: khi nào nên dùng và không nên dùng
- Mô hình Multi-Agent và Blueprint của Virtual Credit Committee
- Guardrails, Compliance và ROI vận hành

### Những gì học được

**Về AI và Context:**
- Hiểu rằng chất lượng output của AI phụ thuộc trực tiếp vào chất lượng context đưa vào — "garbage in, garbage out" vẫn đúng với AI
- Amazon Q với các tính năng Quick Chat, Flows, Spaces, Sight cho thấy AI đang được tích hợp sâu vào toàn bộ workflow doanh nghiệp chứ không chỉ là công cụ chat

**Về CloudFront:**
- CloudFront không chỉ là CDN đơn thuần mà là một lớp nền tảng bảo mật và tối ưu hiệu suất toàn diện — kiến thức này rất liên quan đến project ITCoach tôi đang triển khai
- Cách CloudFront giúp giảm chi phí băng thông và tăng tốc độ phản hồi cho người dùng cuối

**Về LLM và tính xác định:**
- Nhận ra rằng Temperature=0 không đảm bảo output hoàn toàn giống nhau do các tối ưu hóa inference ở tầng phần cứng — quan trọng khi thiết kế hệ thống AI cần reproducibility
- Các chiến lược giảm thiểu non-determinism trong production systems

**Về Multi-Agent Systems:**
- Kiến trúc multi-agent phù hợp cho các bài toán phức tạp cần nhiều loại reasoning khác nhau
- Guardrails và compliance là yếu tố không thể bỏ qua khi triển khai AI vào lĩnh vực tài chính

### Ứng dụng vào project ITCoach

- Áp dụng ngay tư duy "context is everything" vào thiết kế prompt cho Lambda AI Processor — cung cấp đủ context về câu hỏi, level ứng viên và tiêu chí đánh giá trước khi gọi OpenAI
- Cấu hình CloudFront tốt hơn cho ITCoach dựa trên những gì học được: cache behavior, security headers, cost optimization
- Xem xét kiến trúc multi-agent cho tính năng đánh giá phỏng vấn phức tạp hơn trong các phiên bản tương lai

### Trải nghiệm tại sự kiện

Đây là lần đầu tôi tham dự một community day quy mô lớn trong cộng đồng AWS Việt Nam với gần 400 người tham dự tại Bitexco Financial Tower tầng 26. Không khí sự kiện rất sôi động và chuyên nghiệp.

Điều ấn tượng nhất là phần chia sẻ của Team VIB về LotusHacks — nghe một team sinh viên kể lại hành trình xây dựng sản phẩm trong 36 giờ, từ zero đến demo thật, rất truyền cảm hứng. Tôi cũng đang trong giai đoạn xây dựng ITCoach và cảm nhận được sự tương đồng trong những khó khăn kỹ thuật mà họ gặp phải.

Phần Q&A sau mỗi talk tạo cơ hội hỏi trực tiếp các diễn giả những câu hỏi cụ thể — tôi đã hỏi về cách xử lý non-determinism trong hệ thống production và nhận được phản hồi rất thực tế.

### Hình ảnh sự kiện

![FCAJ Community Day - May 2026](/images/event12.jpg)
