# Tài liệu Vision và phân tích phạm vi release cho REBO

## 1. Giới thiệu

REBO là hệ thống đặt chỗ nhà hàng giúp kết nối người dùng có nhu cầu đặt bàn với các nhà hàng có nhu cầu quản lý và tối ưu vận hành đặt chỗ. Hệ thống tập trung vào 3 quy trình cốt lõi:

- Đặt bàn
- Nhận bàn
- Đánh giá sau sử dụng dịch vụ

Tài liệu này xác định tầm nhìn sản phẩm và phân tích phạm vi triển khai theo từng release.

## 2. Vision

### 2.1. Tuyên bố tầm nhìn

REBO hướng tới việc trở thành nền tảng đặt chỗ nhà hàng đơn giản, minh bạch và đáng tin cậy, giúp người dùng dễ dàng tìm và đặt bàn, đồng thời giúp nhà hàng quản lý đặt chỗ hiệu quả, hạn chế sai sót và cải thiện trải nghiệm khách hàng.

### 2.2. Vấn đề cần giải quyết

Hiện nay, việc đặt bàn tại nhà hàng thường gặp các vấn đề sau:

- Người dùng khó biết nhà hàng nào còn chỗ trong khung giờ mong muốn.
- Thông tin nhà hàng, loại bàn, giá đặt và thực đơn chưa được hiển thị tập trung và rõ ràng.
- Nhà hàng dễ gặp sai sót khi quản lý đặt chỗ thủ công.
- Khó theo dõi trạng thái đơn và lịch sử xử lý.
- Người dùng thiếu kênh đánh giá sau khi sử dụng dịch vụ.

REBO được xây dựng để giải quyết các vấn đề trên bằng cách số hóa toàn bộ luồng đặt bàn, nhận bàn và đánh giá.

### 2.3. Khách hàng mục tiêu

- Người dùng cá nhân có nhu cầu tìm và đặt bàn nhà hàng.
- Chủ nhà hàng muốn số hóa quy trình nhận đặt bàn.
- Nhân viên nhà hàng cần công cụ tra cứu và tiếp nhận khách.
- Admin cần công cụ kiểm soát chất lượng nhà hàng và nội dung hệ thống.

### 2.4. Giá trị cốt lõi của sản phẩm

- Đối với người dùng:
  - Tìm nhà hàng nhanh.
  - Biết rõ còn chỗ, giá đặt và tổng chi phí.
  - Đặt bàn và thanh toán thuận tiện.
  - Theo dõi trạng thái đơn minh bạch.
  - Đánh giá trải nghiệm sau sử dụng.
- Đối với nhà hàng:
  - Quản lý thông tin nhà hàng tập trung.
  - Quản lý loại bàn, sức chứa và giá đặt.
  - Giảm rủi ro overbooking.
  - Tiếp nhận và xử lý đơn hiệu quả.
  - Thu thập phản hồi từ khách hàng.
- Đối với đơn vị vận hành:
  - Kiểm soát được nhà hàng tham gia.
  - Truy vết được trạng thái đơn và hoạt động nghiệp vụ.
  - Dễ mở rộng sản phẩm trong tương lai.

### 2.5. Mục tiêu kinh doanh

- Thu hút nhà hàng tham gia nền tảng.
- Tăng số lượng đơn đặt bàn được xử lý qua hệ thống.
- Chuẩn hóa quy trình đặt bàn thay cho xử lý thủ công.
- Tạo nền tảng dữ liệu phục vụ vận hành, kiểm duyệt và phát triển sản phẩm.

### 2.6. Mục tiêu sản phẩm trong giai đoạn đầu

- Hoàn thiện đầy đủ luồng đặt bàn.
- Hoàn thiện luồng nhận bàn tại nhà hàng.
- Hoàn thiện luồng đánh giá sau khi hoàn tất đơn.
- Đảm bảo chỉ nhà hàng được xác thực mới được nhận đặt bàn.
- Đảm bảo dữ liệu đơn, thanh toán và đánh giá được lưu nhất quán.

### 2.7. Chỉ số thành công gợi ý

- Tỷ lệ đơn đặt bàn tạo thành công.
- Tỷ lệ thanh toán thành công.
- Tỷ lệ đơn được nhà hàng xác nhận.
- Tỷ lệ đơn hoàn tất.
- Tỷ lệ người dùng gửi đánh giá sau khi hoàn tất đơn.
- Số lượng nhà hàng được xác thực và hoạt động.

## 3. Phạm vi sản phẩm

### 3.1. Trong phạm vi

