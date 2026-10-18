# Requirements

## 1. Mục tiêu dự án

DAYORA là website thương mại điện tử B2C của một cửa hàng kinh doanh đồ dùng picnic và chuyến đi trong ngày.

Dự án hướng đến xây dựng quy trình mua hàng hoàn chỉnh, từ tìm kiếm sản phẩm, lựa chọn đồ dùng, đặt hàng, thanh toán đến theo dõi trạng thái đơn.

Giá trị dự kiến mang lại cho khách hàng:

* Lựa chọn đồ dùng phù hợp với tình huống sử dụng và số người tham gia.
* Hạn chế mua thiếu hoặc mua trùng những vật dụng đã có.
* Theo dõi tổng chi phí gồm tiền hàng, giảm giá và phí giao hàng.
* Mua từng sản phẩm hoặc tạo bộ đồ dùng có thể điều chỉnh thông qua Kit Builder.
* Hiểu lý do và số lượng sản phẩm được đề xuất.

Đối với cửa hàng, hệ thống hỗ trợ quản lý sản phẩm, khách hàng, tồn kho, đơn hàng, khuyến mãi, voucher và quy tắc Kit Builder.

Các lợi ích về tiết kiệm thời gian, giảm mua trùng và khả năng sử dụng cần được đánh giá qua khảo sát và thử nghiệm thực tế.

## 2. Phạm vi

### Trong phạm vi

Website phục vụ một cửa hàng, với danh mục dự kiến khoảng 30 mã sản phẩm thuộc sáu nhóm:

* Thảm picnic.
* Bình nước và ly.
* Hộp đựng thực phẩm.
* Túi giữ nhiệt.
* Vật dụng vệ sinh.
* Phụ kiện tiện ích.

Kit Builder phục vụ nhóm từ 1 đến 8 người theo ba tình huống: picnic ăn nhẹ, hẹn hò buổi chiều và đi biển trong ngày.

Các nhóm chức năng thực hiện:

* Trang chủ, danh mục, tìm kiếm, lọc, sắp xếp và chi tiết sản phẩm.
* Đăng ký, đăng nhập, hồ sơ, lịch sử mua hàng và sản phẩm đã xem.
* Đánh giá sản phẩm sau mua.
* Kit Builder nhận nhu cầu, tính số lượng còn thiếu, giải thích gợi ý và cho phép thay món.
* Giỏ hàng, voucher, checkout, phí giao hàng và tạo đơn.
* Thanh toán thử nghiệm qua VNPay Sandbox.
* Theo dõi và quản lý trạng thái đơn hàng.
* Quản trị sản phẩm, danh mục, nhóm hàng, người dùng, tồn kho, khuyến mãi và voucher.
* Quản trị quy tắc Kit Builder theo phiên bản và lưu nhật ký thay đổi.
* Dashboard thống kê hoạt động cửa hàng.
* Giao diện trên máy tính và điện thoại, kiểm thử, bảo mật và triển khai bản demo.

Các chức năng FR01 đến FR17 thuộc phạm vi phiên bản đầu.

FR18 về checklist và email nhắc là phần nâng cao có điều kiện, chỉ triển khai khi chức năng cốt lõi đạt kiểm thử, nhóm còn nguồn lực và đã xác nhận tiêu chí với giảng viên.

### Ngoài phạm vi

* Sàn thương mại điện tử có nhiều người bán.
* Kinh doanh thực phẩm chế biến.
* Cho thuê đồ dùng, đặt tour, đặt địa điểm hoặc phương tiện.
* Chatbot AI, gợi ý bằng học máy, bản đồ và dữ liệu thời tiết trực tiếp.
* Trải nghiệm 3D/AR và ứng dụng di động riêng.
* Đồng bộ tồn kho với hệ thống bên ngoài.
* Tự động chuyển tiền hoàn trả.
* Cam kết giao hàng trong ngày hoặc bảo đảm hàng đến trước ngày đi.

## 3. Người dùng

### Khách chưa đăng nhập

