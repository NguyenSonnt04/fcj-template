---
title: "Worklog Tuần 4"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4

- Tối ưu hệ thống AWS về giám sát, bảo mật, hiệu năng và chi phí.
- Tự động hóa công việc vận hành và triển khai ứng dụng container.
- Xây dựng quy trình CI/CD cơ bản trên AWS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | **Đánh giá và giám sát hệ thống**<br>- Đánh giá workload theo các tiêu chí của AWS Well-Architected Framework.<br>- Cấu hình CloudWatch metric, log và alarm cho các tài nguyên chính.<br>- Kết nối dữ liệu giám sát với Grafana để xây dựng dashboard theo dõi tập trung. | 18/05/2026 | 18/05/2026 | <https://cloudjourney.awsstudygroup.com/3-optimize/> |
| 3 | **Tự động hóa vận hành**<br>- Xây dựng AWS Lambda để tự động thực hiện một số tác vụ quản lý tài nguyên.<br>- Tìm hiểu AWS Systems Manager Session Manager, Run Command và Automation.<br>- Kiểm tra log thực thi và xử lý lỗi cho các tác vụ tự động. | 19/05/2026 | 19/05/2026 | <https://cloudjourney.awsstudygroup.com/3-optimize/> |
| 4 | **Tăng cường bảo mật**<br>- Tìm hiểu IAM Permission Boundary và cách giới hạn quyền tối đa của IAM principal.<br>- Khảo sát AWS Security Hub để tập trung cảnh báo và đánh giá trạng thái bảo mật.<br>- Nghiên cứu AWS WAF để bảo vệ ứng dụng web và AWS KMS để quản lý khóa mã hóa. | 20/05/2026 | 20/05/2026 | <https://cloudjourney.awsstudygroup.com/3-optimize/> |
| 5 | **Container và CI/CD**<br>- Đóng gói ứng dụng bằng Docker và chuẩn bị image triển khai.<br>- Triển khai ứng dụng container trên Amazon ECS, cấu hình task definition và service.<br>- Xây dựng pipeline bằng AWS CodePipeline để tự động hóa quá trình build và triển khai. | 21/05/2026 | 21/05/2026 | <https://cloudjourney.awsstudygroup.com/5-container/> |
| 6 | **Tối ưu hiệu năng và chi phí**<br>- Rà soát cấu hình Auto Scaling và quyền sử dụng tài nguyên của workload.<br>- So sánh On-Demand, Savings Plans và Reserved Instances theo nhu cầu vận hành.<br>- Theo dõi chi phí, nhận diện tài nguyên không sử dụng và đề xuất phương án tối ưu. | 22/05/2026 | 22/05/2026 | <https://cloudjourney.awsstudygroup.com/3-optimize/> |

### Kết quả đạt được

- Xây dựng được hệ thống giám sát bằng CloudWatch và Grafana.
- Hiểu cách sử dụng Lambda, Systems Manager, Security Hub, WAF và KMS trong vận hành an toàn.
- Triển khai container trên ECS, xây dựng pipeline cơ bản và đề xuất phương án tối ưu chi phí AWS.
