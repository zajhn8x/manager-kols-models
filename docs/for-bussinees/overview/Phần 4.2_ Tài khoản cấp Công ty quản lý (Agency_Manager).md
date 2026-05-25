# **Phần 4.2: Tài khoản cấp Công ty quản lý (Agency/Manager)**

Việc bổ sung thêm sẽ biến hệ thống của bạn từ một nền tảng B2C (Doanh nghiệp tuyển Cá nhân) thành một sàn giao dịch B2B2C thực thụ. Rất nhiều KOL/Người mẫu không tự nhận show mà mọi lịch trình, chi phí đều do công ty chủ quản quyết định.  
Dưới đây là chi tiết module dành riêng cho cấp độ **Quản lý Công ty (Agency Manager / Sub-Admin)**:

## **1\. Tổng quan Phân cấp Quyền hạn mới**

Kiến trúc phân quyền của hệ thống sẽ được chia làm 3 tầng rõ rệt:

* **Tầng 1 \- Super Admin (Bạn):** Quản lý toàn bộ hệ thống, thu phí cả Đối tác (Nhà tuyển dụng) và Công ty Agency.  
* **Tầng 2 \- Agency Manager (Quản lý Công ty):** Quản lý một nhóm (Roster) các KOL/Model thuộc quyền sở hữu của công ty mình. Đại diện cho KOL để nhận việc, báo giá và nhận tiền.  
* **Tầng 3 \- KOL/Model (Nhân sự):** Hồ sơ hiển thị trên web. Có thể có tài khoản để tự vào xem lịch trình, hoặc thậm chí không cần tài khoản đăng nhập (chỉ là một profile tĩnh do Agency tạo ra và quản lý hộ).

## **2\. Các tính năng cốt lõi cho Agency Dashboard (Trang quản lý của Công ty)**

### **A. Quản lý Hồ sơ nhân sự (Talent Roster)**

* **Tạo & Chỉnh sửa Profile:** Agency có quyền tự tạo hàng loạt hồ sơ cho các KOL/Model trực thuộc công ty mình (không cần KOL phải tự đăng ký bằng số điện thoại).  
* **Gắn thẻ "Độc quyền":** Trên hồ sơ của các KOL này (khi hiển thị ra ngoài trang chủ) sẽ có huy hiệu **"Được quản lý bởi Công ty \[Tên Agency\]"** để tăng độ uy tín và tránh việc đối tác liên hệ chui để phá giá.  
* **Cập nhật hàng loạt:** Agency có thể nhanh chóng cập nhật lịch rảnh, bộ ảnh mới hoặc mức giá cát-xê cho nhiều người đẹp cùng lúc.

### **B. Quản lý Nhận việc tập trung (Centralized Booking)**

* **Đại diện ứng tuyển:** Khi có một Job mới từ Nhà tuyển dụng, tài khoản Agency có thể bấm "Ứng tuyển" và đính kèm 3-4 hồ sơ KOL của công ty mình để nhà tuyển dụng chọn.  
* **Nhận tin nhắn (Chat) tập trung:** Bất kỳ Nhà tuyển dụng nào muốn book một KOL thuộc Agency, tin nhắn sẽ được chuyển thẳng về hộp thư của tài khoản Agency Manager. Quản lý công ty sẽ là người trực tiếp deal giá, chốt lịch thay vì để KOL tự làm.

### **C. Quản lý Tài chính & Phân bổ (Agency Wallet)**

* **Ví Công ty:** Mọi khoản thù lao từ các job thành công của dàn KOL sẽ được đổ về một "Ví Công ty" duy nhất trên hệ thống. Agency Manager sẽ chịu trách nhiệm rút tiền về tài khoản ngân hàng của công ty, sau đó tự chia lại với KOL ở ngoài đời thực (hệ thống của bạn không cần lo việc chia chác phức tạp này).  
* **Lịch sử dòng tiền:** Thống kê chi tiết KOL nào đang mang lại doanh thu cao nhất cho công ty trong tháng.

### **D. Trang Hồ sơ Công ty (Agency Landing Page)**

