---
title: "Tự đánh giá"
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

Trong suốt thời gian thực tập tại **First Cloud Journey - AWS Study Group** từ **11/08/2025** đến **24/10/2025**, tôi đã có cơ hội học hỏi, thực hành và áp dụng kiến thức AWS vào một dự án thực tế.

Trong 8 tuần đầu (tuần 2–8), tôi tập trung học và thực hành 21 labs trên nền tảng cloudjourney.awsstudygroup.com, đi từ các dịch vụ nền tảng như IAM, VPC, EC2 đến các chủ đề nâng cao như EKS, Serverless, Data Lake và SageMaker. Trong 4 tuần tiếp theo (tuần 9–12), tôi thiết kế và triển khai hoàn chỉnh dự án **ITCoach** — một nền tảng luyện phỏng vấn IT sử dụng AI — trên kiến trúc Serverless AWS, bao gồm 8 Lambda functions, 8 DynamoDB tables, API Gateway, CloudFront, WAF, Cognito, SQS, Route 53 và ACM. Website hiện đang vận hành tại https://itcoach24h.xyz.

Qua quá trình thực tập, tôi không chỉ nâng cao kỹ năng kỹ thuật về AWS mà còn rèn luyện được tư duy thiết kế hệ thống, thói quen làm tài liệu và khả năng tự giải quyết vấn đề khi gặp lỗi thực tế.

Để phản ánh khách quan quá trình thực tập, tôi xin tự đánh giá dựa trên các tiêu chí dưới đây:

| STT | Tiêu chí | Mô tả | Tốt | Khá | Trung bình |
| --- | -------- | ----- | --- | --- | ---------- |
| 1 | **Kiến thức và kỹ năng chuyên môn** | Hoàn thành 21 AWS labs; thiết kế và deploy thành công hệ thống ITCoach 12 phần trên AWS Serverless | ✅ | ☐ | ☐ |
| 2 | **Khả năng học hỏi** | Tiếp thu nhanh các dịch vụ AWS từ cơ bản đến nâng cao; tự tìm hiểu thêm ngoài tài liệu hướng dẫn khi gặp vấn đề thực tế | ✅ | ☐ | ☐ |
| 3 | **Chủ động** | Tự lên kế hoạch học tập theo tuần; chủ động đề xuất ý tưởng và kiến trúc cho dự án ITCoach mà không chờ chỉ định | ✅ | ☐ | ☐ |
| 4 | **Tinh thần trách nhiệm** | Hoàn thành đầy đủ các công việc đề ra mỗi tuần; code thật đã build và deploy, hệ thống vận hành ổn định | ✅ | ☐ | ☐ |
| 5 | **Kỷ luật** | Nhìn chung tuân thủ lịch học và kế hoạch đề ra; đôi khi còn trễ deadline trong một số task nhỏ | ☐ | ✅ | ☐ |
| 6 | **Tính cầu tiến** | Sẵn sàng tìm hiểu lại khi làm sai; tự debug khi Lambda lỗi, WAF block nhầm hoặc CloudFront chưa hoạt động đúng | ✅ | ☐ | ☐ |
| 7 | **Giao tiếp** | Trình bày được kiến trúc hệ thống và worklog rõ ràng; khả năng diễn đạt bằng tiếng Anh kỹ thuật còn cần cải thiện | ☐ | ✅ | ☐ |
| 8 | **Hợp tác nhóm** | Tích cực trao đổi trong cộng đồng AWS Study Group; chia sẻ kinh nghiệm khi gặp lỗi thực tế | ✅ | ☐ | ☐ |
| 9 | **Ứng xử chuyên nghiệp** | Tôn trọng môi trường học tập; giữ thái độ tích cực khi gặp khó khăn kỹ thuật | ✅ | ☐ | ☐ |
| 10 | **Tư duy giải quyết vấn đề** | Xử lý được các vấn đề thực tế: WAF block nhầm request, CORS lỗi, Lambda timeout, SQS message không được consume; tuy nhiên đôi khi mất nhiều thời gian tìm nguyên nhân | ☐ | ✅ | ☐ |
| 11 | **Đóng góp vào dự án** | Là người thiết kế kiến trúc và triển khai toàn bộ hạ tầng ITCoach từ đầu đến cuối; sản phẩm thực sự vận hành tại domain thật | ✅ | ☐ | ☐ |
| 12 | **Tổng thể** | Hoàn thành mục tiêu thực tập: nắm vững AWS, xây dựng được sản phẩm thực tế từ thiết kế đến vận hành | ✅ | ☐ | ☐ |

### Điểm mạnh

* Khả năng tiếp thu kiến thức kỹ thuật nhanh và áp dụng vào thực tế ngay trong cùng tuần học.
* Tư duy hệ thống tốt: biết cách thiết kế kiến trúc phù hợp với yêu cầu bài toán thay vì chỉ làm theo mẫu có sẵn.
* Kiên trì khi gặp lỗi kỹ thuật — không bỏ cuộc khi WAF chặn nhầm, SQS không trigger hay CloudFront cache cũ.
* Có tư duy về bảo mật ngay từ giai đoạn thiết kế: phân tách 2 lớp WAF, rate-limit riêng cho endpoint nhạy cảm `/auth`.

### Cần cải thiện

* Kỷ luật thời gian: cần tuân thủ deadline nghiêm hơn, tránh để task nhỏ dồn vào cuối tuần.
* Kỹ năng tiếng Anh kỹ thuật: cần rèn luyện thêm khả năng trình bày và viết tài liệu kỹ thuật bằng tiếng Anh rõ ràng hơn.
* Tư duy debug có hệ thống: thay vì thử từng thứ một, cần học cách đọc CloudWatch Logs và trace lỗi từ gốc nhanh hơn.
* Cost awareness: cần chú ý hơn đến chi phí khi thiết kế hệ thống, đặc biệt khi dùng nhiều dịch vụ có tính phí theo request như WAF.
