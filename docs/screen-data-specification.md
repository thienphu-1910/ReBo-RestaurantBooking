# Đặc tả dữ liệu cho từng màn hình REBO

## 1. Quy ước

- `Dữ liệu đầu vào`: dữ liệu người dùng nhập, chọn hoặc gửi lên hệ thống.
- `Dữ liệu hiển thị`: dữ liệu hệ thống trả ra để hiển thị trên màn hình.
- `Dữ liệu ẩn/xử lý`: dữ liệu dùng để liên kết, tra cứu, cập nhật trạng thái nhưng không nhất thiết hiển thị đầy đủ.

## 2. Màn hình cho người dùng đặt chỗ

### SCR-01. Đăng nhập

- Dữ liệu đầu vào:
  - Email hoặc số điện thoại
  - Mật khẩu
- Dữ liệu hiển thị:
  - Thông báo đăng nhập thành công/thất bại
  - Liên kết quên mật khẩu
- Dữ liệu ẩn/xử lý:
  - User ID
  - Vai trò tài khoản
  - Token phiên đăng nhập

### SCR-02. Trang chủ / Danh sách nhà hàng

- Dữ liệu đầu vào:
  - Từ khoá tìm kiếm
  - Khu vực/địa chỉ
  - Ngày đặt
  - Giờ đặt
  - Số người
- Dữ liệu hiển thị:
  - Mã nhà hàng
  - Tên nhà hàng
  - Ảnh đại diện
  - Địa chỉ
  - Giờ mở cửa/đóng cửa
  - Khoảng giá đặt bàn
  - Điểm đánh giá trung bình
  - Số lượng đánh giá
  - Trạng thái hoạt động
- Dữ liệu ẩn/xử lý:
  - Restaurant ID
  - Trạng thái phê duyệt nhà hàng
  - Điều kiện còn chỗ sơ bộ theo thời gian tìm kiếm

### SCR-03. Chi tiết nhà hàng

- Dữ liệu đầu vào:
  - Ngày đặt
  - Giờ đặt
  - Số người
- Dữ liệu hiển thị:
  - Mã nhà hàng
  - Tên nhà hàng
  - Bộ ảnh nhà hàng
  - Địa chỉ
  - Mô tả
  - Giờ mở cửa/đóng cửa
  - Danh sách loại bàn
  - Sức chứa từng loại bàn
  - Giá đặt từng loại bàn
  - Danh sách món ăn
  - Giá món ăn nếu có
  - Điểm đánh giá trung bình
  - Danh sách đánh giá và bình luận
- Dữ liệu ẩn/xử lý:
  - Restaurant ID
  - Danh sách tableType ID
  - Điều kiện đặt bàn hợp lệ theo giờ hoạt động

### SCR-04. Chọn thông tin đặt bàn

- Dữ liệu đầu vào:
  - Nhà hàng đã chọn
  - Loại bàn
  - Ngày đặt
  - Giờ đặt
  - Số người đi
- Dữ liệu hiển thị:
  - Tên nhà hàng
  - Danh sách loại bàn khả dụng
  - Sức chứa cơ bản của bàn
  - Số lượng bàn còn trống theo khung giờ
  - Giá đặt bàn cơ bản
  - Mức phụ thu dự kiến
- Dữ liệu ẩn/xử lý:
  - Restaurant ID
  - Table type ID
  - Số bàn còn trống
  - Quy tắc phụ thu
  - Kết quả kiểm tra availability

### SCR-05. Xác nhận đặt bàn

- Dữ liệu đầu vào:
  - Ghi chú đặt bàn
  - Xác nhận đặt bàn
- Dữ liệu hiển thị:
  - Tên nhà hàng
  - Địa chỉ nhà hàng
  - Loại bàn
  - Ngày giờ đặt
  - Số người đi
  - Giá đặt bàn
  - Phụ thu
  - Tổng thanh toán
  - Chính sách huỷ/giữ bàn nếu có
- Dữ liệu ẩn/xử lý:
  - Booking draft ID
  - Restaurant ID
  - Table type ID
  - User ID
  - Tổng tiền cuối cùng

### SCR-06. Thanh toán đặt bàn

- Dữ liệu đầu vào:
  - Phương thức thanh toán
  - Thông tin thanh toán theo cổng thanh toán
- Dữ liệu hiển thị:
  - Mã đơn tạm
  - Tổng tiền thanh toán
  - Nội dung thanh toán
  - Trạng thái thanh toán
  - Thông báo thành công/thất bại
- Dữ liệu ẩn/xử lý:
  - Payment ID
  - Booking ID hoặc booking draft ID
  - Transaction code
  - Thời gian thanh toán

### SCR-07. Kết quả đặt bàn

