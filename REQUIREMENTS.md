# TÀI LIỆU ĐẶC TẢ YÊU CẦU HỆ THỐNG (REQUIREMENTS)
**Đề tài:** Website đặt dịch vụ chăm sóc người lớn tuổi (Mô hình sàn kết nối trung gian)

---

## 1. Mục tiêu dự án

### Mục tiêu kinh doanh
* **Xây dựng nền tảng trung gian tập trung:** Kết nối trực tiếp các gia đình có nhu cầu chăm sóc người cao tuổi với các đơn vị cung cấp dịch vụ uy tín (trung tâm điều dưỡng, công ty chăm sóc tại nhà/bệnh viện) trên một hệ thống duy nhất.
* **Tạo nguồn thu bền vững:** Vận hành theo mô hình thu phí chiết khấu hoa hồng (10% – 15%) trên mỗi giao dịch đặt lịch thành công thông qua sàn, kết hợp gói hiển thị ưu tiên cho đối tác.
* **Chuẩn hóa thị trường dịch vụ chăm sóc:** Thiết lập quy trình kiểm duyệt hồ sơ năng lực, chứng chỉ hành nghề của nhân viên chăm sóc và cơ chế đánh giá minh bạch nhằm nâng cao uy tín nền tảng.

### Giá trị mang lại cho khách hàng
* **Tiết kiệm thời gian tìm kiếm:** Thay vì phải liên hệ từng trung tâm rời rạc, khách hàng dễ dàng tra cứu dịch vụ khả dụng theo đúng khu vực sinh sống và khung giờ mong muốn.
* **Minh bạch thông tin & chi phí:** Cho phép so sánh trực quan về mức giá, quyền lợi gói dịch vụ, kinh nghiệm và đánh giá thực tế của nhân viên chăm sóc giữa các bên thứ 3.
* **An tâm đặt lịch:** Quy trình đặt lịch rõ ràng, tránh tình trạng trùng lịch, bảo vệ quyền lợi thanh toán và có cơ chế xử lý khiếu nại qua bên trung gian.

---

## 2. Phạm vi

### Trong phạm vi (In-Scope)
Hệ thống tập trung triển khai các chức năng cốt lõi phục vụ luồng nghiệp vụ đặt dịch vụ trung gian trên nền tảng Web:
* Đăng ký, đăng nhập và phân quyền theo 4 nhóm người dùng (Khách chưa đăng nhập, Khách hàng, Nhà cung cấp dịch vụ, Quản trị viên).
* Quản lý hồ sơ cá nhân và thông tin người cao tuổi cần chăm sóc.
* Tìm kiếm, lọc dịch vụ đa tiêu chí (khu vực, ngày giờ, mức giá, loại hình) và công cụ so sánh trực tiếp 2–3 gói dịch vụ.
* Xem hồ sơ chi tiết nhân viên chăm sóc (kinh nghiệm, chứng chỉ, lịch trống, đánh giá).
* Đặt lịch trực tuyến có kiểm tra chống trùng khung giờ và thanh toán qua cổng giả lập (Sandbox/QR).
* Cổng dành cho Nhà cung cấp (Bên thứ 3): Quản lý gói dịch vụ, quản lý nhân viên chăm sóc, thiết lập lịch rảnh/bận và xác nhận/từ chối đơn đặt lịch.
* Trang Quản trị (Admin): Kiểm duyệt hồ sơ đối tác, quản lý tài khoản, giám sát đơn hàng/khiếu nại và thống kê doanh thu hoa hồng cơ bản.

### Ngoài phạm vi (Out-of-Scope)
Nhằm đảm bảo tiến độ và chất lượng trong khuôn khổ đồ án nhóm 4 thành viên, hệ thống **chưa triển khai** các tính năng sau:
* Ứng dụng di động độc lập (Native App trên iOS/Android).
* Hệ thống định vị GPS theo dõi vị trí thời gian thực (Real-time tracking) của nhân viên chăm sóc khi di chuyển đến nhà khách hàng.
* Tính năng gọi video/nhắn tin trực tiếp (Live Chat/Video Call) tích hợp sẵn trên website giữa khách hàng và nhân viên.
* Tích hợp cổng thanh toán ngân hàng thật và xuất hóa đơn điện tử tự động kết nối cơ quan thuế.
* Hệ thống gợi ý nhân viên chăm sóc tự động bằng trí tuệ nhân tạo (AI Recommendation).

---

## 3. Người dùng