Được xem trang chủ, danh mục, chi tiết sản phẩm, tìm kiếm, lọc, sắp xếp và sử dụng Kit Builder.

Không được truy cập dữ liệu cá nhân của khách hàng hoặc chức năng quản trị.

Theo phạm vi hiện tại, các thao tác giỏ hàng và đặt hàng được thực hiện bằng tài khoản khách hàng. Nếu bổ sung mua hàng không cần tài khoản, nhóm phải cập nhật yêu cầu và kiểm thử tương ứng.

### Khách hàng có tài khoản

Được sử dụng các chức năng công khai và:

* Quản lý hồ sơ cá nhân.
* Quản lý giỏ hàng, sử dụng voucher và đặt hàng.
* Thanh toán và theo dõi đơn của mình.
* Xem lịch sử mua hàng và sản phẩm đã xem.
* Đánh giá sản phẩm khi đáp ứng điều kiện sau mua.

Chỉ được xem và thay đổi dữ liệu thuộc quyền của mình, không được thực hiện chức năng quản trị.

### Quản trị viên

Được quản lý sản phẩm, danh mục, nhóm hàng, người dùng, đơn hàng, tồn kho, khuyến mãi và voucher.

Được cấu hình, kiểm tra và phát hành phiên bản quy tắc Kit Builder; xem nhật ký thay đổi và dashboard.

Mọi thao tác quản trị phải được kiểm tra quyền tại Backend.

## 4. Yêu cầu chức năng

### FR01. Trang chủ và điều hướng

**Mô tả:** Hiển thị danh mục, sản phẩm nổi bật, sản phẩm bán chạy, ưu đãi và hai lối mua: mua lẻ hoặc tạo bộ bằng Kit Builder.

**Người sử dụng:** Khách chưa đăng nhập, khách hàng.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Liên kết danh mục, sản phẩm và Kit Builder dẫn đến đúng nội dung.
* Sản phẩm hiển thị đúng ảnh, tên và giá.
* Khi có khuyến mãi, hiển thị giá gốc, giá giảm và tỷ lệ giảm tương ứng.
* Các nút điều hướng sử dụng được trên máy tính và điện thoại.

### FR02. Tìm kiếm, lọc và sắp xếp

**Mô tả:** Cho phép tìm theo từ khóa, sắp xếp theo giá tăng hoặc giảm và lọc theo thuộc tính sản phẩm.

**Người sử dụng:** Khách chưa đăng nhập, khách hàng.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Có các tiêu chí lọc: giá, nhóm hàng, tình huống, sức chứa, kích thước và chất liệu.
* Thuộc tính lọc được áp dụng phù hợp từng nhóm hàng.
* Kết quả đáp ứng các điều kiện lọc đang chọn.
* Sắp xếp đúng thứ tự và cho phép xóa điều kiện lọc.
* Có thông báo khi không tìm thấy sản phẩm.

### FR03. Chi tiết sản phẩm

**Mô tả:** Hiển thị thông tin sản phẩm và biến thể để khách hàng quyết định mua.

**Người sử dụng:** Khách chưa đăng nhập, khách hàng.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Có ảnh, tên, mô tả, SKU, giá, tồn kho và thông số có đơn vị.
* Có giá khuyến mãi khi áp dụng và sản phẩm liên quan.
* Giá, SKU và tồn kho cập nhật đúng theo biến thể được chọn.
* Không cho chọn số lượng mua vượt tồn kho tại thời điểm kiểm tra.
* Sức chứa dùng cho Kit Builder được lấy từ dữ liệu đã xác định, không tự suy ra từ kích thước.

### FR04. Tài khoản và hồ sơ

**Mô tả:** Cho phép đăng ký, đăng nhập, đăng xuất, quản lý hồ sơ, xem lịch sử mua và sản phẩm đã xem.

