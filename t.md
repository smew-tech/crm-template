### **Mô tả Giao diện Dashboard Quản lý Dịch vụ/Tài chính**

Đây là giao diện của một trang tổng quan (dashboard) dành cho người dùng, được thiết kế theo phong cách tối giản, sạch sẽ và hiện đại. Giao diện sử dụng các thẻ (card) bo góc trên nền xám nhạt, tạo cảm giác phân chia rõ ràng giữa các khu vực chức năng.

Dưới đây là phân tích chi tiết từng thành phần từ trên xuống dưới:

#### **1. Khu vực Tóm tắt Trạng thái Đơn hàng**
Nằm ở trên cùng, khu vực này gồm 4 thẻ nhỏ, cung cấp cái nhìn tổng quan nhanh về quy trình vận chuyển hoặc xử lý đơn hàng. Mỗi thẻ có một biểu tượng và tiêu đề tương ứng:
* **Chờ thanh toán:** `0 đơn hàng`
* **Đến Việt Nam:** `0 đơn hàng`
* **Chờ tất toán:** `0 đơn hàng`
* **Đang được giao:** `0 đơn hàng`

=> **Mục đích:** Giúp người dùng nắm bắt nhanh chóng số lượng đơn hàng ở từng giai đoạn quan trọng.

#### **2. Khu vực Gói dịch vụ & Nâng cấp**
Đây là một thẻ lớn, nổi bật, giới thiệu về gói dịch vụ hiện tại của người dùng.
* **Tiêu đề:** **Gói đấu giá**
* **Cấp độ:** **VIP 2**
* **Mô tả:** "Tối đa 1000 phiên đấu giá cùng thời điểm" - Cho biết quyền lợi của gói.
* **Hành động:** Nút **"Nâng cấp"** màu đỏ, khuyến khích người dùng chuyển sang gói cao hơn.

=> **Mục đích:** Thông báo cho người dùng về cấp độ tài khoản và quyền lợi, đồng thời là một lời kêu gọi hành động (Call-to-Action) để nâng cấp dịch vụ.

#### **3. Khu vực Thông tin Hỗ trợ (Tư vấn viên)**
Thẻ này cung cấp thông tin liên hệ trực tiếp đến nhân viên hỗ trợ được chỉ định cho tài khoản.
* **Tiêu đề:** **Tư vấn viên**
* **Tên & SĐT:** Cẩm Tú - 0346.691.423
* **Hành động:**
    * **Đổi nhân viên:** Cho phép thay đổi người hỗ trợ.
    * **Đánh giá:** Để lại phản hồi về chất lượng dịch vụ.
    * **Liên hệ:** Nút màu đỏ nổi bật để bắt đầu cuộc gọi hoặc chat.

=> **Mục đích:** Tạo sự tin tưởng và cá nhân hóa trải nghiệm, giúp người dùng dễ dàng kết nối với người hỗ trợ khi cần.

#### **4. Khu vực Quản lý Ví điện tử (Ví ODN)**
Đây là khu vực quản lý tài chính chính của người dùng trên nền tảng.
* **Tiêu đề:** **Ví ODN** (có biểu tượng làm mới - refresh)
* **Thông tin tỷ giá:** "Tỷ giá: 1JPY = 190 VNĐ" - Cung cấp thông tin quan trọng cho các giao dịch quốc tế.
* **Các loại số dư:**
    * **Số dư:** 0đ
    * **Đóng băng:** 0đ (Thường là số tiền đang bị tạm giữ trong một giao dịch)
    * **Khả dụng:** 0đ (Số tiền thực tế có thể sử dụng)
* **Hành động:** Nút **"+ Nạp thêm"** màu đỏ, là lối tắt để người dùng nạp tiền vào ví.

=> **Mục đích:** Cung cấp thông tin minh bạch về tài chính và là cổng chính cho các hoạt động nạp/rút tiền.

#### **5. Khu vực Lịch sử Giao dịch**
Nằm ở cuối cùng, khu vực này hiển thị các giao dịch gần nhất.
* **Tiêu đề:** **Lịch sử giao dịch**
* **Hành động:** "Xem tất cả" để truy cập trang lịch sử chi tiết hơn.
* **Bảng giao dịch:**
    * **Thời gian:** Ngày giờ giao dịch.
    * **Số tiền:**
        * `-2,000,000` (màu xám): Giao dịch chi tiêu/trừ tiền.
        * `+2,000,000` (màu xanh lá): Giao dịch nạp tiền/cộng tiền.
    * **Ghi chú:** Mô tả chi tiết nội dung giao dịch (ví dụ: "Kích hoạt đấu giá VIP 2", "Nạp tiền theo số điện thoại...").

=> **Mục đích:** Giúp người dùng theo dõi và đối soát các dòng tiền ra vào tài khoản một cách rõ ràng.