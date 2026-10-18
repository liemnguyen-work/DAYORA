# DAYORA

## 1. Giới thiệu

DAYORA là dự án website thương mại điện tử theo mô hình B2C của một cửa hàng bán đồ dùng picnic và chuyến đi trong ngày, với thông điệp “Gói gọn đồ dùng, mở trọn cuộc vui”.

Dự án hướng đến giải quyết những khó khăn khi chuẩn bị đồ dùng: lựa chọn thiếu món, mua trùng vật dụng đã có, tính số lượng chưa phù hợp và khó kiểm soát tổng chi phí. Đây là các giả thuyết kinh doanh cần tiếp tục kiểm chứng qua khảo sát và thử nghiệm người dùng.

Khách hàng có thể mua từng sản phẩm hoặc sử dụng Kit Builder để nhận gợi ý bộ đồ dùng theo bốn đầu vào:

* Tình huống sử dụng.
* Số người tham gia.
* Ngân sách.
* Số lượng hoặc sức chứa của đồ dùng đã có.

Kit Builder sử dụng quy tắc nghiệp vụ xác định trước, giải thích lý do và số lượng đề xuất, đồng thời cho phép khách điều chỉnh sản phẩm trước khi đặt hàng.

Phạm vi dữ liệu dự kiến gồm khoảng 30 mã sản phẩm thuộc sáu nhóm: thảm picnic; bình nước và ly; hộp đựng thực phẩm; túi giữ nhiệt; vật dụng vệ sinh; phụ kiện tiện ích.

Ba tình huống sử dụng gồm picnic ăn nhẹ, hẹn hò buổi chiều và đi biển trong ngày, phục vụ nhóm từ 1 đến 8 người.

Dự án tập trung bán đồ dùng, không kinh doanh thực phẩm chế biến, cho thuê đồ hoặc cung cấp dịch vụ đặt tour, địa điểm và phương tiện.

## 2. Khách hàng mục tiêu

* Sinh viên có nhu cầu đi chơi cùng bạn bè và cân nhắc ngân sách.
* Các cặp đôi trẻ chuẩn bị đồ dùng cho picnic hoặc buổi hẹn hò ngoài trời.
* Nhóm bạn và người đi làm trẻ muốn chuẩn bị cho chuyến đi trong ngày.
* Khách hàng đã có một số vật dụng và muốn mua bổ sung những món còn thiếu.

Phân khúc ưu tiên và nhu cầu thực tế sẽ tiếp tục được xác minh qua khảo sát và thử nghiệm.

## 3. Chức năng chính

Các chức năng dưới đây là phạm vi dự kiến, chưa phải chức năng đã triển khai.

### Dành cho khách hàng

* Xem trang chủ, danh mục, sản phẩm nổi bật và ưu đãi.
* Tìm kiếm, sắp xếp và lọc sản phẩm theo giá, nhóm hàng, tình huống, sức chứa, kích thước và chất liệu; áp dụng thuộc tính phù hợp từng nhóm sản phẩm.
* Xem chi tiết, hình ảnh, biến thể, giá, tồn kho, thông số và sản phẩm liên quan.
* Đăng ký, đăng nhập, quản lý hồ sơ, xem sản phẩm đã xem và lịch sử mua hàng.
* Sử dụng Kit Builder để tạo bộ đồ dùng, xem lý do gợi ý và thay món phù hợp.
* Quản lý giỏ hàng, áp dụng voucher, nhập địa chỉ và xem phí giao hàng.
* Đặt hàng và thanh toán qua ít nhất một cổng thanh toán ở môi trường thử nghiệm sandbox.
* Theo dõi trạng thái đơn hàng và đánh giá sản phẩm khi đủ điều kiện sau mua.

### Dành cho quản trị viên

* Quản lý sản phẩm, danh mục, nhóm hàng và tồn kho.
* Quản lý người dùng và phân quyền.
* Quản lý đơn hàng và cập nhật trạng thái xử lý, giao hàng.
* Quản lý khuyến mãi và voucher.
* Quản lý, phát hành phiên bản quy tắc Kit Builder và lưu nhật ký thay đổi.
* Xem dashboard về doanh thu, số đơn, sản phẩm bán chạy, đơn chờ giao và số khách hàng.

### Nguyên tắc nghiệp vụ nổi bật

* Kit Builder tính phần còn thiếu dựa trên đồ đã có và phân biệt món thiết yếu với món tùy chọn.
* Chỉ đề xuất sản phẩm còn bán và đủ tồn kho.
* Tổng thực trả gồm tiền hàng sau giảm giá cộng phí giao hàng. Phí giao được ghi là tạm tính khi chưa có địa chỉ.
* Khi không tìm được bộ phù hợp, hệ thống giải thích nguyên nhân, không tự tăng ngân sách hoặc bỏ món thiết yếu.
* Hệ thống kiểm tra lại giá, tồn kho, voucher và phí giao trước khi xác nhận đơn.
* Đơn hàng giữ thông tin đã chốt, không thay đổi theo giá hoặc quy tắc được cập nhật về sau.

