# Quy trình nghiệp vụ

## 1. Tổng quan

DAYORA có hai quy trình mua hàng chính:

1. Tạo bộ đồ dùng và mua hàng bằng Kit Builder.
2. Mua từng sản phẩm.

Hai quy trình sử dụng chung các bước checkout, thanh toán, xử lý đơn và theo dõi giao hàng.

Các bên tham gia gồm khách hàng, hệ thống DAYORA, cổng thanh toán VNPay Sandbox và quản trị viên.

Khách chưa đăng nhập có thể xem sản phẩm và sử dụng Kit Builder. Theo phạm vi hiện tại trong REQUIREMENTS.md, khách cần đăng nhập để sử dụng giỏ hàng và đặt hàng.

## 2. Quy trình tạo bộ và mua hàng

### Bước 1. Chọn tình huống

Khách chọn một trong ba tình huống: picnic ăn nhẹ, hẹn hò buổi chiều hoặc đi biển trong ngày.

### Bước 2. Khai báo nhu cầu

Khách nhập số người, ngân sách và số lượng hoặc sức chứa của đồ dùng đã có.

Số người thuộc phạm vi từ 1 đến 8.

### Bước 3. Kiểm tra đầu vào

Hệ thống kiểm tra tình huống, số người, ngân sách và thông tin đồ đã có.

Nếu dữ liệu không hợp lệ, hệ thống thông báo rõ trường cần sửa và yêu cầu nhập lại.

### Bước 4. Tính nhu cầu còn thiếu

Kit Builder xác định nhu cầu theo tình huống và số người.

Hệ thống phân biệt món theo người với món dùng chung, sau đó trừ phần đồ đã có theo đúng công dụng và sức chứa.

Chỉ lựa chọn sản phẩm còn bán và đủ tồn kho.

### Bước 5. Hiển thị bộ gợi ý

Hệ thống hiển thị sản phẩm, số lượng, lý do đề xuất, món thiết yếu, món tùy chọn và chi phí.

Nếu chưa có địa chỉ giao hàng, phí giao và tổng tiền liên quan được ghi rõ là tạm tính.

Nếu không tìm được bộ phù hợp, hệ thống giải thích nguyên nhân, không tự tăng ngân sách hoặc bỏ món thiết yếu.

### Bước 6. Điều chỉnh bộ

Khách có thể thay sản phẩm hoặc điều chỉnh bộ.

Hệ thống kiểm tra công dụng, sức chứa, tồn kho và ngân sách sau thay đổi, đồng thời cập nhật chi phí.

Nếu khách bỏ món thiết yếu, hệ thống không tiếp tục hiển thị bộ là đầy đủ. Khách vẫn có thể lựa chọn mua các món riêng lẻ.

### Bước 7. Thêm vào giỏ

Khách đăng nhập nếu chưa có phiên hợp lệ, sau đó thêm bộ vào giỏ.

Hệ thống kiểm tra lại dữ liệu cần thiết và thêm đúng sản phẩm, biến thể, số lượng.

### Bước 8. Điều chỉnh giỏ và dùng voucher

Khách thay đổi số lượng, xóa sản phẩm hoặc nhập voucher.

Hệ thống kiểm tra điều kiện áp dụng và cập nhật tiền hàng, giảm giá.

Sản phẩm gợi ý bổ sung chỉ được thêm khi khách chủ động lựa chọn.

### Bước 9. Nhập thông tin giao hàng

Khách nhập thông tin người nhận, liên hệ và địa chỉ.

Hệ thống kiểm tra dữ liệu, xác định phí giao theo bảng quy tắc và cập nhật tổng thực trả.

### Bước 10. Kiểm tra và xác nhận đơn

Backend kiểm tra lại giá, tồn kho, voucher và phí giao.

Nếu thông tin thay đổi, hệ thống hiển thị nội dung thay đổi và yêu cầu khách xác nhận lại.

Khách kiểm tra sản phẩm, số lượng và tổng tiền trước khi xác nhận.

### Bước 11. Tạo đơn và thanh toán

Hệ thống tạo đơn, lưu thông tin đã chốt và xử lý tồn kho theo chính sách của nhóm.

Hệ thống tạo yêu cầu thanh toán VNPay Sandbox gắn với đơn và số tiền tương ứng.

Khi nhận kết quả, Backend xác thực thông tin trước khi cập nhật trạng thái thanh toán.

### Bước 12. Xử lý và giao hàng

Quản trị viên kiểm tra, xử lý đơn và cập nhật trạng thái giao hàng theo quy trình hợp lệ.

Trạng thái giao hàng được quản lý riêng với trạng thái thanh toán.

### Bước 13. Theo dõi và đánh giá

Khách xem lịch sử, chi tiết và trạng thái đơn của mình.

Sau mua, khách được đánh giá sản phẩm khi đáp ứng điều kiện trong REQUIREMENTS.md.

## 3. Quy trình mua lẻ

### Bước 1. Tìm sản phẩm

Khách xem danh mục hoặc sử dụng tìm kiếm, bộ lọc và sắp xếp.

### Bước 2. Xem chi tiết

Khách xem hình ảnh, giá, thông số, sức chứa, tồn kho và đánh giá.

Khách chọn biến thể và số lượng cần mua.

### Bước 3. Thêm vào giỏ

Khách đăng nhập nếu cần và thêm sản phẩm vào giỏ.

Hệ thống kiểm tra dữ liệu, ghi nhận đúng sản phẩm, biến thể và số lượng.

Khách có thể tiếp tục mua thêm.