| Vai trò | Mô tả nhiệm vụ chính | Quyền hạn dự kiến |
| :--- | :--- | :--- |
| **Khách hàng chưa đăng nhập** *(Guest)* | Truy cập website để tham khảo thông tin dịch vụ, lọc và so sánh các bên cung cấp dịch vụ trước khi tạo tài khoản. | • Xem danh sách gói dịch vụ, thông tin bên thứ 3 và hồ sơ nhân viên.<br>• Sử dụng bộ lọc tìm kiếm, công cụ so sánh dịch vụ và xem đánh giá.<br>• Đăng ký tài khoản mới hoặc đăng nhập.<br>• *Hạn chế:* Không thể đặt lịch và không xem được thông tin liên hệ trực tiếp của nhân viên. |
| **Khách hàng** *(Customer)* | Tìm kiếm, chọn đơn vị phù hợp, đặt lịch chăm sóc cho người thân, thanh toán và đánh giá sau khi sử dụng dịch vụ. | • Toàn bộ quyền của Khách hàng chưa đăng nhập.<br>• Cập nhật thông tin cá nhân và hồ sơ sức khỏe cơ bản của người cần chăm sóc.<br>• Thực hiện đặt lịch, thanh toán trực tuyến và hủy lịch theo quy định.<br>• Gửi đánh giá (rating) và tạo yêu cầu khiếu nại sau dịch vụ. |
| **Nhà cung cấp dịch vụ** *(Bên thứ 3 / Partner)* | Đăng tải các gói dịch vụ, quản lý đội ngũ nhân viên trực thuộc và tiếp nhận/xử lý đơn đặt lịch từ khách hàng qua sàn. | • Đăng ký tài khoản đối tác (chờ Admin phê duyệt).<br>• Thêm, sửa, ẩn/hiện các gói dịch vụ và bảng giá của đơn vị.<br>• Quản lý hồ sơ nhân viên chăm sóc, khu vực phục vụ và khung giờ làm việc.<br>• Xác nhận hoặc từ chối đơn đặt lịch; xem báo cáo doanh thu đối soát. |
| **Quản trị viên** *(Admin)* | Vận hành, giám sát hệ thống; kiểm duyệt đối tác để đảm bảo chất lượng sàn; quản lý người dùng và doanh thu. | • Quản lý tài khoản (khóa/mở khóa tài khoản Khách hàng và Bên thứ 3).<br>• Kiểm duyệt hồ sơ đăng ký gian hàng và chứng chỉ nhân viên của Bên thứ 3.<br>• Quản lý danh mục dịch vụ chung và khu vực địa lý.<br>• Giám sát toàn bộ đơn đặt lịch, xử lý tranh chấp/hoàn tiền và xem báo cáo hoa hồng. |

---

## 4. Yêu cầu chức năng