### Chức năng nâng cao có điều kiện

Checklist chuẩn bị chuyến đi và email nhắc chỉ được xem xét sau khi chức năng cốt lõi đạt kiểm thử, nhóm còn nguồn lực và đã xác nhận tiêu chí với giảng viên.

Chi tiết chức năng, mức ưu tiên và điều kiện nghiệm thu được trình bày trong REQUIREMENTS.md.

## 4. Thành viên

* Liêm: Trưởng nhóm kiêm BA.
* Đạt: Product Designer, phụ trách UI/UX.
* Thành: Frontend Developer 1, phụ trách giao diện khách hàng.
* Phúc: Frontend Developer 2, phụ trách giao diện quản trị.
* Hoàn: Backend Developer 1, phụ trách khách hàng và giao dịch.
* Châu: Backend Developer 2, phụ trách quản trị và dữ liệu.
* Ngọc: QA/Tester.
* Kiệt: DevOps Engineer, phụ trách tích hợp và triển khai.

Mỗi thành viên có đầu việc và sản phẩm bàn giao cụ thể, phối hợp với các thành viên liên quan và cập nhật tiến độ qua GitHub Issues.

## 5. Công nghệ dự kiến

Nhóm thống nhất lựa chọn các công nghệ sau để phát triển DAYORA:

### Backend
Sử dụng PHP/Laravel theo kiến trúc MVC để xử lý nghiệp vụ, tài khoản, phân quyền, sản phẩm, Kit Builder, giỏ hàng, đơn hàng và voucher.

### Frontend
Sử dụng HTML, CSS, JavaScript, Bootstrap và Laravel Blade để xây dựng giao diện khách hàng và quản trị, hiển thị dữ liệu từ Backend và đáp ứng trên máy tính, điện thoại.

### Database
Sử dụng MySQL để lưu trữ tài khoản, sản phẩm, tồn kho, đơn hàng, voucher và quy tắc Kit Builder, bảo đảm quan hệ và tính nhất quán dữ liệu.

### API / Services
Sử dụng VNPay Sandbox để tích hợp thanh toán thử nghiệm, tạo giao dịch, tiếp nhận và xác thực kết quả, cập nhật trạng thái và xử lý trường hợp thành công, thất bại hoặc hủy.

### Version Control
Sử dụng Git và GitHub để quản lý phiên bản mã nguồn, lưu lịch sử đóng góp. GitHub Issues được sử dụng để phân công và theo dõi công việc.

### Công cụ và phương án bổ sung
Sử dụng Figma để thiết kế luồng sử dụng và giao diện.

Phí giao hàng được tính bằng bảng quy tắc trong Backend, kết hợp quản lý địa chỉ và trạng thái giao hàng.

Website được triển khai trên hosting hỗ trợ Laravel, MySQL và HTTPS.

Dịch vụ email cho chức năng nhắc chuẩn bị chuyến đi chỉ được bổ sung sau khi các chức năng cốt lõi đạt kiểm thử và nhóm thống nhất triển khai.

## 6. Kế hoạch thực hiện

Thời gian dự kiến là 8 tuần. Ngày bắt đầu, hạn hoàn thành và phân bổ thời gian từng giai đoạn sẽ được nhóm thống nhất trong PROJECT_PLAN.md.

1. Khảo sát và thống nhất yêu cầu: xác định vấn đề kinh doanh, tham khảo FanFan, Đi Outdoor và WeTrek; phân tích, phản biện và chốt phạm vi.
2. Thiết kế: xây dựng luồng sử dụng, giao diện và cơ sở dữ liệu; xác định quy tắc Kit Builder.
3. Xây dựng nền tảng và luồng bán hàng: tài khoản, phân quyền, sản phẩm, giỏ hàng, voucher, đặt hàng, thanh toán và quản trị.
4. Hoàn thiện Kit Builder: tính số lượng, xử lý đồ đã có, thay món, kiểm soát ngân sách và quản lý phiên bản quy tắc.
5. Tích hợp và kiểm thử: kiểm tra hai luồng mua lẻ và mua bằng Kit Builder, các trường hợp lỗi, quyền truy cập và giao diện trên máy tính, điện thoại.
6. Triển khai và bàn giao: đưa bản demo lên môi trường HTTPS, hoàn thiện hướng dẫn chạy, tài liệu và minh chứng kiểm thử.

Các mục tiêu kiểm thử dự kiến gồm tối thiểu 24 trường hợp cho Kit Builder và thử nghiệm với ít nhất 8 người dùng mục tiêu. Đây là mục tiêu đề xuất, chưa phải kết quả đã đạt được.

## 7. Liên kết

- Bảng yêu cầu: REQUIREMENTS.md
- Kế hoạch: PROJECT_PLAN.md
- Phân tích website: docs/competitor-analysis.md
