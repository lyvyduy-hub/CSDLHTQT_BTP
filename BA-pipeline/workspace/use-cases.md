# Đặc Tả Use Case Hệ Thống (Use Cases Specification)

## UC-FR-UC-01: Quản lý vai trò
- **Actor**: Quản trị hệ thống
- **Mô tả ngắn**: Quản trị hệ thống nhập điều kiện tìm kiếm vai trò và chọn tìm kiếm. Hệ thống hiển thị kết quả vai trò theo các tiêu chí đã nhập.   Quản trị hệ thống thực hiện thêm mới thông tin vai trò.   Quản trị hệ thống thực hiện chỉnh sửa thông tin vai trò. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Quản trị hệ thống thực hiện thiết lập quyền cho vai trò. Hệ thống lưu thiết lập quyền và hiển thị kết quả.   Quản trị hệ thống thực hiện xóa vai trò. Hệ thống kiểm tra tính hợp lệ và nếu hợp lệ thực hiện xóa, nếu không hợp lệ hiển thị lỗi cụ thể.   Quản trị hệ thống chọn chức năng khóa/mở khóa vai trò. Hệ thống thực hiện khóa vai trò và hiển thị kết quả.   Quản trị hệ thống thực hiện import danh sách vai trò. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý vai trò trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-02: Quản lý phân quyền
- **Actor**: Quản trị hệ thống
- **Mô tả ngắn**: Quản trị hệ thống nhập điều kiện tìm kiếm quyền và chọn tìm kiếm. Hệ thống hiển thị kết quả thông tin quyền theo các tiêu chí đã nhập.   Quản trị hệ thống thực hiện thêm mới thông tin quyền. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Quản trị hệ thống thực hiện chỉnh sửa thông tin quyền. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Quản trị hệ thống thực hiện xóa thông tin quyền. Hệ thống kiểm tra tính hợp lệ và nếu hợp lệ thực hiện xóa, nếu không hợp lệ hiển thị lỗi cụ thể.   Quản trị hệ thống chọn chức năng khóa./mở khóa quyền. Hệ thống thực hiện khóa quyền và hiển thị kết quả.   Quản trị hệ thống thực hiện import danh sách quyền. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý phân quyền trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-03: Quản lý người dùng
- **Actor**: Quản trị hệ thống
- **Mô tả ngắn**: Quản trị hệ thống nhập điều kiện tìm kiếm người dùng và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách người dùng theo các tiêu chí đã nhập.   Quản trị hệ thống chọn xem danh sách thông tin người dùng. Hệ thống hiển thị danh sách thông tin người dùng.   Quản trị hệ thống thực hiện gán/bỏ gán vai trò cho người dùng. Hệ thống lưu thông tin gán vai trò và hiển thị kết quả.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý người dùng trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-04: Quản lý đơn vị
- **Actor**: Quản trị hệ thống
- **Mô tả ngắn**: Quản trị hệ thống xem danh sách đơn vị; Hệ thống hiển thị thông tin danh sách đơn vị   Quản trị hệ thống tìm kiếm đơn vị; Hệ thống truy vấn dữ liệu và hiển thị kết quả thông tin đơn vị tương ứng với điều kiện tìm kiếm   Quản trị hệ thống xem chi tiết nội dung một đơn vị; Hệ thống hiển thị thông tin chi tiết của đơn vị
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý đơn vị trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-05: Quản lý cấu hình thông báo
- **Actor**: Quản trị hệ thống
- **Mô tả ngắn**: Quản trị hệ thống tìm kiếm cấu hình thông báo. Hệ thống hiển thị kết quả theo tiêu chí đã chọn   Quản trị hệ thống thêm mới cấu hình thông báo. Hệ thống kiểm tra thông tin, nếu hợp lệ thì lưu vào CSDL, nếu không hợp lệ thì thông báo lỗi   Quản trị hệ thống chỉnh sửa cấu hình thông báo. Hệ thống kiểm tra thông tin, nếu hợp lệ thì lưu vào CSDL, nếu không hợp lệ thì thông báo lỗi   Quản trị hệ thống xoá cấu hình thông báo. Hệ thống kiểm tra thông tin, nếu hợp lệ thì lưu vào CSDL, nếu không hợp lệ thì thông báo lỗi   Quản trị hệ thống khoá/mở khóa cấu hình thông báo. Hệ thống kiểm tra thông tin, nếu hợp lệ thì lưu vào CSDL, nếu không hợp lệ thì thông báo lỗi
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý cấu hình thông báo trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-06: Quản lý lịch sử tác động
- **Actor**: Quản trị hệ thống
- **Mô tả ngắn**: Quản trị hệ thống thực hiện tìm kiếm lịch sử tác động. Hệ thống hiển thị kết quả theo tiêu chí đã nhập   Quản trị hệ thống xem chi tiết lịch sử tác động. Hệ thống hiển thị chi tiết thông tin   Quản trị hệ thống xuất file danh sách lịch sử tác động. Hệ thống xuất file lịch sử tác động và cho phép người dùng lưu về máy.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý lịch sử tác động trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-07: Quản lý lịch sử lỗi phát sinh
- **Actor**: Quản trị hệ thống
- **Mô tả ngắn**: Quản trị hệ thống thực hiện tìm kiếm lỗi phát sinh. Hệ thống hiển thị kết quả theo tiêu chí đã nhập   Quản trị hệ thống xem chi tiết lịch sử lỗi phát sinh. Hệ thống hiển thị chi tiết thông tin   Quản trị hệ thống xuất file danh sách lịch sử lỗi phát sinh. Hệ thống xuất file lịch sử lỗi phát sinh và cho phép Quản trị hệ thống lưu về máy.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý lịch sử lỗi phát sinh trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-08: Quản lý chính sách lưu trữ nhật ký tác động hệ thống
- **Actor**: Quản trị hệ thống
- **Mô tả ngắn**: Quản trị hệ thống thực hiện tìm kiếm chính sách. Hệ thống trả về kết quả tìm kiếm theo các tiêu chí Quản trị hệ thống đã chọn.   Quản trị hệ thống thực hiện thêm mới chính sách lưu trữ nhật ký tác động hệ thống. Hệ thống kiểm tra thông tin, nếu hợp lệ thì lưu vào CSDL, nếu không hợp lệ thì thông báo lỗi cho Quản trị hệ thống.   Quản trị hệ thống thực hiện chỉnh sửa chính sách lưu trữ nhật ký tác động hệ thống. Hệ thống kiểm tra thông tin, nếu hợp lệ thì lưu vào CSDL, nếu không hợp lệ thì thông báo lỗi cho Quản trị hệ thống.   Quản trị hệ thống thực hiện xoá chính sách lưu trữ nhật ký tác động hệ thống. Hệ thống kiểm tra thông tin, nếu hợp lệ thì lưu vào CSDL, nếu không hợp lệ thì thông báo lỗi cho Quản trị hệ thống.   Quản trị hệ thống chọn chính sách cần khóa/mở khóa và nhấn Khóa chính sách. Hệ thống thực hiện khóa chính sách đã chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý chính sách lưu trữ nhật ký tác động hệ thống trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-09: Lưu log hệ thống
- **Actor**: Quản trị hệ thống
- **Mô tả ngắn**: Người dùng truy cập Phần mềm. Hệ thống thực hiện kiểm tra chính sách lưu trữ nhật ký tác động hệ thống, nếu tác động của người dùng nằm trong danh sách các tác động cần lưu nhật ký hệ thống theo chính sách đã thiết lập, hệ thống thực hiện lưu nhật ký tác động.   Quản trị hệ thống đăng nhập khi quản trị Phần mềm. Hệ thống thực hiện kiểm tra chính sách lưu trữ nhật ký tác động hệ thống, nếu tác động của người dùng nằm trong danh sách các tác động cần lưu nhật ký hệ thống theo chính sách đã thiết lập, hệ thống thực hiện lưu nhật ký tác động.   Người dùng thực hiện các thao tác tác động vào hệ thống. Hệ thống thực hiện kiểm tra chính sách lưu trữ nhật ký tác động hệ thống, nếu tác động của người dùng nằm trong danh sách các tác động cần lưu nhật ký hệ thống theo chính sách đã thiết lập, hệ thống thực hiện lưu nhật ký tác động.   Người dùng thực hiện các chức năng quản lý tài khoản. Hệ thống thực hiện kiểm tra chính sách lưu trữ nhật ký tác động hệ thống, nếu tác động của người dùng nằm trong danh sách các tác động cần lưu nhật ký hệ thống theo chính sách đã thiết lập, hệ thống thực hiện lưu nhật ký tác động.   Quản trị hệ thống thực hiện thay đổi cấu hình Phần mềm. Hệ thống thực hiện kiểm tra chính sách lưu trữ nhật ký tác động hệ thống, nếu tác động của người dùng nằm trong danh sách các tác động cần lưu nhật ký hệ thống theo chính sách đã thiết lập, hệ thống thực hiện lưu nhật ký tác động.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Lưu log hệ thống trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-10: Gửi thông tin log tác động/log lỗi phát sinh
- **Actor**: Nền tảng kết nối chia sẻ của Bộ Tư pháp (LGSP)
- **Mô tả ngắn**: Nền tảng LGSP kiểm tra kết nối gửi thông tin log tác động/log lỗi phát sinh. Hệ thống nhận kết quả kiểm tra kết nối nếu hợp lệ thì cho phép kết nối, nếu không hợp lệ thì thông báo lại cho nền tảng LGSP   Nền tảng LGSP thực hiện kết nối với API gửi thông tin log tác động/log lỗi phát sinh. Hệ thống nhận thông báo kết quả kết nối .
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Gửi thông tin log tác động/log lỗi phát sinh trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-11: Thiết lập chính sách sao lưu dự phòng
- **Actor**: Quản trị hệ thống
- **Mô tả ngắn**: Quản trị hệ thống truy cập chức năng thiết lập chính sách sao lưu dự phòng. Hệ thống hiển thị màn hình tương ứng   Quản trị hệ thống nhập các tham số thiết lập chính sách và thực hiện lưu. Hệ thống kiểm tra, nếu hợp lệ thì lưu dữ liệu và thông báo thiết lập thành công, nếu không hợp lệ báo lỗi cụ thể   Quản trị hệ thống cấu hình khôi phục dữ liệu. Hệ thống kiểm tra thông tin, nếu hợp lệ thì lưu vào CSDL, nếu không hợp lệ thì thông báo cho người dùng
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Thiết lập chính sách sao lưu dự phòng trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-12: Đăng xuất
- **Actor**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống
- **Mô tả ngắn**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống chọn đăng xuất khỏi hệ thống. Hệ thống gửi yêu cầu đăng xuất sang Nền tảng định danh và xác thực điện tử   Nền tảng định danh và xác thực điện tử kiểm tra yêu cầu, nếu hợp lệ thì thực hiện đăng xuất khỏi hệ thống, nếu không hợp lệ thì thông báo lỗi
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Đăng xuất trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-13: Xem thông tin cá nhân
- **Actor**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống
- **Mô tả ngắn**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống vào xem thông tin cá nhân, hệ thống hiển thị màn hình thông tin cơ bản   Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống yêu cầu xem chi tiết thông tin cá nhân. Hệ thống hiển thị chi tiết thông tin cá nhân
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Xem thông tin cá nhân trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-14: Xem tài liệu hướng dẫn sử dụng
- **Actor**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo chọn xem chi tiết file hướng dẫn sử dụng. Hệ thống thực hiện mở file hướng dẫn.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện tải xuống file hướng dẫn sử dụng. Hệ thống thực hiện tải xuống file hướng dẫn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Xem tài liệu hướng dẫn sử dụng trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-15: Xem biểu đồ thống kê điều ước quốc tế, thỏa thuận quốc tế
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo/Quản trị hệ thống truy cập vào dasboard. Hệ thống hiển thị biểu đồ thống kê điều ước quốc tế, thỏa thuận quốc tế   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo/Quản trị hệ thống thực hiện lọc dữ liệu. Hệ thống xử lý yêu cầu lọc của người dùng và hiển thị thông tin thống kê điều ước quốc tế, thỏa thuận quốc tế với dữ liệu mới.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo/Quản trị hệ thống yêu cầu xem chi tiết các đối tượng trong một phần của biểu đồ. Hệ thống trả về thông tin chi tiết điều ước quốc tế, thỏa thuận quốc tế tương ứng.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Xem biểu đồ thống kê điều ước quốc tế, thỏa thuận quốc tế trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-16: Xem biểu đồ thống kê chương trình dự án
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo/Quản trị hệ thống truy cập vào dasboard. Hệ thống hiển thị biểu đồ thống kê chương trình dự án   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo/Quản trị hệ thống thực hiện lọc dữ liệu. Hệ thống xử lý yêu cầu lọc của người dùng và hiển thị thông tin thống kê chương trình dự án với dữ liệu mới.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo/Quản trị hệ thống yêu cầu xem chi tiết các đối tượng trong một phần của biểu đồ. Hệ thống trả về thông tin chi tiết chương trình dự án tương ứng.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Xem biểu đồ thống kê chương trình dự án trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-17: Thống kê danh sách hội thảo
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo/Quản trị hệ thống thực hiện xem danh sách hội thảo. Hệ thống hiển thị danh sách hội thảo.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo/Quản trị hệ thống nhập điều kiện tìm kiếm nhanh hội thảo và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách hội thảo theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo/Quản trị hệ thống chọn xem chi tiết thông tin hội thảo. Hệ thống hiển thị chi tiết thông tin hội thảo.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Thống kê danh sách hội thảo trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-18: Xem thông báo
- **Actor**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống
- **Mô tả ngắn**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/quản trị hệ thống truy cập hệ thống để xem thông báo. Hệ thống hiển thị số lượng và danh sách thông báo tại màn hình trang chủ   Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo/Quản trị hệ thống xem chi tiết thông báo. Hệ thống hiển thị màn hình chi tiết thông báo
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Xem thông báo trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-19: Quản lý điều ước quốc tế
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm điều ước quốc tế và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách điều ước quốc tế theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết điều ước quốc tế. Hệ thống hiển thị đầy đủ thông tin chi tiết của điều ước quốc tế được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm về điều ước quốc tế. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới điều ước quốc tế. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa điều ước quốc tế. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa điều ước quốc tế. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách điều ước quốc tế. Hệ thống thực hiện xuất dữ liệu danh sách điều ước quốc tế theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý điều ước quốc tế trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-20: Quản lý thỏa thuận quốc tế
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm thỏa thuận quốc tế và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách thỏa thuận quốc tế theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thỏa thuận quốc tế. Hệ thống hiển thị đầy đủ thông tin chi tiết của thỏa thuận quốc tế được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm về thỏa thuận quốc tế. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên/lãnh đạo viên thực hiện thêm mới thỏa thuận quốc tế. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa thỏa thuận quốc tế. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa thỏa thuận quốc tế. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách thỏa thuận quốc tế. Hệ thống thực hiện xuất dữ liệu danh sách thỏa thuận quốc tế theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý thỏa thuận quốc tế trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-21: Quản lý thỏa thuận khác
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm thỏa thuận khác và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách thỏa thuận khác theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thỏa thuận khác. Hệ thống hiển thị đầy đủ thông tin chi tiết của thỏa thuận khác được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm thỏa thuận khác. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới thỏa thuận khác. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa thỏa thuận khác. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa thỏa thuận khác. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách thỏa thuận khác. Hệ thống thực hiện xuất dữ liệu danh sách thỏa thuận khác theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý thỏa thuận khác trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-22: Triển khai điều ước quốc tế, thỏa thuận quốc tế, thỏa thuận khác
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm thông tin triển khai điều ước quốc tế, thỏa thuận quốc tế, thỏa thuận khác và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách thông tin triển khai điều ước quốc tế, thỏa thuận quốc tế, thỏa thuận khác theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thông tin triển khai điều ước quốc tế, thỏa thuận quốc tế, thỏa thuận khác. Hệ thống hiển thị đầy đủ thông tin triển khai điều ước quốc tế, thỏa thuận quốc tế, thỏa thuận khác được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm về thông tin triển khai điều ước quốc tế, thỏa thuận quốc tế, thỏa thuận khác. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới thông tin triển khai điều ước quốc tế, thỏa thuận quốc tế, thỏa thuận khác. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa thông tin triển khai điều ước quốc tế, thỏa thuận quốc tế, thỏa thuận khác. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa thông tin triển khai điều ước quốc tế, thỏa thuận quốc tế, thỏa thuận khác. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách triển khai điều ước quốc tế, thỏa thuận quốc tế, thỏa thuận khác. Hệ thống thực hiện xuất dữ liệu danh sách điều ước quốc tế, thỏa thuận quốc tế, thỏa thuận khác theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Triển khai điều ước quốc tế, thỏa thuận quốc tế, thỏa thuận khác trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-23: Quản lý chương trình dự án
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm Chương trình dự án và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách Chương trình dự án theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết Chương trình dự án. Hệ thống hiển thị đầy đủ thông tin chi tiết của Chương trình dự án được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm Chương trình dự án. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo viên thực hiện thêm mới Chương trình dự án. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa Chương trình dự án. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa Chương trình dự án. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách Chương trình dự án. Hệ thống thực hiện xuất dữ liệu danh sách Chương trình dự án theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý chương trình dự án trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-24: Quản lý kế hoạch hàng năm
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm Kế hoạch hàng năm và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách Kế hoạch hàng năm theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết Kế hoạch hàng năm. Hệ thống hiển thị đầy đủ thông tin chi tiết của Kế hoạch hàng năm được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm Kế hoạch hàng năm. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo viên thực hiện thêm mới Kế hoạch hàng năm. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa Kế hoạch hàng năm. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa Kế hoạch hàng năm. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách Kế hoạch hàng năm. Hệ thống thực hiện xuất dữ liệu danh sách Kế hoạch hàng năm theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý kế hoạch hàng năm trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-25: Cập nhật kết quả triển khai kế hoạch hàng năm
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem kết quả triển khai kế hoạch hàng năm. Hệ thống hiển thị thông tin kết quả triển khai kế hoạch hàng năm   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem file đính kèm về kết quả triển khai kế hoạch hàng năm. Hệ thống thực hiện mở/tải về file đính kèm   Chuyên viên nhập liệu/lãnh đạo thực hiện cập nhật Kết quả triển kế hoạch hàng năm. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Cập nhật kết quả triển khai kế hoạch hàng năm trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-26: Quản lý chuyên gia trong nước
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm chuyên gia trong nước và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách chuyên gia theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm về chuyên gia trong nước. Hệ thống thực hiện mở/tải về file đính kèm .   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thông tin chuyên gia trong nước. Hệ thống hiển thị đầy đủ thông tin chi tiết của chuyên gia được chọn.   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới thông tin chuyên gia trong nước. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa thông tin chuyên gia trong nước. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa thông tin chuyên gia trong nước. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách chuyên gia trong nước. Hệ thống thực hiện xuất dữ liệu danh sách chuyên gia theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý chuyên gia trong nước trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-27: Quản lý chuyên gia quốc tế
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm chuyên gia quốc tế và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách chuyên gia theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm về chuyên gia quốc tế. Hệ thống thực hiện mở/tải về file đính kèm .   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thông tin chuyên gia quốc tế. Hệ thống hiển thị đầy đủ thông tin chi tiết của chuyên gia được chọn.   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới thông tin chuyên gia quốc tế. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa thông tin chuyên gia quốc tế. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa thông tin chuyên gia quốc tế. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách chuyên gia quốc tế. Hệ thống thực hiện xuất dữ liệu danh sách chuyên gia theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý chuyên gia quốc tế trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-28: Quản lý chuyên gia Việt Nam ở nước ngoài
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm Chuyên gia Việt Nam ở nước ngoài và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách chuyên gia theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm về chuyên gia Việt Nam ở nước ngoài. Hệ thống thực hiện mở/tải về file đính kèm .   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thông tin chuyên gia Việt Nam ở nước ngoài. Hệ thống hiển thị đầy đủ thông tin chi tiết của chuyên gia được chọn.   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới thông tin chuyên gia Việt Nam ở nước ngoài. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa thông tin chuyên gia Việt Nam ở nước ngoài. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa thông tin chuyên gia Việt Nam ở nước ngoài. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách chuyên gia Việt Nam ở nước ngoài. Hệ thống thực hiện xuất dữ liệu danh sách chuyên gia theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý chuyên gia Việt Nam ở nước ngoài trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-29: Quản lý đoàn ra do Bộ Tư Pháp chủ trì
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm đoàn ra do Bộ Tư Pháp chủ trì và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách kế hoạch đoàn ra theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thông tin đoàn ra do Bộ Tư Pháp chủ trì. Hệ thống hiển thị đầy đủ thông tin chi tiết của kế hoạch đoàn ra được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm về đoàn ra do Bộ Tư Pháp chủ trì. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới thông tin đoàn ra do Bộ Tư Pháp chủ trì. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa thông tin đoàn ra do Bộ Tư Pháp chủ trì. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa thông tin đoàn ra do Bộ Tư Pháp chủ trì. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách đoàn ra do Bộ Tư Pháp chủ trì. Hệ thống thực hiện xuất dữ liệu danh sách kế hoạch đoàn ra theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý đoàn ra do Bộ Tư Pháp chủ trì trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-30: Quản lý đoàn ra tháp tùng
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm đoàn ra tháp tùng và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách kế hoạch đoàn ra theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thông tin đoàn ra tháp tùng. Hệ thống hiển thị đầy đủ thông tin chi tiết của kế hoạch đoàn ra được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm về đoàn ra tháp tùng. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới thông tin đoàn ra tháp tùng. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa thông tin đoàn ra tháp tùng. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa thông tin đoàn ra tháp tùng. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách đoàn ra tháp tùng. Hệ thống thực hiện xuất dữ liệu danh sách kế hoạch đoàn ra theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý đoàn ra tháp tùng trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-31: Quản lý đoàn ra khác
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm đoàn ra khác và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách kế hoạch đoàn ra theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thông tin đoàn ra khác. Hệ thống hiển thị đầy đủ thông tin chi tiết của kế hoạch đoàn ra được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm về đoàn ra khác. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới thông tin đoàn ra khác. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa thông tin đoàn ra khác. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa thông tin đoàn ra khác. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách đoàn ra khác. Hệ thống thực hiện xuất dữ liệu danh sách kế hoạch đoàn ra theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý đoàn ra khác trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-32: Cập nhật kết quả đoàn ra
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết đoàn ra. Hệ thống hiển thị đầy đủ thông tin chi tiết của kết quả đoàn ra được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm kết quả đoàn ra. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện cập nhật kết quả đoàn ra. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Cập nhật kết quả đoàn ra trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-33: Quản lý đoàn vào
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm đoàn vào và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách kế hoạch đoàn vào theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thông tin đoàn vào. Hệ thống hiển thị đầy đủ thông tin chi tiết của kế hoạch đoàn vào được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết về đoàn vào. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới thông tin đoàn vào. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa thông tin đoàn vào. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa thông tin đoàn vào. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách đoàn vào. Hệ thống thực hiện xuất dữ liệu danh sách kế hoạch đoàn vào theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý đoàn vào trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-34: Cập nhật kết quả đoàn vào
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết đoàn vào. Hệ thống hiển thị đầy đủ thông tin chi tiết của kết quả đoàn ra được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm kết quả đoàn vào. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện cập nhật kết quả đoàn vào. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Cập nhật kết quả đoàn vào trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-35: Quản lý hội nghị, hội thảo
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm thông tin hội nghị hội thảo và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách hội thảo theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết hội nghị hội thảo. Hệ thống hiển thị đầy đủ thông tin chi tiết .   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm hội nghị hội thảo. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới hội nghị hội thảo. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa thông tin hội nghị hội thảo. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa thông tin hội nghị hội thảo. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách hội nghị hội thảo. Hệ thống thực hiện xuất dữ liệu danh sách hội nghị hội thảo theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý hội nghị, hội thảo trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-36: Quản lý đề án hợp tác quốc tế về pháp luật
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm đề án và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách đề án theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thông tin đề án. Hệ thống hiển thị đầy đủ thông tin chi tiết của đề án được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm về đề án. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới đề án. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa đề án. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa đề án. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách đề án. Hệ thống thực hiện xuất dữ liệu danh sách đề án theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý đề án hợp tác quốc tế về pháp luật trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-37: Quản lý hoạt động khác
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm hoạt động khác và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách hoạt động khác theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thông tin hoạt động khác. Hệ thống hiển thị đầy đủ thông tin chi tiết của hoạt động khác được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm về hoạt động khác. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới hoạt động khác. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa hoạt động khác. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa hoạt động khác. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách hoạt động khác. Hệ thống thực hiện xuất dữ liệu danh sách hoạt động khác theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý hoạt động khác trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-38: Quản lý Báo cáo kinh nghiệm quốc tế (ngoài chương trình dự án)
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm Báo cáo kinh nghiệm quốc tế ( ngoài chương trình dự án) và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách Báo cáo kinh nghiệm quốc tế ( ngoài chương trình dự án) theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thông tin Báo cáo kinh nghiệm quốc tế ( ngoài chương trình dự án). Hệ thống hiển thị đầy đủ thông tin chi tiết của Báo cáo kinh nghiệm quốc tế ( ngoài chương trình dự án) được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm Báo cáo kinh nghiệm quốc tế ( ngoài chương trình dự án). Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới Báo cáo kinh nghiệm quốc tế ( ngoài chương trình dự án). Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa Báo cáo kinh nghiệm quốc tế ( ngoài chương trình dự án). Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa Báo cáo kinh nghiệm quốc tế ( ngoài chương trình dự án). Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách Báo cáo kinh nghiệm quốc tế ( ngoài chương trình dự án). Hệ thống thực hiện xuất dữ liệu danh sách Báo cáo kinh nghiệm quốc tế ( ngoài chương trình dự án) theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý Báo cáo kinh nghiệm quốc tế (ngoài chương trình dự án) trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-39: Quản lý khen thưởng phía Việt Nam trao
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm khen thưởng phía Việt Nam trao và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách khen thưởng phía Việt Nam trao theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thông tin khen thưởng phía Việt Nam trao. Hệ thống hiển thị đầy đủ thông tin chi tiết của khen thưởng phía Việt Nam trao được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm về khen thưởng Việt Nam trao. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới khen thưởng phía Việt Nam trao. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa khen thưởng phía Việt Nam trao. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa khen thưởng phía Việt Nam trao. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách khen thưởng phía Việt Nam trao. Hệ thống thực hiện xuất dữ liệu danh sách khen thưởng phía Việt Nam trao theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý khen thưởng phía Việt Nam trao trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-40: Quản lý khen thưởng phía Việt Nam nhận
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm khen thưởng phía Việt Nam nhận và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách khen thưởng phía Việt Nam nhận theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thông tin khen thưởng phía Việt Nam nhận. Hệ thống hiển thị đầy đủ thông tin chi tiết của khen thưởng phía Việt Nam nhận được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm về khen thưởng Việt Nam nhận. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới khen thưởng phía Việt Nam nhận. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa khen thưởng phía Việt Nam nhận. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa khen thưởng phía Việt Nam nhận. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách khen thưởng phía Việt Nam nhận. Hệ thống thực hiện xuất dữ liệu danh sách khen thưởng phía Việt Nam nhận theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý khen thưởng phía Việt Nam nhận trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-41: Quản lý báo cáo thường niên, giai đoạn
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm báo cáo thường niên, giai đoạn và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách báo cáo hợp tác pháp luật theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết báo cáo thường niên, giai đoạn. Hệ thống hiển thị đầy đủ thông tin chi tiết của báo cáo hợp tác pháp luật được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm về báo cáo thường niên, giai đoạn. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới báo cáo thường niên, giai đoạn. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa báo cáo thường niên, giai đoạn. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa báo cáo thường niên, giai đoạn. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách báo cáo thường niên, giai đoạn. Hệ thống thực hiện xuất dữ liệu danh sách báo cáo hợp tác pháp luật theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý báo cáo thường niên, giai đoạn trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-42: Quản lý báo cáo chuyên đề, đặc thù
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm báo cáo chuyên đề, đặc thù và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách báo cáo theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết báo cáo chuyên đề, đặc thù. Hệ thống hiển thị đầy đủ thông tin chi tiết của báo cáo được chọn.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết file đính kèm về báo cáo chuyên đề, đặc thù. Hệ thống thực hiện mở/tải về file đính kèm .   Chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới báo cáo chuyên đề, đặc thù. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa báo cáo chuyên đề, đặc thù. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Chuyên viên nhập liệu/lãnh đạo thực hiện xóa báo cáo chuyên đề, đặc thù. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách báo cáo chuyên đề, đặc thù. Hệ thống thực hiện xuất dữ liệu danh sách báo cáo theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý báo cáo chuyên đề, đặc thù trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-43: Quản lý văn bản quy phạm pháp luật
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm văn bản quy phạm pháp luật và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách văn bản quy phạm pháp luật theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết văn bản quy phạm pháp luật. Hệ thống hiển thị đầy đủ thông tin chi tiết của văn bản quy phạm pháp luật được chọn.   chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới văn bản quy phạm pháp luật. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa văn bản quy phạm pháp luật. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   chuyên viên nhập liệu/lãnh đạo thực hiện xóa văn bản quy phạm pháp luật. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách văn bản quy phạm pháp luật. Hệ thống thực hiện xuất dữ liệu danh sách văn bản quy phạm pháp luật theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý văn bản quy phạm pháp luật trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-44: Quản lý văn bản khác
- **Actor**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện tìm kiếm văn bản khác và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách văn bản khác theo các tiêu chí đã nhập.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem chi tiết thông tin văn bản khác. Hệ thống hiển thị đầy đủ thông tin chi tiết của văn bản khác được chọn.   chuyên viên nhập liệu/lãnh đạo thực hiện thêm mới văn bản khác. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   chuyên viên nhập liệu/lãnh đạo thực hiện chỉnh sửa văn bản khác. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì cập nhật vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   chuyên viên nhập liệu/lãnh đạo thực hiện xóa văn bản khác. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file danh sách văn bản khác. Hệ thống thực hiện xuất dữ liệu danh sách văn bản khác theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý văn bản khác trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-45: Quản lý chia sẻ dữ liệu
- **Actor**: Chuyên viên nhập liệu/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/Lãnh đạo nhập điều kiện tìm kiếm dữ liệu chia sẻ. Hệ thống hiển thị kết quả tìm kiếm theo tiêu chí đã nhập   Chuyên viên nhập liệu/Lãnh đạo chọn thêm dữ liệu để chia sẻ. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện chia sẻ và hiển thị kết quả, nếu không thì báo lỗi.   Chuyên viên nhập liệu/Lãnh đạo cập nhật chia sẻ dữ liệu. Hệ thống kiểm tra tính hợp lệ, nếu hợp lệ thì lưu vào CSDL và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý chia sẻ dữ liệu trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-46: Quản lý dữ liệu đồng bộ
- **Actor**: Chuyên viên nhập liệu/lãnh đạo
- **Mô tả ngắn**: chuyên viên nhập liệu/lãnh đạo nhập điều kiện tìm kiếm dữ liệu đồng bộ và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách dữ liệu được đồng bộ theo các tiêu chí đã nhập.   chuyên viên nhập liệu/lãnh đạo chọn xem chi tiết dữ liệu đồng bộ. Hệ thống hiển thị chi tiết thông tin của dữ liệu được đồng bộ.   chuyên viên nhập liệu/lãnh đạo thực hiện xóa dữ liệu đồng bộ. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì thực hiện xóa và hiển thị kết quả, nếu không hợp lệ báo lỗi cụ thể.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý dữ liệu đồng bộ trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-47: Phân loại dữ liệu
- **Actor**: Chuyên viên nhập liệu/lãnh đạo
- **Mô tả ngắn**: chuyên viên nhập liệu/lãnh đạo chọn chức năng phân loại dữ liệu trên hệ thống. Hệ thống hiển thị danh mục dữ liệu hợp tác quốc tế.   chuyên viên nhập liệu/lãnh đạo chọn danh mục cần phân loại. Hệ thống hiển thị giao diện thêm mới   chuyên viên nhập liệu/lãnh đạo thực hiện nhập dữ liệu bổ sung vào danh mục. Hệ thống kiểm tra tính hợp lệ của dữ liệu, nếu hợp lệ thì lưu và thông báo thành công, nếu không hợp lệ báo lỗi cụ thể.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Phân loại dữ liệu trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-48: Quản lý danh mục đối tác nước ngoài
- **Actor**: Chuyên viên nhập liệu/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/lãnh đạo nhập điều kiện tìm kiếm đối tác nước ngoài và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách đối tác nước ngoài theo các tiêu chí đã nhập.   Chuyên viên nhập liệu/lãnh đạo thực hiện xuất file danh sách đối tác nước ngoài. Hệ thống thực hiện xuất dữ liệu danh sách đối tác nước ngoài theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý danh mục đối tác nước ngoài trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-49: Quản lý danh mục quốc gia
- **Actor**: Chuyên viên nhập liệu/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/lãnh đạo nhập điều kiện tìm kiếm quốc gia và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách quốc gia theo các tiêu chí đã nhập.   Chuyên viên nhập liệu/lãnh đạo thực hiện xuất file danh sách quốc gia. Hệ thống thực hiện xuất dữ liệu danh sách quốc gia theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý danh mục quốc gia trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-50: Quản lý danh mục cơ quan tổ chức trong nước
- **Actor**: Chuyên viên nhập liệu/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/lãnh đạo nhập điều kiện tìm kiếm cơ quan tổ chức trong nước và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách cơ quan tổ chức trong nước theo các tiêu chí đã nhập.   Chuyên viên nhập liệu/lãnh đạo thực hiện xuất file danh sách cơ quan tổ chức trong nước. Hệ thống thực hiện xuất dữ liệu danh sách cơ quan tổ chức trong nước theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý danh mục cơ quan tổ chức trong nước trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-51: Quản lý danh mục lĩnh vực hợp tác
- **Actor**: Chuyên viên nhập liệu/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/lãnh đạo nhập điều kiện tìm kiếm lĩnh vực hợp tác và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách lĩnh vực hợp tác theo các tiêu chí đã nhập.   Chuyên viên nhập liệu/lãnh đạo thực hiện xuất file danh sách lĩnh vực hợp tác. Hệ thống thực hiện xuất dữ liệu danh sách lĩnh vực hợp tác theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý danh mục lĩnh vực hợp tác trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-52: Quản lý danh mục hình thức hợp tác
- **Actor**: Chuyên viên nhập liệu/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/lãnh đạo nhập điều kiện tìm kiếm hình thức hợp tác và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách hình thức hợp tác theo các tiêu chí đã nhập.   Chuyên viên nhập liệu/lãnh đạo thực hiện xuất file danh sách hình thức hợp tác. Hệ thống thực hiện xuất dữ liệu danh sách hình thức hợp tác theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý danh mục hình thức hợp tác trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-53: Quản lý danh mục loại nguồn vốn
- **Actor**: Chuyên viên nhập liệu/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/lãnh đạo nhập điều kiện tìm kiếm loại nguồn vốn và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách loại nguồn vốn theo các tiêu chí đã nhập.   Chuyên viên nhập liệu/lãnh đạo thực hiện xuất file danh sách loại nguồn vốn. Hệ thống thực hiện xuất dữ liệu danh sách loại nguồn vốn theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý danh mục loại nguồn vốn trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-54: Quản lý danh mục hình thức khen thưởng
- **Actor**: Chuyên viên nhập liệu/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/lãnh đạo nhập điều kiện tìm kiếm hình thức khen thưởng và chọn tìm kiếm. Hệ thống hiển thị kết quả danh sách hình thức khen thưởng theo các tiêu chí đã nhập.   Chuyên viên nhập liệu/lãnh đạo thực hiện xuất file danh sách hình thức khen thưởng. Hệ thống thực hiện xuất dữ liệu danh sách hình thức khen thưởng theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Quản lý danh mục hình thức khen thưởng trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-55: Báo cáo về danh mục điều ước quốc tế, thỏa thuận quốc tế
- **Actor**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn chức năng báo cáo về danh mục điều ước quốc tế, thỏa thuận quốc tế trên hệ thống. Hệ thống hiển thị màn hình chức năng báo cáo.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện thống kê báo cáo danh mục điều ước quốc tế, thỏa thuận quốc tế và chọn thống kê. Hệ thống hiển thị kết quả báo cáo theo các tiêu chí đã nhập   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem trước báo cáo danh mục điều ước quốc tế, thỏa thuận quốc tế. Hệ thống hiển thị chi tiết báo cáo trước khi xuất.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file báo cáo danh mục điều ước quốc tế, thỏa thuận quốc tế. Hệ thống thực hiện xuất dữ liệu báo cáo theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Báo cáo về danh mục điều ước quốc tế, thỏa thuận quốc tế trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-56: Báo cáo chương trình dự án
- **Actor**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn chức năng báo cáo chương trình dự án trên hệ thống. Hệ thống hiển thị màn hình chức năng báo cáo.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện thống kê báo cáo chương trình dự án và chọn thống kê. Hệ thống hiển thị kết quả báo cáo chương trình dự án theo các tiêu chí đã nhập.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem báo cáo chương trình dự án. Hệ thống hiển thị chi tiết báo cáo chương trình dự án.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file báo cáo chương trình dự án. Hệ thống thực hiện xuất dữ liệu báo cáo tiến độ thực hiện dự án theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Báo cáo chương trình dự án trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-57: Báo cáo tiến độ chương trình dự án
- **Actor**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn chức năng báo cáo tiến độ chương trình dự án trên hệ thống. Hệ thống hiển thị màn hình chức năng báo cáo.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện thống kê tiến độ chương trình dự án và chọn thống kê. Hệ thống hiển thị kết quả báo cáo theo các tiêu chí đã nhập.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem trước báo cáo tiến độ chương trình dự án. Hệ thống hiển thị chi tiết báo cáo trước khi xuất.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file báo cáo tiến độ chương trình dự án. Hệ thống thực hiện xuất dữ liệu báo cáo theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Báo cáo tiến độ chương trình dự án trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-58: Báo cáo thông tin đoàn ra
- **Actor**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn chức năng báo cáo thông tin đoàn ra trên hệ thống. Hệ thống hiển thị màn hình chức năng báo cáo.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện thống kê báo cáo thông tin đoàn ra và chọn thống kê. Hệ thống hiển thị kết quả báo cáo thông tin đoàn ra theo các tiêu chí đã nhập.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem báo cáo thông tin đoàn ra. Hệ thống hiển thị chi tiết báo cáo thông tin đoàn ra.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file báo cáo thông tin đoàn ra. Hệ thống thực hiện xuất dữ liệu báo cáo thông tin đoàn ra theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Báo cáo thông tin đoàn ra trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-59: Báo cáo thông tin đoàn vào
- **Actor**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn chức năng báo cáo thông tin đoàn vào trên hệ thống. Hệ thống hiển thị màn hình chức năng báo cáo.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện thống kê báo cáo thông tin đoàn vào và chọn thống kê. Hệ thống hiển thị kết quả báo cáo thông tin đoàn vào theo các tiêu chí đã nhập.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem trước báo cáo thông tin đoàn vào. Hệ thống hiển thị chi tiết báo cáo thông tin đoàn vào.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file báo cáo thông tin đoàn vào. Hệ thống thực hiện xuất dữ liệu báo cáo thông tin đoàn vào theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Báo cáo thông tin đoàn vào trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-60: Báo cáo nhân sự đi nước ngoài và chủ trì/tham gia các hoạt động đối ngoại trực tuyến
- **Actor**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn chức năng báo cáo nhân sự đi nước ngoài trên hệ thống. Hệ thống hiển thị màn hình chức năng báo cáo.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện thống kê báo cáo nhân sự đi nước ngoài và chọn thống kê. Hệ thống hiển thị kết quả báo cáo nhân sự đi nước ngoài theo các tiêu chí đã nhập.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem trước báo cáo nhân sự đi nước ngoài. Hệ thống hiển thị chi tiết báo cáo nhân sự đi nước ngoài.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file báo cáo nhân sự đi nước ngoài. Hệ thống thực hiện xuất dữ liệu báo cáo nhân sự đi nước ngoài theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Báo cáo nhân sự đi nước ngoài và chủ trì/tham gia các hoạt động đối ngoại trực tuyến trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-61: Báo cáo thống kê hội thảo
- **Actor**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn chức năng báo cáo thống kê hội thảo trên hệ thống. Hệ thống hiển thị màn hình chức năng báo cáo.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện thống kê báo cáo thống kê hội thảo và chọn thống kê. Hệ thống hiển thị kết quả thống kê hội thảo theo các tiêu chí đã nhập.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem trước báo cáo thống kê hội thảo. Hệ thống hiển thị chi tiết báo cáo trước khi xuất.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file báo cáo thống kê hội thảo. Hệ thống thực hiện xuất dữ liệu báo cáo thống kê hội thảo theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Báo cáo thống kê hội thảo trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-62: Báo cáo thống kê khen thưởng
- **Actor**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn chức năng báo cáo thống kê khen thưởng trên hệ thống. Hệ thống hiển thị màn hình chức năng báo cáo.   Công dân, tổ chức ngoài/chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện thống kê báo cáo thống kê khen thưởng và chọn thống kê. Hệ thống hiển thị kết quả thống kê khen thưởng theo các tiêu chí đã nhập.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem trước báo cáo thống kê khen thưởng. Hệ thống hiển thị chi tiết báo cáo trước khi xuất.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file báo cáo thống kê khen thưởng. Hệ thống thực hiện xuất dữ liệu báo cáo thống kê khen thưởng theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Báo cáo thống kê khen thưởng trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-63: Báo cáo thống kê chuyên gia
- **Actor**: Chuyên viên nhập liệu/chuyên viên khai thác/lãnh đạo
- **Mô tả ngắn**: Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn chức năng báo cáo thống kê chuyên gia trên hệ thống. Hệ thống hiển thị màn hình chức năng báo cáo.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo nhập điều kiện thống kê báo cáo chuyên gia và chọn thống kê. Hệ thống hiển thị kết quả báo cáo theo các tiêu chí đã nhập.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo chọn xem trước báo cáo chuyên gia. Hệ thống hiển thị chi tiết báo cáo trước khi xuất.   Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo thực hiện xuất file báo cáo chuyên gia. Hệ thống thực hiện xuất dữ liệu báo cáo theo định dạng được chọn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Báo cáo thống kê chuyên gia trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-64: Nhận dữ liệu tài liệu theo đơn vị
- **Actor**: Hệ thống quản lý văn bản và điều hành
- **Mô tả ngắn**: Hệ thống QLVBĐH của Bộ gửi kết quả kiểm tra yêu cầu kết nối để đồng bộ thông tin tài liệu theo đơn vị thông qua nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin tài liệu theo đơn vị thông qua nền tảng LGSP.   Hệ thống QLVBĐH của Bộ gửi dữ liệu tài liệu theo đơn vị tới hệ thống thông qua nền tảng LGSP; Hệ thống nhận thông tin dữ liệu đồng bộ thông quan nền tảng LGSP và lưu vào CSDL   Hệ thống QLVBĐH của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ dữ liệu tài liệu theo đơn vị
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Nhận dữ liệu tài liệu theo đơn vị trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-65: Nhận dữ liệu tài liệu theo nhiệm vụ
- **Actor**: Hệ thống quản lý văn bản và điều hành
- **Mô tả ngắn**: Hệ thống QLVBĐH của Bộ gửi kết quả kiểm tra yêu cầu kết nối để đồng bộ thông tin tài liệu theo nhiệm vụ thông qua nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin tài liệu theo nhiệm vụ thông qua nền tảng LGSP.   Hệ thống QLVBĐH của Bộ gửi dữ liệu tài liệu theo nhiệm vụ tới hệ thống thông qua nền tảng LGSP; Hệ thống nhận thông tin dữ liệu đồng bộ thông quan nền tảng LGSP và lưu vào CSDL.   Hệ thống QLVBĐH của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ dữ liệu tài liệu theo nhiệm vụ
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Nhận dữ liệu tài liệu theo nhiệm vụ trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-66: Tra cứu dữ liệu văn bản hợp tác quốc tế về pháp luật
- **Actor**: Hệ thống CSDL pháp luật quốc gia
- **Mô tả ngắn**: Hệ thống CSDL pháp luật quốc gia của nhận yêu cầu tra cứu dữ liệu văn bản hợp tác quốc tế về pháp luật thông qua nền tảng LGSP và trả về kết quả yêu cầu kết nối. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối tra cứu thông tin văn bản hợp tác quốc tế về pháp luật thông qua nền tảng LGSP.   Hệ thống CSDL pháp luật quốc gia của Bộ gửi kết quả tra cứu văn bản hợp tác quốc tế về pháp luật tới hệ thống thông qua nền tảng LGSP; Hệ thống nhận thông tin dữ liệu thông quan nền tảng LGSP và lưu vào CSDL   Hệ thống CSDL pháp luật quốc gia của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ dữ liệu văn bản hợp tác quốc tế về pháp luật
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Tra cứu dữ liệu văn bản hợp tác quốc tế về pháp luật trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-67: Tích hợp đăng nhập nền tảng định danh và xác thực điện tử
- **Actor**: Nền tảng định danh và xác thực điện tử
- **Mô tả ngắn**: Chuyên viên nhập liệu/chuyên viên khai thác/Lãnh đạo truy cập vào hệ thống. Hệ thống gửi yêu cầu xác thực đăng nhập đến Nền tảng định danh và xác thực điện tử.   Nền tảng định danh và xác thực điện tử phản hồi kết quả xác thực, nếu người dùng đã có phiên đăng nhập hợp lệ, hệ thống cho phép người dùng truy cập hệ thống;nếu người dùng chưa đăng nhập hoặc phiên đăng nhập đã hết hiệu lực, hệ thống chuyển hướng người dùng đến màn hình đăng nhập của Nền tảng định danh và xác thực điện tử để thực hiện đăng nhập và xác thực tài khoản.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Tích hợp đăng nhập nền tảng định danh và xác thực điện tử trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-68: Đồng bộ thông tin người dùng
- **Actor**: Nền tảng định danh và xác thực điện tử
- **Mô tả ngắn**: Nền tảng định danh và xác thực điện tử gửi kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin người dùng thông qua Nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin người dùng thông qua nền tảng LGSP.   Nền tảng định danh và xác thực điện tử gửi thông tin người dùng cần đồng bộ đến Hệ thống thông qua Nền tảng LGSP. Hệ thống nhận thông tin người dùng thông qua nền tảng LGSP và lưu vào CSDL.   Nền tảng định danh và xác thực điện tử thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ thông tin người dùng
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Đồng bộ thông tin người dùng trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-69: Chia sẻ thông tin dashboard sang hệ thống khác
- **Actor**: Hệ thống khác
- **Mô tả ngắn**: Hệ thống khác gửi yêu cầu kết nối tới hệ thống CSDLHTQT để chia sẻ thông tin dữ liệu dashboard thông qua nền tảng LGSP. Hệ thống xác thực yêu cầu, nếu hợp lệ thì cho phép kết nối, nếu không hợp lệ thì thông báo lại cho Hệ thống khác thông qua Nền tảng LGSP   Hệ thống khác nhận thông tin dashboard chia sẻ từ hệ thống thông qua Nền tảng LGSP; Hệ thống ghi nhận trạng thái chia sẻ và cập nhật vào nhật ký.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Chia sẻ thông tin dashboard sang hệ thống khác trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-70: Nhận dữ liệu danh mục đối tác nước ngoài
- **Actor**: Hệ thống kho dữ liệu dùng chung
- **Mô tả ngắn**: Hệ thống kho dữ liệu dùng chung của Bộ gửi kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin danh mục đối tác nước ngoài thông qua Nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin danh mục đối tác nước ngoài thông qua nền tảng LGSP.   Hệ thống kho dữ liệu dùng chung gửi thông tin danh mục đối tác nước ngoài cần đồng bộ đến Hệ thống CSDL HTQT thông qua Nền tảng LGSP. Hệ thống CSDL HTQT nhận thông tin danh mục đối tác nước ngoài thông qua nền tảng LGSP và lưu vào CSDL.   Hệ thống kho dữ liệu dùng chung của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ danh mục đối tác nước ngoài.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Nhận dữ liệu danh mục đối tác nước ngoài trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-71: Nhận dữ liệu danh mục quốc gia
- **Actor**: Hệ thống kho dữ liệu dùng chung
- **Mô tả ngắn**: Hệ thống kho dữ liệu dùng chung của Bộ gửi kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin danh mục quốc gia thông qua Nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ danh mục quốc gia thông qua nền tảng LGSP.   Hệ thống kho dữ liệu dùng chung gửi thông tin danh mục quốc gia cần đồng bộ đến Hệ thống CSDL HTQT thông qua Nền tảng LGSP. Hệ thống CSDL HTQT nhận thông tin danh mục quốc gia thông qua nền tảng LGSP và lưu vào CSDL.   Hệ thống kho dữ liệu dùng chung của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ danh mục quốc gia.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Nhận dữ liệu danh mục quốc gia trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-72: Nhận dữ liệu danh mục cơ quan tổ chức trong nước
- **Actor**: Hệ thống kho dữ liệu dùng chung
- **Mô tả ngắn**: Hệ thống kho dữ liệu dùng chung của Bộ gửi kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin danh mục cơ quan tổ chức trong nước thông qua Nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ danh mục cơ quan tổ chức trong nước thông qua nền tảng LGSP.   Hệ thống kho dữ liệu dùng chung gửi thông tin danh mục cơ quan tổ chức trong nước cần đồng bộ đến Hệ thống CSDL HTQT thông qua Nền tảng LGSP. Hệ thống CSDL HTQT nhận thông tin danh mục cơ quan tổ chức trong nước thông qua nền tảng LGSP và lưu vào CSDL.   Hệ thống kho dữ liệu dùng chung của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ danh mục cơ quan tổ chức trong nước.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Nhận dữ liệu danh mục cơ quan tổ chức trong nước trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-73: Nhận dữ liệu danh mục ngôn ngữ
- **Actor**: Hệ thống kho dữ liệu dùng chung
- **Mô tả ngắn**: Hệ thống kho dữ liệu dùng chung của Bộ gửi kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin danh mục ngôn ngữ thông qua Nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ danh mục ngôn ngữ thông qua nền tảng LGSP.   Hệ thống kho dữ liệu dùng chung gửi thông tin danh mục ngôn ngữ cần đồng bộ đến Hệ thống CSDL HTQT thông qua Nền tảng LGSP. Hệ thống CSDL HTQT nhận thông tin danh mục ngôn ngữ thông qua nền tảng LGSP và lưu vào CSDL.   Hệ thống kho dữ liệu dùng chung của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ danh mục ngôn ngữ.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Nhận dữ liệu danh mục ngôn ngữ trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-74: Nhận dữ liệu danh mục loại văn bản
- **Actor**: Hệ thống kho dữ liệu dùng chung
- **Mô tả ngắn**: Hệ thống kho dữ liệu dùng chung của Bộ gửi kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin danh mụcloại văn bản thông qua Nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ danh mục loại văn bản thông qua nền tảng LGSP.   Hệ thống kho dữ liệu dùng chung gửi thông tin danh mục loại văn bản cần đồng bộ đến Hệ thống CSDL HTQT thông qua Nền tảng LGSP. Hệ thống CSDL HTQT nhận thông tin danh mục loại văn bản thông qua nền tảng LGSP và lưu vào CSDL.   Hệ thống kho dữ liệu dùng chung của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ danh mục loại văn bản.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Nhận dữ liệu danh mục loại văn bản trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-75: Nhận dữ liệu danh mục lĩnh vực hợp tác
- **Actor**: Hệ thống kho dữ liệu dùng chung
- **Mô tả ngắn**: Hệ thống kho dữ liệu dùng chung của Bộ gửi kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin danh mục lĩnh vực hợp tác thông qua Nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ danh mục lĩnh vực hợp tác thông qua nền tảng LGSP.   Hệ thống kho dữ liệu dùng chung gửi thông tin danh mục lĩnh vực hợp tác cần đồng bộ đến Hệ thống CSDL HTQT thông qua Nền tảng LGSP. Hệ thống CSDL HTQT nhận thông tin danh mục lĩnh vực hợp tác thông qua nền tảng LGSP và lưu vào CSDL.   Hệ thống kho dữ liệu dùng chung của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ danh mục lĩnh vực hợp tác.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Nhận dữ liệu danh mục lĩnh vực hợp tác trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-76: Nhận dữ liệu danh mục hình thức hợp tác
- **Actor**: Hệ thống kho dữ liệu dùng chung
- **Mô tả ngắn**: Hệ thống kho dữ liệu dùng chung của Bộ gửi kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin danh mục hình thức hợp tác thông qua Nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ danh mục hình thức hợp tác thông qua nền tảng LGSP.   Hệ thống kho dữ liệu dùng chung gửi thông tin danh mục hình thức hợp tác cần đồng bộ đến Hệ thống CSDL HTQT thông qua Nền tảng LGSP. Hệ thống CSDL HTQT nhận thông tin danh mục hình thức hợp tác thông qua nền tảng LGSP và lưu vào CSDL.   Hệ thống kho dữ liệu dùng chung của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ danh mục hình thức hợp tác.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Nhận dữ liệu danh mục hình thức hợp tác trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-77: Nhận dữ liệu danh mục loại nguồn vốn
- **Actor**: Hệ thống kho dữ liệu dùng chung
- **Mô tả ngắn**: Hệ thống kho dữ liệu dùng chung của Bộ gửi kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin danh mục loại nguồn vốn thông qua Nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ danh mục loại nguồn vốn thông qua nền tảng LGSP.   Hệ thống kho dữ liệu dùng chung gửi thông tin danh mục loại nguồn vốn cần đồng bộ đến Hệ thống CSDL HTQT thông qua Nền tảng LGSP. Hệ thống CSDL HTQT nhận thông tin danh mục loại nguồn vốn thông qua nền tảng LGSP và lưu vào CSDL.   Hệ thống kho dữ liệu dùng chung của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ danh mục loại nguồn vốn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Nhận dữ liệu danh mục loại nguồn vốn trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-78: Nhận dữ liệu danh mục lĩnh vực chuyên môn
- **Actor**: Hệ thống kho dữ liệu dùng chung
- **Mô tả ngắn**: Hệ thống kho dữ liệu dùng chung của Bộ gửi kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin danh mục lĩnh vực chuyên môn thông qua Nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ danh mục lĩnh vực chuyên môn thông qua nền tảng LGSP.   Hệ thống kho dữ liệu dùng chung gửi thông tin danh mục lĩnh vực chuyên môn cần đồng bộ đến Hệ thống CSDL HTQT thông qua Nền tảng LGSP. Hệ thống CSDL HTQT nhận thông tin danh mục lĩnh vực chuyên môn thông qua nền tảng LGSP và lưu vào CSDL.   Hệ thống kho dữ liệu dùng chung của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ danh mục lĩnh vực chuyên môn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Nhận dữ liệu danh mục lĩnh vực chuyên môn trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-79: Nhận dữ liệu danh mục hình thức khen thưởng
- **Actor**: Hệ thống kho dữ liệu dùng chung
- **Mô tả ngắn**: Hệ thống kho dữ liệu dùng chung của Bộ gửi kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin danh mục hình thức khen thưởng thông qua Nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ danh mục hình thức khen thưởng thông qua nền tảng LGSP.   Hệ thống kho dữ liệu dùng chung gửi thông tin danh mục hình thức khen thưởng cần đồng bộ đến Hệ thống CSDL HTQT thông qua Nền tảng LGSP. Hệ thống CSDL HTQT nhận thông tin danh mục hình thức khen thưởng thông qua nền tảng LGSP và lưu vào CSDL.   Hệ thống kho dữ liệu dùng chung của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ danh mục hình thức khen thưởng.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Nhận dữ liệu danh mục hình thức khen thưởng trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-80: Nhận dữ liệu danh mục phân loại đoàn
- **Actor**: Hệ thống kho dữ liệu dùng chung
- **Mô tả ngắn**: Hệ thống kho dữ liệu dùng chung của Bộ gửi kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin danh mục phân loại đoàn thông qua Nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ danh mục phân loại đoàn thông qua nền tảng LGSP.   Hệ thống kho dữ liệu dùng chung gửi thông tin danh mục phân loại đoàn cần đồng bộ đến Hệ thống CSDL HTQT thông qua Nền tảng LGSP. Hệ thống CSDL HTQT nhận thông tin danh mục phân loại đoàn thông qua nền tảng LGSP và lưu vào CSDL.   Hệ thống kho dữ liệu dùng chung của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ danh mục phân loại đoàn.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Nhận dữ liệu danh mục phân loại đoàn trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-81: Nhận dữ liệu danh mục nguồn kinh phí
- **Actor**: Hệ thống kho dữ liệu dùng chung
- **Mô tả ngắn**: Hệ thống kho dữ liệu dùng chung của Bộ gửi kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin danh mục nguồn kinh phí thông qua Nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ danh mục nguồn kinh phí thông qua nền tảng LGSP.   Hệ thống kho dữ liệu dùng chung gửi thông tin danh mục nguồn kinh phí cần đồng bộ đến Hệ thống CSDL HTQT thông qua Nền tảng LGSP. Hệ thống CSDL HTQT nhận thông tin danh mục nguồn kinh phí thông qua nền tảng LGSP và lưu vào CSDL.   Hệ thống kho dữ liệu dùng chung của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ danh mục nguồn kinh phí.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Nhận dữ liệu danh mục nguồn kinh phí trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-82: Nhận dữ liệu danh mục danh nghĩa ký
- **Actor**: Hệ thống kho dữ liệu dùng chung
- **Mô tả ngắn**: Hệ thống kho dữ liệu dùng chung của Bộ gửi kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin danh mục danh nghĩa ký thông qua Nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ danh mục danh nghĩa ký thông qua nền tảng LGSP.   Hệ thống kho dữ liệu dùng chung gửi thông tin danh mục danh nghĩa ký cần đồng bộ đến Hệ thống CSDL HTQT thông qua Nền tảng LGSP. Hệ thống CSDL HTQT nhận thông tin danh mục danh nghĩa ký thông qua nền tảng LGSP và lưu vào CSDL.   Hệ thống kho dữ liệu dùng chung của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ danh mục danh nghĩa ký.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Nhận dữ liệu danh mục danh nghĩa ký trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-83: Đồng bộ thông tin đơn vị
- **Actor**: Hệ thống kho dữ liệu dùng chung
- **Mô tả ngắn**: Hệ thống kho dữ liệu dùng chung của Bộ gửi kết quả kiểm tra yêu cầu kết nối đồng bộ thông tin đơn vị thông qua Nền tảng LGSP. Hệ thống nhận kết quả kiểm tra yêu cầu kết nối đồng bộ đơn vị thông qua nền tảng LGSP.   Hệ thống kho dữ liệu dùng chung gửi thông tin đơn vị cần đồng bộ đến Hệ thống CSDL HTQT thông qua Nền tảng LGSP. Hệ thống CSDL HTQT nhận thông tin đơn vị thông qua nền tảng LGSP và lưu vào CSDL.   Hệ thống kho dữ liệu dùng chung của Bộ thực hiện ngắt kết nối tới hệ thống CSDLHTQT thông qua nền tảng LGSP. Hệ thống ngắt kết nối và thực hiện lưu nhật ký đồng bộ thông tin đơn vị.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Đồng bộ thông tin đơn vị trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-84: Chia sẻ thông tin điều ước quốc tế, thỏa thuận quốc tế
- **Actor**: Nền tảng kết nối chia sẻ của Bộ Tư pháp (LGSP)
- **Mô tả ngắn**: Nền tảng LGSP gửi yêu cầu kết nối tới hệ thống CSDLHTQT để lấy thông tin điều ước quốc tế, thỏa thuận quốc tế. Hệ thống xác thực yêu cầu, nếu hợp lệ thì cho phép kết nối, nếu không hợp lệ thì thông báo lại cho Nền tảng LGSP   Nền tảng LGSP nhận thông tin chia sẻ điều ước quốc tế, thỏa thuận quốc tế từ hệ thống; Hệ thống ghi nhận trạng thái chia sẻ và cập nhật vào nhật ký.
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Chia sẻ thông tin điều ước quốc tế, thỏa thuận quốc tế trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-85: Chia sẻ thông tin chương trình dự án
- **Actor**: Nền tảng kết nối chia sẻ của Bộ Tư pháp (LGSP)
- **Mô tả ngắn**: Nền tảng LGSP gửi yêu cầu kết nối tới hệ thống để lấy thông tin chương trình dự án. Hệ thống xác thực yêu cầu, nếu hợp lệ thì cho phép kết nối, nếu không hợp lệ thì thông báo lại cho Nền tảng LGSP   Nền tảng LGSP thực hiện tiếp nhận dữ liệu chia sẻ chương trình dự án từ hệ thống và phản hồi kết quả tiếp nhận cho hệ thống. Hệ thống ghi nhận trạng thái chia sẻ và cập nhật vào nhật ký
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Chia sẻ thông tin chương trình dự án trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-86: Chia sẻ danh sách chuyên gia
- **Actor**: Nền tảng kết nối chia sẻ của Bộ Tư pháp (LGSP)
- **Mô tả ngắn**: Nền tảng LGSP gửi yêu cầu kết nối tới hệ thống để lấy thông tin danh sách chuyên gia. Hệ thống xác thực yêu cầu, nếu hợp lệ thì cho phép kết nối, nếu không hợp lệ thì thông báo lại cho Nền tảng LGSP   Nền tảng LGSP thực hiện tiếp nhận dữ liệu chia sẻ danh sách chuyên gia từ hệ thống và phản hồi kết quả tiếp nhận cho hệ thống. Hệ thống ghi nhận trạng thái chia sẻ và cập nhật vào nhật ký
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Chia sẻ danh sách chuyên gia trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-87: Chia sẻ thông tin hội nghị hội thảo
- **Actor**: Nền tảng kết nối chia sẻ của Bộ Tư pháp (LGSP)
- **Mô tả ngắn**: Nền tảng LGSP gửi yêu cầu kết nối tới hệ thống để lấy thông tin hội nghị hội thảo. Hệ thống xác thực yêu cầu, nếu hợp lệ thì cho phép kết nối, nếu không hợp lệ thì thông báo lại cho Nền tảng LGSP   Nền tảng LGSP thực hiện tiếp nhận dữ liệu chia sẻ danh sách hội nghị hội thảo từ hệ thống và phản hồi kết quả tiếp nhận cho hệ thống. Hệ thống ghi nhận trạng thái chia sẻ và cập nhật vào nhật ký
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Chia sẻ thông tin hội nghị hội thảo trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-88: Chia sẻ Báo cáo kinh nghiệm quốc tế (ngoài chương trình dự án)
- **Actor**: Nền tảng kết nối chia sẻ của Bộ Tư pháp (LGSP)
- **Mô tả ngắn**: Nền tảng LGSP gửi yêu cầu kết nối tới hệ thống để lấy thông tin Báo cáo kinh nghiệm quốc tế (ngoài chương trình dự án). Hệ thống xác thực yêu cầu, nếu hợp lệ thì cho phép kết nối, nếu không hợp lệ thì thông báo lại cho Nền tảng LGSP   Nền tảng LGSP thực hiện tiếp nhận dữ liệu chia sẻ Báo cáo kinh nghiệm quốc tế (ngoài chương trình dự án), truyền thông từ hệ thống và phản hồi kết quả tiếp nhận cho hệ thống. Hệ thống ghi nhận trạng thái chia sẻ và cập nhật vào nhật ký
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Chia sẻ Báo cáo kinh nghiệm quốc tế (ngoài chương trình dự án) trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

