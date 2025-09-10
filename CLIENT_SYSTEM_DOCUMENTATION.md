# CLIENT SYSTEM DOCUMENTATION - eShopGlobal

## 📋 TỔNG QUAN HỆ THỐNG

Hệ thống quản lý khách hàng cho dịch vụ mua hộ và đấu giá quốc tế, kết nối người dùng Việt Nam với các sàn thương mại điện tử quốc tế như Amazon, Yahoo Auctions, Mercari.

## 🏗️ CẤU TRÚC MODULE

### 1. DASHBOARD (_client-dashboard.html)
**Mục đích:** Trang tổng quan cho khách hàng

**Tính năng chính:**
- **Thống kê tổng quan:**
  - Số dư ví khả dụng
  - Số đơn hàng đang xử lý
  - Số kiện hàng chờ
  - Thông báo chưa đọc
  
- **Quick Actions:**
  - Tạo đơn hàng mới
  - Nạp tiền vào ví
  - Rút tiền
  - Theo dõi đơn hàng
  
- **Recent Activities:**
  - Đơn hàng gần đây (bảng)
  - Lịch sử giao dịch gần đây
  - Thông báo mới nhất

- **Modals:**
  - Modal nạp tiền (QR code + thông tin chuyển khoản)
  - Modal tạo đơn hàng nhanh

### 2. ACCOUNT MANAGEMENT (_client-account.html)
**Mục đích:** Quản lý thông tin tài khoản cá nhân

**Tính năng chính:**
- **Hồ sơ cá nhân:**
  - Upload ảnh đại diện
  - Cập nhật thông tin: họ tên, email, SĐT, ngày sinh
  
- **Sổ địa chỉ:**
  - Thêm/sửa/xóa địa chỉ giao hàng
  - Đặt địa chỉ mặc định
  
- **Tài khoản ngân hàng:**
  - Thêm tài khoản ngân hàng
  - Xác thực tài khoản
  - Quản lý danh sách tài khoản
  
- **Đổi mật khẩu:**
  - Form đổi mật khẩu 3 trường
  
- **Cài đặt thông báo:**
  - Toggle nhận thông báo qua email
  - Cài đặt loại thông báo

### 3. WALLET MANAGEMENT (_client-wallet.html)
**Mục đích:** Quản lý ví tiền điện tử nội bộ

**Tính năng chính:**
- **Thông tin ví:**
  - Số dư khả dụng: 15,750,000 ₫
  - Số dư đóng băng: 2,500,000 ₫
  
- **Tab Lịch sử giao dịch:**
  - Bộ lọc: mã GD, loại, trạng thái, ngày
  - Bảng chi tiết giao dịch
  - Trạng thái: Hoàn thành/Đang xử lý/Bị từ chối
  
- **Tab Nạp tiền:**
  - Form tạo lệnh nạp tiền
  - Gợi ý số tiền nhanh
  - Hiển thị QR code + thông tin chuyển khoản
  - Danh sách lệnh đang chờ xử lý
  
- **Tab Rút tiền:**
  - Form yêu cầu rút tiền
  - Chọn tài khoản ngân hàng đã liên kết
  - Thời gian xử lý: 24h

### 4. ORDER MANAGEMENT (_client-order.html)
**Mục đích:** Quản lý toàn bộ đơn hàng

**Tính năng chính:**
- **Trạng thái đơn hàng (11 trạng thái):**
  1. Chờ xác nhận (từ Admin)
  2. Đã đặt cọc
  3. Xác nhận
  4. Đã mua
  5. Đã mua hàng
  6. Kho Nhật
  7. Vận chuyển VN
  8. Kho Việt
  9. Sẵn sàng giao
  10. Đã giao
  11. Tất cả
  
- **Thông tin đơn hàng:**
  - Mã đơn, ngày tạo
  - Hình ảnh, tên sản phẩm
  - Phương thức (Mua thẳng/Đấu giá)
  - Tổng tiền, tiền cọc
  
- **Tính năng đặc biệt:**
  - Đơn được tạo bởi Admin (có badge)
  - Khách hàng xác nhận/từ chối đơn Admin tạo
  - Link thanh toán cọc cho đơn chưa thanh toán