| Mã | Tên chức năng | Mô tả | Người sử dụng | Ưu tiên | Tiêu chí nghiệm thu (Acceptance Criteria) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **F01** | Đăng ký & Đăng nhập | Cho phép người dùng tạo tài khoản mới (chọn vai trò Khách hàng hoặc Đối tác) và đăng nhập vào hệ thống. | Khách hàng, Bên thứ 3, Admin | **Cao** | • Email không được trùng lặp; mật khẩu tối thiểu 8 ký tự.<br>• Đăng nhập thành công điều hướng đúng giao diện theo vai trò.<br>• Tài khoản Đối tác mới đăng ký ở trạng thái "Chờ duyệt" và chưa thể đăng dịch vụ. |
| **F02** | Quản lý hồ sơ cá nhân & Người được chăm sóc | Khách hàng cập nhật thông tin liên hệ và lưu hồ sơ người cao tuổi (tuổi, tình trạng vận động, bệnh nền). | Khách hàng | **Cao** | • Lưu trữ và chỉnh sửa được ít nhất 1 hồ sơ người cần chăm sóc.<br>• Dữ liệu hồ sơ tự động điền vào biểu mẫu khi khách hàng tiến hành đặt lịch. |
| **F03** | Tìm kiếm & Lọc dịch vụ | Tìm kiếm gói dịch vụ chăm sóc theo khu vực (Quận/Huyện), ngày giờ cần đặt, loại hình và khoảng giá. | Khách chưa ĐN, Khách hàng | **Cao** | • Kết quả trả về khớp 100% với khu vực và khung giờ còn trống của nhân viên.<br>• Thời gian phản hồi kết quả lọc dưới 2 giây. |
| **F04** | Xem chi tiết dịch vụ & Hồ sơ nhân viên | Hiển thị đầy đủ mô tả gói dịch vụ, bảng giá, thông tin bên thứ 3 và hồ sơ nhân viên chăm sóc. | Khách chưa ĐN, Khách hàng | **Cao** | • Hiển thị rõ: tên nhân viên, số năm kinh nghiệm, ảnh chứng chỉ hành nghề, điểm đánh giá trung bình và các khung giờ trống. |
| **F05** | So sánh dịch vụ giữa các bên thứ 3 | Cho phép chọn từ 2 đến 3 gói dịch vụ khác nhau để đối chiếu trực quan các tiêu chí trên cùng một màn hình. | Khách chưa ĐN, Khách hàng | **Cao** | • Bảng so sánh hiển thị song song các cột: Tên đơn vị, Đơn giá/giờ, Quyền lợi đi kèm, Kinh nghiệm nhân viên, Điểm đánh giá.<br>• Cho phép bấm "Đặt ngay" trực tiếp từ cột dịch vụ được chọn. |
| **F06** | Đặt lịch dịch vụ (Booking) | Khách hàng chọn gói dịch vụ, nhân viên chăm sóc, ngày giờ cụ thể và gửi yêu cầu đặt lịch. | Khách hàng | **Cao** | • Hệ thống kiểm tra và khóa khung giờ ngay khi tạo đơn, ngăn chặn 2 khách hàng đặt trùng 1 nhân viên trong cùng khung giờ.<br>• Hiển thị rõ tổng chi phí trước khi xác nhận. |
| **F07** | Thanh toán trung gian | Thanh toán phí đặt lịch thông qua cổng thanh toán giả lập (VNPay/MoMo Sandbox hoặc mã QR). | Khách hàng | **Cao** | • Khi thanh toán thành công, trạng thái đơn chuyển sang "Chờ đối tác xác nhận" và lưu lịch sử giao dịch.<br>• Nếu thanh toán thất bại/hết hạn, hệ thống tự động nhả khung giờ đã khóa. |
| **F08** | Quản lý đơn đặt lịch & Hủy lịch | Khách hàng theo dõi trạng thái lịch hẹn và thực hiện hủy lịch khi thay đổi kế hoạch. | Khách hàng | **Cao** | • Hiển thị đầy đủ danh sách đơn theo trạng thái (Chờ xác nhận, Đã xác nhận, Hoàn thành, Đã hủy).<br>• Chỉ cho phép hủy đơn trước thời gian bắt đầu chăm sóc tối thiểu 12 giờ. |
| **F09** | Đánh giá & Nhận xét dịch vụ | Khách hàng chấm điểm (1–5 sao) và viết nhận xét sau khi sử dụng xong dịch vụ. | Khách hàng | **Trung bình** | • Nút "Đánh giá" chỉ hiển thị với các đơn có trạng thái "Hoàn thành".<br>• Điểm trung bình của nhân viên và bên thứ 3 tự động cập nhật sau khi gửi đánh giá. |
| **F10** | Quản lý gói dịch vụ & Bảng giá | Bên thứ 3 tạo mới, cập nhật hoặc tạm ẩn các gói dịch vụ chăm sóc của đơn vị mình. | Bên thứ 3 | **Cao** | • Thực hiện đầy đủ thao tác Thêm/Sửa/Ẩn gói dịch vụ.<br>• Gói dịch vụ bị ẩn sẽ không hiển thị trên trang tìm kiếm của khách hàng nhưng không ảnh hưởng các đơn đã đặt trước đó. |
| **F11** | Quản lý nhân viên & Lịch làm việc | Bên thứ 3 quản lý danh sách nhân viên chăm sóc và thiết lập khung giờ rảnh/bận cho từng người. | Bên thứ 3 | **Cao** | • Thêm/sửa thông tin nhân viên kèm tệp ảnh chứng chỉ.<br>• Cập nhật được lịch làm việc theo ngày/ca; khung giờ đánh dấu "Bận" sẽ không cho phép khách đặt. |
| **F12** | Tiếp nhận & Xử lý đơn đặt lịch | Bên thứ 3 xem đơn hàng mới từ sàn, bấm xác nhận hoặc từ chối lịch và cập nhật hoàn thành. | Bên thứ 3 | **Cao** | • Khi bấm "Từ chối", bắt buộc nhập lý do và hệ thống tự động giải phóng khung giờ.<br>• Khi hoàn thành ca chăm sóc, bên thứ 3 xác nhận "Hoàn thành" để mở quyền đánh giá cho khách. |
| **F13** | Kiểm duyệt đối tác & Dịch vụ | Admin xem xét hồ sơ đăng ký của Bên thứ 3 và phê duyệt hoạt động trên sàn. | Admin | **Cao** | • Admin xem được giấy phép hoạt động của đối tác.<br>• Chỉ sau khi Admin chuyển trạng thái sang "Đã duyệt", gian hàng và dịch vụ của bên thứ 3 mới hiển thị công khai. |
| **F14** | Quản lý người dùng & Danh mục | Admin quản lý danh sách tài khoản hệ thống và cấu hình danh mục khu vực, loại dịch vụ. | Admin | **Trung bình** | • Tài khoản bị Admin "Khóa" sẽ bị đăng xuất ngay lập tức và không thể đăng nhập lại.<br>• Thêm/sửa được danh sách Quận/Huyện áp dụng dịch vụ. |
| **F15** | Giám sát đơn hàng & Xử lý khiếu nại | Admin theo dõi toàn bộ giao dịch và can thiệp hủy đơn/hoàn tiền khi có tranh chấp. | Admin | **Trung bình** | • Admin xem được chi tiết mọi đơn đặt lịch trên sàn.<br>• Có chức năng chuyển trạng thái đơn sang "Đã hủy - Hoàn tiền" khi giải quyết khiếu nại. |
| **F16** | Thống kê doanh thu & Đối soát hoa hồng | Hiển thị báo cáo số lượng đơn thành công, tổng doanh thu và phần trăm hoa hồng sàn giữ lại. | Admin, Bên thứ 3 | **Thấp** | • Tự động tính toán: `Doanh thu thực nhận đối tác = Tổng tiền đơn hoàn thành × (100% - % Hoa hồng sàn)`.<br>• Lọc được số liệu thống kê theo tháng/quý. |