## UC-FR-UC-89: Chia sẻ thông tin đoàn
- **Actor**: Nền tảng kết nối chia sẻ của Bộ Tư pháp (LGSP)
- **Mô tả ngắn**: Nền tảng LGSP gửi yêu cầu kết nối tới hệ thống để lấy thông tin đoàn. Hệ thống xác thực yêu cầu, nếu hợp lệ thì cho phép kết nối, nếu không hợp lệ thì thông báo lại cho Nền tảng LGSP   Nền tảng LGSP thực hiện tiếp nhận dữ liệu chia sẻ thông tin đoàn từ hệ thống và phản hồi kết quả tiếp nhận cho hệ thống. Hệ thống ghi nhận trạng thái chia sẻ và cập nhật vào nhật ký
- **Điều kiện trước**: Actor đã đăng nhập thành công và có quyền tương ứng trên hệ thống.
- **Main Flow**:
  1. Actor gửi yêu cầu thao tác Chia sẻ thông tin đoàn trên giao diện.
  2. Hệ thống kiểm tra tính hợp lệ của dữ liệu đầu vào.
  3. Hệ thống lưu/truy vấn dữ liệu từ CSDL và phản hồi kết quả cho Actor.
- **Exception Flow**:
  - 2a: Dữ liệu không hợp lệ -> Hệ thống hiển thị thông báo lỗi cụ thể và giữ nguyên form.

