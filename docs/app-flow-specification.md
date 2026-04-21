# Đặc tả các luồng của app REBO

## 1. Mục tiêu

Tài liệu này mô tả các luồng điều hướng chính của app REBO theo vai trò sử dụng và theo quy trình nghiệp vụ cốt lõi.

## 2. Thành phần của một luồng

Mỗi luồng gồm:

- Điểm bắt đầu
- Điều kiện vào luồng
- Các bước điều hướng qua màn hình
- Nhánh thành công
- Nhánh ngoại lệ
- Điểm kết thúc

## 3. Luồng tổng thể theo vai trò

### 3.1. Luồng người dùng đặt chỗ

1. `SCR-01` Đăng nhập
2. `SCR-02` Trang chủ / Danh sách nhà hàng
3. `SCR-03` Chi tiết nhà hàng
4. `SCR-04` Chọn thông tin đặt bàn
5. `SCR-05` Xác nhận đặt bàn
6. `SCR-06` Thanh toán đặt bàn
7. `SCR-07` Kết quả đặt bàn
8. `SCR-08` Danh sách đơn đặt bàn
9. `SCR-09` Chi tiết đơn đặt bàn
10. `SCR-10` Gửi đánh giá
11. `SCR-11` Quản lý đánh giá của tôi

### 3.2. Luồng chủ nhà hàng

1. `SCR-12` Đăng nhập chủ nhà hàng
2. `SCR-13` Dashboard chủ nhà hàng
3. `SCR-14` Quản lý thông tin nhà hàng
4. `SCR-15` Quản lý loại bàn và giá đặt
5. `SCR-16` Quản lý thực đơn
6. `SCR-17` Danh sách đơn đặt bàn nhà hàng
7. `SCR-18` Chi tiết đơn đặt bàn nhà hàng
8. `SCR-19` Tiếp nhận khách / Nhận bàn
9. `SCR-20` Cập nhật trạng thái phục vụ
10. `SCR-21` Xem đánh giá nhà hàng

### 3.3. Luồng admin

1. `SCR-22` Đăng nhập admin
2. `SCR-23` Dashboard admin
3. `SCR-24` Quản lý nhà hàng
4. `SCR-25` Chi tiết hồ sơ nhà hàng
5. `SCR-26` Kiểm duyệt đánh giá

## 4. Luồng nghiệp vụ chi tiết

### 4.1. Luồng 1: Đăng nhập

- Điểm bắt đầu: người dùng mở app và chọn đăng nhập.
- Điều kiện vào luồng: tài khoản đã tồn tại.
- Các bước:
  1. Người dùng vào `SCR-01`, `SCR-12` hoặc `SCR-22` tùy vai trò.
  2. Nhập thông tin đăng nhập.
  3. Hệ thống xác thực tài khoản và vai trò.
  4. Hệ thống điều hướng đến màn hình chính phù hợp.
- Nhánh thành công:
  - Người dùng đến `SCR-02`.
  - Chủ nhà hàng đến `SCR-13`.
  - Admin đến `SCR-23`.
- Nhánh ngoại lệ:
  - Sai tài khoản hoặc mật khẩu.
  - Tài khoản bị khóa.
  - Vai trò không hợp lệ.
- Điểm kết thúc: phiên đăng nhập được tạo thành công.

### 4.2. Luồng 2: Tìm kiếm nhà hàng và xem chi tiết

- Điểm bắt đầu: người dùng đã đăng nhập.
- Điều kiện vào luồng: hệ thống có nhà hàng đang hoạt động.
- Các bước:
  1. Người dùng vào `SCR-02`.
  2. Nhập từ khóa, khu vực, ngày giờ và số người nếu cần.
  3. Hệ thống hiển thị danh sách nhà hàng phù hợp.
  4. Người dùng chọn một nhà hàng.
  5. Hệ thống mở `SCR-03` để hiển thị chi tiết nhà hàng.
