---
title: 'Worklog Tuần 12'
date: 2026-07-06
weight: 12
chapter: false
pre: ' <b> 1.12. </b> '
---

### Mục tiêu tuần 12:

- Xây dựng trung tâm giám sát trực quan (Single Pane of Glass) cho toàn bộ hoạt động bảo mật.
- Đóng vai Red Team/Blue Team để kiểm chứng khả năng vận hành của kiến trúc SOC (Detect → Respond → Recover).
- Rà soát đặc quyền, đánh giá bài toán chi phí và hoàn thiện hồ sơ bàn giao dự án.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --- | --- | --- | --- |
| 2 | - Xây dựng SOC Dashboard tập trung: <br>&emsp; + Thiết kế Amazon CloudWatch Dashboard. <br>&emsp; + Trích xuất và biểu diễn các metrics: GuardDuty Findings, Step Functions Executions, Lambda Errors, EC2 Health.
| 3 | - Cấu hình Ngưỡng Cảnh báo (Alerting): <br>&emsp; + Thiết lập CloudWatch Alarms cho các chỉ số dị thường (vd: tỷ lệ lỗi Lambda > 5%). <br>&emsp; + Xác thực luồng Email Notification qua Amazon SNS từ Alarms. | 07/07/2026 | 07/07/2026 | https://docs.aws.amazon.com/cloudwatch/ |
| 4 | - Mô phỏng Tấn công & Phòng thủ (Red/Blue Teaming): <br>&emsp; + Chạy kịch bản tấn công giả lập: Dò quét port EC2, đánh cắp IAM Access Key. <br>&emsp; + Theo dõi luồng sự kiện từ Security Hub tới lúc hệ thống tự động vô hiệu hóa mối đe dọa. | 08/07/2026 | 08/07/2026 | https://docs.aws.amazon.com/guardduty/ |
| 5 | - Rà soát Đặc quyền & Đánh giá Kiến trúc: <br>&emsp; + Chạy IAM Access Analyzer để dò quét các quyền thừa thãi (Over-privileged) và siết lại theo Least Privilege. <br>&emsp; + Phân tích (Post-Incident Review) hiệu năng của quy trình Detect → Respond. | 09/07/2026 | 09/07/2026 | https://docs.aws.amazon.com/iam/ |
| 6 | - Nghiệm thu, Bàn giao & Teardown:** <br>&emsp; + Hoàn thiện System Architecture Document và Hướng dẫn vận hành. <br>&emsp; + Đánh giá chi phí (Billing) và đề xuất nâng cấp (IaC, Multi-Account, Amazon Detective). <br>&emsp; + Dọn dẹp/Hủy tài nguyên (Teardown) trên các tài khoản AWS để tránh phát sinh chi phí. | 10/07/2026 | 10/07/2026 | https://docs.aws.amazon.com/wellarchitected/ |

### Kết quả đạt được tuần 12:

- **Giám sát Trực quan:** Triển khai thành công CloudWatch Dashboard đóng vai trò như một SOC console thu nhỏ, hiển thị real-time các chỉ số sống còn của hệ thống (Findings, Automations metrics, Resource Health).
- **Kiểm chứng Auto-Remediation:** Các kịch bản giả lập tấn công (Red Teaming) đã chứng minh quy trình Detect → Respond → Recover hoạt động trơn tru; hệ thống tự động bóp nghẹt các hành vi xâm phạm chỉ trong vài giây.
- **Tối ưu hóa Phân quyền:** Hoàn tất quá trình Audit IAM, đảm bảo 100% các Roles và Users tuân thủ nguyên tắc quyền hạn tối thiểu (Least Privilege).
- **Hoàn thiện Hồ sơ Dự án:** Đóng gói thành công toàn bộ tài liệu kỹ thuật, sơ đồ hệ thống và kịch bản vận hành. Đã lập danh sách các đề xuất nâng cấp chiến lược (như tích hợp Amazon Macie và triển khai IaC bằng Terraform) cho các phase tiếp theo.
- **Quản trị Rủi ro Chi phí (FinOps):** Hệ thống được kiểm soát chi phí chặt chẽ, các tài nguyên thử nghiệm đã được dọn dẹp an toàn vào cuối chu kỳ dự án.