### Bước 4. Hoàn tất mua hàng

Khách thực hiện các bước điều chỉnh giỏ, dùng voucher, nhập địa chỉ, xác nhận đơn và thanh toán như bước 8 đến bước 11 của quy trình tạo bộ.

### Bước 5. Theo dõi đơn

Quản trị viên xử lý đơn và cập nhật giao hàng.

Khách theo dõi đơn và đánh giá khi đủ điều kiện như bước 12 đến bước 13 của quy trình tạo bộ.

## 4. Quy tắc tính số lượng và tổng tiền

### Món theo người

Tính phần định lượng còn thiếu sau khi trừ đồ đã có phù hợp công dụng.

Số lượng cần mua không được âm.

### Món dùng chung

Tính theo sức chứa còn thiếu và làm tròn lên khi cần mua thêm sản phẩm.

Ví dụ: nhóm 5 người, mỗi thảm có sức chứa được xác định là 4 người. Nếu chưa có thảm thì cần 2 thảm; nếu đã có một thảm đủ cho 4 người thì cần mua thêm 1 thảm.

Sức chứa phải có căn cứ hoặc được ghi rõ là giả định của dữ liệu demo, không tự suy ra số người chỉ từ kích thước.

### Tổng tiền

Tổng thực trả = tiền hàng − giảm giá + phí giao hàng.

Voucher phải được kiểm tra tại Backend.

Khi chưa có địa chỉ, phí giao chỉ là tạm tính. Sau khi xác định phí, hệ thống cập nhật tổng và kiểm tra lại ngân sách đối với bộ đồ dùng.

Nếu thay đổi làm vượt ngân sách, hệ thống thông báo và cho khách điều chỉnh, không tự tăng ngân sách.

## 5. Xử lý ngoại lệ

### Không tìm được bộ phù hợp

Giải thích điều kiện chưa đáp ứng và cho khách thay đổi đầu vào hoặc lựa chọn sản phẩm.

Không tự bỏ món thiết yếu để hiển thị bộ là phù hợp.

### Đồ đã có đáp ứng đủ nhu cầu

Thông báo khách đã có đủ đồ theo quy tắc.

Không tạo số lượng mua âm hoặc buộc khách mua thêm.

### Không đủ tồn kho

Thông báo sản phẩm thiếu hoặc đề xuất thay thế đáp ứng điều kiện.

Backend kiểm tra lại trước khi tạo đơn, không chỉ dựa vào tồn kho đã hiển thị trước đó.

### Voucher không hợp lệ

Thông báo nguyên nhân và không áp dụng giảm giá.

Cập nhật tổng khi khách sửa giỏ hoặc bỏ voucher.

### Giá hoặc phí thay đổi

Hiển thị thông tin mới và yêu cầu khách xác nhận lại trước khi hoàn tất đơn.

### Thanh toán thất bại hoặc hủy

Không ghi nhận đơn là đã thanh toán.

Hiển thị trạng thái và hướng xử lý phù hợp. Việc thanh toán lại hoặc hủy đơn tuân theo chính sách được nhóm thống nhất.

### Kết quả thanh toán không hợp lệ

Không cập nhật đã thanh toán khi chữ ký, mã đơn, số tiền hoặc thông tin cần xác thực không hợp lệ.

Không chỉ dựa vào thông báo trên trình duyệt để xác nhận thanh toán.

### Thao tác hoặc thông báo lặp

Không tạo nhiều đơn cho cùng lần xác nhận.

Không ghi nhận tiền, trừ hoặc hoàn tồn nhiều lần do cùng một sự kiện được xử lý lặp.

### Hai khách cùng mua sản phẩm cuối

Xử lý kiểm tra và cập nhật tồn kho nhất quán, không xác nhận vượt số lượng khả dụng.

### Hủy đơn và kết quả thanh toán đến muộn

Xử lý theo chính sách giữ tồn, thanh toán và hủy đơn đã thống nhất.

Nếu chính sách chưa được chốt, cần xác nhận trước khi triển khai; không tự cập nhật trạng thái gây sai lệch đơn, tiền hoặc tồn.

## 6. Sơ đồ nghiệp vụ

Nhóm đã xây dựng hai sơ đồ BPMN trong NV6:

1. Quy trình tạo bộ và mua hàng.
2. Quy trình mua lẻ.

Các sơ đồ chia làn theo khách hàng, hệ thống DAYORA, cổng thanh toán sandbox và quản trị viên.

[Bản sơ đồ nhóm cung cấp](https://drive.google.com/file/d/1ZsrXA9Tg8GIWAY6LCSLZQuAWME2325tv/view?usp=sharing)

Cần kiểm tra quyền truy cập và bổ sung ảnh xuất của hai sơ đồ vào repository để người xem đối chiếu trực tiếp.

## 7. Nội dung cần thống nhất trước khi triển khai

* Thời điểm giữ tồn, thời hạn giữ và thời điểm trừ hoặc hoàn tồn.
* Chính sách hủy đơn, thanh toán lại và kết quả thanh toán đến muộn.
* Các trạng thái đơn và điều kiện chuyển trạng thái.
* Quy tắc voucher, ghi nhận lượt sử dụng và kết hợp ưu đãi.
* Bảng phí giao hàng.
* Cách xử lý bộ đang tạo khi quy tắc Kit Builder thay đổi phiên bản.

Các chính sách sau khi chốt phải được cập nhật đồng thời trong REQUIREMENTS.md, quy trình này và ca kiểm thử liên quan.
