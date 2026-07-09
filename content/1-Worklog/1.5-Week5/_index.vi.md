---
title: "Worklog Tuần 5"
date: 2026-05-18
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---



### Mục tiêu tuần 5:

* Quản lý an toàn thông tin xác thực, loại bỏ hardcode.
* Khắc phục các lỗi cấu hình lưu trữ và tự động dò quét dữ liệu PII/PHI.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   |- Credentials Management with AWS Secrets Manager: <br>&emsp; + Tìm hiểu kiến trúc Secrets Manager <br>&emsp; + Tạo Secret cho RDS và cấu hình tự động xoay vòng                                                                                             | 18/05/2026   | 18/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 3   |- S3 Security Best Practices: <br>&emsp; + Áp dụng Block Public Access <br>&emsp; + Cấu hình S3 Versioning và Object Lock (chống Ransomware)                                            | 19/05/2026   | 19/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | -Data Protection with Amazon Macie:** <br>&emsp; + Tìm hiểu nguyên lý phát hiện PII bằng Machine Learning <br>&emsp; + Kích hoạt Macie trên tài khoản | 20/05/2026   | 20/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | -Thiết lập Job Amazon Macie: <br>&emsp; + Cấu hình Custom Data Identifiers <br>&emsp; + Lên lịch quét các S3 bucket quan trọng                  | 21/05/2026   | 21/05/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - Thực hành Lab:** <br>&emsp; + Viết code gọi API lấy mật khẩu từ Secrets Manager <br>&emsp; + Phân tích log cảnh báo rò rỉ dữ liệu từ Macie                                                                                         | 22/05/2026   | 22/05/2026      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 5:

* Triển khai thành công quy trình xoay vòng thông tin xác thực tự động.
* Xây dựng được cơ chế giám sát và phát hiện dữ liệu nhạy cảm tự động trên S3.