- Nhánh thành công:
  - Người dùng tiếp tục sang `SCR-04` để đặt bàn.
- Nhánh ngoại lệ:
  - Không có nhà hàng phù hợp.
  - Nhà hàng tạm ngừng hoạt động hoặc chưa được duyệt.
- Điểm kết thúc: người dùng chọn được nhà hàng để đặt bàn.

### 4.3. Luồng 3: Đặt bàn

- Điểm bắt đầu: người dùng đang ở `SCR-03` hoặc `SCR-04`.
- Điều kiện vào luồng:
  - Nhà hàng đang hoạt động.
  - Người dùng đã đăng nhập.
- Các bước:
  1. Người dùng vào `SCR-04`.
  2. Chọn ngày đặt, giờ đặt, loại bàn và số người.
  3. Hệ thống kiểm tra bàn trống.
  4. Hệ thống tính giá đặt và phụ thu.
  5. Người dùng chuyển sang `SCR-05`.
  6. Người dùng kiểm tra lại thông tin đơn và xác nhận đặt bàn.
  7. Hệ thống tạo bản ghi đặt chỗ tạm hoặc booking draft.
- Nhánh thành công:
  - Chuyển sang `SCR-06` để thanh toán.
- Nhánh ngoại lệ:
  - Không còn chỗ trống.
  - Ngoài giờ hoạt động.
  - Số người vượt giới hạn phục vụ.
- Điểm kết thúc: thông tin đặt bàn hợp lệ sẵn sàng để thanh toán.

### 4.4. Luồng 4: Thanh toán đặt bàn

- Điểm bắt đầu: người dùng đang ở `SCR-06`.
- Điều kiện vào luồng: có booking draft hợp lệ.
- Các bước:
  1. Người dùng chọn phương thức thanh toán tại `SCR-06`.
  2. Nhập thông tin thanh toán hoặc được chuyển qua cổng thanh toán.
  3. Hệ thống nhận kết quả thanh toán.
  4. Nếu thành công, hệ thống tạo đơn đặt bàn chính thức.
  5. Hệ thống hiển thị `SCR-07`.
  6. Hệ thống gửi thông báo cho chủ nhà hàng.
- Nhánh thành công:
  - Đơn ở trạng thái `chờ xác nhận` hoặc trạng thái tương đương.
- Nhánh ngoại lệ:
  - Thanh toán thất bại.
  - Người dùng huỷ thanh toán.
  - Phiên thanh toán hết hạn.
- Điểm kết thúc: đơn đặt bàn được tạo hoặc thanh toán thất bại.

### 4.5. Luồng 5: Theo dõi đơn đặt bàn

- Điểm bắt đầu: người dùng muốn xem các đơn đã tạo.
- Điều kiện vào luồng: người dùng có ít nhất một đơn đặt bàn.
- Các bước:
  1. Người dùng mở `SCR-08`.
  2. Hệ thống hiển thị danh sách đơn.
  3. Người dùng chọn một đơn.
  4. Hệ thống mở `SCR-09`.
  5. Hệ thống hiển thị trạng thái đơn, thanh toán và lịch sử cập nhật.
- Nhánh thành công:
  - Người dùng theo dõi được trạng thái đơn.
- Nhánh ngoại lệ:
  - Không tìm thấy đơn.
  - Người dùng không có quyền xem đơn.
- Điểm kết thúc: người dùng nắm được tình trạng xử lý của đơn.

### 4.6. Luồng 6: Chủ nhà hàng xác nhận hoặc từ chối đơn

- Điểm bắt đầu: chủ nhà hàng nhận thông báo đơn mới.
- Điều kiện vào luồng: có đơn đặt bàn mới thuộc nhà hàng của mình.
- Các bước:
  1. Chủ nhà hàng vào `SCR-17`.
  2. Chọn một đơn mới.
  3. Hệ thống mở `SCR-18`.
  4. Chủ nhà hàng xem thông tin đơn.
  5. Chủ nhà hàng chọn xác nhận hoặc từ chối.
  6. Hệ thống cập nhật trạng thái đơn.
  7. Hệ thống gửi thông báo cho người dùng.
