# Project Plan

## 1. Thành viên và vai trò

### Liêm: Trưởng nhóm kiêm BA

Điều phối công việc, theo dõi tiến độ và quản lý GitHub Issues.

Tổng hợp, làm rõ yêu cầu và ghi nhận quyết định của nhóm. Theo dõi thay đổi phạm vi, đầu ra và các vướng mắc giữa các thành viên.

Phụ trách tổng hợp kế hoạch, kiểm tra tính thống nhất của tài liệu và chuẩn bị nội dung giới thiệu dự án.

### Đạt: Product Designer, phụ trách UI/UX

Thiết kế luồng sử dụng, giao diện khách hàng và quản trị trên máy tính, điện thoại.

Xây dựng bộ thành phần giao diện, chuẩn bị tài nguyên có nguồn và bàn giao thiết kế cho Frontend.

Hỗ trợ triển khai, kiểm tra giao diện thực tế và điều chỉnh theo kết quả thử nghiệm.

### Thành: Frontend Developer 1, phụ trách khách hàng

Xây dựng giao diện trang chủ, danh mục, tìm kiếm, lọc, chi tiết sản phẩm, tài khoản, Kit Builder, giỏ hàng, checkout và theo dõi đơn.

Phối hợp với Hoàn để kết nối dữ liệu, xử lý trạng thái tải, lỗi và kết quả giao dịch.

Nhận hỗ trợ về giao diện từ Đạt và Kiệt theo phân công cụ thể khi cần cân bằng khối lượng.

### Phúc: Frontend Developer 2, phụ trách quản trị

Xây dựng giao diện dashboard và các trang quản lý sản phẩm, danh mục, người dùng, đơn hàng, khuyến mãi, voucher và quy tắc Kit Builder.

Phối hợp với Châu để kết nối chức năng; kiểm tra biểu mẫu, bảng dữ liệu và thông báo kết quả.

### Hoàn: Backend Developer 1, phụ trách khách hàng và giao dịch

Xây dựng nghiệp vụ tài khoản, truy xuất sản phẩm, Kit Builder, giỏ hàng, checkout, voucher, phí giao và thanh toán sandbox.

Phối hợp với Châu để thiết kế cơ sở dữ liệu và thống nhất quy tắc xử lý đơn, tồn kho, quyền truy cập.

Bảo đảm khách hàng chỉ được truy cập dữ liệu thuộc quyền của mình.

### Châu: Backend Developer 2, phụ trách quản trị và dữ liệu

Xây dựng nghiệp vụ quản trị sản phẩm, danh mục, người dùng, đơn hàng, tồn kho, khuyến mãi, voucher, quy tắc Kit Builder và dashboard.

Điều phối thay đổi cấu trúc cơ sở dữ liệu sau khi thống nhất với Hoàn.

Phối hợp kiểm tra tính nhất quán giữa nghiệp vụ khách hàng và quản trị.

### Ngọc: QA/Tester

Lập kế hoạch và ca kiểm thử dựa trên REQUIREMENTS.md.

Kiểm tra chức năng, giao diện, phân quyền, dữ liệu biên và các trường hợp lỗi; ghi nhận lỗi và kiểm tra lại sau sửa.

Tổ chức thử nghiệm người dùng cùng nhóm, tổng hợp kết quả và lưu minh chứng.

### Kiệt: DevOps Engineer, phụ trách tích hợp và triển khai

Thiết lập môi trường dùng chung, cấu hình mẫu và quy trình tích hợp.

Phối hợp ghép Frontend, Backend, cơ sở dữ liệu và dịch vụ thanh toán; triển khai bản demo qua HTTPS.

Chuẩn bị hướng dẫn cài đặt, cập nhật, sao lưu và khôi phục; hỗ trợ đầu việc kỹ thuật cụ thể khi nhóm cần.

Mỗi công việc có một người chịu trách nhiệm chính. Người phối hợp và phần hỗ trợ cụ thể được ghi trong GitHub Issues. Mỗi thành viên phải hiểu, giải thích và kiểm tra được phần mình phụ trách.

## 2. Các giai đoạn

Kế hoạch dự kiến gồm 8 tuần. Tuần 1 được tính từ ngày nhóm bắt đầu triển khai chính thức. Liêm cập nhật ngày bắt đầu và hạn hoàn thành thực tế sau khi nhóm thống nhất.

### Giai đoạn 1: Khảo sát và xác định yêu cầu

Thời gian: Tuần 1.

Tổng hợp kết quả NV1 đến NV6, bổ sung phản biện còn thiếu và thống nhất phạm vi, vai trò người dùng, chức năng, quy trình và các chính sách nghiệp vụ.

Kết quả: Bộ yêu cầu làm căn cứ phát triển, phân công và danh sách công việc trên GitHub.

### Giai đoạn 2: Thiết kế giao diện