- Dữ liệu đầu vào:
  - Không có hoặc chỉ có thao tác điều hướng
- Dữ liệu hiển thị:
  - Mã đơn đặt bàn
  - Tên nhà hàng
  - Ngày giờ đặt
  - Loại bàn
  - Số người
  - Tổng tiền
  - Trạng thái đơn
  - Trạng thái thanh toán
  - Thông báo hướng dẫn bước tiếp theo
- Dữ liệu ẩn/xử lý:
  - Booking ID
  - Payment ID
  - Thời điểm tạo đơn

### SCR-08. Danh sách đơn đặt bàn

- Dữ liệu đầu vào:
  - Bộ lọc trạng thái đơn
  - Khoảng thời gian
  - Từ khoá tìm kiếm theo mã đơn/tên nhà hàng
- Dữ liệu hiển thị:
  - Mã đơn
  - Tên nhà hàng
  - Ngày giờ đặt
  - Loại bàn
  - Số người
  - Tổng tiền
  - Trạng thái đơn
  - Trạng thái thanh toán
  - Ngày tạo đơn
- Dữ liệu ẩn/xử lý:
  - Booking ID
  - Restaurant ID
  - Payment status code
  - Booking status code

### SCR-09. Chi tiết đơn đặt bàn

- Dữ liệu đầu vào:
  - Mã đơn hoặc chọn từ danh sách
- Dữ liệu hiển thị:
  - Mã đơn
  - Tên nhà hàng
  - Địa chỉ nhà hàng
  - Thông tin liên hệ nhà hàng
  - Ngày giờ đặt
  - Loại bàn
  - Số người đặt
  - Giá đặt bàn
  - Phụ thu
  - Tổng tiền
  - Trạng thái đơn
  - Trạng thái thanh toán
  - Lịch sử cập nhật trạng thái
  - Ghi chú của người dùng hoặc nhà hàng nếu có
- Dữ liệu ẩn/xử lý:
  - Booking ID
  - User ID
  - Restaurant ID
  - Timeline status entries

### SCR-10. Gửi đánh giá

- Dữ liệu đầu vào:
  - Mã đơn đặt bàn
  - Số sao đánh giá
  - Nội dung bình luận
- Dữ liệu hiển thị:
  - Tên nhà hàng
  - Thông tin đơn đã hoàn tất
  - Số sao được chọn
  - Ký tự còn lại của bình luận nếu có giới hạn
  - Thông báo kết quả gửi đánh giá
- Dữ liệu ẩn/xử lý:
  - Review ID
  - Booking ID
  - Restaurant ID
  - User ID
  - Trạng thái kiểm duyệt đánh giá

### SCR-11. Quản lý đánh giá của tôi

- Dữ liệu đầu vào:
  - Bộ lọc theo thời gian hoặc nhà hàng
- Dữ liệu hiển thị:
  - Mã đánh giá
  - Tên nhà hàng
  - Mã đơn liên quan
  - Số sao
  - Nội dung bình luận
  - Ngày tạo đánh giá
  - Trạng thái hiển thị/kiểm duyệt
- Dữ liệu ẩn/xử lý:
  - Review ID
  - Booking ID
  - Restaurant ID

## 3. Màn hình cho chủ nhà hàng

### SCR-12. Đăng nhập chủ nhà hàng

- Dữ liệu đầu vào:
  - Email hoặc số điện thoại
  - Mật khẩu
- Dữ liệu hiển thị:
  - Thông báo đăng nhập thành công/thất bại
- Dữ liệu ẩn/xử lý:
  - Owner ID
  - Restaurant ID liên kết
  - Token phiên đăng nhập

### SCR-13. Dashboard chủ nhà hàng

- Dữ liệu đầu vào:
  - Khoảng thời gian xem thống kê
- Dữ liệu hiển thị:
  - Tên nhà hàng
  - Trạng thái hoạt động nhà hàng
  - Số đơn mới
  - Số đơn chờ xác nhận
  - Số đơn đã xác nhận
  - Số đơn hoàn tất
  - Số đơn huỷ/no-show
  - Thông báo mới
- Dữ liệu ẩn/xử lý:
  - Restaurant ID
  - Các chỉ số thống kê theo trạng thái

### SCR-14. Quản lý thông tin nhà hàng

- Dữ liệu đầu vào:
  - Tên nhà hàng
  - Địa chỉ
  - Mô tả
  - Giờ mở cửa
  - Giờ đóng cửa
  - Ảnh đại diện/ảnh bộ sưu tập
  - Trạng thái hoạt động
- Dữ liệu hiển thị:
  - Toàn bộ thông tin hồ sơ nhà hàng hiện tại
  - Trạng thái phê duyệt
  - Lý do từ chối nếu có
