# KẾ HOẠCH THỰC HIỆN DỰ ÁN (PROJECT PLAN)

**Đề tài:** Website đặt dịch vụ chăm sóc người lớn tuổi (Mô hình sàn kết nối trung gian)  
**Kho lưu trữ (Repository):** GitHub

---

## 1. Thành viên và vai trò

| STT | Họ và tên | Vai trò chính | Trách nhiệm trọng tâm |
| :--- | :--- | :--- | :--- |
| 1 | *Nguyễn Huỳnh Anh Thư* | **Project Manager (PM) & Business Analyst (BA)** | Lập kế hoạch, điều phối tiến độ nhóm trên GitHub; khảo sát nghiệp vụ sàn trung gian; viết tài liệu đặc tả yêu cầu (`SRS`), thiết kế sơ đồ luồng nghiệp vụ (`BPMN`), `Use Case` và mô hình dữ liệu (`ERD`). |
| 2 | *Nguyễn Thúy Hiền* | **UI/UX Designer & Frontend Developer** | Thiết kế Wireframe/Prototype (Figma); lập trình toàn bộ giao diện người dùng (Storefront cho Khách hàng, Partner Portal cho Bên thứ 3, Admin Dashboard) đảm bảo tính thẩm mỹ và tương thích đa thiết bị. |
| 3 | *Đoàn Thị Anh Thư* | **Backend Developer & Database Admin** | Thiết kế và triển khai Cơ sở dữ liệu; xây dựng hệ thống API xử lý đăng nhập/phân quyền, tìm kiếm/lọc đa tiêu chí, logic đặt lịch chống trùng giờ, thanh toán giả lập và đối soát hoa hồng. |
| 4 | *Bùi Thanh Ngân* | **QA/Tester & E-commerce Operations** | Viết kịch bản kiểm thử (`Test Case`), thực hiện kiểm thử tích hợp và bảo mật cơ bản; xây dựng bộ quy tắc kiểm duyệt đối tác, chuẩn bị dữ liệu mẫu (Mock Data) và hoàn thiện báo cáo/slide thuyết trình. |

---

## 2. Các giai đoạn

Dự án được triển khai theo mô hình phát triển lặp tăng trưởng trong **8 tuần**, chia thành 6 giai đoạn cụ thể:

* **Giai đoạn 1: Khảo sát và xác định yêu cầu (Tuần 1)**
  * Khảo sát mô hình hoạt động các nền tảng đặt dịch vụ trung gian (OTA/Marketplace).
  * Chốt phạm vi đề tài, danh sách vai trò người dùng, danh sách chức năng (`F01`–`F16`) và hoàn thiện tài liệu đặc tả `REQUIREMENTS.md`.
* **Giai đoạn 2: Thiết kế giao diện & Cơ sở dữ liệu (Tuần 2)**
  * Thiết kế sơ đồ cơ sở dữ liệu quan hệ (`ERD`) và cấu trúc API.
  * Thiết kế Wireframe và giao diện mẫu (UI/UX) cho 3 phân hệ: Khách hàng, Bên thứ 3 và Quản trị viên.
* **Giai đoạn 3: Xây dựng các chức năng Frontend (Tuần 3 – Tuần 4)**
  * Khởi tạo cấu trúc thư mục trên GitHub.
  * Cắt giao diện và xử lý tương tác phía người dùng: trang tìm kiếm, bộ lọc, bảng so sánh gói dịch vụ, luồng đặt lịch và khung giao diện quản lý (Dashboard).
* **Giai đoạn 4: Phát triển Backend và Cơ sở dữ liệu (Tuần 3 – Tuần 5)**
  * Tạo bảng dữ liệu và thiết lập ràng buộc trên hệ quản trị CSDL.
  * Lập trình các API nghiệp vụ lõi: xác thực phân quyền (RBAC), quản lý dịch vụ/nhân viên của Bên thứ 3, kiểm tra trùng khung giờ khi đặt lịch và xử lý trạng thái đơn hàng.
