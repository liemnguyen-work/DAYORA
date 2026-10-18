# AI Usage Log

## Lần sử dụng 1

### Công cụ

ChatGPT.

### Mục đích

Phân tích yêu cầu dự án DAYORA dựa trên mô tả đề tài, Project Charter và kết quả khảo sát FanFan, Đi Outdoor, WeTrek.

Xác định mục tiêu, phạm vi, người dùng, chức năng, quy trình nghiệp vụ, yêu cầu phi chức năng và rủi ro.

### Prompt

Bản tóm lược từ prompt chuẩn hóa trong tài liệu Working Space:

“Phân tích yêu cầu cho website thương mại điện tử DAYORA của nhóm 8 sinh viên, dựa trên Project Charter và kết quả khảo sát được cung cấp.

DAYORA là website B2C bán đồ dùng cho chuyến đi trong ngày, dự kiến khoảng 30 SKU thuộc sáu nhóm hàng, phục vụ ba tình huống và nhóm từ 1 đến 8 người.

Khách hàng có thể mua lẻ hoặc sử dụng Kit Builder với bốn đầu vào: tình huống, số người, ngân sách và số lượng hoặc sức chứa đồ đã có.

Hãy đề xuất mục tiêu, phạm vi, vai trò người dùng, chức năng, quy trình nghiệp vụ, yêu cầu phi chức năng, thứ tự phát triển, chức năng nâng cao và rủi ro.

Phân biệt chức năng bắt buộc, có điều kiện và nội dung cần kiểm chứng. Không coi giả thuyết kinh doanh hoặc mục tiêu kiểm thử là kết quả đã đạt được.”

### Kết quả đề xuất

AI đề xuất các nhóm người dùng gồm khách chưa đăng nhập, khách hàng có tài khoản và quản trị viên.

Danh sách chức năng gồm FR01 đến FR17 cho phiên bản đầu và FR18 về checklist, email nhắc là phần nâng cao có điều kiện.

Hai quy trình chính gồm mua lẻ và tạo bộ, mua hàng bằng Kit Builder.

AI đề xuất các quy tắc tính số lượng còn thiếu, sức chứa, ngân sách và tổng tiền; yêu cầu kiểm tra dữ liệu, phân quyền, thanh toán và tồn kho.

Các chính sách chưa rõ được đánh dấu để nhóm tiếp tục kiểm tra và thống nhất.

### Phản biện

Bản Working Space được cung cấp chưa có nội dung phản biện tại NV4.

Cần bổ sung kết quả thực tế từ công cụ AI thứ hai. Các điểm do AI phân tích tự đánh dấu chưa thay thế cho bước phản biện này.

### Quyết định của nhóm

Sử dụng kết quả phân tích làm đầu vào soạn tài liệu yêu cầu.

Các quyết định giữ lại, điều chỉnh hoặc loại bỏ sau phản biện cần được nhóm bổ sung trước khi chốt yêu cầu triển khai.

### Người kiểm tra

Chưa có thông tin xác nhận người kiểm tra cuối cùng trong tài liệu được cung cấp. Nhóm bổ sung sau khi hoàn thành bước kiểm tra và thảo luận.

## Lần sử dụng 2

### Công cụ

Codex.

### Mục đích

Hỗ trợ soạn tài liệu Markdown theo mẫu bài tập và hướng dẫn lưu từng tệp trên GitHub cho dự án DAYORA.

### Prompt

Các yêu cầu chính đã sử dụng:

“Viết theo mẫu của thầy, dựa vào thông tin và file mình gửi bạn hãy viết cho phù hợp.”

“Theo yêu cầu bài tập đi bạn, đi từ trên xuống.”

“Trước mắt trình bày theo từng loại công nghệ này thôi, rồi nếu có mở rộng thì ghi ở dưới.”

### Kết quả đề xuất

AI hỗ trợ soạn README.md, REQUIREMENTS.md, PROJECT_PLAN.md và AGENTS.md.

Nội dung dựa trên tài liệu nhóm, quy định đồ án và tám vai trò đã chốt.

AI đề xuất công nghệ Laravel, Blade, Bootstrap, MySQL, VNPay Sandbox và Git/GitHub; kế hoạch triển khai tương đối trong 8 tuần và các đầu việc theo vai trò.

### Phản biện

Liêm yêu cầu điều chỉnh nội dung theo đúng cấu trúc và thứ tự mẫu của giảng viên.

Phần công nghệ được trình bày theo từng lớp, không dùng bảng.

Vai trò người dùng website được phân biệt với vai trò thành viên dự án.

Liên kết trong README chỉ được bổ sung sau khi tạo các tệp tương ứng.

Đây là phản hồi của thành viên, không thay thế bước phản biện bằng công cụ AI thứ hai ở NV4.

### Quyết định của nhóm

Theo trao đổi với Liêm, sử dụng tên DAYORA, danh sách tám vai trò đã chốt và bộ công nghệ đã lựa chọn để trình bày tài liệu.

Giữ cấu trúc theo mẫu giảng viên và hoàn thiện từng tệp theo thứ tự.

Các tệp README.md, REQUIREMENTS.md, PROJECT_PLAN.md và AGENTS.md đã được lưu lên GitHub.

Các chính sách nghiệp vụ còn mở và thời hạn thực tế cần tiếp tục được nhóm xác nhận. Việc lưu tài liệu chưa phải bằng chứng chức năng đã được triển khai hoặc kiểm thử thành công.

### Người kiểm tra

Liêm đối chiếu mẫu, phản hồi chỉnh sửa và kiểm tra việc lưu tài liệu.

Các thành viên phụ trách tiếp tục rà soát nội dung liên quan trước khi triển khai.
