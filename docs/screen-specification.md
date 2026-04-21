# Đặc tả màn hình hệ thống REBO

## 1. Nguyên tắc mã hoá

- Mã màn hình sử dụng định dạng `SCR-xx`.
- Mã chức năng liên quan sử dụng các mã `FR-xx` trong tài liệu `business-process-fr-nfr.md`.
- Danh sách dưới đây ưu tiên các màn hình phục vụ 3 quy trình chính: đặt bàn, nhận bàn, đánh giá.

## 2. Danh sách màn hình cho người dùng đặt chỗ

| Mã màn hình | Tên màn hình | Mô tả màn hình | Mã chức năng liên quan |
|---|---|---|---|
| SCR-01 | Đăng nhập | Cho phép người dùng đăng nhập để thực hiện đặt bàn, thanh toán và đánh giá. | FR-27 |
| SCR-02 | Trang chủ / Danh sách nhà hàng | Hiển thị danh sách nhà hàng đang hoạt động, hỗ trợ tìm kiếm và chọn nhà hàng để xem chi tiết. | FR-01, FR-30 |
| SCR-03 | Chi tiết nhà hàng | Hiển thị thông tin chi tiết nhà hàng gồm địa chỉ, mô tả, giờ mở/đóng, loại bàn, sức chứa, giá đặt, thực đơn và đánh giá. | FR-02, FR-23, FR-30 |
| SCR-04 | Chọn thông tin đặt bàn | Cho phép người dùng chọn ngày, giờ, loại bàn và số lượng người; hệ thống kiểm tra khả năng phục vụ theo khung giờ. | FR-03, FR-04, FR-30 |
| SCR-05 | Xác nhận đặt bàn | Hiển thị thông tin đặt bàn đã chọn, tổng chi phí, phụ thu và cho phép người dùng xác nhận trước khi thanh toán. | FR-05, FR-06 |
| SCR-06 | Thanh toán đặt bàn | Cho phép người dùng thực hiện thanh toán tiền đặt chỗ và ghi nhận trạng thái thanh toán của đơn. | FR-07, FR-08 |
| SCR-07 | Kết quả đặt bàn | Hiển thị kết quả tạo đơn đặt bàn, mã đơn, trạng thái đơn ban đầu và trạng thái thanh toán. | FR-08, FR-11, FR-29 |
| SCR-08 | Danh sách đơn đặt bàn | Hiển thị toàn bộ các đơn đặt bàn của người dùng để theo dõi trạng thái xử lý. | FR-11, FR-12, FR-29 |
| SCR-09 | Chi tiết đơn đặt bàn | Hiển thị chi tiết một đơn đặt bàn gồm thông tin nhà hàng, thời gian, số người, loại bàn, trạng thái đơn, trạng thái thanh toán và lịch sử cập nhật. | FR-11, FR-12, FR-28, FR-29 |
| SCR-10 | Gửi đánh giá | Cho phép người dùng gửi số sao và bình luận sau khi đơn đặt bàn đã hoàn tất. | FR-19, FR-20, FR-21, FR-22 |
| SCR-11 | Quản lý đánh giá của tôi | Hiển thị các đánh giá do người dùng đã gửi và cho phép chỉnh sửa hoặc xoá nếu chính sách cho phép. | FR-22, FR-24 |

## 3. Danh sách màn hình cho chủ nhà hàng

| Mã màn hình | Tên màn hình | Mô tả màn hình | Mã chức năng liên quan |
|---|---|---|---|
| SCR-12 | Đăng nhập chủ nhà hàng | Cho phép chủ nhà hàng đăng nhập vào khu vực quản trị nhà hàng. | FR-27 |
| SCR-13 | Dashboard chủ nhà hàng | Hiển thị tổng quan đơn đặt bàn mới, trạng thái hoạt động và các thông báo liên quan đến nhà hàng. | FR-09, FR-10, FR-29, FR-30 |
| SCR-14 | Quản lý thông tin nhà hàng | Cho phép chủ nhà hàng khai báo hoặc cập nhật thông tin nhà hàng phục vụ việc hiển thị công khai và nhận đặt bàn. | FR-02, FR-30 |
| SCR-15 | Quản lý loại bàn và giá đặt | Cho phép khai báo loại bàn, sức chứa, giá đặt và số lượng phục vụ theo từng loại. | FR-02, FR-03, FR-04, FR-05 |
| SCR-16 | Quản lý thực đơn | Cho phép cập nhật danh sách món ăn hiển thị tại trang chi tiết nhà hàng. | FR-02 |
| SCR-17 | Danh sách đơn đặt bàn nhà hàng | Hiển thị các đơn đặt bàn mới và đang xử lý để chủ nhà hàng xác nhận hoặc từ chối. | FR-09, FR-10, FR-14 |
| SCR-18 | Chi tiết đơn đặt bàn nhà hàng | Hiển thị đầy đủ thông tin một đơn đặt bàn để chủ nhà hàng xem và xử lý trạng thái. | FR-10, FR-14, FR-28 |
| SCR-19 | Tiếp nhận khách / Nhận bàn | Cho phép chủ nhà hàng hoặc nhân viên tra cứu đơn theo mã đơn, tên khách hoặc thời gian đặt và xác nhận khách đã đến. | FR-13, FR-14, FR-15, FR-16 |
| SCR-20 | Cập nhật trạng thái phục vụ | Cho phép cập nhật trạng thái đơn sang đang phục vụ, hoàn tất, đến trễ, không đến hoặc huỷ. | FR-16, FR-17, FR-18, FR-28 |
| SCR-21 | Xem đánh giá nhà hàng | Hiển thị danh sách đánh giá từ người dùng để chủ nhà hàng theo dõi chất lượng dịch vụ. | FR-23, FR-25 |

