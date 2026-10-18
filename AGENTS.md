# Project Instructions for AI

## 1. Project context

Đây là dự án website thương mại điện tử DAYORA của nhóm 8 sinh viên môn Phát triển ứng dụng thương mại điện tử.

DAYORA hoạt động theo mô hình B2C của một cửa hàng bán đồ dùng picnic và chuyến đi trong ngày.

Khách hàng có thể mua từng sản phẩm hoặc sử dụng Kit Builder để nhận gợi ý bộ đồ dùng theo tình huống, số người, ngân sách và đồ dùng đã có.

Công nghệ nhóm lựa chọn:

* Backend: PHP/Laravel theo kiến trúc MVC.
* Frontend: HTML, CSS, JavaScript, Bootstrap và Laravel Blade.
* Database: MySQL.
* Thanh toán thử nghiệm: VNPay Sandbox.
* Quản lý mã nguồn và công việc: Git, GitHub và GitHub Issues.

AI hỗ trợ phân tích, giải thích, viết mã, sửa lỗi, kiểm thử và tài liệu. Thành viên phụ trách phải kiểm tra đầu ra, hiểu cách hoạt động và giải thích được phần đã sử dụng.

## 2. Scope

Chỉ triển khai các chức năng đã được nhóm thống nhất trong REQUIREMENTS.md.

Đọc PROJECT_PLAN.md và GitHub Issue liên quan để xác định người phụ trách, đầu ra và điều kiện hoàn thành.

Không tự bổ sung chức năng hoặc coi đề xuất của AI là yêu cầu đã được nhóm chấp thuận.

Kit Builder sử dụng các quy tắc nghiệp vụ xác định trước. Không tự bổ sung chatbot hoặc gợi ý bằng học máy.

Giữ các nguyên tắc nghiệp vụ sau:

* Tính nhu cầu còn thiếu dựa trên công dụng, số lượng và sức chứa của đồ đã có.
* Phân biệt món thiết yếu với món tùy chọn.
* Chỉ gợi ý sản phẩm còn bán và đủ tồn.
* Không tự tăng ngân sách hoặc bỏ món thiết yếu để tạo bộ có vẻ phù hợp.
* Tổng thực trả gồm tiền hàng trừ giảm giá cộng phí giao hàng.
* Khi chưa có địa chỉ, phí giao và tổng liên quan phải được ghi rõ là tạm tính.
* Kiểm tra lại giá, tồn kho, voucher và phí giao tại Backend trước khi hoàn tất đơn.
* Không để thay đổi giá hoặc quy tắc mới làm thay đổi thông tin đơn đã chốt.

Checklist và email nhắc chỉ triển khai khi nhóm xác nhận đủ điều kiện.

Nếu phát hiện yêu cầu mâu thuẫn hoặc thiếu chính sách nghiệp vụ, báo lại để nhóm thống nhất trước khi triển khai phần liên quan.

## 3. Coding principles

Giữ mã nguồn dễ đọc, dễ giải thích và dễ bảo trì, phù hợp với năng lực của nhóm.

Tuân theo cấu trúc, cách đặt tên và quy ước đang được sử dụng trong dự án.

Tổ chức đúng trách nhiệm giữa giao diện, xử lý yêu cầu, nghiệp vụ và truy cập dữ liệu. Tránh lặp logic dùng chung giữa phía khách hàng và quản trị.

Không thay đổi kiến trúc lớn, công nghệ, cấu trúc dữ liệu quan trọng hoặc thêm dịch vụ bên ngoài khi chưa được nhóm đồng ý.

Không tự xóa chức năng đang hoạt động hoặc sửa các phần không liên quan đến nhiệm vụ.

Ưu tiên thay đổi nhỏ, có thể kiểm tra và đối chiếu với yêu cầu.

Khi thay đổi cơ sở dữ liệu, sử dụng migration phù hợp; nêu tác động đến dữ liệu và cách khôi phục khi cần. Không tự xóa dữ liệu đang có.

Không tự thêm thư viện khi chức năng sẵn có đã đáp ứng. Nếu cần thêm, giải thích mục đích, nguồn, quyền sử dụng và ảnh hưởng đến dự án.

Với nghiệp vụ quan trọng như Kit Builder, voucher, thanh toán và tồn kho, bổ sung hoặc cập nhật kiểm thử phù hợp.

Không coi mã do AI tạo ra là đúng khi chưa được kiểm tra.

## 4. Workflow

### Trước khi sửa mã nguồn

