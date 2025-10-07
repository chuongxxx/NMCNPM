# PROJECT DEFINITION & SOFTWARE REQUIREMENT SPECIFICATION

---

## 👨‍🎓 Thông tin sinh viên

- **Họ tên:** Đỗ Từ Chương
- **MSSV:** K24DTCN411
- **Lớp:** HKV_NMCNPM
- **Github Profile:** [github.com/chuongxxx](https://github.com/chuongxxx)

## 1. PROJECT DEFINITION

### 1.1 Tên dự án

**Ứng dụng bán lẻ tạp hóa công nghệ 4.0 (SmartGrocery)**

### 1.2 Mục tiêu dự án

Xây dựng một ứng dụng hỗ trợ các cửa hàng tạp hóa trong việc quản lý hàng hóa, bán hàng, theo dõi doanh thu và khách hàng.  
Ứng dụng áp dụng công nghệ 4.0 (AI, Cloud, IoT, phân tích dữ liệu) để tự động hóa và tối ưu hoạt động bán lẻ.

### 1.3 Phạm vi dự án

- Quản lý sản phẩm, tồn kho, nhập – xuất hàng.
- Quản lý đơn hàng, thanh toán (tiền mặt, QR, ví điện tử).
- Quản lý khách hàng (tích điểm, ưu đãi, lịch sử mua hàng).
- Báo cáo doanh thu, thống kê mặt hàng bán chạy.
- Hỗ trợ bán hàng qua di động.

### 1.4 Người dùng mục tiêu

- **Chủ cửa hàng tạp hóa**: quản lý hàng hóa, xem báo cáo.
- **Nhân viên bán hàng**: tạo hóa đơn, nhập kho.
- **Khách hàng**: xem thông tin sản phẩm, đặt hàng online (phiên bản mở rộng).

### 1.5 Công nghệ dự kiến

- Frontend: React Native / Flutter
- Backend: NestJS / Node.js
- Database: PostgreSQL + Redis cache
- AI module: gợi ý sản phẩm, dự báo doanh số
- Triển khai: Docker + Cloud (AWS/Azure)

### 1.6 Mô hình tiến trình phần mềm

**Agile (Scrum):**

- Phát triển theo sprint 2 tuần
- Có backlog, daily meeting, sprint review
- Phù hợp với nhóm nhỏ, yêu cầu thay đổi linh hoạt

---

## 2. SOFTWARE REQUIREMENT SPECIFICATION (SRS)

### 2.1 Giới thiệu

Tài liệu này mô tả yêu cầu phần mềm cho hệ thống **SmartGrocery**, phục vụ cho nhóm phát triển, kiểm thử và khách hàng.

### 2.2 Mô tả tổng quan hệ thống

- Quản lý danh mục hàng hóa
- Quản lý khách hàng
- Quản lý nhập hàng, xuất hàng
- Bán hàng (POS)
- Báo cáo doanh thu và tồn kho

---

### 2.3 Yêu cầu chức năng

| Mã    | Mô tả yêu cầu                              | Người dùng              |
| ----- | ------------------------------------------ | ----------------------- |
| FR-01 | Đăng nhập/đăng xuất hệ thống               | Chủ cửa hàng, Nhân viên |
| FR-02 | Thêm/sửa/xóa sản phẩm                      | Chủ cửa hàng            |
| FR-03 | Tạo hóa đơn bán hàng                       | Nhân viên               |
| FR-04 | Thanh toán bằng tiền mặt hoặc QR code      | Nhân viên               |
| FR-05 | Xem báo cáo doanh thu theo ngày/tháng      | Chủ cửa hàng            |
| FR-06 | Tìm kiếm sản phẩm theo mã, tên             | Nhân viên               |
| FR-07 | Quản lý tồn kho, cảnh báo khi sắp hết hàng | Chủ cửa hàng            |
| FR-08 | Gợi ý sản phẩm thường mua kèm (AI)         | Hệ thống                |

---

### 2.4 Yêu cầu phi chức năng

| Mã     | Mô tả                                         |
| ------ | --------------------------------------------- |
| NFR-01 | Giao diện thân thiện, dễ sử dụng              |
| NFR-02 | Thời gian phản hồi < 1 giây                   |
| NFR-03 | Bảo mật thông tin khách hàng (mã hóa dữ liệu) |
| NFR-04 | Khả năng mở rộng khi số lượng người dùng tăng |
| NFR-05 | Hỗ trợ sao lưu tự động dữ liệu hằng ngày      |

---

### 2.5 Rủi ro & Giải pháp

| Rủi ro               | Mức độ     | Giải pháp                               |
| -------------------- | ---------- | --------------------------------------- |
| Thay đổi yêu cầu     | Cao        | Áp dụng Agile để điều chỉnh linh hoạt   |
| Mất kết nối Internet | Trung bình | Cho phép lưu tạm offline và đồng bộ sau |
| Rò rỉ dữ liệu        | Cao        | Mã hóa + xác thực JWT                   |

---

### 2.6 Kế hoạch phát triển sơ bộ

| Giai đoạn | Mô tả                            | Thời gian |
| --------- | -------------------------------- | --------- |
| Sprint 1  | Phân tích & thiết kế cơ bản      | 2 tuần    |
| Sprint 2  | Xây dựng module quản lý hàng hóa | 2 tuần    |
| Sprint 3  | Xây dựng module bán hàng         | 2 tuần    |
| Sprint 4  | Báo cáo & kiểm thử               | 2 tuần    |

---

**Tổng kết:**  
Tài liệu này mô tả toàn bộ phạm vi, yêu cầu chức năng và phi chức năng của hệ thống **SmartGrocery** – ứng dụng tạp hóa thông minh theo mô hình Agile. Đây là nền tảng để nhóm phát triển tiến hành thiết kế, lập trình và kiểm thử trong các giai đoạn tiếp theo.
