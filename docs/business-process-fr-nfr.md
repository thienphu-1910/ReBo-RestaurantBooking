# Quy trình nghiệp vụ chính, FRs và NFRs cho REBO

## 1. Quy trình nghiệp vụ chính

Hệ thống REBO có 3 quy trình nghiệp vụ chính:

- Đặt bàn
- Nhận bàn
- Đánh giá sau sử dụng dịch vụ

## 2. Quy trình nghiệp vụ 1: Đặt bàn

### 2.1. Mục tiêu

Cho phép người dùng tìm nhà hàng, chọn bàn phù hợp, thanh toán tiền đặt chỗ và tạo đơn đặt bàn hợp lệ.

### 2.2. Tác nhân tham gia

- Người dùng
- Chủ nhà hàng
- Hệ thống thanh toán
- Hệ thống REBO

### 2.3. Tiền điều kiện

- Nhà hàng đã được admin phê duyệt và đang hoạt động
- Chủ nhà hàng đã khai báo loại bàn, giá đặt, sức chứa, giờ mở/đóng
- Người dùng đã đăng nhập

### 2.4. Luồng chính

1. Người dùng tìm kiếm và chọn nhà hàng.
2. Hệ thống hiển thị thông tin nhà hàng, loại bàn, giá đặt, sức chứa, thực đơn và thời gian hoạt động.
3. Người dùng chọn ngày, giờ, loại bàn và số lượng người đi.
4. Hệ thống kiểm tra bàn còn trống theo khung giờ.
5. Hệ thống tính giá đặt bàn và phụ thu nếu số người vượt ngưỡng cơ bản.
6. Người dùng xác nhận thông tin đặt bàn.
7. Người dùng thực hiện thanh toán.
8. Hệ thống ghi nhận thanh toán thành công và tạo đơn đặt bàn.
9. Hệ thống gửi thông báo cho người dùng và chủ nhà hàng.
10. Chủ nhà hàng xác nhận hoặc từ chối đơn đặt bàn.
11. Hệ thống cập nhật trạng thái đơn đặt bàn.

### 2.5. Luồng ngoại lệ

- Không còn bàn trống trong khung giờ đã chọn.
- Nhà hàng ngoài thời gian hoạt động.
- Số người vượt quá giới hạn phục vụ.
- Thanh toán thất bại.
- Chủ nhà hàng từ chối đơn đặt bàn.
- Người dùng huỷ đơn trong thời gian cho phép.

### 2.6. Kết quả đầu ra

- Đơn đặt bàn được tạo và lưu vào hệ thống.
- Trạng thái đơn được cập nhật tương ứng.
- Lịch sử thanh toán và lịch sử đặt bàn được ghi nhận.

## 3. Quy trình nghiệp vụ 2: Nhận bàn

### 3.1. Mục tiêu

Cho phép nhà hàng tiếp nhận khách đến đúng lịch đặt, xác nhận khách đã sử dụng bàn và hoàn tất đơn đặt bàn.

### 3.2. Tác nhân tham gia

- Người dùng
- Chủ nhà hàng hoặc nhân viên nhà hàng
- Hệ thống REBO

### 3.3. Tiền điều kiện

- Đơn đặt bàn đã được xác nhận
- Người dùng đến nhà hàng trong khung giờ đặt

### 3.4. Luồng chính

1. Người dùng đến nhà hàng theo thời gian đã đặt.
2. Chủ nhà hàng hoặc nhân viên tra cứu đơn đặt bàn.
3. Hệ thống hiển thị thông tin đơn: mã đơn, thời gian, số người, loại bàn, trạng thái thanh toán.
4. Nhà hàng xác nhận khách đã đến.
5. Hệ thống cập nhật trạng thái đơn sang đã nhận bàn hoặc đang phục vụ.
6. Sau khi kết thúc bữa ăn, nhà hàng cập nhật trạng thái đơn sang hoàn tất.
7. Hệ thống ghi nhận thời điểm hoàn tất đơn để mở quyền đánh giá cho người dùng.

### 3.5. Luồng ngoại lệ

- Người dùng đến trễ quá thời gian giữ bàn.
- Người dùng không đến nhận bàn.
- Số lượng khách thực tế khác với số lượng đã đặt.
- Đơn chưa thanh toán hoặc thanh toán chưa hợp lệ.
- Nhà hàng không tìm thấy đơn đặt bàn hợp lệ.

### 3.6. Kết quả đầu ra

- Trạng thái đơn được cập nhật chính xác theo tình trạng phục vụ thực tế.
- Hệ thống xác định đơn đủ điều kiện để đánh giá.