**Người sử dụng:** Khách chưa đăng nhập, khách hàng.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Dữ liệu đăng ký được kiểm tra; thông tin định danh tài khoản không bị trùng.
* Đăng nhập sai được thông báo và không tạo phiên đăng nhập hợp lệ.
* Mật khẩu được lưu dưới dạng băm.
* Khách hàng chỉ được xem, sửa hồ sơ và xem lịch sử của mình.
* Đăng xuất kết thúc phiên truy cập tài khoản.

### FR05. Review và rating sau mua

**Mô tả:** Cho khách hàng đánh giá sản phẩm đã mua khi đủ điều kiện.

**Người sử dụng:** Khách hàng.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Backend kiểm tra sản phẩm thuộc đơn của khách và đơn đã giao thành công trước khi nhận đánh giá.
* Chấp nhận mức điểm từ 1 đến 5 và kiểm tra nội dung đầu vào.
* Không cho khách đánh giá sản phẩm chưa mua hoặc dùng đơn của người khác.
* Hiển thị đúng đánh giá và điểm tổng hợp.
* Quy định số lần đánh giá và chỉnh sửa phải được nhóm chốt trước khi triển khai.

### FR06. Nhập nhu cầu tạo bộ

**Mô tả:** Thu thập thông tin để Kit Builder tính bộ đồ dùng.

**Người sử dụng:** Khách chưa đăng nhập, khách hàng.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Nhận đủ tình huống, số người, ngân sách và thông tin đồ đã có.
* Chỉ nhận tình huống thuộc ba trường hợp trong phạm vi.
* Số người là số nguyên từ 1 đến 8; ngân sách là số dương.
* Số lượng hoặc sức chứa đồ đã có không được âm.
* Đầu vào sai được báo rõ để người dùng sửa.

### FR07. Tạo và giải thích bộ

**Mô tả:** Tính nhu cầu còn thiếu và đề xuất sản phẩm theo quy tắc Kit Builder.

**Người sử dụng:** Khách chưa đăng nhập, khách hàng.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Phân biệt món theo người và món dùng chung.
* Trừ đồ đã có theo đúng công dụng, số lượng và sức chứa.
* Món dùng chung được tính theo sức chứa và làm tròn lên khi cần.
* Chỉ đề xuất sản phẩm còn bán và đủ tồn.
* Hiển thị số lượng, lý do đề xuất và phân biệt món thiết yếu với tùy chọn.
* Không tạo số lượng cần mua âm hoặc buộc mua thêm khi đã có đủ đồ.
* Nếu không tìm được bộ phù hợp, giải thích nguyên nhân thay vì tự tăng ngân sách hoặc bỏ món thiết yếu.

### FR08. Thay món và kiểm soát ngân sách

**Mô tả:** Cho phép điều chỉnh bộ gợi ý và theo dõi chi phí.

**Người sử dụng:** Khách chưa đăng nhập, khách hàng.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Món thay thế phải đáp ứng công dụng, sức chứa và tồn kho cần thiết.
* Tổng tiền được tính theo tiền hàng trừ giảm giá cộng phí giao.
* Khi chưa có địa chỉ, phí giao và tổng liên quan được ghi rõ là tạm tính.
* Thay món hoặc số lượng làm cập nhật tổng và trạng thái phù hợp ngân sách.
* Nếu khách bỏ món thiết yếu, không tiếp tục hiển thị bộ là đầy đủ.
* Không tự động thay đổi ngân sách khách đã nhập.

### FR09. Giỏ hàng

**Mô tả:** Quản lý sản phẩm được thêm từ mua lẻ hoặc Kit Builder.

**Người sử dụng:** Khách hàng.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Thêm đúng sản phẩm, biến thể và số lượng.
* Cho phép đổi số lượng, xóa sản phẩm và cập nhật tiền hàng.
* Hiển thị thông báo khi giỏ trống hoặc số lượng không hợp lệ.
* Có gợi ý sản phẩm bổ sung nhưng không tự thêm vào giỏ.
* Khách chỉ truy cập được giỏ hàng của mình.

### FR10. Checkout và tạo đơn

**Mô tả:** Tiếp nhận thông tin giao hàng, xác nhận chi phí và tạo đơn từ giỏ.