- Đăng nhập và phân quyền theo vai trò.
- Quản lý nhà hàng.
- Quản lý loại bàn, sức chứa, giá đặt.
- Quản lý thực đơn.
- Tìm kiếm và xem chi tiết nhà hàng.
- Đặt bàn theo ngày, giờ, số người.
- Kiểm tra còn chỗ và tính phụ thu.
- Thanh toán đặt bàn.
- Theo dõi trạng thái đơn đặt bàn.
- Tiếp nhận khách và cập nhật trạng thái phục vụ.
- Đánh giá nhà hàng sau khi hoàn tất đơn.
- Admin duyệt nhà hàng và kiểm duyệt đánh giá.

### 3.2. Ngoài phạm vi hiện tại

- Giao đồ ăn.
- Đặt món trước tại thời điểm đặt bàn.
- Chương trình thành viên, tích điểm, voucher.
- Gợi ý nhà hàng bằng AI.
- Báo cáo phân tích nâng cao theo thời gian thực.
- Tích hợp đa chi nhánh và mô hình nhượng quyền phức tạp.

## 4. Phân tích phạm vi release

## 4.1. Nguyên tắc chia release

- Ưu tiên giá trị nghiệp vụ cốt lõi trước.
- Ưu tiên luồng end-to-end có thể vận hành thực tế.
- Giảm rủi ro bằng cách triển khai từ quy trình đơn giản nhất đến quy trình mở rộng.
- Giữ phạm vi MVP đủ nhỏ để có thể kiểm chứng sớm với người dùng và nhà hàng.

## 5. Release 1: MVP

### 5.1. Mục tiêu release

Xây dựng phiên bản có thể vận hành được đầy đủ luồng từ tìm nhà hàng đến đặt bàn, thanh toán, nhà hàng xác nhận, nhận bàn và người dùng đánh giá sau sử dụng.

### 5.2. Phạm vi chức năng

- Đăng nhập cho người dùng, chủ nhà hàng, admin.
- Chủ nhà hàng tạo và quản lý hồ sơ nhà hàng.
- Chủ nhà hàng quản lý loại bàn, sức chứa, giá đặt, số lượng bàn.
- Chủ nhà hàng quản lý thực đơn.
- Admin duyệt nhà hàng trước khi cho phép hiển thị công khai.
- Người dùng tìm kiếm nhà hàng.
- Người dùng xem chi tiết nhà hàng.
- Người dùng chọn thời gian, loại bàn, số người.
- Hệ thống kiểm tra còn chỗ.
- Hệ thống tính phụ thu theo số người đi.
- Người dùng xác nhận đơn và thanh toán.
- Hệ thống tạo đơn đặt bàn và gửi thông báo.
- Chủ nhà hàng xác nhận hoặc từ chối đơn.
- Nhà hàng tra cứu đơn khi khách đến.
- Nhà hàng cập nhật trạng thái nhận bàn, đang phục vụ, hoàn tất.
- Người dùng xem trạng thái đơn và lịch sử đơn.
- Người dùng gửi đánh giá bằng số sao và bình luận.
- Admin kiểm duyệt đánh giá vi phạm.

### 5.3. Đối tượng sử dụng chính

- Người dùng đặt bàn
- Chủ nhà hàng
- Nhân viên nhà hàng
- Admin
- Đối tác cổng thanh toán

### 5.4. Giá trị đạt được

- Kiểm chứng được toàn bộ mô hình nghiệp vụ cốt lõi của REBO.
- Có thể tiếp nhận nhà hàng thật và đơn đặt bàn thật.
- Tạo dữ liệu đầu tiên về đơn hàng, thanh toán và đánh giá.

### 5.5. Rủi ro chính

- Xử lý đồng thời có thể dẫn tới sai lệch số lượng bàn trống.
- Thanh toán thất bại hoặc callback chậm từ cổng thanh toán.
- Nhà hàng thao tác trạng thái đơn không nhất quán.

### 5.6. Tiêu chí hoàn thành release

- Người dùng hoàn tất được luồng `tìm nhà hàng -> đặt bàn -> thanh toán -> theo dõi đơn -> đánh giá`.
- Nhà hàng hoàn tất được luồng `nhận đơn -> xác nhận/từ chối -> tiếp nhận khách -> hoàn tất đơn`.
- Admin hoàn tất được luồng `duyệt nhà hàng -> kiểm duyệt đánh giá`.

## 6. Release 2: Mở rộng vận hành

### 6.1. Mục tiêu release

Nâng cao khả năng vận hành thực tế, hỗ trợ quản lý tốt hơn các tình huống ngoại lệ và hỗ trợ khách hàng.

### 6.2. Phạm vi đề xuất

- Quản lý khiếu nại từ người dùng.
- Cải thiện thông báo hệ thống theo sự kiện.
- Tra cứu trạng thái đơn nhanh cho người dùng và nhà hàng.
- Lịch sử trạng thái đơn chi tiết hơn.
- Hỗ trợ vận hành trong các trường hợp đến trễ, không đến, huỷ đơn.
- Bổ sung màn hình và dữ liệu hỗ trợ xử lý sự cố cho bộ phận CS.

### 6.3. Lý do đưa vào Release 2

