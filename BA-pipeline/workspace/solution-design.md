# Thiết Kế Giải Pháp Tổng Thể (Solution Design)

## 1. Kiến Trúc Giải Pháp
Hệ thống CSDL Hợp tác quốc tế Bộ Tư pháp được xây dựng theo kiến trúc 3-Tier Web Application:
- **Frontend Layer**: Web Admin & Web Portal (HTML5, Tailwind/CSS, React/Vue) tương thích Responsive trên Desktop, Tablet, Mobile browser.
- **Backend Service Layer**: RESTful Microservices/Monolith Modular (Java Spring Boot / Node.js), đáp ứng chuẩn OpenAPI 3.0.3, tích hợp OAuth2/JWT & SSO VNeID.
- **Data & Integration Layer**: CSDL Oracle/PostgreSQL (23 bảng chính), kết nối LGSP và Kho dữ liệu dùng chung Bộ Tư pháp.

## 2. Ánh Xạ Giải Pháp Tới 89 Yêu Cầu Chức Năng (Solution Ref)
### FR-UC-01: Quản lý vai trò
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý vai trò theo phân quyền actor Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-02: Quản lý phân quyền
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý phân quyền theo phân quyền actor Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-03: Quản lý người dùng
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý người dùng theo phân quyền actor Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-04: Quản lý đơn vị
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý đơn vị theo phân quyền actor Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-05: Quản lý cấu hình thông báo
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý cấu hình thông báo theo phân quyền actor Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-06: Quản lý lịch sử tác động
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý lịch sử tác động theo phân quyền actor Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-07: Quản lý lịch sử lỗi phát sinh
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý lịch sử lỗi phát sinh theo phân quyền actor Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-08: Quản lý chính sách lưu trữ nhật ký tác động hệ thống
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý chính sách lưu trữ nhật ký tác động hệ thống theo phân quyền actor Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-09: Lưu log hệ thống
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Lưu log hệ thống theo phân quyền actor Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-10: Gửi thông tin log tác động/log lỗi phát sinh
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Gửi thông tin log tác động/log lỗi phát sinh theo phân quyền actor Nền tảng kết nối chia sẻ của Bộ Tư pháp (LGSP).
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-11: Thiết lập chính sách sao lưu dự phòng
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Thiết lập chính sách sao lưu dự phòng theo phân quyền actor Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-12: Đăng xuất
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Đăng xuất theo phân quyền actor Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-13: Xem thông tin cá nhân
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Xem thông tin cá nhân theo phân quyền actor Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-14: Xem tài liệu hướng dẫn sử dụng
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Xem tài liệu hướng dẫn sử dụng theo phân quyền actor Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-15: Xem biểu đồ thống kê điều ước quốc tế, thỏa thuận quốc tế
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Xem biểu đồ thống kê điều ước quốc tế, thỏa thuận quốc tế theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-16: Xem biểu đồ thống kê chương trình dự án
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Xem biểu đồ thống kê chương trình dự án theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-17: Thống kê danh sách hội thảo
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Thống kê danh sách hội thảo theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, CONFERENCE.

### FR-UC-18: Xem thông báo
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Xem thông báo theo phân quyền actor Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-19: Quản lý điều ước quốc tế
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý điều ước quốc tế theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-20: Quản lý thỏa thuận quốc tế
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý thỏa thuận quốc tế theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-21: Quản lý thỏa thuận khác
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý thỏa thuận khác theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-22: Triển khai điều ước quốc tế, thỏa thuận quốc tế, thỏa thuận khác
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Triển khai điều ước quốc tế, thỏa thuận quốc tế, thỏa thuận khác theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-23: Quản lý chương trình dự án
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý chương trình dự án theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-24: Quản lý kế hoạch hàng năm
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý kế hoạch hàng năm theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-25: Cập nhật kết quả triển khai kế hoạch hàng năm
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Cập nhật kết quả triển khai kế hoạch hàng năm theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-26: Quản lý chuyên gia trong nước
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý chuyên gia trong nước theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, EXPERT.

