# Danh sách chức năng hoàn chỉnh cho REBO

## 1. Phạm vi hệ thống

REBO là hệ thống đặt chỗ nhà hàng cho 3 nhóm người dùng chính:

- Chủ nhà hàng
- Người dùng đặt chỗ
- Quản trị viên (Admin)

## 2. Chức năng cho người dùng đặt chỗ

### 2.1. Tài khoản người dùng

- Đăng ký tài khoản
- Đăng nhập, đăng xuất
- Cập nhật thông tin cá nhân
- Xem lịch sử đặt bàn

### 2.2. Tìm kiếm và xem nhà hàng

- Xem danh sách nhà hàng đang hoạt động
- Tìm kiếm nhà hàng theo tên
- Lọc nhà hàng theo địa chỉ/khu vực
- Tìm kiếm món ăn => nhà hàng
- Xem chi tiết nhà hàng
- Xem mô tả nhà hàng
- Xem thời gian mở cửa và đóng cửa
- Xem loại bàn hiện có
- Xem sức chứa của từng loại bàn
- Xem giá đặt bàn
- Xem danh sách món ăn của nhà hàng
- Xem đánh giá và bình luận từ người dùng khác

### 2.3. Đặt bàn

- Chọn nhà hàng và loại bàn muốn đặt
- Chọn ngày và giờ đặt bàn
- Nhập số lượng người đi ăn
- Tính phụ thu khi số người vượt mức cơ bản của bàn
- Kiểm tra tình trạng còn chỗ theo thời gian đặt
- Xác nhận thông tin đặt bàn trước khi thanh toán
- Tạo đơn đặt bàn
- Nhận trạng thái đặt bàn: chờ xác nhận, đã xác nhận, đã huỷ, đã hoàn tất

### 2.4. Thanh toán

- Thanh toán tiền đặt chỗ
- Hiển thị tổng chi phí gồm giá đặt bàn và phụ thu
- Xem trạng thái thanh toán
- Lưu lịch sử thanh toán theo đơn đặt bàn

### 2.5. Quản lý đơn đặt bàn

- Xem danh sách đơn đặt bàn của mình
- Xem chi tiết từng đơn đặt bàn
- Huỷ đơn đặt bàn trong điều kiện cho phép
- Theo dõi trạng thái xử lý của đơn đặt bàn

### 2.6. Đánh giá và phản hồi

- Gửi đánh giá bằng số sao
- Gửi bình luận sau khi sử dụng dịch vụ
- Xem lại đánh giá đã gửi
- Chỉnh sửa hoặc xoá đánh giá của mình trong điều kiện cho phép

### 2.7. Khiếu nại

- Gửi khiếu nại liên quan đến nhà hàng hoặc đơn đặt bàn
- Theo dõi trạng thái xử lý khiếu nại
- Xem phản hồi từ Admin

## 3. Chức năng cho chủ nhà hàng

### 3.1. Tài khoản chủ nhà hàng

- Đăng ký tài khoản chủ nhà hàng
- Đăng nhập, đăng xuất
- Cập nhật thông tin liên hệ

### 3.2. Đăng ký và quản lý nhà hàng

- Tạo hồ sơ nhà hàng
- Nhập tên nhà hàng
- Nhập địa chỉ nhà hàng
- Nhập mô tả nhà hàng
- Thiết lập thời gian mở cửa và đóng cửa
- Cập nhật thông tin nhà hàng
- Tạm ngừng hoặc mở lại trạng thái hoạt động của nhà hàng

### 3.3. Quản lý loại bàn

- Thêm loại bàn
- Cập nhật loại bàn
- Xoá loại bàn
- Khai báo số lượng bàn theo từng loại
- Khai báo sức chứa/số người tối đa cho từng loại bàn
- Khai báo giá đặt cho từng loại bàn

### 3.4. Quản lý thực đơn

- Thêm món ăn vào danh sách món ăn của nhà hàng
- Cập nhật thông tin món ăn
- Xoá món ăn khỏi thực đơn
- Hiển thị danh sách món ăn cho người dùng xem

### 3.5. Quản lý đặt chỗ

- Nhận thông báo khi có đơn đặt bàn mới
- Xem danh sách đơn đặt bàn
- Xem chi tiết đơn đặt bàn
- Xác nhận hoặc từ chối đơn đặt bàn
- Cập nhật trạng thái đơn: chờ xác nhận, đã xác nhận, đã phục vụ, đã huỷ
- Quản lý số lượng chỗ trống theo khung giờ

### 3.6. Quản lý đánh giá

- Xem đánh giá và bình luận của người dùng
- Phản hồi đánh giá nếu hệ thống cho phép

### 3.7. Xác thực nhà hàng

- Tải lên giấy phép kinh doanh và giấy tờ liên quan
- Gửi yêu cầu xác thực nhà hàng
- Theo dõi trạng thái xác thực: chờ duyệt, đã duyệt, bị từ chối
- Nhận lý do từ chối và bổ sung hồ sơ khi cần