* **Giai đoạn 5: Tích hợp và kiểm thử (Tuần 6 – Tuần 7)**
  * Ghép nối (Integrate) toàn bộ API từ Backend vào giao diện Frontend.
  * Nạp dữ liệu mẫu thực tế (các trung tâm chăm sóc, nhân viên, chứng chỉ, bảng giá).
  * Thực hiện kiểm thử chức năng, kiểm thử luồng đặt lịch đồng thời và sửa lỗi (Fix bugs).
* **Giai đoạn 6: Triển khai và hoàn thiện (Tuần 8)**
  * Đưa hệ thống lên môi trường chạy thử nghiệm (Deploy lên Cloud/Hosting miễn phí từ GitHub).
  * Rà soát toàn bộ mã nguồn, hoàn thiện tài liệu hướng dẫn (`README.md`), báo cáo tổng kết và chuẩn bị kịch bản demo bảo vệ đồ án.

---

## 3. Công việc

| Mã CV | Tên công việc | Giai đoạn | Người phụ trách | Kết quả cần đạt (Deliverables) | Thời hạn | Trạng thái |
| :--- | :--- | :---: | :--- | :--- | :---: | :---: |
| **W01** | Khởi tạo GitHub Repo, thiết lập nhánh (`main`, `dev`) & `PROJECT_PLAN.md` | GĐ 1 | Thành viên 1 | Repository hoạt động ổn định, phân quyền đầy đủ cho 4 thành viên. | Cuối Tuần 1 | Hoàn thành |
| **W02** | Phân tích nghiệp vụ, xác định vai trò & viết tài liệu `REQUIREMENTS.md` | GĐ 1 | Thành viên 1 | Tài liệu đặc tả hoàn chỉnh với 4 vai trò và 16 chức năng kèm tiêu chí nghiệm thu. | Cuối Tuần 1 | Hoàn thành |
| **W03** | Thiết kế mô hình dữ liệu quan hệ (`ERD`) và đặc tả API | GĐ 2 | Thành viên 1 & 3 | Sơ đồ ERD chuẩn hóa và danh sách endpoint API thống nhất giữa FE và BE. | Cuối Tuần 2 | Đang thực hiện |
| **W04** | Thiết kế UI/UX (Wireframe & Prototype) cho 3 phân hệ giao diện | GĐ 2 | Thành viên 2 | File thiết kế Figma hoàn chỉnh cho trang Khách hàng, Partner Portal và Admin. | Cuối Tuần 2 | Đang thực hiện |
| **W05** | Xây dựng giao diện Khách hàng (Tìm kiếm, Bộ lọc, So sánh dịch vụ, Đặt lịch) | GĐ 3 | Thành viên 2 | Giao diện hiển thị chuẩn trên Desktop/Mobile, chạy mượt các thao tác so sánh và chọn lịch. | Cuối Tuần 4 | Chưa bắt đầu |
| **W06** | Xây dựng giao diện Dashboard dùng chung cho Bên thứ 3 và Admin | GĐ 3 | Thành viên 2 | Hoàn thiện các màn hình quản lý gói dịch vụ, nhân viên, duyệt đối tác và thống kê. | Cuối Tuần 4 | Chưa bắt đầu |
| **W07** | Khởi tạo Database và xây dựng API Xác thực, Phân quyền & Quản lý hồ sơ (`F01`, `F02`) | GĐ 4 | Thành viên 3 | File `schema.sql`, API đăng ký/đăng nhập trả về đúng vai trò và bảo mật mật khẩu. | Cuối Tuần 3 | Chưa bắt đầu |
| **W08** | Xây dựng API Tìm kiếm, Lọc đa tiêu chí & Quản lý dịch vụ/nhân viên (`F03`–`F05`, `F10`, `F11`) | GĐ 4 | Thành viên 3 | API truy vấn chính xác dịch vụ theo khu vực, khung giờ trống của nhân viên. | Cuối Tuần 4 | Chưa bắt đầu |
| **W09** | Xây dựng API Đặt lịch chống trùng giờ, Thanh toán giả lập & Duyệt đơn (`F06`–`F09`, `F12`–`F16`) | GĐ 4 | Thành viên 3 | Logic khóa khung giờ hoạt động chính xác, không cho phép 2 khách đặt trùng 1 nhân viên/giờ. | Cuối Tuần 5 | Chưa bắt đầu |
| **W10** | Xây dựng bộ tiêu chuẩn kiểm duyệt đối tác & chuẩn bị dữ liệu mẫu (`mock_data.sql`) | GĐ 5 | Thành viên 4 | Tối thiểu 5 đơn vị cung cấp dịch vụ mẫu, 15 nhân viên chăm sóc và 20 gói dịch vụ đa dạng. | Cuối Tuần 5 | Chưa bắt đầu |
| **W11** | Tích hợp Frontend – Backend & chạy kiểm thử theo `TEST_CASES.md` | GĐ 5 | Thành viên 2, 3, 4 | Toàn bộ 16 chức năng hoạt động thông suốt trên nhánh `dev`; ghi nhận và xử lý 100% lỗi nghiêm trọng. | Cuối Tuần 7 | Chưa bắt đầu |
| **W12** | Deploy hệ thống lên môi trường Cloud, viết `README.md` & Slide thuyết trình | GĐ 6 | Cả nhóm | Link website chạy trực tuyến phục vụ demo; mã nguồn sạch trên nhánh `main`. | Cuối Tuần 8 | Chưa bắt đầu |

