# **Luồng 3: Quản trị Admin**

## **Tổng quan**

Hệ thống Admin là "trung tâm điều khiển" của toàn bộ nền tảng, đảm bảo chất lượng, an toàn và hiệu quả vận hành. Admin Dashboard cần cung cấp đầy đủ công cụ để:
- Quản lý và kiểm duyệt nội dung
- Xử lý tranh chấp và hỗ trợ người dùng
- Theo dõi tài chính và doanh thu
- Phân tích dữ liệu và đưa ra quyết định

### **Nguyên tắc Thiết kế Admin System**

1. **Security First:** Bảo mật tuyệt đối, audit trail đầy đủ
2. **Efficiency:** Xử lý nhanh, bulk actions, keyboard shortcuts
3. **Transparency:** Mọi hành động đều được ghi log
4. **Scalability:** Có thể xử lý hàng nghìn requests/ngày
5. **User-friendly:** Giao diện đơn giản, dễ training nhân viên mới

---

Dưới đây là chi tiết các tính năng bắt buộc phải có cho hệ thống Admin:

## **1\. Quản lý Người dùng (User Management)**

**Mục tiêu:** Đảm bảo chất lượng cộng đồng, ngăn chặn gian lận, bảo vệ người dùng

Admin cần nắm toàn quyền sinh sát đối với các tài khoản trên hệ thống để đảm bảo chất lượng cộng đồng.

### **1.1. Duyệt Hồ sơ (KYC \- Xác minh danh tính)**

#### **Quy trình KYC Verification:**

```
Step 1: User Submit
  - Upload CCCD/CMND (front + back)
  - Upload selfie holding ID
  - Submit for review
  ↓
Step 2: Auto Check (AI)
  - Face matching (selfie vs ID photo)
  - Document validation (check format, blur, fake)
  - OCR extract info (name, DOB, ID number)
  - Result: Pass → Queue for manual review
           Fail → Auto reject with reason
  ↓
Step 3: Manual Review (Admin)
  - Check AI results
  - Verify info matches profile
  - Look for red flags
  - Decision: Approve / Reject / Request more info
  ↓
Step 4: Result
  - Approved: Grant "Verified" badge
  - Rejected: Send reason, allow resubmit
  - Pending: Request additional documents
```

#### **Admin Review Interface:**

| Field | Display | Actions |
|-------|---------|---------|
| **User Info** | Name, Age, City, Join date | View full profile |
| **ID Documents** | Front/Back images (zoomable) | Download, Flag suspicious |
| **Selfie** | Photo with ID | Compare with portfolio |
| **AI Results** | Face match: 95%, Doc valid: Yes | Override if needed |
| **OCR Data** | Extracted name, DOB, ID# | Copy, Edit |
| **Decision** | Approve / Reject / Request more | Bulk actions available |
| **Notes** | Internal notes field | Save for future reference |

#### **KYC Metrics & SLA:**

| Metric | Target | Current |
|--------|--------|---------|
| **Review time** | <24 hours | Track average |
| **Approval rate** | 70-80% | Monitor trends |
| **Rejection reasons** | Top 3: Blur, Mismatch, Fake | Analyze patterns |
| **Resubmit rate** | <30% | Improve instructions |
| **Fraud detection** | >95% accuracy | AI + Manual |

#### **Common Rejection Reasons:**

| Reason | % of Rejections | Solution |
|--------|----------------|----------|
| **Blurry photo** | 35% | Better upload instructions |
| **Info mismatch** | 25% | Clear error messages |
| **Suspected fake ID** | 15% | AI improvement |
| **Incomplete docs** | 15% | Checklist before submit |
| **Underage** | 10% | Age verification |

### **1.2. Quản lý Trạng thái Tài khoản**

#### **Account Status Types:**

| Status | Description | User Impact | Admin Actions |
|--------|-------------|-------------|---------------|
| **Active** | Normal, good standing | Full access | Monitor activity |
| **Pending** | New, not verified | Limited access | Review KYC |
| **Warned** | Minor violation | Warning message | Send warning email |
| **Suspended** | Temporary ban (7-30 days) | Cannot login | Set duration, reason |
| **Banned** | Permanent ban | Account disabled | Cannot reactivate |
| **Deleted** | User requested deletion | Data anonymized | GDPR compliance |

#### **Violation Types & Penalties:**

| Violation | Severity | First Offense | Second Offense | Third Offense |
|-----------|----------|---------------|----------------|---------------|
| **No-show (KOL)** | High | Warning + Rating drop | 7-day suspension | 30-day ban |
| **Fake profile** | Critical | Immediate ban | N/A | N/A |
| **Harassment** | High | Warning | 30-day suspension | Permanent ban |
| **Spam** | Medium | Warning | 7-day suspension | 30-day ban |
| **Payment fraud** | Critical | Immediate ban + Legal | N/A | N/A |
| **Inappropriate content** | Medium | Content removal + Warning | 7-day suspension | Permanent ban |

#### **Bulk Actions:**

Admin có thể xử lý nhiều users cùng lúc:
- Select multiple users (checkbox)
- Bulk approve/reject KYC
- Bulk send messages
- Bulk change status
- Export to Excel

### **1.3. Hỗ trợ Cấp lại Mật khẩu/Đăng nhập**

#### **Support Ticket System:**

```
User Request Types:
├── Password Reset (40%)
├── Account Recovery (25%)
├── Payment Issues (15%)
├── Profile Problems (10%)
└── Other (10%)

Priority Levels:
- P0 (Critical): Payment stuck, Account hacked
- P1 (High): Cannot login, Cannot book
- P2 (Medium): Profile issues, Feature requests
- P3 (Low): General questions
```

