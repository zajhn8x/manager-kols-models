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