### FR-UC-27: Quản lý chuyên gia quốc tế
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý chuyên gia quốc tế theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, EXPERT.

### FR-UC-28: Quản lý chuyên gia Việt Nam ở nước ngoài
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý chuyên gia Việt Nam ở nước ngoài theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, EXPERT.

### FR-UC-29: Quản lý đoàn ra do Bộ Tư Pháp chủ trì
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý đoàn ra do Bộ Tư Pháp chủ trì theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, DELEGATION.

### FR-UC-30: Quản lý đoàn ra tháp tùng
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý đoàn ra tháp tùng theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, DELEGATION.

### FR-UC-31: Quản lý đoàn ra khác
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý đoàn ra khác theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, DELEGATION.

### FR-UC-32: Cập nhật kết quả đoàn ra
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Cập nhật kết quả đoàn ra theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, DELEGATION.

### FR-UC-33: Quản lý đoàn vào
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý đoàn vào theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, DELEGATION.

### FR-UC-34: Cập nhật kết quả đoàn vào
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Cập nhật kết quả đoàn vào theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, DELEGATION.

### FR-UC-35: Quản lý hội nghị, hội thảo
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý hội nghị, hội thảo theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, CONFERENCE.

### FR-UC-36: Quản lý đề án hợp tác quốc tế về pháp luật
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý đề án hợp tác quốc tế về pháp luật theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-37: Quản lý hoạt động khác
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý hoạt động khác theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-38: Quản lý Báo cáo kinh nghiệm quốc tế (ngoài chương trình dự án)
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý Báo cáo kinh nghiệm quốc tế (ngoài chương trình dự án) theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-39: Quản lý khen thưởng phía Việt Nam trao
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý khen thưởng phía Việt Nam trao theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, EMULATION_COMMENDATION.

### FR-UC-40: Quản lý khen thưởng phía Việt Nam nhận
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý khen thưởng phía Việt Nam nhận theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, EMULATION_COMMENDATION.

### FR-UC-41: Quản lý báo cáo thường niên, giai đoạn
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý báo cáo thường niên, giai đoạn theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-42: Quản lý báo cáo chuyên đề, đặc thù
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý báo cáo chuyên đề, đặc thù theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-43: Quản lý văn bản quy phạm pháp luật
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý văn bản quy phạm pháp luật theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-44: Quản lý văn bản khác
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý văn bản khác theo phân quyền actor Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-45: Quản lý chia sẻ dữ liệu
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý chia sẻ dữ liệu theo phân quyền actor Chuyên viên nhập liệu/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-46: Quản lý dữ liệu đồng bộ
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý dữ liệu đồng bộ theo phân quyền actor Chuyên viên nhập liệu/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-47: Phân loại dữ liệu
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Phân loại dữ liệu theo phân quyền actor Chuyên viên nhập liệu/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-48: Quản lý danh mục đối tác nước ngoài
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý danh mục đối tác nước ngoài theo phân quyền actor Chuyên viên nhập liệu/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-49: Quản lý danh mục quốc gia
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý danh mục quốc gia theo phân quyền actor Chuyên viên nhập liệu/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-50: Quản lý danh mục cơ quan tổ chức trong nước
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý danh mục cơ quan tổ chức trong nước theo phân quyền actor Chuyên viên nhập liệu/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-51: Quản lý danh mục lĩnh vực hợp tác
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý danh mục lĩnh vực hợp tác theo phân quyền actor Chuyên viên nhập liệu/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-52: Quản lý danh mục hình thức hợp tác
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý danh mục hình thức hợp tác theo phân quyền actor Chuyên viên nhập liệu/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-53: Quản lý danh mục loại nguồn vốn
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý danh mục loại nguồn vốn theo phân quyền actor Chuyên viên nhập liệu/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-54: Quản lý danh mục hình thức khen thưởng
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Quản lý danh mục hình thức khen thưởng theo phân quyền actor Chuyên viên nhập liệu/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, EMULATION_COMMENDATION.

