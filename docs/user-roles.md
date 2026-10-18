# Vai trò người dùng

## 1. Tổng quan

DAYORA có ba nhóm truy cập: khách chưa đăng nhập, khách hàng có tài khoản và quản trị viên.

Khách chưa đăng nhập là trạng thái truy cập công khai. Khách hàng và quản trị viên được xác định thông qua tài khoản và quyền trong hệ thống.

## 2. Khách chưa đăng nhập

### Nhiệm vụ chính

Tìm hiểu sản phẩm và sử dụng Kit Builder để lựa chọn đồ dùng phù hợp trước khi mua.

### Quyền hạn

* Xem trang chủ, danh mục và thông tin sản phẩm.
* Tìm kiếm, lọc và sắp xếp sản phẩm.
* Xem giá, biến thể, thông số và đánh giá được công khai.
* Sử dụng Kit Builder, xem bộ gợi ý, lý do đề xuất và điều chỉnh sản phẩm.
* Đăng ký tài khoản hoặc đăng nhập.

### Giới hạn

Không được truy cập thông tin cá nhân, giỏ hàng, đơn hàng của khách hàng hoặc chức năng quản trị.

Theo phạm vi hiện tại trong REQUIREMENTS.md, khách cần đăng nhập để sử dụng giỏ hàng và đặt hàng. Nếu thay đổi chính sách này, nhóm phải cập nhật các tài liệu và kiểm thử liên quan.

## 3. Khách hàng có tài khoản

### Nhiệm vụ chính

Mua hàng, quản lý thông tin cá nhân và theo dõi đơn hàng của mình.

### Quyền hạn

Được sử dụng các chức năng công khai và:

* Đăng nhập, đăng xuất và cập nhật hồ sơ cá nhân.
* Xem sản phẩm đã xem.
* Thêm sản phẩm mua lẻ hoặc bộ từ Kit Builder vào giỏ.
* Thay đổi số lượng và xóa sản phẩm trong giỏ.
* Sử dụng voucher khi đáp ứng điều kiện.
* Nhập thông tin giao hàng, xem phí và tổng tiền.
* Đặt hàng và thanh toán qua môi trường sandbox.
* Xem lịch sử, chi tiết và trạng thái đơn của mình.
* Đánh giá sản phẩm khi đáp ứng điều kiện sau mua.

### Giới hạn

Chỉ được truy cập và thay đổi dữ liệu thuộc quyền của mình.

Không được xem hoặc sửa hồ sơ, giỏ hàng và đơn của khách hàng khác.

Không được tự sửa giá, tồn kho, mức giảm, trạng thái thanh toán hoặc trạng thái giao hàng.

Không được thực hiện chức năng quản trị.

Checklist và email nhắc chỉ được sử dụng nếu nhóm triển khai FR18 theo điều kiện trong REQUIREMENTS.md.

## 4. Quản trị viên

### Nhiệm vụ chính

Quản lý dữ liệu và hoạt động bán hàng của cửa hàng DAYORA.

### Quyền hạn

* Quản lý sản phẩm, biến thể, danh mục và nhóm hàng.
* Quản lý thông tin tồn kho theo nghiệp vụ.
* Quản lý người dùng và quyền truy cập.
* Xem, xử lý đơn hàng và cập nhật trạng thái hợp lệ.
* Quản lý khuyến mãi, voucher và điều kiện áp dụng.
* Cấu hình, kiểm tra và phát hành phiên bản quy tắc Kit Builder.
* Xem nhật ký thay đổi quy tắc.
* Xem dashboard doanh thu, đơn hàng, sản phẩm bán chạy, chờ giao và số khách hàng.

### Giới hạn

Phải đăng nhập bằng tài khoản có quyền quản trị.

Không được bỏ qua quy tắc chuyển trạng thái đơn hoặc kiểm tra dữ liệu.

Không sửa thông tin đơn đã chốt theo giá hoặc quy tắc mới.

Không tự đánh dấu đã thanh toán khi chưa có căn cứ xác minh hợp lệ.

Không xem được mật khẩu gốc của người dùng vì mật khẩu được lưu dưới dạng băm.

## 5. Nguyên tắc phân quyền

Backend kiểm tra quyền ở mỗi thao tác cần bảo vệ. Việc ẩn nút hoặc menu trên giao diện không thay thế kiểm tra quyền tại máy chủ.

Khách hàng chỉ truy cập dữ liệu thuộc quyền sở hữu của mình, kể cả khi thay đổi mã hồ sơ, giỏ hoặc đơn trên đường dẫn hay yêu cầu gửi lên.

Các chức năng quản trị phải từ chối tài khoản không có quyền, kể cả khi truy cập trực tiếp đường dẫn.

Những trường như giá, mức giảm, quyền, tồn kho và trạng thái thanh toán phải được kiểm tra hoặc xác định tại Backend.

Mọi thay đổi về vai trò và quyền phải được cập nhật đồng thời trong REQUIREMENTS.md, chức năng liên quan và ca kiểm thử.

## 6. Các trường hợp kiểm tra chính

* Khách chưa đăng nhập xem được thông tin công khai nhưng không mở được trang quản trị.
* Khách chưa đăng nhập được yêu cầu đăng nhập khi thực hiện chức năng dành cho tài khoản.
* Khách hàng xem và cập nhật được hồ sơ của mình.
* Khách hàng không xem hoặc sửa được hồ sơ, giỏ và đơn của người khác.
* Khách hàng không thực hiện được thao tác quản trị qua đường dẫn hoặc yêu cầu trực tiếp.
* Quản trị viên thực hiện được các nghiệp vụ thuộc quyền.
* Tài khoản không đủ quyền bị từ chối mà không làm thay đổi dữ liệu.