- Dữ liệu ẩn/xử lý:
  - Restaurant ID
  - Approval status
  - Last updated at/by

### SCR-15. Quản lý loại bàn và giá đặt

- Dữ liệu đầu vào:
  - Tên loại bàn
  - Sức chứa cơ bản
  - Số người tối đa
  - Giá đặt bàn
  - Số lượng bàn của loại đó
  - Quy tắc phụ thu
- Dữ liệu hiển thị:
  - Danh sách loại bàn
  - Sức chứa từng loại
  - Giá đặt
  - Số lượng đang khai báo
  - Trạng thái áp dụng
- Dữ liệu ẩn/xử lý:
  - Table type ID
  - Restaurant ID
  - Availability rule

### SCR-16. Quản lý thực đơn

- Dữ liệu đầu vào:
  - Tên món
  - Mô tả món
  - Giá món
  - Hình ảnh món
  - Trạng thái hiển thị
- Dữ liệu hiển thị:
  - Danh sách món ăn
  - Tên món
  - Giá món
  - Ảnh món
  - Trạng thái hiển thị
- Dữ liệu ẩn/xử lý:
  - Menu item ID
  - Restaurant ID

### SCR-17. Danh sách đơn đặt bàn nhà hàng

- Dữ liệu đầu vào:
  - Bộ lọc trạng thái
  - Ngày đặt
  - Từ khoá theo mã đơn hoặc tên khách
- Dữ liệu hiển thị:
  - Mã đơn
  - Tên khách
  - Số điện thoại khách
  - Ngày giờ đặt
  - Loại bàn
  - Số người
  - Trạng thái đơn
  - Trạng thái thanh toán
  - Thời điểm tạo đơn
- Dữ liệu ẩn/xử lý:
  - Booking ID
  - User ID
  - Restaurant ID

### SCR-18. Chi tiết đơn đặt bàn nhà hàng

- Dữ liệu đầu vào:
  - Mã đơn
- Dữ liệu hiển thị:
  - Mã đơn
  - Thông tin khách hàng
  - Số điện thoại liên hệ
  - Ngày giờ đặt
  - Loại bàn
  - Số người đặt
  - Ghi chú
  - Tổng tiền
  - Trạng thái đơn
  - Trạng thái thanh toán
  - Lịch sử trạng thái
- Dữ liệu ẩn/xử lý:
  - Booking ID
  - User ID
  - Payment ID
  - Audit log ID

### SCR-19. Tiếp nhận khách / Nhận bàn

- Dữ liệu đầu vào:
  - Mã đơn
  - Tên khách
  - Thời gian đặt
  - Xác nhận khách đến
- Dữ liệu hiển thị:
  - Mã đơn
  - Tên khách
  - Số điện thoại
  - Thời gian đặt
  - Loại bàn
  - Số người đặt
  - Trạng thái đơn hiện tại
  - Trạng thái thanh toán
- Dữ liệu ẩn/xử lý:
  - Booking ID
  - Check-in time
  - Operator ID

### SCR-20. Cập nhật trạng thái phục vụ

- Dữ liệu đầu vào:
  - Trạng thái mới
  - Lý do cập nhật trạng thái
  - Ghi chú nội bộ
- Dữ liệu hiển thị:
  - Mã đơn
  - Trạng thái hiện tại
  - Danh sách trạng thái cho phép chuyển tiếp
  - Lịch sử cập nhật gần nhất
- Dữ liệu ẩn/xử lý:
  - Booking ID
  - Previous status
  - New status
  - Updated by
  - Updated at

### SCR-21. Xem đánh giá nhà hàng

- Dữ liệu đầu vào:
  - Bộ lọc số sao
  - Khoảng thời gian
- Dữ liệu hiển thị:
  - Điểm trung bình
  - Tổng số đánh giá
  - Tên người đánh giá
  - Số sao
  - Bình luận
  - Ngày đánh giá
  - Đơn đặt bàn liên quan nếu cho phép hiển thị
- Dữ liệu ẩn/xử lý:
  - Review ID
  - Restaurant ID
  - Review status

## 4. Màn hình cho admin

### SCR-22. Đăng nhập admin

- Dữ liệu đầu vào:
  - Tên đăng nhập
  - Mật khẩu
- Dữ liệu hiển thị:
  - Thông báo đăng nhập thành công/thất bại
- Dữ liệu ẩn/xử lý:
  - Admin ID
  - Token phiên đăng nhập

### SCR-23. Dashboard admin

- Dữ liệu đầu vào:
  - Khoảng thời gian
- Dữ liệu hiển thị:
  - Số nhà hàng chờ duyệt
  - Số đánh giá chờ kiểm duyệt
  - Số nhà hàng đang hoạt động
  - Cảnh báo vi phạm nếu có
