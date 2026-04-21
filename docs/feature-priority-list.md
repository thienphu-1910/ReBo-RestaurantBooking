# Danh sách chức năng theo độ ưu tiên cho REBO

## 1. Mục tiêu

Tài liệu này phân loại các chức năng của hệ thống REBO theo 3 mức độ ưu tiên:

- Must Have
- Should Have
- Nice to Have

Việc phân loại dựa trên các tiêu chí:

- Mức độ cần thiết để hệ thống vận hành được end-to-end
- Mức độ ảnh hưởng đến giá trị cốt lõi của sản phẩm
- Mức độ cần thiết cho release MVP
- Mức độ hỗ trợ vận hành hoặc tăng trưởng về sau

## 2. Must Have

Đây là các chức năng bắt buộc phải có để REBO vận hành được trong giai đoạn đầu.

| STT | Chức năng | Lý do ưu tiên |
|---|---|---|
| 1 | Đăng nhập và phân quyền cho người dùng, chủ nhà hàng, admin | Là điều kiện nền tảng để truy cập đúng chức năng theo vai trò |
| 2 | Chủ nhà hàng tạo và quản lý hồ sơ nhà hàng | Không có dữ liệu nhà hàng thì hệ thống không thể cung cấp dịch vụ đặt bàn |
| 3 | Quản lý loại bàn, sức chứa, giá đặt, số lượng bàn | Là cơ sở để kiểm tra còn chỗ và tính chi phí đặt bàn |
| 4 | Quản lý thực đơn nhà hàng | Là dữ liệu quan trọng giúp người dùng xem xét và chọn nhà hàng |
| 5 | Admin xác thực/phê duyệt nhà hàng | Đảm bảo chỉ nhà hàng hợp lệ mới được hiển thị và nhận đặt bàn |
| 6 | Người dùng tìm kiếm và xem danh sách nhà hàng | Là điểm bắt đầu của toàn bộ luồng đặt bàn |
| 7 | Người dùng xem chi tiết nhà hàng | Cần để người dùng biết thông tin nhà hàng, loại bàn, giá đặt, thực đơn |
| 8 | Người dùng chọn ngày, giờ, loại bàn, số người | Là thao tác cốt lõi của quy trình đặt bàn |
| 9 | Hệ thống kiểm tra bàn còn trống theo khung giờ | Tránh overbooking và bảo đảm tính đúng đắn của đơn |
| 10 | Hệ thống tính giá đặt bàn và phụ thu | Cần để hiển thị chi phí minh bạch trước khi thanh toán |
| 11 | Người dùng xác nhận đơn đặt bàn | Là bước chốt thông tin trước khi thanh toán |
| 12 | Thanh toán đơn đặt bàn | Là một phần cốt lõi của luồng nghiệp vụ MVP |
| 13 | Hệ thống tạo đơn đặt bàn và lưu lịch sử đơn | Là kết quả chính của quy trình đặt bàn |
| 14 | Chủ nhà hàng nhận thông báo đơn mới | Giúp đơn được xử lý kịp thời |
| 15 | Chủ nhà hàng xác nhận hoặc từ chối đơn | Là bước bắt buộc để đơn chuyển sang trạng thái phục vụ thực tế |
| 16 | Người dùng xem trạng thái đơn đặt bàn | Đảm bảo tính minh bạch cho khách hàng |
| 17 | Nhà hàng tra cứu đơn khi khách đến | Là đầu vào của quy trình nhận bàn |
| 18 | Nhà hàng xác nhận khách đã đến nhận bàn | Cần để chuyển trạng thái đơn sang phục vụ |
| 19 | Nhà hàng cập nhật trạng thái đang phục vụ và hoàn tất | Là điều kiện để đóng vòng đời đơn và mở quyền đánh giá |
| 20 | Người dùng gửi đánh giá bằng số sao và bình luận | Là quy trình cốt lõi thứ ba của hệ thống |
| 21 | Admin kiểm duyệt đánh giá vi phạm | Cần để bảo đảm chất lượng nội dung trên nền tảng |
| 22 | Ghi nhận lịch sử thay đổi trạng thái đơn | Cần cho đối soát, hỗ trợ và truy vết nghiệp vụ |
| 23 | Gửi thông báo khi trạng thái đơn thay đổi | Giúp người dùng và nhà hàng theo dõi tiến trình xử lý |

## 3. Should Have

Đây là các chức năng quan trọng, nên có để hệ thống vận hành tốt hơn, nhưng có thể triển khai sau MVP nếu nguồn lực hạn chế.