---

## 4. Rủi ro

| STT | Rủi ro dự kiến | Mức độ ảnh hưởng | Phương án phòng ngừa và xử lý |
| :--- | :--- | :---: | :--- |
| **R01** | **Lỗi logic đặt trùng lịch (Race Condition):** Hai khách hàng cùng đặt một nhân viên chăm sóc vào cùng một khung giờ tại cùng thời điểm. | **Cao** | Thiết kế ràng buộc duy nhất (Unique Constraint) trên cặp `(caregiver_id, booking_date, time_slot)` trong Database kết hợp giao dịch (Transaction) ở Backend để khóa lịch ngay khi tạo đơn. |
| **R02** | **Xung đột mã nguồn (Merge Conflict) trên GitHub** khi 4 thành viên cùng chỉnh sửa và đẩy code lên kho chung. | **Trung bình** | Phân tách thư mục rõ ràng (`frontend/`, `backend/`, `docs/`); quy định bắt buộc tạo nhánh riêng cho từng tính năng và kiểm tra (Review) qua Pull Request trước khi gộp vào nhánh `dev`. |
| **R03** | **Khối lượng giao diện lớn** do phải làm cho cả Khách hàng, Bên thứ 3 và Admin dẫn đến trễ tiến độ. | **Cao** | Tái sử dụng chung một bộ khung giao diện quản trị (Admin/Partner Dashboard Layout) và dùng chung 1 trang đăng nhập điều hướng tự động theo vai trò để giảm 40% thời gian lập trình UI. |
| **R04** | **Dữ liệu mẫu sơ sài** khiến tính năng tìm kiếm, lọc theo khu vực và so sánh giữa các bên thứ 3 không thể hiện rõ hiệu quả khi demo. | **Trung bình** | Phân công riêng Thành viên 4 chuẩn bị sẵn bộ dữ liệu mẫu đa dạng (nhiều quận/huyện, nhiều mức giá và chứng chỉ khác nhau) ngay từ Tuần 5 để nạp vào hệ thống. |
| **R05** | **Sự cố môi trường khi bảo vệ đồ án** (mất mạng, lỗi cổng thanh toán giả lập hoặc lỗi server miễn phí bị ngủ đông). | **Cao** | Chuẩn bị song song 2 phương án: bản chạy trực tuyến (Deploy Cloud) và bản chạy cục bộ (Localhost) đã cấu hình sẵn dữ liệu trên laptop thuyết trình, kèm video quay lại luồng chạy hoàn chỉnh dự phòng. |