**Người sử dụng:** Khách hàng.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Kiểm tra thông tin người nhận, liên hệ và địa chỉ.
* Backend kiểm tra lại giá, tồn kho, voucher và phí giao.
* Nếu dữ liệu thay đổi, khách được thông báo và xác nhận lại trước khi hoàn tất.
* Không tạo đơn từ giỏ trống hoặc dữ liệu không hợp lệ.
* Lưu chi tiết sản phẩm, số lượng, giá, giảm giá, phí giao, tổng tiền và dữ liệu bộ đã chốt.
* Thao tác gửi lặp không tạo nhiều đơn cho cùng một lần xác nhận.

### FR11. Thanh toán sandbox

**Mô tả:** Tích hợp VNPay Sandbox để thanh toán thử nghiệm và cập nhật kết quả.

**Người sử dụng:** Khách hàng.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Tạo yêu cầu thanh toán gắn đúng đơn và số tiền.
* Tiếp nhận kết quả và xác thực chữ ký, thông tin đơn, số tiền trước khi ghi nhận thanh toán.
* Xử lý được thành công, thất bại, hủy và kết quả không hợp lệ.
* Không chỉ dựa vào trang chuyển hướng trên trình duyệt để xác nhận đã thanh toán.
* Thông báo lặp không ghi nhận tiền hoặc trừ tồn nhiều lần.
* Khóa cấu hình không được công khai trong mã nguồn.

### FR12. Phí và trạng thái giao hàng

**Mô tả:** Tính phí theo bảng quy tắc và quản lý trạng thái giao hàng.

**Người sử dụng:** Khách hàng, quản trị viên.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Phí được xác định theo địa chỉ và quy tắc đã thống nhất.
* Phí giao được tính vào tổng tiền và lưu trong đơn.
* Khách xem được trạng thái giao của đơn mình.
* Chỉ quản trị viên được cập nhật trạng thái.
* Trạng thái giao hàng được quản lý riêng với trạng thái thanh toán.
* Không hiển thị cam kết hàng đến trước ngày đi khi chưa có cơ sở.

### FR13. Ưu đãi và voucher

**Mô tả:** Quản lý chương trình ưu đãi và áp dụng mã giảm giá.

**Người sử dụng:** Quản trị viên, khách hàng.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Quản trị viên cấu hình thời hạn, điều kiện đơn, mức giảm, giới hạn sử dụng và đối tượng nếu có.
* Backend kiểm tra voucher tồn tại, còn hiệu lực và đáp ứng điều kiện.
* Tính đúng mức giảm và mức giảm tối đa.
* Tổng tiền cập nhật khi thêm, bỏ voucher hoặc thay đổi giỏ.
* Voucher không hợp lệ có thông báo nguyên nhân.
* Việc ghi nhận lượt sử dụng nhất quán khi tạo, thanh toán hoặc hủy đơn theo chính sách đã chốt.

### FR14. Quản trị dữ liệu cửa hàng

**Mô tả:** Quản lý sản phẩm, danh mục, nhóm hàng và người dùng.

**Người sử dụng:** Quản trị viên.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Cho phép thêm, xem, sửa và ngừng sử dụng dữ liệu theo quyền.
* Kiểm tra trường bắt buộc, mã trùng và giá trị không hợp lệ.
* Không cho lưu giá hoặc tồn kho âm.
* Thay đổi hoặc ngừng bán sản phẩm không làm mất lịch sử đơn hàng.
* Người không có quyền không thực hiện được thao tác quản trị dù truy cập trực tiếp đường dẫn.

### FR15. Quản lý đơn và tồn kho

**Mô tả:** Xử lý đơn hàng và kiểm soát số lượng hàng khả dụng.

**Người sử dụng:** Quản trị viên.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Xem được danh sách, chi tiết và trạng thái đơn.
* Chỉ chuyển trạng thái theo quy trình được thống nhất.
* Giữ, trừ và hoàn tồn đúng chính sách xử lý đơn.
* Hai đơn cạnh tranh sản phẩm cuối không cùng được xác nhận vượt lượng tồn.
* Hủy đơn hoặc thông báo thanh toán lặp không làm tồn sai.
* Thông tin đơn cũ không đổi khi giá sản phẩm được cập nhật.