Thời gian: Tuần 1 đến tuần 2.

Thiết kế luồng mua lẻ, tạo bộ, checkout và quản trị; xây dựng giao diện máy tính, điện thoại và bộ thành phần dùng chung.

Kết quả: Thiết kế đủ rõ để Frontend triển khai, có các trạng thái thông thường và lỗi quan trọng.

### Giai đoạn 3: Xây dựng các chức năng Frontend

Thời gian: Tuần 3 đến tuần 6.

Phát triển giao diện khách hàng và quản trị theo từng nhóm chức năng; kết nối Backend ngay khi phần tương ứng sẵn sàng.

Kết quả: Các màn hình và luồng tương tác chạy được trên máy tính, điện thoại.

### Giai đoạn 4: Phát triển Backend và cơ sở dữ liệu

Thời gian: Tuần 2 đến tuần 6.

Thiết kế cơ sở dữ liệu, dữ liệu mẫu, phân quyền và các nghiệp vụ bán hàng, quản trị, thanh toán, tồn kho và Kit Builder.

Kết quả: Backend và cơ sở dữ liệu hoạt động; các quy tắc nghiệp vụ có kiểm tra và kiểm thử.

Giai đoạn 3 và 4 thực hiện song song. Hai nhóm thống nhất cấu trúc dữ liệu và cách kết nối trước khi triển khai từng chức năng.

### Giai đoạn 5: Tích hợp và kiểm thử

Thời gian: Kiểm thử từng phần từ tuần 2; kiểm thử toàn hệ thống tập trung trong tuần 6 đến tuần 7.

Tích hợp các phần theo từng luồng, kiểm tra yêu cầu, sửa lỗi và thử nghiệm với người dùng.

Kết quả: Biên bản kiểm thử, danh sách lỗi, kết quả sửa lỗi và minh chứng cho các yêu cầu chính.

### Giai đoạn 6: Triển khai và hoàn thiện

Thời gian: Chuẩn bị môi trường từ tuần 1; hoàn thiện bản bàn giao trong tuần 8.

Triển khai bản demo, kiểm tra thanh toán trên môi trường triển khai, hoàn thiện tài liệu và tập dượt bảo vệ.

Kết quả: Website HTTPS, hướng dẫn chạy, dữ liệu demo, tài liệu và minh chứng có thể truy cập.

## 3. Công việc

Trạng thái sử dụng: Dự kiến, Đang thực hiện, Chờ kiểm tra, Hoàn thành, Đang vướng mắc.

Trạng thái ban đầu dưới đây là kế hoạch triển khai. Chỉ chuyển sang Hoàn thành sau khi đầu ra được kiểm tra. Khi đưa lên GitHub Issues, bổ sung người phối hợp và điều kiện nghiệm thu cụ thể.

### CV01. Tổng hợp và chốt yêu cầu

**Người phụ trách:** Liêm.

**Kết quả cần đạt:** Tổng hợp kết quả NV1 đến NV6; bổ sung kết quả phản biện; ghi quyết định của nhóm và cập nhật REQUIREMENTS.md. Chốt các chính sách còn mở trước khi triển khai chức năng liên quan.

**Thời hạn:** Cuối tuần 1.

**Trạng thái:** Dự kiến.

### CV02. Hoàn thiện kho tài liệu và phân công

**Người phụ trách:** Liêm.

**Kết quả cần đạt:** Hoàn thiện các tệp theo yêu cầu bài tập; tổ chức GitHub Issues có người phụ trách, đầu ra và điều kiện hoàn thành; cập nhật kế hoạch hằng tuần.

**Thời hạn:** Bộ khung trong tuần 1; cập nhật xuyên suốt dự án.

**Trạng thái:** Dự kiến.

### CV03. Thiết kế UI/UX

**Người phụ trách:** Đạt.

**Kết quả cần đạt:** Luồng sử dụng, thiết kế các màn hình khách hàng và quản trị, phiên bản máy tính và điện thoại, bộ thành phần và tài nguyên có nguồn.

**Thời hạn:** Cuối tuần 2; điều chỉnh theo kết quả kiểm thử.

**Trạng thái:** Dự kiến.

### CV04. Thiết lập môi trường và bản triển khai thử

**Người phụ trách:** Kiệt.

**Kết quả cần đạt:** Dự án Laravel chạy được trên môi trường dùng chung; kết nối MySQL; có cấu hình mẫu không chứa thông tin bí mật, hướng dẫn chạy và bản triển khai thử.

**Thời hạn:** Tuần 1 đến tuần 2.

**Trạng thái:** Dự kiến.

### CV05. Thiết kế cơ sở dữ liệu và dữ liệu mẫu

**Người phụ trách:** Châu.