* Hệ thống cấp cho mỗi Agency một trang riêng (Ví dụ: \[tenweb.com/agency/abc-models\](https://tenweb.com/agency/abc-models)).  
* Trang này hiển thị logo công ty, thông tin liên hệ của người quản lý, danh sách các chiến dịch đã làm, và hiển thị toàn bộ danh sách người đẹp trực thuộc. Nhà tuyển dụng có thể vào đây để "chọn gói" hoặc book nhiều người cùng lúc cho tiện.

## **3\. Lợi ích của việc mở tính năng này**

* **Gom Data cực nhanh:** Thay vì phải đi thuyết phục từng cá nhân người đẹp vào đăng ký, bạn chỉ cần chốt được 1 công ty Agency là trên hệ thống tự động có ngay vài chục đến hàng trăm Profile chất lượng cao được cập nhật sẵn.  
* **Dễ thu tiền hơn:** Các công ty Agency có sẵn ngân sách marketing. Họ sẵn sàng trả phí (mua gói Subscription) cho hệ thống của bạn để đẩy toàn bộ danh sách "gà nhà" lên vị trí nổi bật.  
* **Chuyên nghiệp hóa:** Giảm thiểu rủi ro bùng show, làm việc qua Agency luôn uy tín và đúng hợp đồng hơn là làm việc với các cá nhân tự do.

Việc bổ sung module này sẽ làm thay đổi một chút ở khâu vận hành ban đầu. Đối với các KOL trực thuộc Agency, bạn muốn Công ty chủ động tự tạo hồ sơ cho họ (KOL không có quyền sửa chữa, chỉ làm theo chỉ định), hay KOL tự đăng ký tài khoản rồi gửi yêu cầu "Xin gia nhập" vào tài khoản của Công ty trên hệ thống?

---

## **4. Agency Pricing & Revenue Model**

### **4.1. Các Gói Dịch Vụ cho Agency (Agency Subscription Tiers)**

**Chiến lược giá:** Giá theo số lượng talent để khuyến khích các agency lớn tham gia

**Giải thích chi tiết:**

Module Agency là nguồn thu chính của nền tảng vì:
- **1 Agency = 20-50 talents:** Thay vì phải tuyển từng KOL lẻ, bạn chỉ cần thuyết phục 1 agency là có ngay hàng chục profile chất lượng
- **Agency có ngân sách:** Các công ty quản lý sẵn sàng chi tiền cho công cụ giúp họ tăng doanh thu
- **Dễ thu tiền hơn:** Agency trả phí đều đặn hàng tháng, không như KOL cá nhân có thể bỏ cuộc bất cứ lúc nào

| Gói | Số lượng Talent | Phí tháng | Tính năng | Đối tượng phù hợp |
|------|-------------------|-------------|----------|----------------|
| **Starter (Khởi đầu)** | 1-10 talents | 4.990.000đ | - Quản lý danh sách cơ bản<br>- 50 lượt ứng tuyển/tháng<br>- Hỗ trợ tiêu chuẩn<br>- Thống kê cơ bản | Agency nhỏ, mới thành lập |
| **Professional (Chuyên nghiệp)** | 11-30 talents | 12.990.000đ | - Tất cả tính năng Starter<br>- 200 lượt ứng tuyển/tháng<br>- Trang giới thiệu agency<br>- Hỗ trợ ưu tiên<br>- Thống kê nâng cao<br>- Thao tác hàng loạt | Agency cỡ trung |
| **Enterprise (Doanh nghiệp)** | 31-100 talents | 29.990.000đ | - Tất cả tính năng Professional<br>- Không giới hạn ứng tuyển<br>- Tùy chỉnh thương hiệu<br>- Quản lý tài khoản riêng<br>- Truy cập API<br>- Tùy chọn white-label | Agency lớn |
| **Custom (Tùy chỉnh)** | 100+ talents | Báo giá riêng | - Tất cả tính năng Enterprise<br>- Tích hợp tùy chỉnh<br>- Cam kết SLA<br>- Đào tạo & hỗ trợ<br>- Tính năng riêng biệt | Agency rất lớn, mạng lưới |

**Ưu đãi thanh toán trước:**
- Trả trước 3 tháng: Giảm 5%
- Trả trước 6 tháng: Giảm 10%
- Trả trước 12 tháng: Giảm 20%

**Dịch vụ bổ sung (Add-ons):**

| Dịch vụ | Giá | Mô tả |
|--------|-------|-------------|
| **Thêm slot talent** | 200K/talent/tháng | Vượt quá giới hạn gói |
| **Huy hiệu Agency nổi bật** | 2M/tháng | Hiển thị ưu tiên trong danh sách agency |
| **Thống kê cao cấp** | 1M/tháng | Báo cáo chi tiết, xuất dữ liệu |
| **Thêm tài khoản quản lý** | 500K/người/tháng | Cho nhân viên agency thêm |
| **Ưu tiên ghép job** | 3M/tháng | Nhận thông báo job mới trước |

**Tại sao phân tầng như vậy?**

1. **Gói Starter (4.99M):** Giá thấp để thu hút agency nhỏ thử nghiệm. Họ sẽ nâng cấp khi thấy hiệu quả.
2. **Gói Professional (12.99M):** Đây là gói "sweet spot" - phù hợp với 70% agency, mang lại doanh thu ổn định.
3. **Gói Enterprise (29.99M):** Cho agency lớn, họ cần tính năng cao cấp và sẵn sàng trả nhiều hơn.
4. **Gói Custom:** Đàm phán riêng với các "cá voi" - agency có 100+ talents, có thể mang về 50-100M/tháng.

### **4.2. Mô hình Hoa hồng (Commission Structure) - Phương án thay thế**

**Áp dụng cho agency sử dụng hệ thống Escrow (Ký quỹ):**

Thay vì trả phí cố định hàng tháng, agency có thể chọn mô hình hoa hồng - nền tảng chỉ thu phí khi có giao dịch thành công.

**Bảng hoa hồng theo giá trị giao dịch:**

| Giá trị giao dịch | Hoa hồng nền tảng | Agency giữ lại |
|-------------------|-------------------|--------------|
| 0 - 10M | 8% | 92% |
| 10M - 50M | 7% | 93% |
| 50M - 100M | 6% | 94% |
| 100M+ | 5% | 95% |

**Ví dụ tính toán thực tế:**

```
Agency ABC có 20 booking trong tháng với tổng giá trị 150M:

Tính hoa hồng theo bậc thang:
- 10M đầu tiên: 10M × 8% = 800.000đ
- 40M tiếp theo (10M-50M): 40M × 7% = 2.800.000đ
- 50M tiếp theo (50M-100M): 50M × 6% = 3.000.000đ
- 50M còn lại (100M+): 50M × 5% = 2.500.000đ

Tổng hoa hồng nền tảng thu: 9.100.000đ
Agency nhận về: 140.900.000đ (94% tổng giá trị)
```

**Giải thích:**
- Hoa hồng giảm dần theo giá trị để khuyến khích agency làm nhiều việc hơn
- Agency lớn (doanh thu cao) sẽ trả % thấp hơn → động lực scale up
- Nền tảng vẫn có lợi vì tổng số tiền tăng lên

### **4.3. So sánh: Subscription vs Commission - Nên chọn mô hình nào?**

**Kịch bản: Agency cỡ trung với 25 talents**

| Mô hình | Doanh thu tháng | Ưu điểm | Nhược điểm |
|-------|----------------|------|------|
| **Chỉ Subscription** | 12.99M cố định | - Dự đoán được<br>- Không cần theo dõi giao dịch<br>- Đơn giản | - Tiềm năng doanh thu thấp<br>- Không liên kết với thành công |
| **Chỉ Commission** | 5-15M biến động | - Tăng theo thành công<br>- Tiềm năng cao hơn<br>- Động lực cùng phát triển | - Không dự đoán được<br>- Cần hệ thống Escrow<br>- Phức tạp hơn |
| **Hybrid (Kết hợp)** | 6.99M + 3-8M hoa hồng | - Cân bằng<br>- Có thu nhập cơ bản<br>- Vẫn có tiềm năng tăng | - Phức tạp hơn<br>- Khó giải thích |

**Khuyến nghị triển khai:**

**Giai đoạn MVP (Tháng 1-6):**
- Chỉ dùng **Subscription** để đơn giản hóa
- Tập trung vào việc thu hút agency tham gia
- Giá thấp để dễ thuyết phục (có thể giảm 50% cho early adopters)

**Giai đoạn Scale (Tháng 7+):**
- Thêm tùy chọn **Commission** cho agency muốn thử không rủi ro
- Hoặc chuyển sang **Hybrid** để tối ưu doanh thu
- Cho phép agency tự chọn mô hình phù hợp

**Tại sao bắt đầu với Subscription?**
1. **Dễ giải thích:** "Trả 12.99M/tháng, dùng thoải mái" - đơn giản, rõ ràng
2. **Dòng tiền ổn định:** Biết chắc mỗi tháng thu được bao nhiêu
3. **Không cần Escrow:** Tiết kiệm chi phí phát triển tính năng phức tạp
4. **Dễ kế toán:** Không phải theo dõi từng giao dịch, tính hoa hồng

### **4.4. Phân tích ROI cho Agency - Có đáng để tham gia không?**

**Case Study: Agency Professional Tier (25 talents)**

**Chi phí hàng tháng của Agency:**
- Phí nền tảng: 12.990.000đ
- Nhân sự (2 coordinator): 20.000.000đ
- Marketing: 5.000.000đ
- **Tổng chi phí: 37.990.000đ**

**Doanh thu (Kịch bản thực tế):**

Để có lãi, agency cần:
- 25 talents, tỷ lệ làm việc: 70% (17-18 người active)
- Giá trị booking trung bình: 8.000.000đ/talent/tháng
- Doanh thu gộp: 17.5 × 8M = 140.000.000đ/tháng
- Agency lấy hoa hồng: 30% = 42.000.000đ/tháng
- **Lợi nhuận ròng: 42M - 37.99M = 4.010.000đ/tháng** ✅

**Phân tích chi tiết:**

| Chỉ số | Giá trị | Giải thích |
|--------|---------|------------|
| **Break-even point** | 127M doanh thu gộp | Agency cần đạt 127M/tháng để hòa vốn |
| **Profit margin** | 9.5% | Lợi nhuận/Doanh thu agency |
| **ROI** | 10.6% | Lợi nhuận/Tổng chi phí |
| **Payback period** | 9.5 tháng | Thời gian hoàn vốn đầu tư ban đầu |

**Tại sao con số này hợp lý?**

1. **Tỷ lệ làm việc 70%:** Không phải lúc nào cũng có việc cho tất cả talents. 70% là con số thực tế.
2. **Booking 8M/talent/tháng:** Trung bình 2-3 job nhỏ hoặc 1 job lớn. Không quá cao, không quá thấp.
3. **Agency lấy 30%:** Đây là tỷ lệ chuẩn trong ngành. Talent nhận 70%, agency 30%.
4. **Lợi nhuận 4M/tháng:** Tuy không cao nhưng đủ để duy trì. Khi scale lên 50-100 talents, lợi nhuận sẽ tăng đáng kể.

**Khi nào Agency thấy đáng?**

✅ **Đáng tham gia khi:**
- Agency đã có sẵn 15+ talents
- Đang dùng Excel/WhatsApp để quản lý (mất thời gian)
- Muốn mở rộng quy mô
- Cần công cụ chuyên nghiệp để tăng uy tín

❌ **Chưa đáng khi:**
- Agency mới thành lập, chỉ có 3-5 talents
- Doanh thu hiện tại dưới 50M/tháng
- Chưa có quy trình quản lý rõ ràng

---

## **5. Quy trình Đăng ký & Xác minh Agency (Agency Onboarding & Verification)**

### **5.1. Quy trình Đăng ký từng bước**

**Tổng quan:** Từ khi agency đăng ký đến khi bắt đầu sử dụng mất khoảng 2-3 ngày làm việc.

```
Bước 1: Đăng ký ban đầu (5 phút)
  ├─ Tên công ty
  ├─ Loại hình (Agency, Quản lý, Studio)
  ├─ Thông tin người liên hệ
  └─ Xác minh Email + Số điện thoại
  ↓
Bước 2: Nộp hồ sơ xác minh (15 phút)
  ├─ Giấy phép kinh doanh
  ├─ Mã số thuế
  ├─ Giấy tờ chứng minh địa chỉ
  └─ Thông tin tài khoản ngân hàng
  ↓
Bước 3: Admin kiểm duyệt (24-48 giờ)
  ├─ Xác minh giấy tờ
  ├─ Tra cứu đăng ký kinh doanh
  ├─ Kiểm tra lý lịch
  └─ Phê duyệt/Từ chối
  ↓
Bước 4: Thiết lập tài khoản (10 phút)
  ├─ Chọn gói subscription
  ├─ Thiết lập phương thức thanh toán
  ├─ Tạo trang giới thiệu agency
  └─ Thêm thành viên team
  ↓
Bước 5: Import danh sách Talent (30 phút)
  ├─ Upload hàng loạt qua CSV
  ├─ Hoặc tạo từng profile thủ công
  └─ Phân quyền cho từng talent
  ↓
Bước 6: Đào tạo & Ra mắt (1 giờ)
  ├─ Hướng dẫn sử dụng nền tảng
  ├─ Tài liệu best practices
  ├─ Hỏi đáp
  └─ Chính thức hoạt động!
```

**Giải thích chi tiết từng bước:**

**Bước 1 - Đăng ký ban đầu:**
- Agency điền form đơn giản với thông tin cơ bản
- Hệ thống gửi OTP qua SMS và email để xác minh
- Tạo tài khoản tạm thời với trạng thái "Pending"

**Bước 2 - Nộp hồ sơ:**
- Agency upload các giấy tờ pháp lý (scan hoặc chụp ảnh)
- Hệ thống tự động OCR để đọc thông tin từ giấy phép kinh doanh
- Yêu cầu chuyển khoản thử 1.000đ để xác minh tài khoản ngân hàng

**Bước 3 - Kiểm duyệt:**
- Admin xem xét hồ sơ trong vòng 24-48 giờ
- Tra cứu mã số thuế trên website Tổng cục Thuế
- Gọi điện xác nhận địa chỉ văn phòng
- Kiểm tra portfolio có hợp lệ không (không phải ảnh đánh cắp)

**Bước 4 - Thiết lập:**
- Agency chọn gói phù hợp (Starter/Professional/Enterprise)
- Liên kết thẻ tín dụng hoặc tài khoản ngân hàng để thanh toán tự động
- Tùy chỉnh trang giới thiệu agency (logo, mô tả, portfolio)

**Bước 5 - Import talent:**
- Agency có thể upload file CSV với danh sách talent (tên, SĐT, email, chiều cao, số đo...)
- Hoặc tạo từng profile thủ công nếu số lượng ít
- Phân quyền: Talent có được đăng nhập xem lịch không? Hay chỉ là "ghost profile"?

**Bước 6 - Đào tạo:**
- Video hướng dẫn 15 phút về cách sử dụng dashboard
- Tài liệu PDF về best practices (cách viết mô tả, chụp ảnh đẹp, báo giá...)
- Session Q&A trực tiếp với support team

### **5.2. Giấy tờ Yêu cầu & Cách Xác minh**

**Danh sách giấy tờ bắt buộc:**

| Giấy tờ | Mục đích | Cách xác minh | Lưu trữ |
|----------|---------|-------------------|-----------|
| **Giấy phép kinh doanh** | Chứng minh pháp nhân hợp lệ | Tra cứu trên cơ sở dữ liệu Chính phủ | Vĩnh viễn |
| **Mã số thuế** | Tuân thủ thuế | Xác minh với Tổng cục Thuế | Vĩnh viễn |
| **Tài khoản ngân hàng** | Xử lý thanh toán | Chuyển khoản thử (1.000đ) | Đến khi đóng tài khoản |
| **CMND/CCCD người đại diện** | KYC tuân thủ | So khớp khuôn mặt + OCR | 2 năm sau khi đóng |
| **Địa chỉ văn phòng** | Xác minh liên hệ | Google Maps + gọi điện | Đến khi cập nhật |
| **Portfolio** | Giới thiệu công việc | Kiểm tra thủ công | Vĩnh viễn |

**Giải thích chi tiết:**

**1. Giấy phép kinh doanh:**
- Phải còn hiệu lực (chưa hết hạn)
- Tên công ty khớp với tất cả giấy tờ khác
- Ngành nghề kinh doanh phù hợp (dịch vụ quảng cáo, giải trí, người mẫu...)
- Hệ thống tự động OCR để đọc thông tin, sau đó admin kiểm tra lại

**2. Mã số thuế:**
- Định dạng đúng (10 chữ số)
- Tra cứu trên website Tổng cục Thuế để xác nhận công ty đang hoạt động
- Kiểm tra có nợ thuế không (nếu có API)

**3. Tài khoản ngân hàng:**
- Phải là tài khoản doanh nghiệp (không chấp nhận tài khoản cá nhân)
- Tên chủ tài khoản khớp với tên công ty
- Chuyển khoản thử 1.000đ với nội dung mã xác nhận, agency phải xác nhận đã nhận

**4. CMND/CCCD người đại diện:**
- Chụp rõ mặt trước/sau
- Hệ thống dùng AI so khớp khuôn mặt với ảnh selfie
- OCR để đọc thông tin (tên, số CMND, ngày sinh...)
- Lưu trữ mã hóa, chỉ admin cấp cao mới xem được

**5. Địa chỉ văn phòng:**
- Phải là địa chỉ thật (không phải P.O. Box)
- Kiểm tra trên Google Maps có tồn tại không
- Gọi điện xác nhận có người trả lời
- Có thể yêu cầu ảnh chụp văn phòng nếu nghi ngờ

**6. Portfolio:**
- Ít nhất 5-10 dự án đã làm
- Ảnh/video chất lượng cao
- Kiểm tra bằng Google Image Search để phát hiện ảnh đánh cắp
- Có thể yêu cầu link đến website/fanpage chính thức

### **5.3. Checklist Kiểm duyệt của Admin**

**Quy trình kiểm tra từng bước:**

```
☐ Giấy phép kinh doanh hợp lệ và chưa hết hạn
☐ Tên công ty khớp trên tất cả giấy tờ
☐ Mã số thuế đúng định dạng (10 chữ số)
☐ CMND/CCCD người đại diện đã xác minh
☐ Tài khoản ngân hàng thuộc về công ty (không phải cá nhân)
☐ Địa chỉ văn phòng thật (không phải P.O. Box)
☐ Số điện thoại liên lạc được
☐ Email domain khớp với công ty (ưu tiên)
☐ Không có cờ đỏ trong kiểm tra lý lịch
☐ Portfolio cho thấy công việc hợp pháp
```

**Các "Cờ đỏ" cần cảnh giác:**

| Cờ đỏ | Hành động | Lý do |
|----------|--------|--------|
| **Công ty mới đăng ký (<3 tháng)** | Yêu cầu thêm chứng cứ | Rủi ro gian lận cao |
| **Tài khoản ngân hàng cá nhân** | Từ chối | Không phải doanh nghiệp hợp pháp |
| **Địa chỉ giả** | Từ chối | Dấu hiệu gian lận |
| **Portfolio đáng ngờ** | Yêu cầu làm rõ | Ảnh có thể bị đánh cắp |
| **Đăng ký nhiều lần** | Đánh dấu để xem xét | Có thể trùng lặp |
| **Đã bị blacklist trước đây** | Tự động từ chối | Vi phạm trước đó |

**Giải thích chi tiết:**

**Công ty mới (<3 tháng):**
- Rủi ro: Có thể là công ty "ma" được thành lập để lừa đảo
- Hành động: Yêu cầu thêm giấy tờ chứng minh (hợp đồng thuê văn phòng, hóa đơn điện nước...)
- Hoặc yêu cầu đặt cọc trước khi kích hoạt

**Tài khoản cá nhân:**
- Rủi ro: Không phải doanh nghiệp thật, có thể là cá nhân giả mạo
- Hành động: Từ chối ngay, yêu cầu mở tài khoản doanh nghiệp

**Địa chỉ giả:**
- Rủi ro: Không thể liên lạc khi có vấn đề
- Cách phát hiện: Google Maps không có địa chỉ, hoặc gọi điện không ai trả lời
- Hành động: Từ chối, yêu cầu địa chỉ thật

**Portfolio đáng ngờ:**
- Rủi ro: Ảnh đánh cắp từ agency khác
- Cách phát hiện: Google Image Search tìm thấy ảnh giống hệt trên website khác
- Hành động: Yêu cầu chứng minh (hợp đồng với client, ảnh hậu trường...)

**Đăng ký nhiều lần:**
- Rủi ro: Cố tình tạo nhiều tài khoản để lợi dụng ưu đãi
- Cách phát hiện: Cùng số điện thoại, email, hoặc mã số thuế
- Hành động: Liên hệ để làm rõ, có thể là nhầm lẫn hoặc cố ý

**Đã bị blacklist:**
- Rủi ro: Đã vi phạm điều khoản trước đây (lừa đảo, bùng show, spam...)
- Hành động: Tự động từ chối, không cho đăng ký lại

### **5.4. Chỉ số Đánh giá Thành công Onboarding**

**Các KPI quan trọng để theo dõi:**

| Chỉ số | Mục tiêu | Hiện tại | Trạng thái |
|--------|--------|---------|--------|
| **Thời gian từ đăng ký đến phê duyệt** | <48 giờ | 36 giờ | ✅ Tốt |
| **Tỷ lệ phê duyệt** | 70-80% | 75% | ✅ Tốt |
| **Thời gian đến booking đầu tiên** | <14 ngày | 18 ngày | ⚠️ Cần cải thiện |
| **Tỷ lệ giữ chân 30 ngày** | >80% | 72% | ⚠️ Dưới mục tiêu |
| **Tỷ lệ giữ chân 90 ngày** | >60% | 58% | ⚠️ Gần đạt |

**Giải thích từng chỉ số:**

**1. Thời gian phê duyệt (36 giờ - Tốt):**
- Mục tiêu: Dưới 48 giờ để agency không phải chờ lâu
- Hiện tại: 36 giờ là tốt, cho thấy team admin làm việc hiệu quả
- Cải thiện: Có thể tự động hóa một số bước để giảm xuống 24 giờ

**2. Tỷ lệ phê duyệt (75% - Tốt):**
- Mục tiêu: 70-80% là hợp lý (không quá lỏng, không quá chặt)
- 75% nghĩa là 3/4 agency đăng ký được chấp nhận
- 25% bị từ chối do giấy tờ không hợp lệ hoặc cờ đỏ
- Nếu tỷ lệ quá cao (>90%): Có thể đang chấp nhận cả agency kém chất lượng
- Nếu tỷ lệ quá thấp (<50%): Tiêu chuẩn quá khắt khe, mất khách hàng tiềm năng

**3. Thời gian đến booking đầu tiên (18 ngày - Cần cải thiện):**
- Mục tiêu: Dưới 14 ngày (2 tuần)
- Hiện tại: 18 ngày là hơi lâu
- Nguyên nhân có thể:
  - Agency chưa quen cách sử dụng nền tảng
  - Chưa có đủ job phù hợp
  - Profile talent chưa đủ hấp dẫn
- Giải pháp:
  - Onboarding tốt hơn (video hướng dẫn, support 1-1)
  - Gợi ý job phù hợp ngay sau khi đăng ký
  - Hỗ trợ tối ưu profile trong tuần đầu

**4. Tỷ lệ giữ chân 30 ngày (72% - Dưới mục tiêu):**
- Mục tiêu: >80% agency còn active sau 1 tháng
- Hiện tại: 72% nghĩa là 28% agency rời bỏ sau tháng đầu
- Nguyên nhân:
  - Không có booking nào trong tháng đầu → thất vọng
  - Giao diện khó dùng
  - Giá quá cao so với giá trị nhận được
- Giải pháp:
  - Miễn phí tháng đầu để agency có thời gian thử nghiệm
  - Check-in định kỳ: Gọi điện hỏi thăm sau 1 tuần, 2 tuần
  - Tặng credit để đẩy profile lên top

**5. Tỷ lệ giữ chân 90 ngày (58% - Gần đạt):**
- Mục tiêu: >60% agency còn active sau 3 tháng
- Hiện tại: 58% là gần đạt, chấp nhận được
- Sau 3 tháng, agency đã có đủ thời gian đánh giá giá trị
- Những agency còn lại thường là khách hàng trung thành lâu dài

**Hành động cải thiện:**

1. **Giảm thời gian đến booking đầu:**
   - Gán account manager riêng cho agency mới
   - Gợi ý 5-10 job phù hợp ngay sau khi onboard
   - Tặng 3 lượt "Featured" miễn phí để tăng visibility

2. **Tăng retention 30 ngày:**
   - Miễn phí hoặc giảm 50% tháng đầu
   - Email/SMS nhắc nhở hàng tuần với tips sử dụng
   - Tổ chức webinar "How to succeed" cho agency mới

3. **Tăng retention 90 ngày:**
   - Chương trình loyalty: Giảm giá cho agency trung thành
   - Tính năng mới dựa trên feedback
   - Case study về agency thành công để truyền cảm hứng

---

## **6. Tính năng Dashboard cho Agency (Chi tiết)**

### **6.1. Quản lý Danh sách Talent (Talent Roster Management)**

**Giao diện Tổng quan Danh sách:**

```
┌─────────────────────────────────────────────────────────────┐
│ Danh sách Talent của tôi (25 người)                         │
├─────────────────────────────────────────────────────────────┤
│ [+ Thêm Talent] [Import CSV] [Xuất dữ liệu] [Thao tác hàng loạt] │
│                                                             │
│ Lọc: [Tất cả] [Đang hoạt động] [Tạm ngưng] [Rảnh] [Đã book] │
│ Sắp xếp: [Tên ▼] [Đánh giá] [Số booking] [Doanh thu]      │
│                                                             │
│ ┌──────────────────────────────────────────────────────┐  │
│ │ [Ảnh] Nguyễn Thị Lan                    ⭐ 4.8      │  │
│ │ Model | 24 tuổi | 168cm | TP.HCM                     │  │
│ │ 📊 15 bookings | 💰 45M doanh thu | 🟢 Rảnh         │  │
│ │ [Xem] [Sửa] [Lịch] [Thống kê] [Tạm ngưng]          │  │
│ └──────────────────────────────────────────────────────┘  │
│                                                             │
│ [20 người tiếp theo →]                                     │
└─────────────────────────────────────────────────────────────┘
```

**Giải thích chi tiết:**

**Thông tin hiển thị cho mỗi talent:**
- **Ảnh đại diện:** Ảnh profile chính, click để xem portfolio đầy đủ
- **Tên & thông tin cơ bản:** Tên, nghề nghiệp (Model/KOL/PG), tuổi, chiều cao, địa điểm
- **Đánh giá:** Điểm trung bình từ các client đã làm việc (1-5 sao)
- **Số booking:** Tổng số job đã hoàn thành (càng nhiều càng có kinh nghiệm)
- **Doanh thu:** Tổng tiền đã kiếm được cho agency (để đánh giá hiệu suất)
- **Trạng thái:** 
  - 🟢 Rảnh: Có thể nhận job ngay
  - 🟡 Đã book: Đang có job, nhưng vẫn có thể nhận thêm
  - 🔴 Bận: Không thể nhận job mới
  - ⚪ Tạm ngưng: Không hoạt động (nghỉ phép, ốm...)

**Phân quyền Quản lý Profile:**

| Trường thông tin | Agency kiểm soát | Talent kiểm soát | Ghi chú |
|-------|---------------|----------------|-------|
| **Thông tin cơ bản** | ✅ Sửa toàn bộ | ⚪ Chỉ xem | Tên, tuổi, số đo |
| **Ảnh/Video** | ✅ Upload/xóa | ⚠️ Chỉ đề xuất | Agency phê duyệt |
| **Giá cả** | ✅ Đặt giá | ❌ Không truy cập | Agency quyết định |
| **Lịch rảnh** | ✅ Quản lý | ⚠️ Xem + yêu cầu | Agency xác nhận |
| **Tiểu sử** | ✅ Sửa | ⚠️ Đề xuất | Agency phê duyệt |
| **Link mạng xã hội** | ⚪ Chỉ xem | ✅ Quản lý | Talent sở hữu |
| **Tài khoản ngân hàng** | ❌ Không truy cập | ❌ Không truy cập | Nền tảng giữ |

**Giải thích phân quyền:**

**Tại sao Agency kiểm soát giá cả?**
- Agency hiểu rõ thị trường và biết cách định giá cạnh tranh
- Tránh talent tự ý hạ giá để cạnh tranh không lành mạnh
- Đảm bảo tính nhất quán trong chiến lược giá của agency

**Tại sao Talent không truy cập tài khoản ngân hàng?**
- Tiền được chuyển về ví agency, sau đó agency tự chia cho talent
- Nền tảng không can thiệp vào việc chia tiền nội bộ
- Giảm phức tạp trong quản lý tài chính

**Thao tác Hàng loạt (Bulk Operations):**

```
Chọn nhiều talent (checkbox):
☑ Nguyễn Thị Lan
☑ Trần Minh Anh
☑ Lê Thu Hà
☐ Phạm Văn Nam
☐ ...

Hành động:
- Cập nhật trạng thái rảnh (tất cả đã chọn)
- Thay đổi giá (tất cả đã chọn)
- Gửi tin nhắn (tất cả đã chọn)
- Xuất dữ liệu (tất cả đã chọn)
- Tạm ngưng (tất cả đã chọn)
```

**Ví dụ sử dụng:**
- **Cập nhật hàng loạt:** Tết đến, tăng giá 20% cho tất cả talent
- **Gửi tin nhắn:** Thông báo lịch họp team cho 10 người cùng lúc
- **Tạm ngưng:** Khi có sự kiện lớn, tạm ngưng những người không phù hợp để tập trung vào talent phù hợp

### **6.2. Quản lý Booking Tập trung (Centralized Booking Management)**

**Quy trình Ứng tuyển Job:**

```
Job mới được đăng
  ↓
Agency thấy job trong feed
  ↓
Agency xem xét yêu cầu
  ↓
Agency chọn 3-5 talent phù hợp
  ↓
Agency gửi đơn ứng tuyển nhóm
  ↓
Client xem xét tất cả 5 profile
  ↓
Client chọn 2 talent
  ↓
Agency nhận thông báo
  ↓
Agency xác nhận lịch rảnh
  ↓
Booking được xác nhận
  ↓
Agency quản lý thực hiện
  ↓
Job hoàn thành
  ↓
Tiền về ví agency
```

**Giải thích từng bước:**

**1. Job mới được đăng:**
- Client (nhà tuyển dụng) đăng job với yêu cầu cụ thể
- Ví dụ: "Cần 3 PG cho sự kiện ra mắt iPhone 16, ngày 15/06, tại SECC Q7, budget 15M"

**2. Agency thấy job trong feed:**
- Hệ thống tự động gợi ý job phù hợp dựa trên:
  - Loại talent agency có (Model/PG/KOL)
  - Địa điểm (ưu tiên job gần)
  - Lịch sử làm việc (đã làm job tương tự)

**3. Agency xem xét yêu cầu:**
- Đọc kỹ job description
- Kiểm tra ngày giờ có conflict với job khác không
- Đánh giá budget có hợp lý không

**4. Agency chọn 3-5 talent phù hợp:**
- Không chỉ gửi 1 người (client muốn có lựa chọn)
- Không gửi quá nhiều (làm client choáng ngợp)
- Chọn những người có kinh nghiệm tương tự

**5. Agency gửi đơn ứng tuyển nhóm:**
- Đính kèm profile của 3-5 talent
- Viết cover letter ngắn giới thiệu
- Đề xuất giá (có thể thương lượng)

**6. Client xem xét và chọn:**
- Client xem profile, ảnh, video của từng người
- Chọn 2-3 người phù hợp nhất
- Có thể yêu cầu phỏng vấn trước

**7. Agency xác nhận:**
- Kiểm tra lại lịch rảnh của talent được chọn
- Xác nhận có thể tham gia
- Nếu có vấn đề, đề xuất người thay thế

**8. Thực hiện & thanh toán:**
- Agency quản lý talent đến đúng giờ
- Theo dõi quá trình làm việc
- Sau khi hoàn thành, tiền được chuyển về ví agency

**Dashboard Quản lý Booking:**

```
┌─────────────────────────────────────────────────────────────┐
│ Booking Đang hoạt động (12)                                 │
├─────────────────────────────────────────────────────────────┤
│ Sắp tới (8) | Đang diễn ra (2) | Hoàn thành (2) | Đã hủy   │
│                                                             │
│ ┌──────────────────────────────────────────────────────┐  │
│ │ Sự kiện Ra mắt iPhone 16                             │  │
│ │ 📅 15/06/2026 | 📍 SECC, Q7 | 💰 15M                 │  │
│ │ Talents: Lan, Anh, Hà (3 người)                      │  │
│ │ Trạng thái: ⏰ Sắp tới (còn 5 ngày)                  │  │
│ │ [Chi tiết] [Nhắn tin Client] [Quản lý Talents]      │  │
│ └──────────────────────────────────────────────────────┘  │
│                                                             │
│ ┌──────────────────────────────────────────────────────┐  │
│ │ Chụp ảnh Sản phẩm                                    │  │
│ │ 📅 25/05/2026 | 📍 Studio A | 💰 8M                  │  │
│ │ Talents: Nam (1 người)                               │  │
│ │ Trạng thái: 🔴 Đang diễn ra (Hôm nay)               │  │
│ │ [Check-in] [Upload ảnh] [Hoàn thành]                │  │
│ └──────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────┘
```

**Thống kê Booking:**

| Chỉ số | Tháng này | Tháng trước | Thay đổi |
|--------|-----------|------------|--------|
| **Tổng Bookings** | 28 | 24 | +16.7% |
| **Tổng Doanh thu** | 140M | 120M | +16.7% |
| **Giá trị TB/Booking** | 5M | 5M | 0% |
| **Tỷ lệ Sử dụng** | 70% | 65% | +5% |
| **Tỷ lệ Hủy** | 5% | 8% | -3% |
| **Hài lòng Client** | 4.7/5 | 4.6/5 | +0.1 |

**Giải thích các chỉ số:**

**Tỷ lệ Sử dụng (Utilization Rate):**
- Công thức: (Số ngày làm việc / Tổng số ngày có thể làm) × 100%
- Ví dụ: 25 talents × 30 ngày = 750 ngày có thể làm
- Thực tế làm: 525 ngày → 70% utilization
- Càng cao càng tốt (nghĩa là talent ít thời gian rảnh)

**Tỷ lệ Hủy (Cancellation Rate):**
- Công thức: (Số booking bị hủy / Tổng booking) × 100%
- 5% là tốt (nghĩa là 95% booking thành công)
- Nếu >10%: Có vấn đề (talent bùng show, client hủy phút chót...)

**Hài lòng Client:**
- Điểm đánh giá trung bình từ client sau mỗi job
- 4.7/5 là rất tốt (tương đương 94%)
- Nếu <4.0: Cần cải thiện chất lượng dịch vụ

### **6.3. Agency Wallet & Financial Management**

**Wallet Structure:**

```
Agency Wallet
├── Available Balance: 45.000.000đ
│   └── Can withdraw to bank
│
├── Pending Balance: 15.000.000đ
│   └── Jobs in progress, not yet completed
│
├── Escrow Balance: 30.000.000đ
│   └── Jobs confirmed, waiting for completion
│
└── Total: 90.000.000đ
```

**Transaction History:**

| Date | Type | Description | Amount | Balance |
|------|------|-------------|--------|---------|
| 25/05 16:00 | Credit | Job completed: iPhone Launch | +15.000.000đ | 45M |
| 25/05 14:00 | Debit | Platform fee (10%) | -1.500.000đ | 30M |
| 24/05 10:00 | Escrow | Job confirmed: Photoshoot | -8.000.000đ | 31.5M |
| 23/05 09:00 | Withdrawal | To bank account | -20.000.000đ | 39.5M |

**Withdrawal Process:**

```
Step 1: Request Withdrawal
  - Minimum: 1.000.000đ
  - Maximum: Available balance
  - Bank account (pre-verified)
  ↓
Step 2: Platform Review (Auto for <10M, Manual for >10M)
  - Check for disputes
  - Verify bank details
  - Approve/Reject
  ↓
Step 3: Processing
  - Transfer to bank (1-2 business days)
  - Send confirmation email
  ↓
Step 4: Completed
  - Update wallet balance
  - Generate receipt
```

**Financial Reports:**

```
Monthly Financial Report - May 2026

Revenue Breakdown:
├── Gross Revenue: 150.000.000đ
├── Platform Commission (10%): -15.000.000đ
├── Refunds: -2.000.000đ
└── Net Revenue: 133.000.000đ

By Talent:
1. Nguyễn Thị Lan: 45M (30%)
2. Trần Minh Anh: 32M (21%)
3. Lê Thu Hà: 28M (19%)
4. Others: 45M (30%)

By Job Type:
1. Events: 80M (53%)
2. Photoshoots: 40M (27%)
3. Videos: 20M (13%)
4. Other: 10M (7%)

Expenses:
├── Platform Fee: 15M
├── Staff Salaries: 20M
├── Marketing: 5M
└── Total: 40M

Net Profit: 93M
```

### **6.4. Agency Landing Page**

**Public Agency Profile:**

```
URL: platform.com/agency/abc-models

┌─────────────────────────────────────────────────────────────┐
│ [Logo] ABC Models Agency                    ⭐ 4.8 (120)   │
├─────────────────────────────────────────────────────────────┤
│ About Us:                                                   │
│ Leading model management agency in Vietnam with 10+ years  │
│ experience. Representing 50+ professional models and        │
│ influencers.                                                │
│                                                             │
│ 📊 Stats:                                                   │
│ • 50 Talents                                                │
│ • 500+ Completed Projects                                   │
│ • 200+ Happy Clients                                        │
│ • 4.8★ Average Rating                                       │
│                                                             │
│ 📸 Featured Talents:                                        │
│ [Grid of top 12 talents with photos]                       │
│                                                             │
│ 🏆 Recent Projects:                                         │
│ • Vietnam Fashion Week 2026                                 │
│ • Samsung Galaxy Launch                                     │
│ • Vinamilk TVC Campaign                                     │
│                                                             │
│ 📞 Contact:                                                 │
│ • Email: contact@abcmodels.com                             │
│ • Phone: 0901234567                                         │
│ • Address: 123 Nguyen Hue, Q1, TP.HCM                      │
│                                                             │
│ [Book This Agency] [View All Talents] [Contact]            │
└─────────────────────────────────────────────────────────────┘
```

**SEO Optimization:**

- Custom URL slug
- Meta description
- Open Graph tags
- Schema.org markup
- Sitemap inclusion

**Analytics:**

| Metric | This Month | Last Month |
|--------|-----------|------------|
| **Page Views** | 1,234 | 980 |
| **Unique Visitors** | 567 | 445 |
| **Avg Time on Page** | 3:45 | 3:12 |
| **Bounce Rate** | 35% | 42% |
| **Inquiries** | 45 | 38 |
| **Conversion Rate** | 7.9% | 8.5% |

---

> **📌 Lưu ý:** Chi tiết kỹ thuật về Database Schema, API Endpoints, và Permission System đã được tách sang tài liệu riêng tại: [`/docs/for-tech/plans/Agency-Module-Technical-Specs.md`](../../for-tech/plans/Agency-Module-Technical-Specs.md)

---

## **8. Success Stories & Case Studies**

### **8.1. Case Study: Elite Models Vietnam**

**Background:**
- Established agency with 35 models
- Previously using Excel + WhatsApp
- 15-20 bookings per month
- Revenue: ~80M/month

**Implementation:**
- Onboarded in Week 1 of platform launch
- Migrated all 35 models in 2 days
- Trained 3 staff members
- Chose Professional tier (12.99M/month)

**Results after 6 months:**

| Metric | Before | After | Change |
|--------|--------|-------|--------|
| **Bookings/month** | 18 | 42 | +133% |
| **Revenue/month** | 80M | 185M | +131% |
| **Time spent on admin** | 40 hours | 12 hours | -70% |
| **Client satisfaction** | 4.2/5 | 4.8/5 | +14% |
| **Talent utilization** | 45% | 72% | +60% |

**ROI:**
- Platform cost: 12.99M/month
- Additional revenue: 105M/month
- ROI: 808%

**Testimonial:**
> "Platform này đã thay đổi hoàn toàn cách chúng tôi vận hành. Trước đây mất cả ngày để quản lý lịch và tìm việc cho models, giờ chỉ mất vài giờ. Doanh thu tăng gấp đôi trong 6 tháng!" - Nguyễn Văn A, CEO Elite Models

### **8.2. Case Study: Startup Agency**

**Background:**
- New agency, just 8 models
- Founder working solo
- 5-8 bookings per month
- Revenue: ~25M/month

**Implementation:**
- Started with Starter tier (4.99M/month)
- Built roster from scratch on platform
- Used platform to attract new talents

**Results after 3 months:**

| Metric | Before | After | Change |
|--------|--------|-------|--------|
| **Roster size** | 8 | 15 | +88% |
| **Bookings/month** | 6 | 18 | +200% |
| **Revenue/month** | 25M | 65M | +160% |
| **Profit margin** | 15% | 28% | +87% |

**Key Success Factors:**
- Professional agency landing page attracted new talents
- Centralized booking system saved time
- Analytics helped optimize pricing
- Verified badge increased trust

---

**Kết luận:** Module Agency Management biến nền tảng từ B2C thành B2B2C, mở ra nguồn doanh thu mới và tăng tốc độ tăng trưởng. Với pricing linh hoạt, features toàn diện, và ROI rõ ràng, agencies có động lực mạnh để tham gia. Technical implementation được thiết kế để scale, và case studies thực tế chứng minh giá trị của module này.