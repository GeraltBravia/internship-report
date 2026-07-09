---
title: 'Worklog Tuần 9'
date: 2026-06-15
weight: 9
chapter: false
pre: ' <b> 1.9. </b> '
---

### Mục tiêu tuần 9:

- Xây dựng nền tảng giám sát an ninh (Security Monitoring Foundation) cho toàn bộ hạ tầng đám mây của dự án.
- Triển khai tự động hóa quá trình thu thập log, phát hiện mối đe dọa (Threat Detection) và cảnh báo tài nguyên.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                             | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                           |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ---------------------------------------- |
| 2   | - Thiết lập Baseline Security:** <br>&emsp; + Khởi tạo tài khoản AWS dự án, kích hoạt MFA cho Root User. <br>&emsp; + Phân quyền quản trị thông qua IAM Groups và cấp phát IAM User (AdministratorAccess) để vận hành hằng ngày thay cho Root.                                                                      | 15/06/2026   | 15/06/2026      | https://docs.aws.amazon.com/iam/         |
| 3   | - Triển khai Logging & Networking Visibility:** <br>&emsp; + Cấu hình AWS CloudTrail để ghi vết (audit) toàn bộ API Calls. <br>&emsp; + Kích hoạt VPC Flow Logs nhằm phân tích lưu lượng mạng và xuất dữ liệu tập trung về Amazon CloudWatch Logs.                                                                         | 16/06/2026   | 16/06/2026      | https://docs.aws.amazon.com/cloudtrail/  |
| 4   | - Giám sát Tuân thủ & Ngân sách (FinOps):** <br>&emsp; + Thiết lập AWS Config để theo dõi và đối chiếu liên tục các thay đổi cấu hình tài nguyên. <br>&emsp; + Cấu hình AWS Budgets và định tuyến cảnh báo chi phí hằng tháng (Cost Alarms) để kiểm soát tài nguyên.                                                              | 17/06/2026   | 17/06/2026      | https://docs.aws.amazon.com/config/      |
| 5   | - Phát hiện Mối đe dọa Tập trung:** <br>&emsp; + Kích hoạt Amazon GuardDuty (region ap-southeast-1) để phân tích log thông minh. <br>&emsp; + Triển khai AWS Security Hub, áp dụng chuẩn NIST 800-53 và đồng bộ các GuardDuty Findings về một Dashboard duy nhất.                           | 18/06/2026   | 18/06/2026      | https://docs.aws.amazon.com/securityhub/ |
| 6   | - Kiểm thử & Cảnh báo Tự động:** <br>&emsp; + Khởi chạy IAM Access Analyzer rà soát các chính sách cấp quyền chia sẻ ra bên ngoài (Cross-account/Public). <br>&emsp; + Xây dựng CloudWatch Alarms giám sát sự kiện đăng nhập thất bại và sử dụng Root account. <br>&emsp; + Sinh GuardDuty Sample Findings để kiểm chứng luồng cảnh báo trên Security Hub. | 19/06/2026   | 19/06/2026      | https://docs.aws.amazon.com/guardduty/   |

### Kết quả đạt được tuần 9:

**Bảo mật Định danh & Quyền truy cập:** Hoàn thiện lớp phòng thủ đầu tiên với MFA và kiến trúc IAM User/Group tuân thủ nguyên tắc quyền hạn tối thiểu (Least Privilege).
- **Thu thập & Phân tích Log toàn diện:** Đảm bảo khả năng truy vết hệ thống bằng cách cấu hình thành công CloudTrail (API activities) và VPC Flow Logs (Network traffic).
- **Kiểm soát Ngân sách & Tuân thủ:** Thiết lập thành công hệ thống giám sát sự thay đổi cấu hình tài nguyên (AWS Config) và cơ chế cảnh báo tự động khi chi phí vượt ngưỡng (AWS Budgets).
- **Phát hiện Mối đe dọa (Threat Detection):** Đưa Amazon GuardDuty vào hoạt động, đảm bảo khả năng phát hiện các hành vi dò quét và xâm nhập bất thường.
- **Tập trung hóa Quản trị An ninh:** Hợp nhất thành công các cảnh báo rủi ro về AWS Security Hub, đáp ứng yêu cầu đánh giá bảo mật theo tiêu chuẩn NIST 800-53.
- **Xác thực Hệ thống Cảnh báo:** Hệ thống CloudWatch Alarms đã phản hồi chính xác với các mẫu test (GuardDuty Sample Findings và Failed Logins), sẵn sàng cho việc tự động hóa phản ứng sự cố ở các tuần tiếp theo.
