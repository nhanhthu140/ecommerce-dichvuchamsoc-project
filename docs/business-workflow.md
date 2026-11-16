# NHIỆM VỤ 6 – XÁC ĐỊNH QUY TRÌNH NGHIỆP VỤ (3 QUY TRÌNH)

## 1. Quy trình tìm kiếm và lựa chọn dịch vụ

* **Đối tượng tham gia:** Khách hàng, Hệ thống website.
* **Các bước thực hiện:**
  1. Khách hàng truy cập vào website.
  2. Hệ thống hiển thị danh mục các dịch vụ chăm sóc người lớn tuổi.
  3. Khách hàng nhập tiêu chí tìm kiếm gồm loại hình dịch vụ, khu vực và thời gian mong muốn sử dụng.
  4. Hệ thống tìm kiếm và hiển thị danh sách dịch vụ phù hợp.
  5. Khách hàng xem thông tin chi tiết về dịch vụ, giá cả và đơn vị cung cấp.
  6. Khách hàng so sánh và lựa chọn dịch vụ phù hợp với nhu cầu.
  7. Khách hàng chuyển sang quy trình đặt lịch dịch vụ.
* **Trường hợp phát sinh:**
  * Nếu không tìm thấy dịch vụ phù hợp, hệ thống thông báo và đề nghị khách hàng thay đổi tiêu chí tìm kiếm.

### Sơ đồ quy trình tìm kiếm và lựa chọn dịch vụ

```mermaid
flowchart TD
    subgraph KH [Khách hàng]
        Start((Bắt đầu)) --> B1[Truy cập website]
        B3[Nhập tiêu chí tìm kiếm]
        B5[Xem chi tiết, giá cả & đơn vị cung cấp]
        B6[So sánh & lựa chọn dịch vụ phù hợp]
        End(((Kết thúc)))
    end

    subgraph HT [Hệ thống website]
        B2[Hiển thị danh mục dịch vụ]
        B4[Tìm kiếm dịch vụ theo tiêu chí]
        D1{Có dịch vụ phù hợp?}
        Err1[Thông báo & yêu cầu đổi tiêu chí]
        B4_Ok[Hiển thị danh sách dịch vụ phù hợp]
    end

    B1 --> B2
    B2 --> B3
    B3 --> B4
    B4 --> D1
    D1 -- Không --> Err1
    Err1 --> B3
    D1 -- Có --> B4_Ok
    B4_Ok --> B5
    B5 --> B6
    B6 --> End
```

---

## 2. Quy trình đặt lịch dịch vụ

* **Đối tượng tham gia:** Khách hàng, Hệ thống website.
* **Các bước thực hiện:**
  1. Khách hàng lựa chọn dịch vụ muốn sử dụng và bắt đầu đặt lịch.
  2. Hệ thống kiểm tra trạng thái đăng nhập của khách hàng.
  3. Nếu khách hàng đã đăng nhập, hệ thống hiển thị biểu mẫu đặt lịch.
  4. Khách hàng nhập thông tin người cần chăm sóc, thông tin liên hệ, địa chỉ, thời gian, thời lượng sử dụng dịch vụ, nhân viên mong muốn (nếu có) và các lưu ý liên quan.
  5. Hệ thống kiểm tra tính hợp lệ của thông tin đặt lịch.
  6. Hệ thống tính toán và hiển thị chi phí dự kiến để khách hàng kiểm tra.
  7. Khách hàng xác nhận gửi yêu cầu đặt lịch.
  8. Hệ thống lưu thông tin, tạo mã đặt lịch và cập nhật trạng thái `"Chờ xác nhận"`.
* **Trường hợp phát sinh:**
  * Nếu khách hàng chưa đăng nhập, hệ thống yêu cầu đăng nhập hoặc đăng ký tài khoản trước khi tiếp tục.
  * Nếu thông tin chưa đầy đủ hoặc không hợp lệ, hệ thống thông báo để khách hàng bổ sung hoặc chỉnh sửa.
  * Nếu dịch vụ không còn hoạt động, hệ thống thông báo để khách hàng lựa chọn dịch vụ khác.

### Sơ đồ quy trình đặt lịch dịch vụ

```mermaid
flowchart TD
    subgraph KH [Khách hàng]
        Start((Bắt đầu)) --> B1[Chọn dịch vụ & nhấn đặt lịch]
        Auth[Đăng nhập / Đăng ký]
        B4[Nhập thông tin đặt lịch]
        Fix[Bổ sung/chỉnh sửa thông tin]
        Other[Chọn dịch vụ khác]
        B7[Kiểm tra và xác nhận yêu cầu đặt lịch]
    end

    subgraph HT [Hệ thống website]
        B2[Kiểm tra đăng nhập]
        D1{Đã đăng nhập?}
        B3[Hiển thị biểu mẫu]
        B5[Kiểm tra thông tin]
        D2{Thông tin hợp lệ?}
        ErrInfo[Thông báo thông tin thiếu hoặc không hợp lệ]
        D3{Dịch vụ còn hoạt động?}
        ErrInactive[Thông báo dịch vụ không còn hoạt động]
        B6[Tính và hiển thị chi phí dự kiến]
        B8_1[Lưu thông tin và tạo mã đặt lịch]
        B8_2["Cập nhật trạng thái 'Chờ xác nhận'"]
        End(((Kết thúc)))
    end

    B1 --> B2
    B2 --> D1
    D1 -- Chưa --> Auth
    Auth --> B3
    D1 -- Rồi --> B3
    B3 --> B4
    B4 --> B5
    B5 --> D2
    D2 -- Không --> ErrInfo
    ErrInfo --> Fix
    Fix --> B4
    D2 -- Có --> D3
    D3 -- Không --> ErrInactive
    ErrInactive --> Other
    Other --> B1
    D3 -- Có --> B6
    B6 --> B7
    B7 --> B8_1
    B8_1 --> B8_2
    B8_2 --> End
```