### 5. CREATE ORDER (_client-create-order.html)
**Mục đích:** Tạo đơn hàng mua hộ mới

**Tính năng chính:**
- **Chọn sàn TMĐT:**
  - Amazon JP
  - Yahoo Auctions
  - Mercari JP
  - All website JP
  
- **Form đơn hàng:**
  - Thêm nhiều link sản phẩm
  - Nhập thông tin: tên, số lượng, đơn giá, phụ phí
  - Ghi chú (màu sắc, size)
  
- **Tính toán tự động:**
  - Tổng tiền JPY
  - Quy đổi VND (tỷ giá 165)
  - Phí mua hộ 4%
  - Tiền cọc 50%
  
- **Import/Export:**
  - Nhập từ Excel
  - Tải file mẫu

### 6. ORDER DETAIL (_client-order-detail.html)
**Mục đích:** Xem chi tiết một đơn hàng

**Tính năng chính:**
- **Timeline đơn hàng:**
  - Trạng thái hiện tại
  - Lịch sử các mốc thời gian
  - Dự kiến thời gian hoàn thành
  
- **Thông tin kiện hàng:**
  - Mã kiện
  - Cân nặng
  - Tracking number (có link)
  
- **Chi tiết tài chính:**
  - Tiền hàng
  - Phí mua hộ 5%
  - Phí ship nội địa
  - Phí vận chuyển quốc tế
  - Tổng tiền
  - Đã cọc
  - Còn lại phải trả
  
- **Danh sách sản phẩm:**
  - Hình ảnh, tên, số lượng, giá
  
- **Chat với admin:**
  - Trao đổi real-time
  - Lịch sử tin nhắn

### 7. WAREHOUSE (_client-store.html)
**Mục đích:** Quản lý kho hàng và yêu cầu giao hàng

**Tính năng chính:**
- **Tab Hàng tại kho VN:**
  - Danh sách sản phẩm đã về kho
  - Checkbox chọn nhiều sản phẩm
  - Tạo đơn giao hàng gộp
  
- **Tab Đơn đã giao:**
  - Lịch sử đơn giao hàng
  - Tracking giao hàng nội địa
  
- **Modal thanh toán giao hàng:**
  - Chọn địa chỉ nhận
  - Chọn đơn vị vận chuyển (GHTK, Viettel Post, J&T)
  - Tính phí giao hàng tự động

### 8. AUCTION (_client-auction.html)
**Mục đích:** Quản lý đấu giá trên Yahoo Auctions

**Tính năng chính:**
- **Tab phân loại:**
  - Đang tham gia
  - Đã thắng
  - Đã thua
  
- **Thông tin phiên đấu giá:**
  - Hình ảnh, tên sản phẩm
  - Thông tin người bán (rating)
  - Giá hiện tại
  - Giá của khách hàng
  - Thời gian còn lại (đếm ngược real-time)
  - Trạng thái: Đang dẫn đầu/Bị vượt qua
  
- **Quick action:**
  - Đặt giá/Đặt lại giá
  - Link đến trang chi tiết

### 9. AUCTION DETAIL (_client-auction-detail.html)
**Mục đích:** Chi tiết và đặt giá cho một phiên đấu giá

**Tính năng chính:**
- **Thông tin sản phẩm:**
  - Hình ảnh lớn
  - Mô tả chi tiết
  - Link gốc Yahoo Auctions
  
- **Thông tin đấu giá:**
  - Giá hiện tại
  - Người giữ giá
  - Countdown timer (real-time)
  - Thời gian kết thúc
  
- **Form đặt giá:**
  - Nhập Max Bid (giá tối đa)
  - Auto-bid system
  - Kiểm tra số dư ví
  - Tính tiền cọc 10%
  
- **Lịch sử bid:**
  - Danh sách các lần đặt giá
  - Highlight bid của user

## 🎨 UI/UX COMPONENTS

### Shared Components:
- **Sidebar Navigation:**
  - Logo + tên hệ thống
  - 6 menu items với icon
  - Active state highlight
  - Logout button

