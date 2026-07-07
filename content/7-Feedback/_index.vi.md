---
title: "Chia sẻ, đóng góp ý kiến"
date: 2024-01-01
weight: 7
chapter: false
pre: " <b> 7. </b> "
---

### Đánh giá chung

**1. Môi trường học tập và làm việc**

Môi trường của First Cloud Journey - AWS Study Group rất cởi mở và thực chiến. Toàn bộ chương trình được thiết kế theo hướng hands-on — không chỉ đọc lý thuyết mà phải tự tay làm trên AWS Console, tự debug khi gặp lỗi, tự tìm cách giải quyết.

Điều tôi ấn tượng nhất là không khí cộng đồng: mọi người chia sẻ kinh nghiệm thực tế, hỗ trợ nhau qua group, không ai bị bỏ lại phía sau khi gặp khó khăn kỹ thuật. Hai sự kiện FCAJ Community Day tại Bitexco tháng 5 và tháng 6 năm 2026 cũng tạo thêm cơ hội kết nối với cộng đồng AWS Việt Nam rộng lớn hơn.

**2. Sự hỗ trợ từ mentor và cộng đồng**

Tài liệu hướng dẫn trên cloudjourney.awsstudygroup.com được chuẩn bị rất kỹ lưỡng, có ảnh chụp màn hình từng bước, dễ theo dõi ngay cả khi giao diện AWS thay đổi. Khi gặp lỗi không có trong tài liệu — như WAF block nhầm request, CloudFront cache cũ, SQS trigger không hoạt động — tôi phải tự tìm hiểu qua CloudWatch Logs và AWS documentation, điều này thực ra giúp tôi học sâu hơn nhiều so với chỉ làm theo hướng dẫn.

Cộng đồng AWS Study Group trên Facebook cũng là nguồn hỗ trợ quan trọng khi có câu hỏi kỹ thuật cụ thể.

**3. Sự phù hợp giữa chương trình và thực tế nghề nghiệp**

Lộ trình 12 tuần được thiết kế hợp lý: 8 tuần học các dịch vụ AWS cốt lõi qua 21 labs có thứ tự từ nền tảng đến nâng cao, sau đó 4 tuần áp dụng vào dự án thực tế. Cách tiếp cận này giúp tôi không chỉ biết cách dùng từng dịch vụ riêng lẻ mà còn hiểu cách kết hợp chúng thành một hệ thống hoàn chỉnh.

Project ITCoach là phần tôi học được nhiều nhất: từ thiết kế kiến trúc Serverless, chọn đúng dịch vụ AWS cho từng bài toán, xử lý các vấn đề thực tế khi deploy, đến quản lý chi phí và bảo mật hệ thống production.

**4. Cơ hội học hỏi và phát triển kỹ năng**

Sau 12 tuần, tôi đã có thể:
- Thiết kế và triển khai kiến trúc Serverless từ đầu trên AWS
- Viết và debug Lambda functions, cấu hình API Gateway với Cognito auth
- Thiết kế DynamoDB data model cho ứng dụng thực tế
- Cấu hình CloudFront, WAF, Route 53, ACM
- Đọc CloudWatch Logs để trace lỗi trong production
- Quản lý chi phí AWS và nhận biết các dịch vụ có thể tốn tiền ngoài dự kiến

Đây là những kỹ năng tôi không thể học được chỉ từ sách vở hay khóa học online thông thường.

**5. Văn hóa cộng đồng**

FCAJ có văn hóa chia sẻ tích cực. Các buổi Community Day không chỉ là nơi nghe talk mà còn là cơ hội nhìn thấy người đi trước đang dùng AWS như thế nào trong công việc thực tế — từ autonomous incident response đến voice AI, từ multi-agent systems đến MCP security. Điều này giúp tôi hiểu rõ hơn mình đang học để làm gì và sẽ áp dụng vào đâu.

**6. Chương trình và lộ trình học**

Chương trình có độ khó tăng dần hợp lý. Tuy nhiên, 21 labs trong 8 tuần là khá dày — trung bình 3 labs/tuần, mỗi lab cần 1-2 tiếng để đọc, làm và hiểu. Những tuần đầu còn quen dần với AWS Console, nên tốc độ chậm hơn. Tôi nghĩ việc phân bổ thêm thời gian cho các labs phức tạp (EKS, SageMaker) sẽ giúp học sâu hơn thay vì phải chạy theo tiến độ.

---

### Điều hài lòng nhất

Hoàn thành project ITCoach và thấy website chạy thật tại `https://itcoach24h.xyz` với HTTPS, WAF protection, CloudWatch monitoring — tất cả những gì tôi đã build từ tuần 9 đến tuần 12. Đây không phải demo hay mockup mà là hệ thống thật đang chạy trên AWS.

### Điều chương trình nên cải thiện

Phần documentation cho một số labs chưa cập nhật kịp với giao diện mới của AWS Console — đặc biệt là Cognito (giao diện mới khác hoàn toàn wizard cũ) và CloudFront (workflow tạo distribution đã thay đổi). Tôi mất khá nhiều thời gian đối chiếu giữa tài liệu cũ và giao diện mới để tìm đúng option cần chọn.

### Có khuyên bạn bè tham gia không?

Có, đặc biệt với những bạn muốn vào vị trí Cloud Engineer, DevOps, hoặc Backend Developer với kinh nghiệm AWS. Chương trình cho trải nghiệm thực tế mà các khóa học có chứng chỉ thông thường không có được.

### Đề xuất

- Cập nhật ảnh chụp màn hình trong tài liệu hướng dẫn theo giao diện AWS mới nhất
- Thêm phần "Common Errors & Troubleshooting" cho mỗi lab — những lỗi hay gặp và cách xử lý
- Có thể mở rộng phase project (tuần 9-12) thêm 1-2 tuần để có thời gian hoàn thiện và test kỹ hơn
- Tổ chức thêm buổi demo day cuối chương trình để các học viên trình bày project của mình