| STT | Chức năng | Lý do ưu tiên |
|---|---|---|
| 1 | Người dùng xem lịch sử đặt bàn | Hữu ích cho việc tra cứu lại đơn cũ nhưng không ảnh hưởng trực tiếp đến tạo đơn mới |
| 2 | Người dùng quản lý đánh giá của mình | Tăng trải nghiệm người dùng nhưng không phải điều kiện tối thiểu của MVP |
| 3 | Tra cứu trạng thái đơn nhanh | Hỗ trợ tra cứu thuận tiện hơn cho người dùng và nhà hàng |
| 4 | Lịch sử trạng thái đơn chi tiết | Hữu ích cho đối soát và vận hành nâng cao |
| 5 | Hỗ trợ xử lý ngoại lệ đến trễ, không đến, huỷ đơn | Quan trọng cho vận hành thực tế nhưng có thể đơn giản hóa ở bản đầu |
| 6 | Thông báo hệ thống tập trung | Tốt cho trải nghiệm nhưng có thể thay bằng thông báo cơ bản ở giai đoạn đầu |
| 7 | Admin chỉnh sửa hoặc xoá nhà hàng vi phạm | Quan trọng cho kiểm soát vận hành nhưng chưa nhất thiết là luồng cốt lõi ban đầu |
| 8 | Quản lý khiếu nại | Quan trọng cho giai đoạn mở rộng vận hành sau khi có người dùng thật |
| 9 | Bộ phận hỗ trợ tra cứu đơn và thanh toán | Phục vụ CS tốt hơn nhưng có thể tạm dựa vào admin trong giai đoạn đầu |
| 10 | Tối ưu giao diện cho thao tác nhận bàn nhanh | Quan trọng với nhân viên nhà hàng nhưng có thể triển khai cải tiến sau khi thử nghiệm MVP |

## 4. Nice to Have

Đây là các chức năng mang tính tối ưu trải nghiệm, tăng trưởng hoặc mở rộng, không bắt buộc trong giai đoạn đầu.

| STT | Chức năng | Lý do ưu tiên |
|---|---|---|
| 1 | Nhiều phương thức thanh toán | Có ích cho mở rộng nhưng chỉ cần một phương thức ổn định ở giai đoạn đầu |
| 2 | Tối ưu tìm kiếm và lọc nâng cao | Tăng chuyển đổi nhưng không phải điều kiện tối thiểu để sử dụng hệ thống |
| 3 | Dashboard và báo cáo nâng cao cho chủ nhà hàng | Hữu ích về quản trị nhưng không thuộc luồng cốt lõi |
| 4 | Dashboard vận hành nâng cao cho admin | Giúp theo dõi hệ thống tốt hơn sau khi đã có dữ liệu thực tế |
| 5 | Phản hồi đánh giá từ phía nhà hàng | Tăng tương tác nhưng chưa bắt buộc với MVP |
| 6 | Chương trình khuyến mãi, voucher, loyalty | Mang tính tăng trưởng và giữ chân người dùng |
| 7 | Gợi ý nhà hàng thông minh | Tăng trải nghiệm nhưng không thuộc bài toán cốt lõi ban đầu |
| 8 | Phân tích dữ liệu thời gian thực | Phù hợp giai đoạn mở rộng, không cần cho bản đầu |
| 9 | Đặt món trước tại thời điểm đặt bàn | Mở rộng nghiệp vụ, làm tăng đáng kể độ phức tạp hệ thống |
| 10 | Hỗ trợ mô hình đa chi nhánh phức tạp | Chưa cần nếu sản phẩm mới ở giai đoạn kiểm chứng thị trường |

## 5. Tóm tắt theo release

### 5.1. Must Have tương ứng Release 1

- Phần lớn các chức năng Must Have thuộc Release 1 vì đây là nhóm chức năng cần để hoàn thiện 3 luồng cốt lõi:
  - Đặt bàn
  - Nhận bàn
  - Đánh giá

### 5.2. Should Have tương ứng Release 2

- Phần lớn các chức năng Should Have phù hợp với Release 2 vì tập trung vào:
  - Ổn định vận hành
  - Đối soát dữ liệu
  - Hỗ trợ khách hàng
  - Xử lý ngoại lệ nghiệp vụ

### 5.3. Nice to Have tương ứng Release 3

- Phần lớn các chức năng Nice to Have phù hợp với Release 3 vì tập trung vào:
  - Tăng trưởng
  - Tối ưu chuyển đổi
  - Mở rộng năng lực sản phẩm

## 6. Khuyến nghị triển khai

- Trong giai đoạn MVP, chỉ nên cam kết đầy đủ nhóm Must Have.
- Nhóm Should Have nên được xem là phạm vi mở rộng ngay sau khi MVP ổn định.
- Nhóm Nice to Have nên được cân nhắc dựa trên dữ liệu thực tế từ người dùng và nhà hàng sau khi hệ thống đã vận hành.

## 7. Kết luận

Việc phân loại chức năng theo `Must Have`, `Should Have`, `Nice to Have` giúp REBO tập trung nguồn lực vào giá trị cốt lõi trước, giảm rủi ro triển khai và tạo nền tảng tốt cho các giai đoạn mở rộng sau này.