---

## 5. Yêu cầu phi chức năng

* **Tính tương thích & Đáp ứng (Responsive Design):** Giao diện hiển thị tốt, không vỡ bố cục trên các kích thước màn hình phổ biến (Desktop 1920x1080, Laptop 1366x768, Tablet và điện thoại di động). Thiết kế phông chữ rõ ràng, độ tương phản cao, thao tác đơn giản để phù hợp với cả người dùng trung niên và người cao tuổi.
* **Kiểm tra dữ liệu đầu vào (Data Validation):** Toàn bộ biểu mẫu (đăng ký, nhập thông tin sức khỏe, chọn ngày giờ đặt lịch, tạo gói dịch vụ) phải được kiểm tra tính hợp lệ ở cả phía giao diện (Client-side) và máy chủ (Server-side); ngăn chặn chọn ngày đặt lịch trong quá khứ hoặc nhập ký tự đặc biệt gây lỗi hệ thống.
* **Bảo mật & Phân quyền (Security & Authorization):**
  * Áp dụng cơ chế phân quyền chặt chẽ theo vai trò (RBAC); người dùng không thể truy cập trái phép vào đường dẫn URL quản trị của Admin hoặc cổng quản lý của Bên thứ 3 khác.
  * Mật khẩu người dùng phải được mã hóa một chiều (Hashing) trước khi lưu vào cơ sở dữ liệu.
  * Không công khai thông tin nhạy cảm (số điện thoại cá nhân, địa chỉ nhà riêng của người cao tuổi, giấy tờ định danh/CCCD của nhân viên chăm sóc) ra giao diện công cộng.
* **Hiệu năng (Performance):** Thời gian tải trang chủ và truy vấn kết quả tìm kiếm/so sánh dịch vụ trung bình dưới 3 giây trong điều kiện mạng ổn định.
* **Khả năng bảo trì (Maintainability):** Mã nguồn được tổ chức theo cấu trúc thư mục rõ ràng (tách biệt tầng giao diện, xử lý logic và truy vấn dữ liệu), đặt tên biến/hàm thống nhất và quản lý phiên bản tập trung qua Git/GitHub để thuận tiện cho việc phối hợp nhóm 4 người.

---

## 6. Giới hạn và giả định

### Giới hạn dự án
* **Giới hạn về thời gian:** Dự án được thực hiện trong khuôn khổ thời gian một học kỳ (khoảng 7–10 tuần), do đó tập trung hoàn thiện luồng nghiệp vụ chính (MVP - Minimum Viable Product) thay vì phát triển các tính năng mở rộng phức tạp.
* **Giới hạn về nguồn lực:** Nhóm thực hiện gồm 4 thành viên sinh viên, vừa đảm nhận phân tích nghiệp vụ, thiết kế, lập trình vừa thực hiện kiểm thử và nhập liệu mẫu.
* **Giới hạn về công nghệ & hạ tầng:** Hệ thống triển khai trên môi trường phát triển cục bộ (Localhost) hoặc máy chủ miễn phí/giá rẻ (Cloud Hosting/VPS cấu hình cơ bản); cổng thanh toán sử dụng môi trường thử nghiệm (Sandbox) nên không phát sinh giao dịch tiền thật.

### Giả định
* Các đơn vị cung cấp dịch vụ (Bên thứ 3) khi đăng ký tham gia sàn đều cung cấp thông tin giấy phép hoạt động và chứng chỉ nhân viên trung thực; Admin thực hiện kiểm duyệt thủ công dựa trên hồ sơ tải lên.
* Bên thứ 3 chủ động cập nhật chính xác lịch làm việc (rảnh/bận) của nhân viên chăm sóc trực thuộc lên hệ thống để đảm bảo tính đồng bộ khi khách hàng đặt lịch.
* Người dùng truy cập hệ thống bằng các trình duyệt web (Google Chrome, Microsoft Edge, Safari, Firefox) và có kết nối Internet ổn định.