- Dữ liệu ẩn/xử lý:
  - Tổng số bản ghi theo trạng thái

### SCR-24. Quản lý nhà hàng

- Dữ liệu đầu vào:
  - Bộ lọc trạng thái phê duyệt
  - Từ khoá theo tên nhà hàng
  - Khu vực
- Dữ liệu hiển thị:
  - Mã nhà hàng
  - Tên nhà hàng
  - Chủ sở hữu
  - Địa chỉ
  - Trạng thái phê duyệt
  - Trạng thái hoạt động
  - Ngày tạo
- Dữ liệu ẩn/xử lý:
  - Restaurant ID
  - Owner ID
  - Approval status code

### SCR-25. Chi tiết hồ sơ nhà hàng

- Dữ liệu đầu vào:
  - Mã nhà hàng
- Dữ liệu hiển thị:
  - Mã nhà hàng
  - Tên nhà hàng
  - Thông tin chủ nhà hàng
  - Địa chỉ
  - Mô tả
  - Giờ hoạt động
  - Danh sách loại bàn
  - Danh sách món ăn
  - Tài liệu xác thực nếu có
  - Trạng thái phê duyệt
  - Lý do từ chối trước đó nếu có
- Dữ liệu ẩn/xử lý:
  - Restaurant ID
  - Owner ID
  - Verification document IDs

### SCR-26. Kiểm duyệt đánh giá

- Dữ liệu đầu vào:
  - Bộ lọc trạng thái đánh giá
  - Từ khoá nội dung
  - Số sao
- Dữ liệu hiển thị:
  - Mã đánh giá
  - Tên nhà hàng
  - Người đánh giá
  - Mã đơn liên quan
  - Số sao
  - Nội dung bình luận
  - Trạng thái đánh giá
  - Ngày tạo
- Dữ liệu ẩn/xử lý:
  - Review ID
  - Restaurant ID
  - Booking ID
  - Moderation status

## 5. Màn hình dùng chung

### SCR-27. Thông báo hệ thống

- Dữ liệu đầu vào:
  - Bộ lọc loại thông báo
- Dữ liệu hiển thị:
  - Mã thông báo
  - Tiêu đề thông báo
  - Nội dung tóm tắt
  - Loại thông báo
  - Thời gian tạo
  - Trạng thái đã đọc/chưa đọc
- Dữ liệu ẩn/xử lý:
  - Notification ID
  - Related object ID
  - Recipient ID

### SCR-28. Tra cứu trạng thái đơn nhanh

- Dữ liệu đầu vào:
  - Mã đơn
  - Tên khách hoặc số điện thoại nếu hệ thống cho phép
- Dữ liệu hiển thị:
  - Mã đơn
  - Tên nhà hàng
  - Ngày giờ đặt
  - Số người
  - Trạng thái đơn
  - Trạng thái thanh toán
- Dữ liệu ẩn/xử lý:
  - Booking ID
  - Restaurant ID

### SCR-29. Lịch sử trạng thái đơn

- Dữ liệu đầu vào:
  - Mã đơn
- Dữ liệu hiển thị:
  - Mã đơn
  - Danh sách các lần đổi trạng thái
  - Trạng thái cũ
  - Trạng thái mới
  - Thời gian cập nhật
  - Người cập nhật
  - Ghi chú hoặc lý do thay đổi
- Dữ liệu ẩn/xử lý:
  - Booking ID
  - Status history ID
  - Updated by role

## 6. Nhóm dữ liệu lõi cần có trong hệ thống

Để hỗ trợ toàn bộ các màn hình trên, hệ thống cần tối thiểu các nhóm dữ liệu sau:

- Người dùng: user ID, họ tên, email, số điện thoại, vai trò, trạng thái tài khoản.
- Nhà hàng: restaurant ID, tên, địa chỉ, mô tả, giờ mở/đóng, trạng thái hoạt động, trạng thái phê duyệt.
- Loại bàn: table type ID, tên loại bàn, sức chứa cơ bản, số người tối đa, giá đặt, số lượng bàn.
- Đơn đặt bàn: booking ID, user ID, restaurant ID, table type ID, ngày giờ đặt, số người, tổng tiền, trạng thái đơn.
- Thanh toán: payment ID, booking ID, phương thức thanh toán, mã giao dịch, số tiền, trạng thái thanh toán.
- Đánh giá: review ID, booking ID, restaurant ID, user ID, số sao, bình luận, trạng thái kiểm duyệt.
- Thông báo: notification ID, người nhận, loại thông báo, nội dung, trạng thái đọc.
- Lịch sử trạng thái: history ID, booking ID, trạng thái cũ, trạng thái mới, người cập nhật, thời gian cập nhật.