## 4. Chức năng cho Admin

### 4.1. Quản lý người dùng và chủ nhà hàng

- Xem danh sách tài khoản người dùng
- Xem danh sách tài khoản chủ nhà hàng
- Khoá hoặc mở khoá tài khoản vi phạm

### 4.2. Quản lý nhà hàng

- Xem danh sách tất cả nhà hàng
- Xem chi tiết hồ sơ nhà hàng
- Chỉnh sửa thông tin nhà hàng khi cần
- Xoá nhà hàng vi phạm hoặc không hợp lệ
- Duyệt hoặc từ chối nhà hàng trước khi hiển thị công khai

### 4.3. Xác thực hồ sơ pháp lý

- Xem hồ sơ giấy phép kinh doanh do chủ nhà hàng cung cấp
- Kiểm tra tính hợp lệ của giấy tờ
- Phê duyệt hoặc từ chối xác thực
- Gửi phản hồi cho chủ nhà hàng khi hồ sơ chưa hợp lệ

### 4.4. Quản lý khiếu nại

- Xem danh sách khiếu nại
- Phân loại khiếu nại theo trạng thái
- Xem nội dung khiếu nại và thông tin liên quan
- Phản hồi hoặc xử lý khiếu nại
- Cập nhật trạng thái khiếu nại: mới tạo, đang xử lý, đã giải quyết, từ chối

### 4.5. Kiểm duyệt nội dung

- Kiểm duyệt đánh giá và bình luận vi phạm
- Ẩn hoặc xoá nội dung không phù hợp

## 5. Chức năng hệ thống chung

### 5.1. Phân quyền

- Phân quyền theo 3 vai trò: người dùng, chủ nhà hàng, admin
- Giới hạn quyền truy cập đúng theo vai trò

### 5.2. Thông báo

- Thông báo khi đơn đặt bàn được tạo
- Thông báo khi đơn được xác nhận hoặc từ chối
- Thông báo khi thanh toán thành công hoặc thất bại
- Thông báo khi có phản hồi khiếu nại
- Thông báo kết quả xác thực nhà hàng

### 5.3. Quản lý trạng thái dữ liệu

- Quản lý trạng thái nhà hàng: chờ duyệt, hoạt động, tạm ngừng, bị khoá
- Quản lý trạng thái đơn đặt bàn
- Quản lý trạng thái thanh toán
- Quản lý trạng thái khiếu nại

### 5.4. Lưu vết và lịch sử

- Lưu lịch sử đặt bàn
- Lưu lịch sử thanh toán
- Lưu lịch sử xử lý khiếu nại
- Lưu lịch sử xác thực nhà hàng

## 6. Luồng nghiệp vụ chính

### 6.1. Luồng đăng nhà hàng

- Chủ nhà hàng tạo tài khoản
- Chủ nhà hàng nhập thông tin nhà hàng
- Chủ nhà hàng khai báo loại bàn, giá đặt, sức chứa, thực đơn
- Chủ nhà hàng tải hồ sơ xác thực
- Admin kiểm tra và phê duyệt
- Nhà hàng được hiển thị công khai sau khi được duyệt

### 6.2. Luồng đặt bàn

- Người dùng tìm nhà hàng
- Người dùng xem thông tin, loại bàn, giá đặt, thực đơn
- Người dùng chọn thời gian, loại bàn, số người đi
- Hệ thống tính tổng chi phí và phụ thu nếu có
- Người dùng xác nhận và thanh toán
- Hệ thống tạo đơn đặt bàn
- Chủ nhà hàng xác nhận đơn

### 6.3. Luồng đánh giá

- Người dùng hoàn tất bữa ăn/đơn đặt bàn
- Người dùng gửi rating và bình luận
- Đánh giá được hiển thị tại trang nhà hàng

### 6.4. Luồng khiếu nại

- Người dùng gửi khiếu nại
- Admin tiếp nhận và xử lý
- Admin phản hồi kết quả xử lý cho người dùng

## 7. Danh sách chức năng cốt lõi ưu tiên MVP

- Đăng ký/đăng nhập cho 3 vai trò
- Chủ nhà hàng đăng ký và quản lý nhà hàng
- Quản lý loại bàn, giá đặt, số người, địa chỉ, mô tả, giờ mở/đóng
- Quản lý thực đơn nhà hàng
- Người dùng tìm kiếm, xem chi tiết nhà hàng
- Người dùng đặt bàn theo thời gian và số lượng người
- Tính phụ thu theo số người đi
- Thanh toán đơn đặt bàn
- Người dùng đánh giá bằng rating và bình luận
- Admin xác thực nhà hàng
- Admin xử lý khiếu nại
- Admin chỉnh sửa/xoá nhà hàng
