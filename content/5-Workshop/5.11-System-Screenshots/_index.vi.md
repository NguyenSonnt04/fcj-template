---
title: "Ảnh chụp giao diện hệ thống"
date: 2024-01-01
weight: 11
chapter: false
pre: " <b> 5.11. </b> "
---

### 1. Overview of the Admin Portal Interface
Cổng quản trị của hệ thống **TrustBite** được xây dựng trên nền tảng **Next.js** kết hợp **TailwindCSS**, mang lại giao diện hiện đại, trực quan, hỗ trợ tối ưu việc vận hành hệ thống xác thực và chống gian lận.

Dưới đây là mô tả chi tiết các phân hệ giao diện trong hệ thống kèm theo các mốc ảnh chụp minh chứng:

---

### 2. Giao diện Tổng quan (Dashboard Overview)
Trang điều hành trung tâm hiển thị sức khỏe thời gian thực của hệ thống, bao gồm trạng thái API (Trực tuyến/Ngoại tuyến), tổng số lượng nhà hàng hoạt động, và trạng thái quyền hạn bảo mật của tài khoản admin đang đăng nhập.

Giao diện được phân chia rõ ràng theo các nhóm chức năng ở thanh menu bên trái (Sidebar):
*   **Chính:** Tổng quan Dashboard.
*   **Quản lý:** Danh mục Nhà hàng & Người dùng.
*   **Tin cậy:** Kiểm duyệt Đánh giá & Hàng đợi Xác minh Hóa đơn.
*   **Hệ thống:** Nhật ký vận hành (Audit log) & Giám sát sức khỏe API.

> [!IMPORTANT]
> **Mốc ảnh chụp minh chứng:**
> * **Ảnh chụp màn hình 19:** Giao diện trang chủ quản trị **Admin Portal** hiển thị Dashboard điều hành trung tâm và danh sách trạng thái trực tuyến của các module dịch vụ.

---

### 3. Giao diện Quản lý Nhà hàng (Restaurant Management)
Trang hiển thị danh sách toàn bộ nhà hàng trên hệ thống, cho phép tìm kiếm theo tên, lọc theo trạng thái hiển thị (Hoạt động, Bản nháp, Tạm ngưng, Đóng cửa) và xem điểm số tin cậy (Trust Score) được tính toán tự động.

Khi bấm vào chi tiết một nhà hàng, hệ thống hiển thị hộp thoại chỉnh sửa thông tin cho phép thay đổi:
*   Tên, Địa chỉ, Số điện thoại.
*   Tọa độ **Kinh độ (Longitude)** và **Vĩ độ (Latitude)** dùng để đối chiếu GPS chống gian lận.
*   Quản lý danh sách hình ảnh nhà hàng (Thiết lập ảnh đại diện chính).

> [!IMPORTANT]
> **Mốc ảnh chụp minh chứng:**
> * **Ảnh chụp màn hình 20:** Giao diện danh sách nhà hàng và Hộp thoại chỉnh sửa thông tin chi tiết nhà hàng bao gồm các trường nhập tọa độ vĩ độ/kinh độ GPS.

---

### 4. Giao diện Quản lý Người dùng (User Management)
Trang hiển thị danh sách tất cả các tài khoản đăng ký trên hệ thống kèm số điện thoại, tên hiển thị, điểm kinh nghiệm (EXP), cấp bậc (Rank) và vai trò phân quyền.

Hộp thoại phân quyền cho phép admin gán vai trò nhanh:
*   **USER**: Người dùng cuối viết đánh giá.
*   **MERCHANT**: Chủ quán để quản trị cửa hàng.
*   **ADMIN**: Quản trị viên hệ thống có toàn quyền.

> [!IMPORTANT]
> **Mốc ảnh chụp minh chứng:**
> * **Ảnh chụp màn hình 21:** Giao diện trang quản lý người dùng hiển thị bảng danh sách tài khoản kèm theo giao diện gán vai trò bảo mật Cognito.

---

### 5. Giao diện Hàng đợi Xác minh Hóa đơn (Receipt Verification Queue)
Đây là màn hình cốt lõi nhất của bộ máy chống gian lận, nơi hiển thị tất cả các bài đánh giá ẩm thực đi kèm hóa đơn đang ở trạng thái **PENDING_ADMIN_REVIEW** (chờ rà soát do điểm rủi ro trung bình từ 31-60).

Giao diện chi tiết rà soát hiển thị:
1.  Ảnh chụp hóa đơn gốc do người dùng tải lên.
2.  Bảng kết quả trích xuất văn bản OCR tự động từ AWS Textract (Tên quán trên hóa đơn, mã hóa đơn, tổng tiền).
3.  **Điểm rủi ro gian lận (Fraud Risk Score)** cùng danh sách chi tiết các cờ cảnh báo (ví dụ: *Lệch GPS vị trí ghi nhận > 200m*, *Tài khoản mới tạo dưới 24 giờ*,...).
4.  Nút quyết định duyệt (**APPROVE** / **REJECT** / **REFERENCE ONLY**) kèm ô nhập lý do bắt buộc để lưu vào nhật ký hệ thống.

> [!IMPORTANT]
> **Mốc ảnh chụp minh chứng:**
> * **Ảnh chụp màn hình 22:** Giao diện hàng đợi rà soát hóa đơn hiển thị chi tiết ảnh hóa đơn, kết quả trích xuất Textract OCR và bảng phân tích điểm rủi ro gian lận của hệ thống.