1. Đọc AGENTS.md, REQUIREMENTS.md, PROJECT_PLAN.md, GitHub Issue và các tệp liên quan.
2. Phân tích cách hệ thống hiện tại xử lý chức năng, dữ liệu và quyền truy cập.
3. Đề xuất phương án; nêu các tệp dự kiến sửa, tác động và cách kiểm tra.
4. Chờ nhóm xác nhận phương án trước khi sửa. Nếu yêu cầu giao việc đã xác nhận rõ phương án và phạm vi, thực hiện trong phạm vi đó; xin xác nhận lại khi phát sinh thay đổi ngoài phạm vi.

### Khi thực hiện

1. Chỉ sửa phần liên quan đến nhiệm vụ đã được xác nhận.
2. Giữ nguyên công việc của thành viên khác, không tự ghi đè hoặc hoàn tác thay đổi không liên quan.
3. Kiểm tra từng phần và xử lý lỗi phát sinh thuộc phạm vi thay đổi.
4. Báo lại nếu gặp trở ngại cần nhóm quyết định.

### Sau khi sửa mã nguồn

1. Giải thích đã thay đổi gì và lý do.
2. Liệt kê các tệp đã sửa.
3. Hướng dẫn cách chạy và kiểm thử.
4. Nêu các kiểm tra đã thực hiện, kết quả và phần chưa kiểm tra được.
5. Báo giới hạn, lỗi còn tồn và ảnh hưởng đến các phần khác nếu có.
6. Cập nhật tài liệu, Issue và nhật ký sử dụng AI khi liên quan.

Không ghi công việc là hoàn thành hoặc kiểm thử thành công khi chưa có kết quả xác minh.

## 5. Security

Không đưa mật khẩu, API key, token, khóa thanh toán hoặc cấu hình bí mật vào mã nguồn, tài liệu hay GitHub.

Sử dụng biến môi trường cho thông tin bí mật. Tệp cấu hình mẫu chỉ chứa giá trị minh họa.

Không tự vô hiệu hóa kiểm tra bảo mật để làm chức năng chạy được.

Kiểm tra dữ liệu ở Backend, không tin giá, mức giảm, quyền hoặc trạng thái thanh toán do trình duyệt gửi lên.

Kiểm tra đăng nhập, quyền quản trị và quyền sở hữu dữ liệu. Không để khách xem hoặc sửa hồ sơ, giỏ hàng và đơn của người khác.

Sử dụng các cơ chế phù hợp để hạn chế XSS, SQL injection và CSRF. Mật khẩu phải được băm bằng cơ chế của framework.

Với VNPay Sandbox, kiểm tra chữ ký, thông tin đơn, số tiền và tính hợp lệ của kết quả trước khi cập nhật thanh toán.

Xử lý thao tác lặp và thông báo thanh toán lặp để tránh tạo đơn, ghi nhận tiền hoặc trừ tồn nhiều lần.

Không sử dụng dữ liệu cá nhân thật hoặc tài khoản thanh toán thật khi chưa được phép. Dữ liệu demo phải được ghi rõ là dữ liệu mẫu.

Không ghi thông tin bí mật hoặc dữ liệu cá nhân nhạy cảm vào nhật ký, ảnh minh chứng hoặc câu lệnh gửi cho AI.

Nếu phát hiện lộ khóa hoặc lỗ hổng, báo ngay cho nhóm và đề xuất cách xử lý; không công khai thông tin bí mật trong báo cáo lỗi.

## 6. Communication

Trao đổi bằng tiếng Việt rõ ràng, giải thích thuật ngữ khi cần.

Nếu yêu cầu chưa rõ, hỏi lại trước khi triển khai phần phụ thuộc vào thông tin đó.

Phân biệt thông tin đã được nhóm xác nhận, giả định và đề xuất mới.

Khi đề xuất giải pháp, giải thích mục đích, tác động và cách kiểm tra; ưu tiên phương án phù hợp phạm vi và nguồn lực của nhóm.

Không tự quyết định thay nhóm về chính sách nghiệp vụ chưa được thống nhất.

Không bịa kết quả khảo sát, kiểm thử, triển khai hoặc mức đóng góp của thành viên.

Mọi nội dung do AI hỗ trợ phải được thành viên phụ trách kiểm tra trước khi tích hợp và ghi nhận trung thực trong AI_USAGE_LOG.md.

Nhóm cập nhật AGENTS.md khi có thay đổi về công nghệ, cấu trúc hoặc quy trình làm việc đã được thống nhất.
