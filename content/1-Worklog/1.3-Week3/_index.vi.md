---
title: "Worklog Tuần 3"
date: 2026-05-04
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Hiểu và triển khai giải pháp quản lý định danh tập trung trên AWS.
* Tích hợp xác thực đa luồng cho cả người dùng nội bộ và người dùng ứng dụng.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | - **Identity Federation with AWS SSO:** <br>&emsp; + Tìm hiểu khái niệm Single Sign-On <br>&emsp; + Tìm hiểu vai trò của AWS IAM Identity Center.                                                                                             | 04/05/2026 | 04/05/2026 | AWS Docs |
| 3   | - Cấu hình IAM Identity Center: <br>&emsp; + Quản lý truy cập đa tài khoản <br>&emsp; + Thiết lập Permission Sets.                                                                                             | 05/05/2026 | 05/05/2026 | AWS Docs |
| 4   | - **Cross-Domain Authentication with Amazon Cognito:** <br>&emsp; + Tìm hiểu kiến trúc User Pools <br>&emsp; + Tìm hiểu kiến trúc Identity Pools.                                                                                             | 06/05/2026 | 06/05/2026 | AWS Docs |
| 5   | - Khởi tạo Cognito Pools <br> - Cấu hình tích hợp các Identity Providers (IdP): <br>&emsp; + Facebook <br>&emsp; + Google.                                                                                             | 07/05/2026 | 07/05/2026 | AWS Docs |
| 6   | - **Thực hành Lab:** <br>&emsp; + Mô phỏng quy trình cấp và thu hồi quyền truy cập qua SSO <br>&emsp; + Viết script/dùng Postman test luồng đăng nhập Cognito lấy JWT Token <br>&emsp; + Troubleshoot lỗi xác thực.                                                                                              | 08/05/2026 | 09/05/2026 | Lab Guide |


### Kết quả đạt được tuần 3:

* Thiết lập thành công cổng đăng nhập tập trung SSO cho tổ chức.
* Hoàn thiện luồng xác thực (Authentication flow) qua Cognito cho ứng dụng