---

## 3. Quy trình theo dõi và đánh giá dịch vụ

* **Đối tượng tham gia:** Khách hàng, Quản trị viên, Hệ thống website.
* **Các bước thực hiện:**
  1. Khách hàng đăng nhập vào website và truy cập mục lịch sử đặt lịch.
  2. Hệ thống hiển thị danh sách các dịch vụ đã đặt kèm trạng thái hiện tại.
  3. Khách hàng chọn một lịch đặt cụ thể để xem thông tin và tiến độ thực hiện.
  4. Quản trị viên tiếp nhận thông tin về tình trạng thực hiện dịch vụ do đơn vị cung cấp gửi đến, sau đó cập nhật trạng thái tương ứng trên website.
  5. Hệ thống ghi nhận trạng thái `"Đã hoàn thành"` và gửi thông báo mời đánh giá đến khách hàng.
  6. Khách hàng chọn mức độ hài lòng (số sao) và nhập nhận xét về chất lượng dịch vụ.
  7. Hệ thống kiểm tra, lưu thông tin đánh giá và hiển thị trên trang chi tiết dịch vụ.
* **Trường hợp phát sinh:**
  * Nếu dịch vụ chưa hoàn thành, hệ thống chỉ hiển thị thông tin theo dõi và chưa mở chức năng đánh giá.
  * Nếu khách hàng chưa muốn đánh giá ngay, hệ thống vẫn lưu lịch sử để khách hàng có thể đánh giá sau.
  * Nếu nội dung đánh giá thiếu thông tin bắt buộc, hệ thống thông báo để khách hàng bổ sung trước khi gửi.

### Sơ đồ quy trình theo dõi và đánh giá dịch vụ

```mermaid
flowchart TD
    subgraph KH [Khách hàng]
        Start((Bắt đầu)) --> B1[Đăng nhập và truy cập lịch sử đặt lịch]
        B3[Chọn lịch đặt cần theo dõi]
        D2{Khách hàng đánh giá ngay?}
        B6[Chọn số sao và nhập nhận xét]
        FixReview[Bổ sung / chỉnh sửa đánh giá]
    end

    subgraph QTV [Quản trị viên]
        B4_1[Tiếp nhận thông tin cập nhật tình trạng dịch vụ do đơn vị cung cấp gửi đến]
        B4_2[Cập nhật trạng thái dịch vụ trên website]
    end

    subgraph HT [Hệ thống website]
        B2[Hiển thị danh sách dịch vụ đã đặt và trạng thái]
        B3_HT[Hiển thị thông tin chi tiết và tiến độ dịch vụ]
        Note[/"Ghi chú: Đơn vị cung cấp chủ động gửi thông tin tiến độ dịch vụ cho Quản trị viên"/]
        D1{Dịch vụ đã hoàn thành?}
        Wait[Hiển thị trạng thái hiện tại, tiếp tục theo dõi và chờ cập nhật mới]
        B5["Ghi nhận 'Đã hoàn thành' và gửi thông báo mời đánh giá"]
        SaveLater[Lưu lịch sử đặt dịch vụ để khách hàng đánh giá sau]
        B7_1[Kiểm tra nội dung đánh giá]
        D3{Đánh giá đầy đủ và hợp lệ?}
        ErrReview[Thông báo yêu cầu bổ sung thông tin]
        B7_2[Lưu đánh giá và hiển thị trên trang chi tiết dịch vụ]
        End(((Kết thúc)))
    end

    Start --> B1
    B1 --> B2
    B2 --> B3
    B3 --> B3_HT
    B3_HT --> B4_1
    Note -.-> B4_1
    B4_1 --> B4_2
    B4_2 --> D1
    D1 -- Chưa --> Wait
    Wait --> B4_1
    D1 -- Rồi --> B5
    B5 --> D2
    D2 -- Không --> SaveLater
    SaveLater --> End
    D2 -- Có --> B6
    B6 --> B7_1
    B7_1 --> D3
    D3 -- Không --> ErrReview
    ErrReview --> FixReview
    FixReview --> B6
    D3 -- Có --> B7_2
    B7_2 --> End
```v_6_quy_tr_nh_nghi_p_v.md…]()

