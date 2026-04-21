# Xác định stakeholder và đặc tả stakeholder requests cho REBO

## 1. Mục tiêu

Tài liệu này xác định các stakeholder chính của hệ thống REBO và mô tả các yêu cầu, mong đợi, mối quan tâm của từng stakeholder đối với hệ thống.

## 2. Danh sách stakeholder

Các stakeholder chính của REBO gồm:

- Người dùng đặt bàn
- Chủ nhà hàng
- Nhân viên nhà hàng
- Quản trị viên hệ thống (Admin)
- Chủ đầu tư / Chủ sản phẩm
- Bộ phận vận hành và hỗ trợ khách hàng
- Đối tác cổng thanh toán

## 3. Đặc tả stakeholder

### 3.1. Stakeholder: Người dùng đặt bàn

- Mô tả:
  - Là khách hàng sử dụng app để tìm kiếm nhà hàng, đặt bàn, thanh toán và đánh giá sau khi sử dụng dịch vụ.
- Mục tiêu:
  - Tìm được nhà hàng phù hợp nhanh chóng.
  - Đặt bàn dễ dàng, chính xác.
  - Biết rõ tình trạng đơn và chi phí phải trả.
  - Có thể phản hồi trải nghiệm sau bữa ăn.
- Mối quan tâm chính:
  - Dễ tìm nhà hàng phù hợp.
  - Biết còn chỗ hay không trước khi thanh toán.
  - Thanh toán an toàn.
  - Trạng thái đơn rõ ràng.
  - Được phép đánh giá sau khi hoàn tất.

### 3.2. Stakeholder: Chủ nhà hàng

- Mô tả:
  - Là đối tác cung cấp dịch vụ ăn uống trên nền tảng, quản lý nhà hàng, bàn, thực đơn và xử lý các đơn đặt chỗ.
- Mục tiêu:
  - Đăng tải nhà hàng lên hệ thống.
  - Quản lý thông tin nhà hàng, loại bàn, giá đặt, thực đơn.
  - Nhận và xử lý đơn đặt bàn hiệu quả.
  - Theo dõi đánh giá để cải thiện chất lượng phục vụ.
- Mối quan tâm chính:
  - Nhà hàng được duyệt nhanh.
  - Thông tin hiển thị đúng và đầy đủ.
  - Không bị overbooking.
  - Có thể xác nhận, từ chối, tiếp nhận và hoàn tất đơn dễ dàng.
  - Có dữ liệu đánh giá từ khách hàng.

### 3.3. Stakeholder: Nhân viên nhà hàng

- Mô tả:
  - Là người trực tiếp tiếp nhận khách tại nhà hàng và thao tác trên hệ thống ở bước nhận bàn, phục vụ, hoàn tất đơn.
- Mục tiêu:
  - Tra cứu đơn nhanh khi khách đến.
  - Xác nhận nhận bàn chính xác.
  - Cập nhật trạng thái phục vụ kịp thời.
- Mối quan tâm chính:
  - Dễ tra cứu đơn theo mã, tên khách hoặc thời gian.
  - Giao diện thao tác nhanh, ít bước.
  - Tránh nhầm trạng thái đơn.

### 3.4. Stakeholder: Quản trị viên hệ thống (Admin)

- Mô tả:
  - Là người quản lý hoạt động hệ thống, xác thực nhà hàng, kiểm duyệt nội dung và xử lý các vấn đề vận hành.
- Mục tiêu:
  - Kiểm soát chất lượng nhà hàng tham gia nền tảng.
  - Kiểm duyệt đánh giá, nội dung vi phạm.
  - Đảm bảo hệ thống vận hành đúng quy định.
- Mối quan tâm chính:
  - Có đủ dữ liệu để duyệt hoặc từ chối nhà hàng.
  - Kiểm soát được nội dung đánh giá.
  - Truy vết được lịch sử thay đổi trạng thái.

### 3.5. Stakeholder: Chủ đầu tư / Chủ sản phẩm

- Mô tả:
  - Là bên định hướng sản phẩm, đầu tư phát triển hệ thống và chịu trách nhiệm về hiệu quả kinh doanh.
- Mục tiêu:
  - Hệ thống đáp ứng đúng bài toán đặt chỗ nhà hàng.
  - Thu hút được người dùng và nhà hàng tham gia.
  - Vận hành ổn định, giảm lỗi nghiệp vụ.
- Mối quan tâm chính:
  - MVP phải tập trung vào luồng cốt lõi.
  - Có khả năng mở rộng trong tương lai.
  - Có dữ liệu phục vụ phân tích vận hành và tăng trưởng.