### FR-UC-55: Báo cáo về danh mục điều ước quốc tế, thỏa thuận quốc tế
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Báo cáo về danh mục điều ước quốc tế, thỏa thuận quốc tế theo phân quyền actor Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-56: Báo cáo chương trình dự án
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Báo cáo chương trình dự án theo phân quyền actor Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-57: Báo cáo tiến độ chương trình dự án
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Báo cáo tiến độ chương trình dự án theo phân quyền actor Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-58: Báo cáo thông tin đoàn ra
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Báo cáo thông tin đoàn ra theo phân quyền actor Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, DELEGATION.

### FR-UC-59: Báo cáo thông tin đoàn vào
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Báo cáo thông tin đoàn vào theo phân quyền actor Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, DELEGATION.

### FR-UC-60: Báo cáo nhân sự đi nước ngoài và chủ trì/tham gia các hoạt động đối ngoại trực tuyến
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Báo cáo nhân sự đi nước ngoài và chủ trì/tham gia các hoạt động đối ngoại trực tuyến theo phân quyền actor Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-61: Báo cáo thống kê hội thảo
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Báo cáo thống kê hội thảo theo phân quyền actor Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, CONFERENCE.

### FR-UC-62: Báo cáo thống kê khen thưởng
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Báo cáo thống kê khen thưởng theo phân quyền actor Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, EMULATION_COMMENDATION.

### FR-UC-63: Báo cáo thống kê chuyên gia
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Báo cáo thống kê chuyên gia theo phân quyền actor Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, EXPERT.

### FR-UC-64: Nhận dữ liệu tài liệu theo đơn vị
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Nhận dữ liệu tài liệu theo đơn vị theo phân quyền actor Hệ thống quản lý văn bản và điều hành.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-65: Nhận dữ liệu tài liệu theo nhiệm vụ
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Nhận dữ liệu tài liệu theo nhiệm vụ theo phân quyền actor Hệ thống quản lý văn bản và điều hành.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-66: Tra cứu dữ liệu văn bản hợp tác quốc tế về pháp luật
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Tra cứu dữ liệu văn bản hợp tác quốc tế về pháp luật theo phân quyền actor Hệ thống CSDL pháp luật quốc gia.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-67: Tích hợp đăng nhập nền tảng định danh và xác thực điện tử
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Tích hợp đăng nhập nền tảng định danh và xác thực điện tử theo phân quyền actor Nền tảng định danh và xác thực điện tử.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-68: Đồng bộ thông tin người dùng
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Đồng bộ thông tin người dùng theo phân quyền actor Nền tảng định danh và xác thực điện tử.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-69: Chia sẻ thông tin dashboard sang hệ thống khác
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Chia sẻ thông tin dashboard sang hệ thống khác theo phân quyền actor Hệ thống khác.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-70: Nhận dữ liệu danh mục đối tác nước ngoài
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Nhận dữ liệu danh mục đối tác nước ngoài theo phân quyền actor Hệ thống kho dữ liệu dùng chung.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-71: Nhận dữ liệu danh mục quốc gia
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Nhận dữ liệu danh mục quốc gia theo phân quyền actor Hệ thống kho dữ liệu dùng chung.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-72: Nhận dữ liệu danh mục cơ quan tổ chức trong nước
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Nhận dữ liệu danh mục cơ quan tổ chức trong nước theo phân quyền actor Hệ thống kho dữ liệu dùng chung.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-73: Nhận dữ liệu danh mục ngôn ngữ
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Nhận dữ liệu danh mục ngôn ngữ theo phân quyền actor Hệ thống kho dữ liệu dùng chung.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-74: Nhận dữ liệu danh mục loại văn bản
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Nhận dữ liệu danh mục loại văn bản theo phân quyền actor Hệ thống kho dữ liệu dùng chung.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-75: Nhận dữ liệu danh mục lĩnh vực hợp tác
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Nhận dữ liệu danh mục lĩnh vực hợp tác theo phân quyền actor Hệ thống kho dữ liệu dùng chung.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-76: Nhận dữ liệu danh mục hình thức hợp tác
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Nhận dữ liệu danh mục hình thức hợp tác theo phân quyền actor Hệ thống kho dữ liệu dùng chung.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-77: Nhận dữ liệu danh mục loại nguồn vốn
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Nhận dữ liệu danh mục loại nguồn vốn theo phân quyền actor Hệ thống kho dữ liệu dùng chung.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-78: Nhận dữ liệu danh mục lĩnh vực chuyên môn
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Nhận dữ liệu danh mục lĩnh vực chuyên môn theo phân quyền actor Hệ thống kho dữ liệu dùng chung.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-79: Nhận dữ liệu danh mục hình thức khen thưởng
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Nhận dữ liệu danh mục hình thức khen thưởng theo phân quyền actor Hệ thống kho dữ liệu dùng chung.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, EMULATION_COMMENDATION.