## 4. Danh sách màn hình cho admin

| Mã màn hình | Tên màn hình | Mô tả màn hình | Mã chức năng liên quan |
|---|---|---|---|
| SCR-22 | Đăng nhập admin | Cho phép admin đăng nhập vào hệ thống quản trị. | FR-27 |
| SCR-23 | Dashboard admin | Hiển thị tổng quan các nhà hàng chờ duyệt, đánh giá cần kiểm duyệt và các cảnh báo vận hành. | FR-26, FR-30 |
| SCR-24 | Quản lý nhà hàng | Hiển thị danh sách nhà hàng và cho phép admin xem trạng thái, kiểm tra điều kiện hoạt động và quản lý khả năng hiển thị. | FR-30 |
| SCR-25 | Chi tiết hồ sơ nhà hàng | Hiển thị chi tiết nhà hàng và các thông tin cần thiết để admin xem xét phê duyệt hoặc kiểm tra tính hợp lệ. | FR-30 |
| SCR-26 | Kiểm duyệt đánh giá | Cho phép admin xem, ẩn hoặc xoá các đánh giá vi phạm chính sách hệ thống. | FR-26 |

## 5. Màn hình dùng chung và hỗ trợ nghiệp vụ

| Mã màn hình | Tên màn hình | Mô tả màn hình | Mã chức năng liên quan |
|---|---|---|---|
| SCR-27 | Thông báo hệ thống | Hiển thị thông báo về đơn đặt bàn mới, thay đổi trạng thái đơn, kết quả thanh toán và các cập nhật nghiệp vụ liên quan. | FR-09, FR-29 |
| SCR-28 | Tra cứu trạng thái đơn nhanh | Cho phép tra cứu nhanh trạng thái một đơn đặt bàn bằng mã đơn hoặc thông tin liên quan. | FR-11, FR-13, FR-14 |
| SCR-29 | Lịch sử trạng thái đơn | Hiển thị nhật ký thay đổi trạng thái của một đơn đặt bàn để phục vụ tra cứu và đối soát. | FR-12, FR-28 |

## 6. Nhóm màn hình cốt lõi theo quy trình

### 6.1. Quy trình đặt bàn

- SCR-02: Trang chủ / Danh sách nhà hàng
- SCR-03: Chi tiết nhà hàng
- SCR-04: Chọn thông tin đặt bàn
- SCR-05: Xác nhận đặt bàn
- SCR-06: Thanh toán đặt bàn
- SCR-07: Kết quả đặt bàn
- SCR-08: Danh sách đơn đặt bàn
- SCR-09: Chi tiết đơn đặt bàn

### 6.2. Quy trình nhận bàn

- SCR-17: Danh sách đơn đặt bàn nhà hàng
- SCR-18: Chi tiết đơn đặt bàn nhà hàng
- SCR-19: Tiếp nhận khách / Nhận bàn
- SCR-20: Cập nhật trạng thái phục vụ
- SCR-29: Lịch sử trạng thái đơn

### 6.3. Quy trình đánh giá

- SCR-03: Chi tiết nhà hàng
- SCR-10: Gửi đánh giá
- SCR-11: Quản lý đánh giá của tôi
- SCR-21: Xem đánh giá nhà hàng
- SCR-26: Kiểm duyệt đánh giá

## 7. Ghi chú

- Nếu cần mức đặc tả chi tiết hơn, mỗi màn hình có thể được mở rộng thêm các mục: actor sử dụng, dữ liệu đầu vào, dữ liệu đầu ra, hành động chính, điều kiện kiểm tra và thông báo lỗi.
- Trong bước tiếp theo, có thể chuyển danh sách này thành ma trận truy vết `Screen -> FR -> Actor -> Use Case`.
