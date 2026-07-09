---
title: 'Worklog Tuần 11'
date: 2026-06-29
weight: 11
chapter: false
pre: ' <b> 1.11. </b> '
---

### Mục tiêu tuần 11:

- Hoàn thiện và đóng gói (package) quy trình phản ứng sự cố tự động bằng AWS Step Functions.
- Mở rộng năng lực Auto-Remediation: Cô lập tài nguyên mạng và vô hiệu hóa định danh xâm nhập ngay trong thời gian thực.
- Chuẩn hóa luồng lưu vết (Audit Trail) để phục vụ công tác điều tra số (Forensics) và tuân thủ.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                     | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                              |
| --- | ----------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------- |
| 2   | - Điều phối Sự kiện (Workflow Orchestration):** <br>&emsp; + Hoàn thiện State Machine trên AWS Step Functions để nối luồng xử lý có điều kiện (Choice state). <br>&emsp; + Dịch chuyển nguồn trigger: Kết nối EventBridge trực tiếp với AWS Security Hub để thống nhất luồng cảnh báo.                    | 29/06/2026   | 29/06/2026      | https://docs.aws.amazon.com/step-functions/ |
| 3   | - Cô lập Mạng (Network Containment):** <br>&emsp; + Phát triển Lambda tự động bóc tách ID của EC2 bị nhiễm mã độc. <br>&emsp; + Cấu hình kịch bản thay thế Security Group hiện tại bằng "Isolation Security Group" (Block toàn bộ Inbound/Outbound trừ cổng quản trị)                             | 30/06/2026   | 30/06/2026      | https://docs.aws.amazon.com/ec2/            |
| 4   | - Vô hiệu hóa Định danh (Identity Revocation):** <br>&emsp; + Nâng cấp Lambda Function xử lý lộ lọt Credential Compromise. <br>&emsp; + Bổ sung logic: Vô hiệu hóa Access Key, đồng thời thu hồi phiên đăng nhập (Revoke sessions) và chặn Console Access của IAM User. | 01/07/2026   | 01/07/2026      | https://docs.aws.amazon.com/iam/            |
| 5   | - Lưu vết Điều tra (Forensic Logging):** <br>&emsp; + Viết logic xuất báo cáo hành động (Remediation Logs) định dạng JSON. <br>&emsp; + Lưu trữ vào Amazon S3 với cấu trúc thư mục theo thời gian (Partitioning) để sẵn sàng truy vấn. <br>&emsp; + Đảm bảo Lambda/Step Functions đẩy full metrics lên CloudWatch.                                    | 02/07/2026   | 02/07/2026      | https://docs.aws.amazon.com/s3/             |
| 6   | - Kiểm thử Toàn trình (End-to-End Testing):** <br>&emsp; + Bắn payload giả lập nhiều loại Security Findings khác nhau từ Security Hub. <br>&emsp; + Verify toàn bộ flow: Phát hiện -> Kích hoạt Rule -> Điều phối Step Functions -> Cô lập EC2/IAM -> Gửi Noti SNS -> Lưu log S3.                         | 03/07/2026   | 03/07/2026      | https://docs.aws.amazon.com/guardduty/      |

### Kết quả đạt được tuần 11:

- **Hoàn thiện Kiến trúc SOAR:** Xây dựng thành công quy trình điều phối phản ứng sự cố hoàn chỉnh, linh hoạt xử lý rẽ nhánh cho từng loại mối đe dọa thông qua AWS Step Functions.
- **Tối ưu hóa Thời gian Phản hồi (MTTR):** Giảm thiểu thời gian cô lập EC2 bị thỏa hiệp và vô hiệu hóa IAM Access Key xuống mức tính bằng giây thay vì thao tác thủ công.
- **Tập trung hóa Cảnh báo:** Chuyển đổi thành công nguồn sự kiện, cho phép EventBridge lấy dữ liệu tổng hợp trực tiếp từ AWS Security Hub làm Trigger trung tâm.
- **Sẵn sàng Điều tra số (Forensics-Ready):** Lịch sử xử lý sự cố được cấu trúc hóa và đẩy về lưu trữ an toàn (Immutable S3 bucket), đáp ứng tốt các yêu cầu về kiểm toán (Auditing).
- **Vận hành Đáng tin cậy:** Toàn bộ quá trình thử nghiệm (End-to-End) chứng minh hệ thống hoạt động chính xác, log thực thi được thu thập đầy đủ trên Amazon CloudWatch.