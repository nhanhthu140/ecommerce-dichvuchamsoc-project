# ecommerce-dichvuchamsoc-project
## 1.Giới thiệu
Đề tài: Website đặt dịch vụ chăm sóc người lớn tuổi 
Ý tưởng: website cho phép người dùng truy cập và xem các dịch vụ chăm sóc người lớn tuổi từ bên thứ 3, có thể so sánh về giá của các bên, xem theo khu vực sinh sống, ngày giờ, nhân viên chăm sóc từ đó lựa chọn bên thứ 3 mong muốn và book lịch 

**Vấn đề kinh doanh cần giải quyết:**
* **Đối với gia đình/khách hàng:** Thị trường dịch vụ chăm sóc người lớn tuổi hiện nay còn phân mảnh, thiếu minh bạch về bảng giá và chất lượng nhân sự. Khách hàng mất nhiều thời gian để liên hệ từng đơn vị rời rạc, khó so sánh quyền lợi và lo ngại về chuyên môn của người chăm sóc.
* **Đối với đơn vị cung cấp dịch vụ (Bên thứ 3):** Các trung tâm/công ty chăm sóc gặp khó khăn trong việc tiếp cận đúng tệp khách hàng theo khu vực và tối ưu hóa lịch làm việc trống của đội ngũ điều dưỡng viên.
* **Giải pháp của hệ thống:** Xây dựng một sàn giao dịch tập trung cho phép khách hàng tìm kiếm theo khu vực, khung giờ, so sánh trực quan giá cả – chứng chỉ nhân viên giữa các bên thứ 3 và đặt lịch trực tuyến an toàn thông qua cơ chế kiểm duyệt và thanh toán trung gian.

## 2. Khách hàng mục tiêu
Hệ thống hướng đến 3 nhóm người dùng chính trong hệ sinh thái dịch vụ:
* **Khách hàng đặt dịch vụ (Người thân / Gia đình có người cao tuổi):** Những người bận rộn (độ tuổi 25–55) sinh sống tại các đô thị, có nhu cầu tìm kiếm điều dưỡng viên, người chăm sóc chuyên nghiệp theo giờ hoặc theo ngày cho cha mẹ, ông bà tại nhà hoặc tại bệnh viện.
* **Nhà cung cấp dịch vụ (Bên thứ 3 / Partner):** Các trung tâm chăm sóc sức khỏe, công ty cung ứng dịch vụ điều dưỡng tại nhà đã được cấp phép hoạt động, muốn mở rộng kênh bán hàng và quản lý lịch điều phối nhân viên hiệu quả.
* **Quản trị viên hệ thống (Admin):** Đội ngũ vận hành sàn, chịu trách nhiệm kiểm duyệt hồ sơ năng lực đối tác, giám sát chất lượng dịch vụ, xử lý khiếu nại và quản lý doanh thu chiết khấu.

## 3. Chức năng chính
Hệ thống được chia thành 3 phân hệ giao diện trên cùng một nền tảng Web với 16 chức năng cốt lõi (`F01`–`F16`):
* **Phân hệ Khách hàng (Storefront):**
  * Đăng ký, đăng nhập và quản lý hồ sơ sức khỏe cơ bản của người lớn tuổi cần chăm sóc.
  * Tìm kiếm và lọc dịch vụ đa tiêu chí (khu vực sinh sống, ngày giờ, loại hình chăm sóc, khoảng giá).
  * So sánh trực quan từ 2–3 gói dịch vụ giữa các bên thứ 3 khác nhau (giá cả, quyền lợi, kinh nghiệm, đánh giá sao).
  * Xem hồ sơ chi tiết nhân viên chăm sóc (kinh nghiệm, chứng chỉ hành nghề, lịch trống).
  * Đặt lịch trực tuyến có kiểm tra chống trùng khung giờ, thanh toán qua cổng giả lập, quản lý/hủy lịch hẹn và đánh giá sau dịch vụ.
* **Phân hệ Nhà cung cấp dịch vụ (Partner Portal):**
  * Đăng ký hồ sơ đối tác lên sàn; tự tạo, cập nhật và quản lý các gói dịch vụ kèm bảng giá.
  * Quản lý danh sách nhân viên chăm sóc trực thuộc và thiết lập khung giờ rảnh/bận.
  * Tiếp nhận, xác nhận hoặc từ chối đơn đặt lịch từ khách hàng và theo dõi doanh thu đối soát.
* **Phân hệ Quản trị viên (Admin Dashboard):**
  * Kiểm duyệt hồ sơ pháp lý của Bên thứ 3 trước khi cho phép hiển thị dịch vụ lên sàn.
  * Quản lý tài khoản người dùng, danh mục khu vực địa lý, giám sát đơn hàng/khiếu nại và thống kê hoa hồng toàn sàn.

## 4. Thành viên
Nhóm thực hiện dự án gồm **4 thành viên**:
* **Thành viên 1** – Project Manager (PM) & Business Analyst (BA)
* **Thành viên 2** – UI/UX Designer & Frontend Developer
* **Thành viên 3** – Backend Developer & Database Admin
* **Thành viên 4** – QA/Tester & E-commerce Operations

## 5. Công nghệ dự kiến
* **Frontend:** HTML5, CSS3, JavaScript (ReactJS / Tailwind CSS)
* **Backend:** Node.js (Express) *(hoặc PHP / Java Spring Boot)*
* **Cơ sở dữ liệu (Database):** MySQL / PostgreSQL
* **Thiết kế UI/UX:** Figma
* **Quản lý mã nguồn & Triển khai:** Git, GitHub, Vercel / Render

## 6. Kế hoạch thực hiện
Dự án được triển khai trong **8 tuần** qua 6 giai đoạn chính:
1. **Giai đoạn 1 – Khảo sát và xác định yêu cầu (Tuần 1):** Phân tích mô hình sàn trung gian, chốt phạm vi và hoàn thiện tài liệu đặc tả.
2. **Giai đoạn 2 – Thiết kế giao diện & Cơ sở dữ liệu (Tuần 2):** Thiết kế sơ đồ ERD, đặc tả API và vẽ Wireframe/Prototype cho 3 phân hệ.
3. **Giai đoạn 3 – Xây dựng các chức năng Frontend (Tuần 3 – Tuần 4):** Lập trình giao diện khách hàng (tìm kiếm, lọc, so sánh, đặt lịch) và khung Dashboard cho Đối tác/Admin.
4. **Giai đoạn 4 – Phát triển Backend và Cơ sở dữ liệu (Tuần 3 – Tuần 5):** Khởi tạo CSDL, xây dựng API xác thực phân quyền, logic đặt lịch chống trùng giờ và thanh toán giả lập.
5. **Giai đoạn 5 – Tích hợp và kiểm thử (Tuần 6 – Tuần 7):** Kết nối Frontend – Backend, nạp dữ liệu mẫu thực tế và chạy kiểm thử toàn diện.
6. **Giai đoạn 6 – Triển khai và hoàn thiện (Tuần 8):** Deploy hệ thống lên môi trường Cloud, hoàn thiện tài liệu và chuẩn bị demo bảo vệ.

## 7. Liên kết
* **Bảng đặc tả yêu cầu:** [REQUIREMENTS.md](./REQUIREMENTS.md)
* **Kế hoạch thực hiện dự án:** [PROJECT_PLAN.md](./PROJECT_PLAN.md)
* **Nguyên tắc AI hỗ trợ dự án:** [AI_INSTRUCTIONS.md](./AI_INSTRUCTIONS.md)