- Nhánh thành công:
  - Đơn chuyển sang `đã xác nhận` hoặc `đã từ chối`.
- Nhánh ngoại lệ:
  - Đơn đã được xử lý trước đó.
  - Không còn khả năng phục vụ.
- Điểm kết thúc: trạng thái đơn được cập nhật.

### 4.7. Luồng 7: Nhận bàn / tiếp nhận khách

- Điểm bắt đầu: khách đến nhà hàng theo giờ đặt.
- Điều kiện vào luồng:
  - Đơn đã được xác nhận.
  - Nhà hàng tìm thấy đơn hợp lệ.
- Các bước:
  1. Nhà hàng vào `SCR-19`.
  2. Tra cứu đơn theo mã đơn, tên khách hoặc thời gian đặt.
  3. Hệ thống hiển thị thông tin đơn.
  4. Nhà hàng xác nhận khách đã đến.
  5. Hệ thống cập nhật trạng thái sang `đã nhận bàn` hoặc `đang phục vụ`.
  6. Khi kết thúc phục vụ, nhà hàng chuyển sang `SCR-20`.
  7. Hệ thống cập nhật trạng thái đơn sang `hoàn tất`.
- Nhánh thành công:
  - Đơn đủ điều kiện để người dùng đánh giá.
- Nhánh ngoại lệ:
  - Khách đến trễ.
  - Khách không đến.
  - Số khách thực tế vượt quá khả năng phục vụ.
- Điểm kết thúc: đơn được hoàn tất hoặc gắn trạng thái ngoại lệ.

### 4.8. Luồng 8: Gửi đánh giá

- Điểm bắt đầu: người dùng có đơn ở trạng thái hoàn tất.
- Điều kiện vào luồng:
  - Người dùng là chủ đơn.
  - Đơn đủ điều kiện đánh giá.
- Các bước:
  1. Người dùng vào `SCR-09` hoặc khu vực đánh giá.
  2. Chọn `SCR-10` để gửi đánh giá.
  3. Nhập số sao và bình luận.
  4. Hệ thống kiểm tra tính hợp lệ.
  5. Hệ thống lưu đánh giá.
  6. Đánh giá hiển thị ở `SCR-03` và `SCR-11`.
- Nhánh thành công:
  - Đánh giá được lưu và hiển thị hoặc chờ kiểm duyệt.
- Nhánh ngoại lệ:
  - Đơn chưa hoàn tất.
  - Nội dung vi phạm chính sách.
  - Đã tồn tại đánh giá cho đơn nếu hệ thống chỉ cho một lần đánh giá.
- Điểm kết thúc: đánh giá được ghi nhận.

### 4.9. Luồng 9: Quản lý đánh giá của tôi

- Điểm bắt đầu: người dùng muốn xem hoặc cập nhật đánh giá đã gửi.
- Điều kiện vào luồng: người dùng đã có ít nhất một đánh giá.
- Các bước:
  1. Người dùng mở `SCR-11`.
  2. Hệ thống hiển thị danh sách đánh giá đã gửi.
  3. Người dùng chọn chỉnh sửa hoặc xoá nếu được phép.
  4. Hệ thống cập nhật trạng thái hiển thị của đánh giá.
- Nhánh thành công:
  - Đánh giá được cập nhật.
- Nhánh ngoại lệ:
  - Đánh giá không còn được phép chỉnh sửa.
- Điểm kết thúc: danh sách đánh giá cá nhân được cập nhật.

### 4.10. Luồng 10: Admin quản lý nhà hàng

