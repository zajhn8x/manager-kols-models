# Tài liệu Kinh doanh - Nền tảng Quản lý KOLs/Models

Chào mừng bạn đến với tài liệu kinh doanh của nền tảng quản lý KOLs, Models, PG và Người đẹp. Đây là hệ thống kết nối giữa các nhà tuyển dụng, công ty quản lý (Agency) và các nghệ sĩ/người mẫu.

## 📚 Tổng quan Tài liệu

Tài liệu này được chia thành các phần chính sau:

### [Luồng 1: Vận hành & Tính năng chính](./overview/Luồng%201_%20Về%20luồng%20vận%20hành%20&%20Tính%20năng%20chính.md)
Mô tả chi tiết về luồng vận hành cốt lõi của hệ thống, bao gồm:
- Quản lý hồ sơ người đẹp (Portfolio, thông tin cá nhân, lịch rảnh)
- Tính năng cho đối tác (Tìm kiếm, đăng chiến dịch tuyển dụng)
- Quy trình kết nối giữa hai bên (Kết nối mở vs Quản lý khép kín)

**Điểm nhấn:** Phương án kết nối mở kết hợp thu phí theo lượt mở khóa liên hệ (Pay-per-lead) cho giai đoạn MVP.

### [Luồng 2: Mô hình Kinh doanh](./overview/Luồng%202_%20Mô%20hình%20kinh%20doanh%20(Monetization%20Model)%20.md)
Phân tích 4 nguồn thu chính của nền tảng:
1. **Thu từ Đối tác (B2B):** Gói subscription và Pay-per-lead
2. **Thu từ Người đẹp (B2C):** Đẩy top profile, hồ sơ VIP
3. **Hoa hồng theo Dự án:** Commission/Escrow (5-15%)
4. **Dịch vụ Giá trị gia tăng:** Premium booking, gói trọn gói

**Chiến lược Launch:** Miễn phí 3 tháng đầu để gom data, sau đó áp dụng mô hình thu phí.

### [Luồng 3: Quản trị Admin](./overview/Luồng%203_%20Quản%20trị%20Admin.md)
Các tính năng quản trị hệ thống:
- Quản lý người dùng (KYC, xác minh danh tính)
- Kiểm duyệt nội dung (Hình ảnh, video, bài đăng tuyển dụng)
- Quản lý tài chính & giao dịch
- Thống kê & báo cáo (Dashboard analytics)
- Phân quyền admin nội bộ

### [Phần 4: Mô hình Quản lý Linh hoạt](./overview/Phần%204_%20Mô%20hình%20Quản%20lý%20linh%20hoạt%20(Hybrid%20Management)..md)
Giải pháp kết hợp cả hai chiều quản lý:
- **Top-down:** Agency tự tạo và quản lý hồ sơ KOL
- **Bottom-up:** KOL độc lập xin gia nhập Agency
- Tính năng ràng buộc và hủy liên kết khi hết hợp đồng

### [Phần 4.2: Tài khoản Agency/Manager](./overview/Phần%204.2_%20Tài%20khoản%20cấp%20Công%20ty%20quản%20lý%20(Agency_Manager).md)
Chi tiết về module dành cho công ty quản lý:
- Quản lý hồ sơ nhân sự (Talent Roster)
- Nhận việc tập trung (Centralized Booking)
- Quản lý tài chính & phân bổ (Agency Wallet)
- Trang hồ sơ công ty (Agency Landing Page)

**Kiến trúc phân quyền 3 tầng:**
1. Super Admin (Quản lý toàn hệ thống)
2. Agency Manager (Quản lý nhóm KOL)
3. KOL/Model (Nhân sự)

## 🎯 Mô hình Kinh doanh Tổng quan

Nền tảng hoạt động theo mô hình **B2B2C** với 3 nhóm đối tượng chính:

```
┌─────────────────┐
│  Nhà tuyển dụng │ ──► Trả phí subscription/pay-per-lead
│   (Đối tác)     │
└─────────────────┘
         │
         ▼
┌─────────────────┐
│   Nền tảng      │ ──► Thu hoa hồng, phí dịch vụ
│   (Bạn)         │
└─────────────────┘
         │
         ▼
┌─────────────────┐     ┌─────────────────┐
│  Agency/Manager │ ──► │  KOL/Model      │
│                 │     │  (Người đẹp)    │
└─────────────────┘     └─────────────────┘
         │                       │
         └───────────────────────┘
              Trả phí đẩy top, VIP badge
```

## 🚀 Lộ trình Triển khai

### Giai đoạn 1 (Tháng 1-3): MVP Launch
- Tính năng cơ bản: Đăng ký, tạo profile, tìm kiếm, đăng job
- Miễn phí 100% để gom data
- Mục tiêu: 500 profiles + 50 đối tác active

### Giai đoạn 2 (Tháng 4+): Monetization
- Áp dụng Pay-per-lead cho đối tác
- Bán vị trí đẩy top cho người đẹp
- Tích hợp cổng thanh toán (VietQR)

### Giai đoạn 3: Scale Up
- Module Agency Manager
- Hệ thống Escrow & Commission
- Dịch vụ Premium Booking

## 💡 Lợi thế Cạnh tranh

1. **Tích hợp API mạng xã hội:** Đồng bộ follower thực tế từ TikTok, Instagram, Facebook
2. **Quản lý linh hoạt:** Hỗ trợ cả KOL độc lập và Agency
3. **Lịch rảnh thông minh:** Tránh book trùng lịch
4. **Kiểm duyệt chặt chẽ:** Đảm bảo chất lượng và tính chuyên nghiệp

## 📞 Liên hệ

Để biết thêm chi tiết về từng phần, vui lòng tham khảo các tài liệu trong thư mục `overview/`.

---

**Lưu ý:** Tài liệu này được thiết kế cho mục đích kinh doanh và chiến lược sản phẩm. Để biết thông tin kỹ thuật, vui lòng tham khảo tài liệu dành cho developer.