## 4. Quy trình nghiệp vụ 3: Đánh giá

### 4.1. Mục tiêu

Cho phép người dùng gửi đánh giá về trải nghiệm nhà hàng sau khi hoàn tất đơn đặt bàn.

### 4.2. Tác nhân tham gia

- Người dùng
- Chủ nhà hàng
- Admin
- Hệ thống REBO

### 4.3. Tiền điều kiện

- Đơn đặt bàn đã ở trạng thái hoàn tất
- Người dùng là người thực hiện đơn đặt bàn

### 4.4. Luồng chính

1. Hệ thống mở quyền đánh giá cho người dùng sau khi đơn hoàn tất.
2. Người dùng chọn số sao đánh giá.
3. Người dùng nhập bình luận.
4. Hệ thống kiểm tra dữ liệu đánh giá hợp lệ.
5. Hệ thống lưu đánh giá và gắn với nhà hàng, người dùng, đơn đặt bàn.
6. Hệ thống hiển thị đánh giá tại trang chi tiết nhà hàng.
7. Chủ nhà hàng xem đánh giá và có thể phản hồi nếu hệ thống hỗ trợ.
8. Admin kiểm duyệt hoặc xử lý đánh giá vi phạm nếu phát sinh.

### 4.5. Luồng ngoại lệ

- Người dùng chưa hoàn tất bữa ăn nhưng cố gửi đánh giá.
- Người dùng gửi nội dung không hợp lệ hoặc vi phạm chính sách.
- Người dùng gửi trùng đánh giá cho cùng một đơn đặt bàn nếu hệ thống chỉ cho phép một lần.

### 4.6. Kết quả đầu ra

- Đánh giá được lưu và hiển thị công khai hoặc chờ kiểm duyệt.
- Dữ liệu đánh giá được dùng để phản ánh chất lượng nhà hàng.

## 5. Functional Requirements (FRs)

### 5.1. FRs cho quy trình đặt bàn

- FR-01: Hệ thống phải cho phép người dùng tìm kiếm và xem danh sách nhà hàng đang hoạt động.
- FR-02: Hệ thống phải hiển thị chi tiết nhà hàng gồm địa chỉ, mô tả, thời gian mở/đóng, loại bàn, sức chứa, giá đặt và danh sách món ăn.
- FR-03: Hệ thống phải cho phép người dùng chọn ngày, giờ, loại bàn và số lượng người khi đặt bàn.
- FR-04: Hệ thống phải kiểm tra khả năng phục vụ của nhà hàng theo khung giờ được chọn.
- FR-05: Hệ thống phải tính tổng chi phí đặt bàn gồm giá đặt và phụ thu theo số lượng người đi.
- FR-06: Hệ thống phải cho phép người dùng xác nhận thông tin đặt bàn trước khi thanh toán.
- FR-07: Hệ thống phải hỗ trợ ghi nhận trạng thái thanh toán của đơn đặt bàn.
- FR-08: Hệ thống phải tạo đơn đặt bàn sau khi thanh toán thành công hoặc theo chính sách giữ chỗ của hệ thống.
- FR-09: Hệ thống phải gửi thông báo cho chủ nhà hàng khi có đơn đặt bàn mới.
- FR-10: Hệ thống phải cho phép chủ nhà hàng xác nhận hoặc từ chối đơn đặt bàn.
- FR-11: Hệ thống phải cho phép người dùng xem trạng thái đơn đặt bàn.
- FR-12: Hệ thống phải lưu lịch sử đặt bàn và lịch sử thanh toán.

### 5.2. FRs cho quy trình nhận bàn

- FR-13: Hệ thống phải cho phép nhà hàng tra cứu đơn đặt bàn theo mã đơn, tên khách hoặc thời gian đặt.
- FR-14: Hệ thống phải hiển thị đầy đủ thông tin đơn đặt bàn khi nhà hàng tiếp nhận khách.
- FR-15: Hệ thống phải cho phép nhà hàng xác nhận khách đã đến nhận bàn.
- FR-16: Hệ thống phải cập nhật trạng thái đơn sang đã nhận bàn hoặc đang phục vụ.
- FR-17: Hệ thống phải cho phép nhà hàng cập nhật trạng thái đơn sang hoàn tất sau khi kết thúc phục vụ.
- FR-18: Hệ thống phải xử lý các trạng thái bất thường như đến trễ, không đến, hoặc huỷ đơn.

### 5.3. FRs cho quy trình đánh giá