**Kết quả cần đạt:** Cùng Hoàn thống nhất sơ đồ dữ liệu, ràng buộc và cách thay đổi cấu trúc; tạo dữ liệu mẫu khoảng 30 SKU, ba tình huống và dữ liệu phục vụ kiểm thử.

**Thời hạn:** Bản đầu cuối tuần 2; cập nhật có kiểm soát.

**Trạng thái:** Dự kiến.

### CV06. Xây dựng nền tảng tài khoản và phân quyền

**Người phụ trách:** Hoàn.

**Kết quả cần đạt:** Đăng ký, đăng nhập, đăng xuất, hồ sơ và cơ chế kiểm tra quyền dùng chung. Phối hợp Châu kiểm tra quyền quản trị và quyền sở hữu dữ liệu.

**Thời hạn:** Cuối tuần 3.

**Trạng thái:** Dự kiến.

### CV07. Xây dựng giao diện khách hàng

**Người phụ trách:** Thành.

**Kết quả cần đạt:** Các màn hình mua lẻ, tài khoản, Kit Builder, giỏ, checkout và theo dõi đơn kết nối Backend, hiển thị đúng trên máy tính và điện thoại.

**Thời hạn:** Bàn giao từng phần từ tuần 3; hoàn thiện cuối tuần 6.

**Trạng thái:** Dự kiến.

### CV08. Xây dựng giao diện quản trị

**Người phụ trách:** Phúc.

**Kết quả cần đạt:** Dashboard và các màn hình quản lý dữ liệu, đơn hàng, ưu đãi và quy tắc Kit Builder; biểu mẫu, tìm kiếm, lọc và thông báo hoạt động đúng.

**Thời hạn:** Bàn giao từng phần từ tuần 3; hoàn thiện cuối tuần 6.

**Trạng thái:** Dự kiến.

### CV09. Phát triển Backend mua hàng và thanh toán

**Người phụ trách:** Hoàn.

**Kết quả cần đạt:** Truy xuất sản phẩm, giỏ, voucher, phí giao, checkout, thanh toán VNPay Sandbox và theo dõi đơn. Kiểm tra lại dữ liệu trên máy chủ và xử lý kết quả thanh toán không hợp lệ hoặc lặp.

**Thời hạn:** Kết nối thử sandbox trong tuần 2; hoàn thiện luồng giao dịch cuối tuần 5.

**Trạng thái:** Dự kiến.

### CV10. Phát triển Backend quản trị

**Người phụ trách:** Châu.

**Kết quả cần đạt:** Quản lý sản phẩm, danh mục, người dùng, khuyến mãi, voucher, đơn và tồn kho; dashboard có công thức thống nhất và đối chiếu được bằng dữ liệu mẫu.

**Thời hạn:** Bàn giao từng phần từ tuần 3; hoàn thiện cuối tuần 6.

**Trạng thái:** Dự kiến.

### CV11. Phát triển logic Kit Builder

**Người phụ trách:** Hoàn.

**Kết quả cần đạt:** Nhận bốn đầu vào; tính phần còn thiếu, sức chứa và số lượng; đề xuất hàng đủ tồn; giải thích, thay món và kiểm soát ngân sách. Có xử lý khi không tìm được bộ phù hợp.

**Thời hạn:** Bản thử quy tắc trong tuần 3; hoàn thiện cuối tuần 6.

**Trạng thái:** Dự kiến.

### CV12. Quản trị quy tắc Kit Builder

**Người phụ trách:** Châu.

**Kết quả cần đạt:** Cấu hình, kiểm tra và phát hành phiên bản quy tắc; lưu nhật ký thay đổi; phối hợp Hoàn bảo đảm đơn đã chốt không thay đổi theo quy tắc mới.

**Thời hạn:** Cuối tuần 6.

**Trạng thái:** Dự kiến.

### CV13. Chuẩn bị kiểm thử và kiểm tra từng phần

**Người phụ trách:** Ngọc.

**Kết quả cần đạt:** Bộ ca kiểm thử liên kết với yêu cầu; tối thiểu 24 ca Kit Builder; các ca trọng yếu về giao dịch, phân quyền, dữ liệu biên và tồn kho. Có danh sách lỗi và kết quả kiểm tra lại.

**Thời hạn:** Bản đầu trong tuần 2; cập nhật đến tuần 8.

**Trạng thái:** Dự kiến.

### CV14. Tích hợp hệ thống

**Người phụ trách:** Kiệt.

**Kết quả cần đạt:** Phối hợp các bạn phát triển ghép và chạy được hai luồng mua lẻ, mua bằng Kit Builder; kiểm tra cấu hình, kết nối thanh toán và xử lý lỗi tích hợp.

**Thời hạn:** Tích hợp từng phần từ tuần 3; bản đầy đủ cuối tuần 6.

**Trạng thái:** Dự kiến.

### CV15. Kiểm thử toàn hệ thống và thử người dùng