- Điểm bắt đầu: admin đăng nhập thành công.
- Điều kiện vào luồng: có nhà hàng cần duyệt hoặc kiểm tra.
- Các bước:
  1. Admin vào `SCR-23`.
  2. Chọn khu vực quản lý nhà hàng tại `SCR-24`.
  3. Lọc hoặc tìm kiếm nhà hàng.
  4. Chọn một nhà hàng để xem `SCR-25`.
  5. Kiểm tra thông tin và trạng thái hợp lệ.
  6. Duyệt, từ chối hoặc cập nhật trạng thái nhà hàng.
- Nhánh thành công:
  - Nhà hàng được duyệt và có thể nhận đặt bàn.
- Nhánh ngoại lệ:
  - Hồ sơ thiếu dữ liệu.
  - Nhà hàng vi phạm quy định.
- Điểm kết thúc: trạng thái nhà hàng được admin cập nhật.

### 4.11. Luồng 11: Admin kiểm duyệt đánh giá

- Điểm bắt đầu: admin cần xử lý đánh giá vi phạm.
- Điều kiện vào luồng: hệ thống có đánh giá bị báo cáo hoặc cần kiểm duyệt.
- Các bước:
  1. Admin vào `SCR-26`.
  2. Tìm kiếm hoặc lọc đánh giá.
  3. Xem nội dung chi tiết.
  4. Chọn ẩn, xoá hoặc giữ nguyên.
  5. Hệ thống cập nhật trạng thái kiểm duyệt.
- Nhánh thành công:
  - Đánh giá được xử lý theo chính sách.
- Nhánh ngoại lệ:
  - Đánh giá đã được xử lý trước đó.
- Điểm kết thúc: trạng thái kiểm duyệt đánh giá được cập nhật.

## 5. Luồng phụ trợ dùng chung

### 5.1. Luồng thông báo hệ thống

1. Hệ thống phát sinh sự kiện nghiệp vụ.
2. Hệ thống tạo bản ghi thông báo.
3. Người dùng hoặc chủ nhà hàng mở `SCR-27`.
4. Chọn một thông báo để điều hướng tới màn hình liên quan như `SCR-09` hoặc `SCR-18`.

### 5.2. Luồng tra cứu trạng thái đơn nhanh

1. Người dùng hoặc nhà hàng mở `SCR-28`.
2. Nhập mã đơn hoặc thông tin tra cứu.
3. Hệ thống trả về trạng thái hiện tại của đơn.
4. Có thể điều hướng sang `SCR-09`, `SCR-18` hoặc `SCR-29`.

### 5.3. Luồng xem lịch sử trạng thái đơn

1. Từ chi tiết đơn, người dùng chọn xem lịch sử.
2. Hệ thống mở `SCR-29`.
3. Hiển thị toàn bộ các lần đổi trạng thái, thời gian và người cập nhật.

## 6. Luồng điều hướng cốt lõi cho MVP

### 6.1. User flow MVP

`SCR-01 -> SCR-02 -> SCR-03 -> SCR-04 -> SCR-05 -> SCR-06 -> SCR-07 -> SCR-08 -> SCR-09 -> SCR-10`

### 6.2. Merchant flow MVP

`SCR-12 -> SCR-13 -> SCR-17 -> SCR-18 -> SCR-19 -> SCR-20`

### 6.3. Admin flow MVP

`SCR-22 -> SCR-23 -> SCR-24 -> SCR-25 -> SCR-26`

## 7. Điểm cần lưu ý khi triển khai luồng app

- Các trạng thái đơn phải nhất quán giữa luồng người dùng và luồng nhà hàng.
- Chỉ đơn ở trạng thái `hoàn tất` mới được mở luồng đánh giá.
- Luồng thanh toán cần xử lý rõ các tình huống quay lại app, timeout và thanh toán thất bại.
- Luồng nhận bàn cần có kiểm soát các trường hợp `đến trễ`, `không đến` và `huỷ`.
- Mỗi luồng nên có nhật ký trạng thái để phục vụ đối soát và hỗ trợ người dùng.
