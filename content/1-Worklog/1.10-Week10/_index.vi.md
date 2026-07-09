---
title: 'Worklog Tuần 10'
date: 2026-06-22
weight: 10
chapter: false
pre: ' <b> 1.10. </b> '
---

---

### Mục tiêu tuần 10:

- Xây dựng quy trình phản ứng sự cố tự động (Auto-remediation) ứng dụng kiến trúc Serverless.
- Lập trình các kịch bản tự động hóa (Automation Scripts) bằng AWS Lambda để vô hiệu hóa các mối đe dọa ngay khi bị phát hiện.
- Ứng dụng Event-driven architecture thông qua Amazon EventBridge và Step Functions để điều phối quy trình xử lý sự cố.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                              | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                              |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ | --------------- | ------------------------------------------- |
| 2   | -Cấu hình Kênh Cảnh báo:** <br>&emsp; + Triển khai Amazon SNS Topic làm kênh trung chuyển thông báo bảo mật. <br>&emsp; + Đăng ký (Subscribe) các email của đội dự án và xác thực endpoint.                                                                       | 22/06/2026   | 22/06/2026      | https://docs.aws.amazon.com/sns/            |
| 3   | - Xử lý Cảnh báo tự động (Lambda #1):** <br>&emsp; + Thiết lập IAM Execution Role với quyền hạn tối thiểu. <br>&emsp; + Viết script Python (Boto3) phân tích cú pháp (parse) GuardDuty Findings, lọc các cảnh báo mức High/Medium và đẩy payload sang SNS.                               | 23/06/2026   | 23/06/2026      | https://docs.aws.amazon.com/lambda/         |
| 4   | - Cách ly Mạng Tự động (Lambda #2):** <br>&emsp; + Cấp quyền `ec2:AuthorizeSecurityGroupIngress` cho Lambda. <br>&emsp; + Phát triển kịch bản tự động lấy IP độc hại từ GuardDuty finding và inject luật `Deny` vào Security Group của EC2 bị nhắm mục tiêu.                                          | 24/06/2026   | 24/06/2026      | https://docs.aws.amazon.com/ec2/            |
| 5   | - Định tuyến Sự kiện (Event Routing):** <br>&emsp; + Cấu hình EventBridge Rules lắng nghe các sự kiện bất thường từ GuardDuty. <br>&emsp; + Kích hoạt Lambda tương ứng. <br>&emsp; + Inject GuardDuty Sample Findings để kiểm thử toàn trình (End-to-end testing). | 25/06/2026   | 25/06/2026      | https://docs.aws.amazon.com/eventbridge/    |
| 6   | - Vô hiệu hóa Định danh & Điều phối (Lambda #3 & Step Functions):** <br>&emsp; + Phát triển script tự động đổi trạng thái IAM Access Key thành `Inactive` khi nghi ngờ lộ lọt. <br>&emsp; + Thiết kế State Machine cơ bản trên AWS Step Functions để nối luồng xử lý nhiều bước.    | 26/06/2026   | 26/06/2026      | https://docs.aws.amazon.com/step-functions/ |

### Kết quả đạt được tuần 10:

- **Hệ thống Cảnh báo Thời gian thực:** Thiết lập thành công luồng thông báo khẩn cấp qua email thông qua tích hợp EventBridge và Amazon SNS.
- **Cách ly Mối đe dọa (Network Containment):** Triển khai thành công Lambda Function tự động thao tác với EC2 Security Group, chặn đứng ngay lập tức các IP kết nối C&C (Command & Control) hoặc dò quét mạng.
- **Bảo vệ Định danh (Identity Revocation):** Hoàn thiện script Python 3.12 thu hồi IAM Access Key tự động, ngăn chặn rủi ro chiếm quyền điều khiển tài khoản (Account Takeover).
- **Kiến trúc Hướng sự kiện (Event-driven Security):** Chuẩn hóa việc điều hướng sự kiện thông qua Amazon EventBridge, đảm bảo độ trễ (latency) từ lúc GuardDuty phát hiện đến khi Lambda thực thi chỉ trong vài giây.
- **Thực hành Lập trình An toàn:** Tuân thủ nghiêm ngặt nguyên tắc Least Privilege thông qua IAM Roles; mã nguồn Lambda được xử lý ngoại lệ (try/except) toàn diện và lưu trữ log thực thi minh bạch trên CloudWatch Logs.
- **Sẵn sàng Vận hành SOAR:** Đặt nền móng thành công cho việc điều phối quy trình phản ứng sự cố phức tạp thông qua AWS Step Functions.