- Các chức năng này quan trọng cho vận hành nhưng chưa phải điều kiện tối thiểu để kiểm chứng mô hình sản phẩm.
- Nên triển khai sau khi đã có dữ liệu thực từ MVP để thiết kế đúng mức cần thiết.

### 6.4. Giá trị đạt được

- Giảm áp lực xử lý thủ công cho bộ phận hỗ trợ.
- Tăng minh bạch khi giải quyết khiếu nại và đối soát đơn hàng.
- Nâng chất lượng vận hành hệ thống.

## 7. Release 3: Tăng trưởng và tối ưu

### 7.1. Mục tiêu release

Mở rộng trải nghiệm người dùng, tối ưu chuyển đổi và bổ sung năng lực tăng trưởng cho nền tảng.

### 7.2. Phạm vi đề xuất

- Nhiều phương thức thanh toán hơn.
- Tối ưu tìm kiếm và lọc nhà hàng.
- Báo cáo thống kê cho chủ nhà hàng.
- Dashboard vận hành nâng cao cho admin.
- Cải thiện trải nghiệm đánh giá và phản hồi đánh giá.
- Các chương trình khuyến mãi, voucher hoặc loyalty nếu cần.

### 7.3. Lý do đưa vào Release 3

- Đây là các chức năng tăng trưởng hoặc tối ưu, phụ thuộc vào việc sản phẩm đã vận hành ổn định ở các release trước.
- Chúng mang lại giá trị lớn hơn khi hệ thống đã có lượng người dùng và dữ liệu đủ nhiều.

### 7.4. Giá trị đạt được

- Tăng tỷ lệ chuyển đổi từ xem nhà hàng sang đặt bàn.
- Tăng khả năng giữ chân người dùng và nhà hàng.
- Tăng khả năng quản trị và ra quyết định dựa trên dữ liệu.

## 8. Ma trận ưu tiên release

| Hạng mục | Release 1 | Release 2 | Release 3 |
|---|---|---|---|
| Đăng nhập, phân quyền | Có | Tối ưu | Tối ưu |
| Quản lý nhà hàng | Có | Mở rộng | Tối ưu |
| Quản lý loại bàn và giá đặt | Có | Tối ưu | Tối ưu |
| Quản lý thực đơn | Có | Tối ưu | Tối ưu |
| Tìm kiếm và xem nhà hàng | Có | Tối ưu | Nâng cao |
| Đặt bàn và kiểm tra còn chỗ | Có | Tối ưu | Nâng cao |
| Thanh toán | Có | Tối ưu lỗi nghiệp vụ | Mở rộng phương thức |
| Theo dõi trạng thái đơn | Có | Mở rộng tra cứu | Nâng cao phân tích |
| Nhận bàn và cập nhật phục vụ | Có | Mở rộng ngoại lệ | Tối ưu |
| Đánh giá | Có | Kiểm duyệt tốt hơn | Mở rộng phản hồi |
| Khiếu nại | Chưa ưu tiên | Có | Tối ưu |
| Dashboard và báo cáo nâng cao | Cơ bản | Mở rộng | Có |

## 9. Khuyến nghị phạm vi release

### 9.1. Khuyến nghị cho Release 1

Release 1 nên giữ phạm vi chặt vào 3 luồng:

- Đặt bàn
- Nhận bàn
- Đánh giá

Không nên đưa quá nhiều chức năng vận hành phụ như khiếu nại phức tạp, báo cáo nâng cao hay chương trình khuyến mãi vào MVP vì sẽ làm tăng độ phức tạp nhưng không giúp kiểm chứng nhanh giá trị cốt lõi.

### 9.2. Khuyến nghị cho Release 2

Release 2 nên tập trung vào ổn định vận hành:

- Khiếu nại
- Đối soát
- Tra cứu nhanh
- Lịch sử trạng thái chi tiết
- Hỗ trợ xử lý ngoại lệ

### 9.3. Khuyến nghị cho Release 3

Release 3 nên tập trung vào tăng trưởng và mở rộng:

- Tối ưu chuyển đổi
- Báo cáo và phân tích
- Mở rộng thanh toán
- Khuyến mãi và giữ chân người dùng

## 10. Kết luận

Vision của REBO là xây dựng một nền tảng đặt chỗ nhà hàng minh bạch, dễ dùng và đáng tin cậy cho cả người dùng lẫn nhà hàng. Để đạt mục tiêu này, phạm vi release nên được chia theo hướng triển khai trước các luồng cốt lõi, sau đó mới mở rộng vận hành và tăng trưởng.

Thứ tự ưu tiên phù hợp là:

1. Release 1: MVP cho đặt bàn, nhận bàn, đánh giá
2. Release 2: Mở rộng vận hành và xử lý ngoại lệ
3. Release 3: Tăng trưởng, tối ưu và mở rộng hệ sinh thái