- **Top Header:**
  - Tiêu đề trang
  - User info (avatar + name + role)
  - Notification badge

- **Color Scheme:**
  - Primary: Blue (#2563eb)
  - Success: Green
  - Warning: Yellow/Orange
  - Danger: Red
  - Background: Gray (#f3f4f6)

- **Status Badges:**
  - Màu sắc theo trạng thái
  - Rounded pills style
  - Font size nhỏ

### Interactive Elements:
- **Modals:**
  - Overlay backdrop
  - Close button (X)
  - Cancel/Confirm buttons
  - Click outside to close

- **Forms:**
  - Floating labels
  - Required field indicators (*)
  - Validation states
  - Help text

- **Tables:**
  - Striped rows
  - Hover effects
  - Sortable headers
  - Pagination (implied)

- **Real-time Updates:**
  - Countdown timers
  - Auto-refresh data
  - Live chat

## 🔧 TECHNICAL DETAILS

### Frontend Stack:
- **HTML5** - Structure
- **Tailwind CSS** (CDN) - Styling
- **Font Awesome** - Icons
- **Vanilla JavaScript** - Interactions

### Key JavaScript Features:
- Tab switching
- Modal controls
- Form calculations
- Countdown timers
- Dynamic content updates
- Local state management

### Data Patterns:
- Mock data trong JavaScript
- Currency formatting (VND, JPY)
- Date/time formatting
- Status mapping

## 📊 BUSINESS LOGIC

### Pricing Structure:
- **Phí mua hộ:** 4-5%
- **Tỷ giá JPY-VND:** 165
- **Tiền cọc đơn hàng:** 50%
- **Tiền cọc đấu giá:** 10%
- **Phí giao hàng nội địa:** 30,000-45,000 VND

### Order Flow:
1. Khách tạo đơn/Admin tạo đơn
2. Khách xác nhận (nếu Admin tạo)
3. Đặt cọc 50%
4. Mua hàng
5. Hàng về kho nước ngoài
6. Vận chuyển quốc tế
7. Hàng về kho VN
8. Thanh toán phần còn lại
9. Giao hàng nội địa
10. Hoàn thành

### Wallet System:
- Nạp tiền qua chuyển khoản ngân hàng
- Mã nội dung bắt buộc
- Rút tiền trong 24h
- Đóng băng tiền khi có giao dịch

## 🔐 SECURITY & PERMISSIONS

### User Capabilities:
- Xem thông tin cá nhân
- Quản lý đơn hàng của mình
- Nạp/rút tiền
- Đặt giá đấu giá
- Chat với admin
- Xác nhận/từ chối đơn Admin tạo

### Restrictions:
- Email không thể chỉnh sửa
- Không thể xóa đơn hàng
- Không thể thay đổi tỷ giá
- Giới hạn rút tiền theo số dư

## 📱 RESPONSIVE DESIGN

- Mobile-first approach
- Grid system với breakpoints
- Collapsible sidebar (implied)
- Touch-friendly buttons
- Scrollable areas cho mobile

## 🚀 RECOMMENDATIONS FOR REBUILD

### UI/UX Improvements:
1. **Modern Design System:**
   - Consistent spacing scale
   - Better typography hierarchy
   - Smoother animations
   - Better loading states

2. **Enhanced Components:**
   - Advanced data tables with filtering
   - Better form validation
   - Rich text editor for chat
   - Image gallery với zoom

3. **User Experience:**
   - Progressive disclosure
   - Better error handling
   - Success feedback
   - Tooltips for complex features

### Technical Improvements:
1. **Architecture:**
   - Component-based structure
   - State management (Redux/Context)
   - API integration layer
   - WebSocket for real-time

2. **Performance:**
   - Code splitting
   - Lazy loading
   - Image optimization
   - Caching strategies

3. **Accessibility:**
   - ARIA labels
   - Keyboard navigation
   - Screen reader support
   - High contrast mode

### New Features to Consider:
- Push notifications
- Multi-language support
- Dark mode
- Export reports (PDF/Excel)
- Advanced search/filters
- Wishlist/Favorites
- Price alerts for auctions
- Bulk operations