### FR16. Quản trị quy tắc Builder

**Mô tả:** Quản lý dữ liệu và phiên bản quy tắc tạo bộ.

**Người sử dụng:** Quản trị viên.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Cấu hình nhu cầu theo tình huống, món thiết yếu, món tùy chọn, công dụng và sức chứa.
* Kiểm tra quy tắc hợp lệ trước khi phát hành.
* Mỗi phiên bản có mã và thông tin người, thời điểm thay đổi.
* Bộ được tạo có thông tin phiên bản quy tắc đã sử dụng.
* Đơn hàng đã chốt không thay đổi khi phát hành phiên bản mới.

### FR17. Dashboard

**Mô tả:** Hiển thị số liệu phục vụ quản lý cửa hàng.

**Người sử dụng:** Quản trị viên.

**Mức độ ưu tiên:** Bắt buộc.

**Tiêu chí nghiệm thu:**
* Có tổng doanh thu, số đơn, sản phẩm bán chạy, đơn hoặc sản phẩm chờ giao và số khách hàng.
* Mỗi chỉ số có định nghĩa, trạng thái đơn được tính và khoảng thời gian rõ ràng.
* Số liệu khớp với bộ dữ liệu kiểm thử có kết quả biết trước.
* Người không có quyền quản trị không truy cập được dashboard.

### FR18. Checklist và email nhắc

**Mô tả:** Tạo danh sách chuẩn bị từ bộ đã mua và đồ đã có; gửi email nhắc theo ngày khách chọn.

**Người sử dụng:** Khách hàng.

**Mức độ ưu tiên:** Nâng cao có điều kiện.

**Tiêu chí nghiệm thu nếu triển khai:**
* Checklist phản ánh đúng dữ liệu bộ và đồ đã có.
* Chỉ gửi nhắc khi khách chủ động đăng ký.
* Cho phép chọn, đổi ngày và hủy nhắc.
* Xử lý lịch nhắc liên quan khi hủy đơn.
* Có nhật ký và cơ chế tránh gửi trùng.
* Không đưa ra cam kết về thời điểm giao hàng dựa trên lịch nhắc.

## 5. Yêu cầu phi chức năng

### Giao diện và trải nghiệm

Các trang chính sử dụng được ở độ rộng 1366 px và 390 px, không che nút, mất thông tin quan trọng hoặc tràn ngang ngoài ý muốn.

Bố cục, màu sắc, chữ và thành phần giao diện nhất quán.

Có ít nhất ba tương tác phục vụ UX: báo lỗi tại đầu vào Kit Builder; cập nhật tổng và cảnh báo khi thay món; hiển thị thay đổi cần xác nhận ở checkout.

### Kiểm tra dữ liệu và bảo mật

Kiểm tra đầu vào ở cả Frontend và Backend.

Backend tự xác định giá, quyền truy cập, tồn kho và mức giảm, không tin các giá trị do trình duyệt gửi lên.

Thực hiện biện pháp phù hợp để hạn chế XSS, SQL injection và CSRF.

Kiểm tra quyền sở hữu dữ liệu để khách không xem hoặc sửa hồ sơ, giỏ và đơn của người khác.

Không công khai mật khẩu, token, khóa thanh toán hoặc cấu hình bí mật trong GitHub và nhật ký.

### Tính nhất quán dữ liệu

Không để tồn kho âm, ghi nhận đơn hoặc thanh toán trùng.

Các thao tác liên quan đơn, thanh toán và tồn kho phải có cơ chế bảo đảm nhất quán.

Thông tin đơn đã chốt không thay đổi theo dữ liệu sản phẩm hoặc quy tắc tương lai.

### Tổ chức mã nguồn

Sử dụng PHP/Laravel theo kiến trúc MVC, Laravel Blade, HTML, CSS, JavaScript, Bootstrap và MySQL.