### 3.6. Stakeholder: Bộ phận vận hành và hỗ trợ khách hàng

- Mô tả:
  - Là bộ phận xử lý các tình huống phát sinh như khiếu nại, lỗi đơn, hỗ trợ tra cứu thông tin cho người dùng hoặc nhà hàng.
- Mục tiêu:
  - Nhanh chóng xác định vấn đề phát sinh.
  - Hỗ trợ người dùng và nhà hàng dựa trên dữ liệu hệ thống.
- Mối quan tâm chính:
  - Có thể tra cứu đơn, lịch sử trạng thái, thanh toán.
  - Có log và thông báo để đối soát vấn đề.

### 3.7. Stakeholder: Đối tác cổng thanh toán

- Mô tả:
  - Là hệ thống bên ngoài cung cấp dịch vụ xử lý thanh toán cho đơn đặt bàn.
- Mục tiêu:
  - Nhận yêu cầu thanh toán chính xác.
  - Trả kết quả giao dịch rõ ràng cho REBO.
- Mối quan tâm chính:
  - Dữ liệu giao dịch đầy đủ, nhất quán.
  - Có cơ chế xử lý callback, timeout, thất bại giao dịch.

## 4. Đặc tả stakeholder requests

### 4.1. Stakeholder requests của người dùng đặt bàn

- SR-01: Người dùng muốn tìm kiếm nhà hàng theo tên hoặc khu vực.
- SR-02: Người dùng muốn xem chi tiết nhà hàng gồm địa chỉ, mô tả, giờ mở/đóng, loại bàn, giá đặt và thực đơn.
- SR-03: Người dùng muốn biết nhà hàng còn chỗ theo ngày giờ và số người dự kiến.
- SR-04: Người dùng muốn biết tổng chi phí trước khi xác nhận đặt bàn.
- SR-05: Người dùng muốn thanh toán đặt chỗ trực tuyến.
- SR-06: Người dùng muốn xem trạng thái đơn đặt bàn sau khi tạo đơn.
- SR-07: Người dùng muốn nhận thông báo khi trạng thái đơn thay đổi.
- SR-08: Người dùng muốn xem lịch sử các đơn đã đặt.
- SR-09: Người dùng muốn đánh giá nhà hàng bằng số sao và bình luận sau khi hoàn tất bữa ăn.
- SR-10: Người dùng muốn chỉnh sửa hoặc xoá đánh giá của mình khi chính sách hệ thống cho phép.

### 4.2. Stakeholder requests của chủ nhà hàng

- SR-11: Chủ nhà hàng muốn đăng ký và khai báo thông tin nhà hàng trên hệ thống.
- SR-12: Chủ nhà hàng muốn quản lý loại bàn, sức chứa, giá đặt và số lượng bàn.
- SR-13: Chủ nhà hàng muốn quản lý thực đơn hiển thị cho khách hàng.
- SR-14: Chủ nhà hàng muốn nhận thông báo khi có đơn đặt bàn mới.
- SR-15: Chủ nhà hàng muốn xác nhận hoặc từ chối đơn đặt bàn.
- SR-16: Chủ nhà hàng muốn tra cứu và tiếp nhận khách đến nhận bàn.
- SR-17: Chủ nhà hàng muốn cập nhật trạng thái phục vụ và hoàn tất đơn.
- SR-18: Chủ nhà hàng muốn xem đánh giá từ khách hàng.
- SR-19: Chủ nhà hàng muốn chỉ được nhận đặt bàn khi nhà hàng đã được xác thực và phê duyệt.

### 4.3. Stakeholder requests của nhân viên nhà hàng

- SR-20: Nhân viên nhà hàng muốn tra cứu đơn nhanh theo mã đơn, tên khách hoặc thời gian đặt.
- SR-21: Nhân viên nhà hàng muốn xác nhận khách đã đến nhận bàn.
- SR-22: Nhân viên nhà hàng muốn cập nhật các trạng thái như đang phục vụ, hoàn tất, đến trễ, không đến.

### 4.4. Stakeholder requests của admin

- SR-23: Admin muốn xem danh sách nhà hàng và trạng thái phê duyệt.
- SR-24: Admin muốn xem chi tiết hồ sơ nhà hàng để phê duyệt hoặc từ chối.
- SR-25: Admin muốn chỉ cho phép nhà hàng hợp lệ được nhận đặt bàn.
- SR-26: Admin muốn kiểm duyệt, ẩn hoặc xoá đánh giá vi phạm.
- SR-27: Admin muốn truy vết lịch sử thay đổi trạng thái đơn đặt bàn.

### 4.5. Stakeholder requests của chủ đầu tư / chủ sản phẩm