#### **Admin Support Dashboard:**

| Column | Info | Actions |
|--------|------|---------|
| **Ticket ID** | #12345 | Click to view details |
| **User** | Name + ID | View profile |
| **Type** | Password reset | Filter by type |
| **Priority** | P1 - High | Sort by priority |
| **Status** | Open / In Progress / Resolved | Update status |
| **Assigned to** | Admin name | Reassign |
| **Created** | 2 hours ago | Sort by time |
| **SLA** | 4h remaining | Alert if overdue |

#### **Support SLA:**

| Priority | Response Time | Resolution Time |
|----------|---------------|-----------------|
| **P0** | <15 minutes | <2 hours |
| **P1** | <1 hour | <4 hours |
| **P2** | <4 hours | <24 hours |
| **P3** | <24 hours | <72 hours |

#### **Common Support Actions:**

1. **Password Reset:**
   - Verify user identity (email, phone, ID)
   - Generate temporary password
   - Send via SMS/Email
   - Log action

2. **Account Recovery:**
   - Check account status
   - Verify ownership (security questions)
   - Unlock account
   - Reset 2FA if needed

3. **Payment Issues:**
   - Check transaction history
   - Verify payment gateway status
   - Manual credit adjustment if needed
   - Refund if necessary

## **2\. Kiểm duyệt Nội dung (Content Moderation)**

Đây là chốt chặn quan trọng nhất để nền tảng của bạn luôn sạch sẽ và chuyên nghiệp.

* **Duyệt Hình ảnh/Video Portfolio:** Mọi hình ảnh người đẹp tải lên cần qua Admin duyệt trước khi hiển thị (Public) để tránh hình ảnh phản cảm, 18+ hoặc vi phạm pháp luật.  
* **Duyệt Bài đăng Tuyển dụng:** Admin kiểm tra nội dung Job của đối tác xem có rõ ràng về công việc, địa điểm và mức lương không. Nếu bài đăng có dấu hiệu mờ ám (ví dụ: tuyển "sugar baby", công việc vi phạm pháp luật), Admin sẽ từ chối hiển thị.

## **3\. Quản lý Tài chính & Giao dịch (Financial Management)**

Dựa trên Mô hình kiếm tiền (Luồng 2\) chúng ta vừa chốt, Admin cần công cụ để theo dõi dòng tiền:

* **Lịch sử Nạp tiền:** Theo dõi các giao dịch nạp tiền của đối tác/người đẹp (qua chuyển khoản VietQR hoặc cổng thanh toán). Admin có thể cộng/trừ tiền hoặc "Xu" thủ công cho người dùng khi cần xử lý sự cố.  
* **Quản lý Gói Dịch vụ (Packages):** Cấu hình giá tiền, thời hạn và quyền lợi của các gói VIP (ví dụ: Gói Gold 500k/tháng được đăng 10 bài, mở khóa 50 số điện thoại). Admin có thể linh hoạt thay đổi giá các gói này để chạy khuyến mãi.  
* **Lịch sử Tiêu dùng:** Theo dõi chi tiết đối tác A đã dùng "Xu" để mở khóa số điện thoại của những người đẹp nào.

## **4\. Thống kê & Báo cáo (Dashboard & Analytics)**

Ngay khi đăng nhập, Admin cần thấy một biểu đồ tổng quan để biết "sức khỏe" của hệ thống:

* **Chỉ số Tăng trưởng:** Tổng số user mới đăng ký, số lượng profile người đẹp đang active, số lượng đối tác mới trong ngày/tuần/tháng.  
* **Chỉ số Tương tác:** Số lượng bài Job được đăng, số lượt apply (ứng tuyển) thành công, số lượt mở khóa số điện thoại.  
* **Báo cáo Doanh thu:** Tổng tiền nạp vào hệ thống theo từng khoảng thời gian.

## **5\. Phân quyền Admin Nội bộ (Internal Roles)**

Khi hệ thống lớn lên, bạn không thể tự làm mọi thứ mà sẽ cần thuê nhân viên. Hệ thống cần chia quyền rõ ràng:

* **Super Admin (Chủ hệ thống):** Thấy toàn bộ doanh thu, cấu hình giá, xóa tài khoản và quản lý nhân sự.  
* **Nhân viên Duyệt bài/CSKH:** Chỉ được quyền xem/duyệt hồ sơ người đẹp, duyệt bài đăng tuyển dụng, hỗ trợ chat với khách hàng, nhưng **không** được xem báo cáo doanh thu hay rút tiền.

**Gợi ý cho phiên bản MVP (Ra mắt lần đầu):** Để tiết kiệm chi phí lập trình ban đầu, bạn chỉ cần làm một cấp độ **Super Admin** duy nhất và tập trung mạnh vào tính năng **Duyệt bài/Duyệt hình ảnh**. Các tính năng thống kê biểu đồ phức tạp có thể xuất ra file Excel để tự tính toán trước, chưa cần lập trình vội.  
Như vậy, chúng ta đã đi qua toàn bộ 3 luồng xương sống: **Vận hành cốt lõi \- Mô hình kiếm tiền \- Quản trị hệ thống**.  
Để tôi có thể tổng hợp thành một bản Kế hoạch triển khai (Roadmap) hoàn chỉnh kèm dự toán cho bạn, bạn muốn nền tảng này chạy trên định dạng **Website (Web App)** trước, hay muốn làm thẳng thành **Ứng dụng di động (Mobile App tải trên App Store/Google Play)**?