Mã nguồn được chia theo trách nhiệm, đặt tên rõ ràng và có hướng dẫn cài đặt.

Nghiệp vụ dùng chung giữa khách hàng và quản trị cần được xử lý nhất quán.

### Kiểm thử

Xây dựng tối thiểu 24 ca kiểm thử Kit Builder, gồm tình huống thông thường, dữ liệu sai, ngân sách không đủ, đã có đủ đồ và sản phẩm thiếu tồn.

Kiểm thử luồng mua lẻ, checkout, voucher, thanh toán, quyền truy cập và cạnh tranh tồn kho.

Mỗi ca có đầu vào, kết quả mong đợi, kết quả thực tế và trạng thái; lỗi được ghi nhận và kiểm tra lại sau sửa.

Thử nghiệm với ít nhất 8 người dùng mục tiêu, hướng đến ít nhất 6 người hoàn thành tác vụ không cần hướng dẫn trực tiếp. Đây là mục tiêu đánh giá, chưa phải kết quả đạt được.

### Triển khai và khả năng bảo trì

Bản demo truy cập qua HTTPS, có hướng dẫn chạy và dữ liệu mẫu.

GitHub có lịch sử phát triển, phân công và đóng góp có thể kiểm chứng.

Lưu nguồn, quyền sử dụng tài nguyên và nhật ký sử dụng AI.

## 6. Giới hạn và giả định

### Thời gian và nguồn lực

Nhóm gồm 8 thành viên với vai trò đã thống nhất.

Thời gian thực hiện dự kiến 8 tuần. Ngày bắt đầu, hạn nộp và thời hạn từng đầu việc được xác định trong PROJECT_PLAN.md.

Chức năng nâng cao chỉ triển khai khi không ảnh hưởng việc hoàn thành và kiểm thử phần cốt lõi.

### Công nghệ và môi trường

Hệ thống sử dụng Laravel, Blade, Bootstrap và MySQL; được triển khai trên môi trường tương thích có HTTPS.

VNPay Sandbox chỉ phục vụ thử nghiệm, không đại diện cho việc đã vận hành thanh toán thương mại thực tế.

Phí giao hàng được tính bằng bảng quy tắc trong hệ thống, chưa tích hợp API vận chuyển.

### Dữ liệu và quy tắc

Danh mục khoảng 30 SKU, ba tình huống và giới hạn từ 1 đến 8 người là phạm vi dữ liệu dự kiến.

Sức chứa, định lượng và công dụng sản phẩm phải có căn cứ hoặc được ghi rõ là giả định của dữ liệu demo.

Kit Builder tìm phương án theo quy tắc được xác định trước, không cam kết tìm được phương án tối ưu toàn cục.

Khách tự khai báo đồ đã có; hệ thống không xác minh tình trạng thực tế của các vật dụng này.

Không sử dụng dữ liệu cá nhân thật hoặc tài khoản thanh toán thật khi chưa được phép.

### Nội dung cần thống nhất trước khi triển khai

* Cách đếm SKU và biến thể; bảng định lượng cho từng tình huống.
* Điều kiện, số lần và quyền chỉnh sửa đánh giá sau mua.
* Bảng phí giao hàng, cách làm tròn và chính sách kết hợp ưu đãi.
* Thời điểm giữ tồn, thời hạn thanh toán, hủy đơn và xử lý kết quả thanh toán đến muộn.
* Quy trình chuyển trạng thái đơn hàng.
* Cách xử lý bộ đang tạo khi quy tắc Builder có phiên bản mới.
* Công thức và khoảng thời gian tính các chỉ số dashboard.

Kết quả phản biện AI và quyết định giữ, sửa hoặc bỏ của nhóm phải được cập nhật vào tài liệu trước khi chốt phạm vi triển khai.

Mọi thay đổi lớn sau khi chốt yêu cầu cần ghi nhận lý do, người thống nhất và tác động đến tiến độ, dữ liệu, kiểm thử.