- SR-28: Chủ sản phẩm muốn hệ thống ưu tiên triển khai đầy đủ luồng đặt bàn, nhận bàn và đánh giá trong giai đoạn MVP.
- SR-29: Chủ sản phẩm muốn hệ thống có thể mở rộng thêm phương thức thanh toán trong tương lai.
- SR-30: Chủ sản phẩm muốn hệ thống hoạt động ổn định trên cả mobile và desktop.
- SR-31: Chủ sản phẩm muốn dữ liệu đơn hàng, thanh toán và đánh giá được lưu nhất quán để phục vụ vận hành và phân tích.

### 4.6. Stakeholder requests của bộ phận vận hành và hỗ trợ khách hàng

- SR-32: Bộ phận hỗ trợ muốn tra cứu được lịch sử đơn đặt bàn và lịch sử thanh toán khi xử lý sự cố.
- SR-33: Bộ phận hỗ trợ muốn xem log thay đổi trạng thái đơn để đối soát khiếu nại.
- SR-34: Bộ phận hỗ trợ muốn có thông báo và dữ liệu trạng thái rõ ràng để hỗ trợ người dùng nhanh hơn.

### 4.7. Stakeholder requests của đối tác cổng thanh toán

- SR-35: Đối tác thanh toán yêu cầu hệ thống gửi đầy đủ dữ liệu giao dịch thanh toán.
- SR-36: Đối tác thanh toán yêu cầu hệ thống xử lý chính xác kết quả giao dịch thành công, thất bại hoặc hết hạn.

## 5. Ma trận liên kết stakeholder requests với yêu cầu hệ thống

| Mã SR | Stakeholder | Liên kết yêu cầu |
|---|---|---|
| SR-01 | Người dùng đặt bàn | FR-01 |
| SR-02 | Người dùng đặt bàn | FR-02 |
| SR-03 | Người dùng đặt bàn | FR-03, FR-04 |
| SR-04 | Người dùng đặt bàn | FR-05, FR-06 |
| SR-05 | Người dùng đặt bàn | FR-07, FR-08 |
| SR-06 | Người dùng đặt bàn | FR-11 |
| SR-07 | Người dùng đặt bàn | FR-29 |
| SR-08 | Người dùng đặt bàn | FR-12 |
| SR-09 | Người dùng đặt bàn | FR-19, FR-20, FR-21, FR-22, FR-23 |
| SR-10 | Người dùng đặt bàn | FR-24 |
| SR-11 | Chủ nhà hàng | FR-27, FR-30 |
| SR-12 | Chủ nhà hàng | FR-02, FR-03, FR-04, FR-05 |
| SR-13 | Chủ nhà hàng | FR-02 |
| SR-14 | Chủ nhà hàng | FR-09 |
| SR-15 | Chủ nhà hàng | FR-10 |
| SR-16 | Chủ nhà hàng | FR-13, FR-14, FR-15 |
| SR-17 | Chủ nhà hàng | FR-16, FR-17, FR-18 |
| SR-18 | Chủ nhà hàng | FR-25 |
| SR-19 | Chủ nhà hàng | FR-30 |
| SR-20 | Nhân viên nhà hàng | FR-13 |
| SR-21 | Nhân viên nhà hàng | FR-15 |
| SR-22 | Nhân viên nhà hàng | FR-16, FR-17, FR-18 |
| SR-23 | Admin | FR-30 |
| SR-24 | Admin | FR-30 |
| SR-25 | Admin | FR-30 |
| SR-26 | Admin | FR-26 |
| SR-27 | Admin | FR-28 |
| SR-28 | Chủ sản phẩm | FR-01 đến FR-30 |
| SR-29 | Chủ sản phẩm | NFR-16 |
| SR-30 | Chủ sản phẩm | NFR-12 |
| SR-31 | Chủ sản phẩm | NFR-05, NFR-06 |
| SR-32 | Bộ phận hỗ trợ | FR-12 |
| SR-33 | Bộ phận hỗ trợ | FR-28, NFR-10 |
| SR-34 | Bộ phận hỗ trợ | FR-29, NFR-14, NFR-15 |
| SR-35 | Đối tác thanh toán | FR-07, FR-08 |
| SR-36 | Đối tác thanh toán | FR-07, NFR-06 |

## 6. Kết luận

Các stakeholder quan trọng nhất trong phạm vi MVP là:

- Người dùng đặt bàn
- Chủ nhà hàng
- Nhân viên nhà hàng
- Admin
- Đối tác cổng thanh toán

Đây là các bên tác động trực tiếp đến 3 quy trình cốt lõi của REBO: đặt bàn, nhận bàn và đánh giá.