### FR-UC-80: Nhận dữ liệu danh mục phân loại đoàn
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Nhận dữ liệu danh mục phân loại đoàn theo phân quyền actor Hệ thống kho dữ liệu dùng chung.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, DELEGATION.

### FR-UC-81: Nhận dữ liệu danh mục nguồn kinh phí
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Nhận dữ liệu danh mục nguồn kinh phí theo phân quyền actor Hệ thống kho dữ liệu dùng chung.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-82: Nhận dữ liệu danh mục danh nghĩa ký
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Nhận dữ liệu danh mục danh nghĩa ký theo phân quyền actor Hệ thống kho dữ liệu dùng chung.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-83: Đồng bộ thông tin đơn vị
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Đồng bộ thông tin đơn vị theo phân quyền actor Hệ thống kho dữ liệu dùng chung.
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-84: Chia sẻ thông tin điều ước quốc tế, thỏa thuận quốc tế
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Chia sẻ thông tin điều ước quốc tế, thỏa thuận quốc tế theo phân quyền actor Nền tảng kết nối chia sẻ của Bộ Tư pháp (LGSP).
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-85: Chia sẻ thông tin chương trình dự án
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Chia sẻ thông tin chương trình dự án theo phân quyền actor Nền tảng kết nối chia sẻ của Bộ Tư pháp (LGSP).
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-86: Chia sẻ danh sách chuyên gia
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Chia sẻ danh sách chuyên gia theo phân quyền actor Nền tảng kết nối chia sẻ của Bộ Tư pháp (LGSP).
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, EXPERT.

### FR-UC-87: Chia sẻ thông tin hội nghị hội thảo
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Chia sẻ thông tin hội nghị hội thảo theo phân quyền actor Nền tảng kết nối chia sẻ của Bộ Tư pháp (LGSP).
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, CONFERENCE.

### FR-UC-88: Chia sẻ Báo cáo kinh nghiệm quốc tế (ngoài chương trình dự án)
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Chia sẻ Báo cáo kinh nghiệm quốc tế (ngoài chương trình dự án) theo phân quyền actor Nền tảng kết nối chia sẻ của Bộ Tư pháp (LGSP).
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, INTERNATIONAL_AGREEMENT.

### FR-UC-89: Chia sẻ thông tin đoàn
- **Giải pháp**: Xây dựng màn hình UI & API backend xử lý luồng Chia sẻ thông tin đoàn theo phân quyền actor Nền tảng kết nối chia sẻ của Bộ Tư pháp (LGSP).
- **Bảng CSDL liên quan**: SYS_USER, ROLE, ATTACHMENT, DELEGATION.