**Người phụ trách:** Ngọc.

**Kết quả cần đạt:** Kiểm tra toàn bộ luồng chính, giao diện và quyền truy cập; tổ chức thử với ít nhất 8 người dùng mục tiêu, ghi nhận kết quả thực tế và lỗi còn tồn.

**Thời hạn:** Cuối tuần 7.

**Trạng thái:** Dự kiến.

### CV16. Triển khai bản bàn giao

**Người phụ trách:** Kiệt.

**Kết quả cần đạt:** Website HTTPS, dữ liệu và tài khoản demo; hướng dẫn cài đặt, cập nhật, sao lưu và khôi phục. Kiểm tra các đường dẫn và thanh toán sandbox trên môi trường triển khai.

**Thời hạn:** Tuần 8.

**Trạng thái:** Dự kiến.

### CV17. Hoàn thiện tài liệu và chuẩn bị bảo vệ

**Người phụ trách:** Liêm.

**Kết quả cần đạt:** Tổng hợp tài liệu, mức đóng góp, nhật ký AI, nguồn tài nguyên và minh chứng. Mỗi thành viên cung cấp phần mình phụ trách, giải thích luồng xử lý và thực hành sửa đổi, kiểm thử.

**Thời hạn:** Cuối tuần 8, trước hạn nộp chính thức.

**Trạng thái:** Dự kiến.

FR18 về checklist và email nhắc chưa được đưa vào lịch bắt buộc. Nếu triển khai, nhóm tạo công việc riêng, đánh giá nguồn lực và cập nhật kế hoạch trước khi thực hiện.

## 4. Rủi ro

### Khối lượng công việc vượt thời gian hoặc phân bổ không đều

**Phương án xử lý:** Liêm kiểm tra tiến độ hằng tuần, chia công việc lớn thành Issues nhỏ và cân lại đầu việc. Đạt và Kiệt hỗ trợ triển khai phần cụ thể khi cần. Hoãn phần nâng cao nếu chức năng cốt lõi còn lỗi.

### Yêu cầu chưa rõ hoặc thay đổi sau khi phát triển

**Phương án xử lý:** Chốt chính sách nghiệp vụ trước chức năng liên quan; ghi quyết định trong REQUIREMENTS.md. Thay đổi lớn phải có lý do và đánh giá tác động đến tiến độ, dữ liệu, kiểm thử.

### Frontend và Backend không thống nhất cách kết nối

**Phương án xử lý:** Thống nhất cấu trúc dữ liệu, đường dẫn xử lý, thông báo lỗi và cách kiểm tra quyền trước khi triển khai. Tích hợp từng phần từ sớm.

### Quy tắc Kit Builder tính sai hoặc chưa sát nhu cầu

**Phương án xử lý:** Chuẩn hóa công dụng, định lượng, đơn vị và sức chứa; ghi rõ căn cứ hoặc giả định. Kiểm thử trường hợp biên và điều chỉnh theo thử nghiệm người dùng.

### Sai giá, tồn kho, voucher hoặc thanh toán

**Phương án xử lý:** Kiểm tra lại dữ liệu tại Backend; xử lý nhất quán giữa đơn, tiền và tồn; kiểm thử cạnh tranh sản phẩm cuối, thao tác lặp và kết quả thanh toán không hợp lệ.

### Sandbox hoặc hosting không hoạt động

**Phương án xử lý:** Thử tích hợp và triển khai từ đầu dự án; kiểm tra HTTPS, cấu hình và callback. Ghi nhận trở ngại và thống nhất phương án thay thế nếu cần thay đổi dịch vụ.

### Lộ thông tin bí mật hoặc thiếu kiểm tra quyền

**Phương án xử lý:** Không đưa cấu hình bí mật lên GitHub; dùng dữ liệu demo, kiểm tra quyền tại Backend và kiểm thử truy cập trái phép. Nếu lộ khóa, thu hồi và thay khóa.

### Xung đột mã nguồn hoặc mất dữ liệu

**Phương án xử lý:** Cập nhật mã trước khi làm việc, chia thay đổi nhỏ và có người kiểm tra trước khi ghép. Sao lưu cơ sở dữ liệu trước thay đổi quan trọng và kiểm tra khả năng khôi phục.

### Tài liệu, minh chứng hoặc đóng góp không đầy đủ

**Phương án xử lý:** Mỗi thành viên cập nhật Issues, commit và minh chứng theo từng đầu việc. Liêm kiểm tra định kỳ; không dồn ghi nhận vào cuối kỳ.

### Sử dụng tài nguyên hoặc đầu ra AI chưa được kiểm tra

**Phương án xử lý:** Lưu nguồn và quyền sử dụng tài nguyên; ghi nhật ký AI. Thành viên phụ trách phải đọc, kiểm tra, chỉnh sửa và giải thích được nội dung trước khi tích hợp.
