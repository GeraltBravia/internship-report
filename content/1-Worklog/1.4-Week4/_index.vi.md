---
title: "Worklog Tuần 4"
date: 2026-05-11
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Siết chặt quyền hạn bằng các ranh giới bảo mật và điều kiện (Conditions) trong IAM.
* Bảo vệ dữ liệu nhạy cảm bằng mã hóa cấp độ hạ tầng (AWS KMS).

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2   | **Permission Management with IAM Permission Boundaries:** <br>&emsp; + Tìm hiểu rủi ro leo thang đặc quyền <br>&emsp; + Thiết lập Permission Boundaries cho IAM Role                                                                                             | 11/06/2026   | 11/06/2026      |
| 3   | - **Access Control with IAM Policies and Conditions:** <br>&emsp; + Phân tích cấu trúc JSON Policy <br>&emsp; + Áp dụng `Condition` keys (IP, Time)                                             |12/06/2026   | 12/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | - **Encryption with AWS Key Management Service (KMS):** <br>&emsp; + Tìm hiểu mã hóa đối xứng/bất đối xứng <br>&emsp; + Phân biệt AWS Managed Keys và CMK | 13/06/2026   | 13/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Cấu hình AWS KMS: <br>&emsp; + Khởi tạo Customer Managed Keys (CMK) <br>&emsp; + Thiết lập Key Policy và tự động xoay vòng khóa                  | 14/06/2026   | 15/06/2026      | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Thực hành Lab:** <br>&emsp; + Triển khai IAM Policy chặn truy cập sai IP <br>&emsp; + Tích hợp KMS để mã hóa ổ cứng EBS <br>&emsp; + Xử lý lỗi `AccessDenied`                                                                                         | 15/05/2026   | 16/05/2026      | <https://cloudjourney.awsstudygroup.com/> |


### Kết quả đạt được tuần 4:

* Ngăn chặn thành công rủi ro leo thang đặc quyền (Privilege Escalation).
* Hoàn thiện cơ chế mã hóa dữ liệu tĩnh (Data at rest).