- FR-19: Hệ thống chỉ cho phép người dùng đánh giá khi đơn đặt bàn đã hoàn tất.
- FR-20: Hệ thống phải cho phép người dùng gửi đánh giá theo số sao.
- FR-21: Hệ thống phải cho phép người dùng gửi bình luận kèm theo đánh giá.
- FR-22: Hệ thống phải lưu đánh giá gắn với nhà hàng, người dùng và đơn đặt bàn.
- FR-23: Hệ thống phải hiển thị đánh giá tại trang chi tiết nhà hàng.
- FR-24: Hệ thống phải cho phép người dùng chỉnh sửa hoặc xoá đánh giá của mình nếu chính sách hệ thống cho phép.
- FR-25: Hệ thống phải cho phép chủ nhà hàng xem đánh giá từ người dùng.
- FR-26: Hệ thống phải cho phép admin kiểm duyệt, ẩn hoặc xoá đánh giá vi phạm.

### 5.4. FRs dùng chung

- FR-27: Hệ thống phải phân quyền theo vai trò người dùng, chủ nhà hàng và admin.
- FR-28: Hệ thống phải ghi nhận lịch sử thay đổi trạng thái của đơn đặt bàn.
- FR-29: Hệ thống phải gửi thông báo cho người dùng khi trạng thái đơn thay đổi.
- FR-30: Hệ thống phải đảm bảo chỉ nhà hàng đã được xác thực và phê duyệt mới được nhận đặt bàn.

## 6. Non-functional Requirements (NFRs)

### 6.1. Hiệu năng

- NFR-01: Thời gian phản hồi cho thao tác tìm kiếm nhà hàng không vượt quá 3 giây trong điều kiện tải thông thường.
- NFR-02: Thời gian phản hồi cho thao tác kiểm tra bàn trống và tính chi phí không vượt quá 2 giây.
- NFR-03: Hệ thống phải hỗ trợ đồng thời nhiều người dùng đặt bàn mà không làm sai lệch số lượng bàn còn trống.

### 6.2. Độ tin cậy và toàn vẹn dữ liệu

- NFR-04: Hệ thống phải đảm bảo không phát sinh trùng đặt bàn cho cùng một bàn hoặc cùng một suất phục vụ ngoài khả năng khai báo.
- NFR-05: Trạng thái đơn đặt bàn, thanh toán và đánh giá phải được lưu nhất quán và có thể truy vết.
- NFR-06: Dữ liệu giao dịch thanh toán phải được lưu an toàn và không bị mất khi xảy ra lỗi hệ thống tạm thời.

### 6.3. Bảo mật

- NFR-07: Hệ thống phải yêu cầu xác thực người dùng trước khi đặt bàn, thanh toán hoặc đánh giá.
- NFR-08: Hệ thống phải phân quyền chặt chẽ giữa người dùng, chủ nhà hàng và admin.
- NFR-09: Dữ liệu cá nhân và dữ liệu thanh toán phải được bảo vệ trong quá trình truyền và lưu trữ.
- NFR-10: Hệ thống phải lưu nhật ký cho các thao tác quan trọng như xác nhận đơn, huỷ đơn, hoàn tất đơn và kiểm duyệt đánh giá.

### 6.4. Khả dụng

- NFR-11: Hệ thống phải sẵn sàng phục vụ tối thiểu 99.5% thời gian mỗi tháng.
- NFR-12: Hệ thống phải hỗ trợ sử dụng trên thiết bị di động và máy tính để bàn.

### 6.5. Khả năng sử dụng

- NFR-13: Quy trình đặt bàn phải được hoàn thành với số bước tối thiểu và giao diện rõ ràng.
- NFR-14: Hệ thống phải hiển thị rõ trạng thái đơn đặt bàn, trạng thái thanh toán và quyền đánh giá.
- NFR-15: Các thông báo lỗi phải dễ hiểu và hướng dẫn người dùng cách xử lý.

### 6.6. Khả năng mở rộng và bảo trì

- NFR-16: Hệ thống phải cho phép mở rộng thêm phương thức thanh toán trong tương lai.
- NFR-17: Hệ thống phải cho phép mở rộng thêm chính sách phụ thu, giữ bàn và kiểm duyệt đánh giá mà không ảnh hưởng lớn đến luồng hiện tại.

## 7. Tóm tắt phạm vi ưu tiên

Trong giai đoạn MVP, nên ưu tiên triển khai đầy đủ 3 quy trình sau:

- Đặt bàn có kiểm tra chỗ trống và thanh toán
- Nhận bàn với cập nhật trạng thái đơn
- Đánh giá sau khi hoàn tất đơn đặt bàn

Đây là 3 quy trình cốt lõi tạo nên giá trị chính của hệ thống REBO.
