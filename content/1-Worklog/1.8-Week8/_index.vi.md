---
title: 'Worklog Tuần 8'
date: 2026-06-08
weight: 8
chapter: false
pre: ' <b> 1.8. </b> '
---

---

### Mục tiêu tuần 8:

- Hoàn thiện bản vẽ kiến trúc (Architecture Diagram) cho dự án Cloud Security.
- Phân bổ quyền hạn, tài nguyên và thiết lập môi trường AWS độc lập cho từng thành viên trong nhóm.
- Nghiên cứu khả năng tích hợp của các dịch vụ bảo mật (Security Hub, GuardDuty) và công cụ IaC (Terraform).
- Chốt lộ trình Sprint và thiết lập quy trình CI/CD/Git cơ bản để phối hợp triển khai.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu      |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------- |
| 2   | -Phân tích yêu cầu & Kiến trúc:** <br>&emsp; + Rà soát scope dự án bảo mật mạng trên AWS. <br>&emsp; + Thảo luận và phác thảo bản vẽ System Topology sơ bộ.                                                                 | 08/06/2026   | 08/06/2026      | Tài liệu dự án      |
| 3   | - Thiết lập môi trường làm việc:** <br>&emsp; + Quy hoạch 3 tài khoản AWS riêng biệt cho các thành viên. <br>&emsp; + Thiết lập IAM Role/Cross-account access để tiện phối hợp.                                                   | 09/06/2026   | 09/06/2026      | Thảo luận nhóm      |
| 4   | - Phân công trách nhiệm (Role Assignment):** <br>&emsp; + Chia task theo domain: Network Security, Identity Management, và Threat Detection. <br>&emsp; + Thống nhất quy ước đặt tên (Naming Convention) cho tài nguyên đám mây                                           | 10/06/2026   | 10/06/2026      | Kế hoạch nhóm       |
| 5   | -Nghiên cứu công nghệ (R&D):** <br>&emsp; + Đánh giá các module Terraform cần thiết để tự động hóa hạ tầng. <br>&emsp; + Tìm hiểu luồng thu thập log bảo mật tập trung.                                  | 11/06/2026   | 12/06/2026      | Tài liệu chính thức |
| 6   | -Lên lộ trình & Chốt kế hoạch:** <br>&emsp; + Xây dựng backlog công việc trên công cụ quản lý (Jira/Trello). <br>&emsp; + Chốt các mốc thời gian (Milestones) triển khai cụ thể cho từng Sprint.      | 12/06/2026   | 12/06/2026      | Kế hoạch nhóm       |

### Kết quả đạt được tuần 8:

- Bản vẽ kiến trúc hệ thống tổng thể đã được cả nhóm thông qua.
- Hoàn tất cấu hình môi trường AWS ban đầu, đảm bảo phân lập quyền truy cập an toàn giữa các tài khoản của thành viên.
- Chốt danh sách các công cụ và AWS Services sẽ sử dụng (Terraform, IAM, VPC, v.v.).
- Quy trình phối hợp code (Git workflow) và báo cáo tiến độ đã được thiết lập rõ ràng.
- Các thành viên nắm rõ phần việc chịu trách nhiệm cốt lõi của mình (Network, IAM, hay Logging).
- Lộ trình triển khai (Roadmap) đã sẵn sàng để nhóm chính thức bắt tay vào cấu hình hệ thống từ tuần tiếp theo.