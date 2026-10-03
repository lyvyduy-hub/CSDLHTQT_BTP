# Từ Điển Dữ Liệu (Data Dictionary)

## Bảng: RESOURCES (15 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | resource_id | number(10,0) |  |  | ID tài nguyên |
| 2 | resource_code | varchar(255) |  | x | Mã tài nguyên |
| 3 | resource_name | varchar(255) |  | x | Tên tài nguyên |
| 4 | resource_url | varchar(255) |  | x | Đường dẫn |
| 5 | resource_order | number(5,0) |  | x | Thứ tự sắp xếp |
| 6 | application_id | number(10,0) |  | x | ID ứng dụng |
| 7 | description | varchar(500) |  | x | Mô tả |
| 8 | is_lock | number(1,0) |  | x | Trạng thái hoạt động
1: Khóa
0: Không khóa |
| 9 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 10 | org_id | number(10,0) |  | x | ID đơn vị tạo dữ liệu |
| 11 | manage_department | number(10,0) |  | x | ID đơn vị quản lý dữ liệu |
| 12 | created_by | varchar(255) |  | x | Người tạo bản ghi |
| 13 | created_date | datetime |  | x | Ngày tạo |
| 14 | modified_by | varchar(255) |  | x | Người chỉnh sửa |
| 15 | modified_date | datetime |  | x | Ngày sửa |

## Bảng: MENU_CONFIG (28 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | menu_config_id | number(10,0) |  |  | ID menu |
| 2 | menu_code | varchar(255) |  | x | Mã menu |
| 3 | menu_name | varchar(255) |  | x | Tên menu |
| 4 | url | varchar(255) |  | x | Đường dẫn |
| 5 | menu_order | number(5,0) |  | x | Thứ tự sắp xếp |
| 6 | application_id | number(10,0) |  | x | ID ứng dụng |
| 7 | parent_id | number(10,0) |  | x | ID menu cha |
| 8 | policy_type | number(1,0) |  | x | Loại chính sách:
1: Chính sách theo người dùng
2: Chính sách theo vai trò
3: Chính sách theo đơn vị
4: Chính sách tổng hợp |
| 9 | description | varchar(500) |  | x | Mô tả |
| 10 | icon_menu | varchar(255) |  | x | Icon menu |
| 11 | visible | number(1,0) |  |  | Hiển thị Menu:
0: Không hiển thị
1: Có hiển thị |
| 12 | is_lock | number(1,0) |  | x | Trạng thái hoạt động
1: Khóa
0: Không khóa |
| 13 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 14 | org_id | number(10,0) |  | x | ID đơn vị tạo dữ liệu |
| 15 | manage_department | number(10,0) |  | x | ID đơn vị quản lý dữ liệu |
| 16 | created_by | varchar(255) |  | x | Người tạo bản ghi |
| 17 | created_date | datetime |  | x | Ngày tạo |
| 18 | modified_by | varchar(255) |  | x | Người chỉnh sửa |
| 19 | modified_date | datetime |  | x | Ngày sửa |
| 20 | menu_resource_id | number(10,0) |  |  | ID bảng tự tăng |
| 21 | resource_id | number(10,0) |  | x | ID tài nguyên |
| 22 | resource_name | varchar(255) |  | x | Tên tài nguyên |
| 23 | menu_id | number(10,0) |  | x | ID menu |
| 24 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 25 | created_by | varchar(255) |  | x | Người tạo bản ghi |
| 26 | created_date | datetime |  | x | Ngày tạo |
| 27 | modified_by | varchar(255) |  | x | Người chỉnh sửa |
| 28 | modified_date | datetime |  | x | Ngày sửa |

## Bảng: NOTIFICATION_CONFIG USER_NOTIFI (31 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | notification_id | number(10,0) |  |  | ID cấu hình thông báo |
| 2 | notification_title | varchar(500) |  |  | Tiêu đề thông báo |
| 3 | notification_content | varchar(2000) |  |  | Nội dung thông báo |
| 4 | send_type | varchar(255) |  |  | Hình thức gửi 
1 - Hệ thống
2 - email
3 - SMS |
| 5 | send_mode | number(1,0) |  |  | Chế độ gửi: 1 - Gửi ngay, 2 - Đặt lịch |
| 6 | scheduled_time | datetime |  | x | Thời gian gửi theo lịch (chỉ có data nếu send_mode = 2) |
| 7 | target_scope | number(1,0) |  | x | Phạm vi nhận: 1 - Toàn hệ thống, 2 - Tùy chọn |
| 8 | target_account_type | varchar(255) |  | x | Lưu chuỗi loại tài khoản được chọn |
| 9 | target_org_level | varchar(255) |  | x | Lưu chuỗi cấp bậc đơn vị được chọn |
| 10 | target_org_ids | varchar(2000) |  | x | Lưu chuỗi ID cơ quan/đơn vị được chọn (Cách nhau bởi dấu phẩy) |
| 11 | target_role_ids | varchar(2000) |  | x | Lưu chuỗi ID vai trò được chọn. |
| 12 | send_status | number(1,0) |  | x | Trạng thái gửi: 0 - Chờ gửi, 1 - Đã gửi, 2 - Lỗi |
| 13 | is_lock | number(1,0) |  | x | Trạng thái hoạt động (1: Khóa, 0: Không khóa) |
| 14 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 15 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 16 | created_date | datetime |  | x | Ngày tạo |
| 17 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 18 | modified_date | datetime |  | x | Ngày được chỉnh sửa |
| 19 | org_id | number(10,0) |  | x | ID đơn vị tạo dữ liệu |
| 20 | manage_department | number(10,0) |  | x | ID đơn vị quản lý dữ liệu |
| 21 | user_notification_id | number(10,0) |  |  | ID bản ghi trạng thái thông báo. |
| 22 | notification_id | number(10,0) |  | x | ID cấu hình thông báo gốc. Tham chiếu tới khóa chính của bảng NOTIFICATION_CONFIG |
| 23 | sys_user_id | number(10,0) |  | x | ID người nhận thông báo. Tham chiếu tới khóa chính của bảng SYS_USER |
| 24 | is_read | number(1,0) |  | x | Trạng thái đọc thông báo của người dùng: 
- 0: Chưa đọc 
- 1: Đã đọc |
| 25 | read_date | datetime |  | x | Thời gian người dùng click xem chi tiết/đánh dấu đã đọc. |
| 26 | is_deleted_by_user | number(1,0) |  | x | Trạng thái người dùng xóa thông báo khỏi danh sách hiển thị của riêng họ: 
- 0: Chưa xóa 
- 1: Đã xóa |
| 27 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 28 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 29 | created_date | datetime |  | x | Ngày tạo |
| 30 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 31 | modified_date | datetime |  | x | Ngày được chỉnh sửa |

## Bảng: STAGING_SYNC_DATA  (11 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | staging_id | Number(1,0) |  |  | ID bản ghi dữ liệu |
| 2 | destination_module_type | Number(1,0) |  | x | Lưu loại phân hệ đích sau khi di chuyển. 
1. INTERNATIONAL_AGREEMENT
2. EXPERT
3. EMULATION_COMMENDATION
4. DELEGATION
5. DOCUMENT
6. CONFERENCE
7. PROJECT_PROGRAM 
8. EXPERIENCE_REPORT
9. ANNUAL_PLAN
10. ACTIVITY_RESULT
11. LEGAL_SCHEME
12. COOPERATION_REPORT
13. OTHER_ACTIVITY" |
| 3 | destination_object_id | Number(10,0) |  | x | Lưu ID khóa chính của bản ghi vừa được tạo ra sau khi người dùng di chuyển dữ liệu và bấm [Lưu]
(VD: di chuyển sang Đoàn ra, sau khi thực hiện thêm mới đoàn ra thì sẽ lưu ID của Đoàn ra này) |
| 4 | source_system | Varchar(255) |  |  | Tên hệ thống nguồn đẩy dữ liệu sang (VD: VNeID, SSO, LGSP...). |
| 5 | sync_status | Number(1,0) |  |  | Trạng thái phân loại: 
- 0: Chưa phân loại
- 1: Đã phân loại (Đã map sang form thêm mới thành công) |
| 6 | receive_time | Datetime |  |  | Thời gian hệ thống nhận được dữ liệu. Dùng để hiển thị lên lưới và sắp xếp (Mới nhất lên đầu). |
| 7 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 8 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 9 | created_date | datetime |  | x | Ngày tạo |
| 10 | modified_by | varchar (255) |  | x | Lưu ID của tài khoản người dùng cuối cùng thao tác bấm "Di chuyển vào danh mục" hoặc xóa |
| 11 | modified_date | datetime |  | x | Ngày được chỉnh sửa |

## Bảng: ACTION_HISTORY (6 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | action_history_id | number(10,0) |  |  | ID bản ghi lịch sử tác động |
| 2 | sys_user_id | number(10,0) |  | x | ID tài khoản thực hiện thao tác. Tham chiếu tới bảng SYS_USER |
| 3 | module_name | varchar(255) |  | x | Tên phân hệ |
| 4 | action_type | varchar(255) |  | x | Loại thao tác |
| 5 | description | varchar(2000) |  | x | Mô tả chi tiết nội dung thao tác 
Công thức chung sinh log: Hệ thống sẽ tự động bắt các tham số để ghép thành chuỗi mô tả theo cấu trúc sau:
[Loại hành động] + [Loại đối tượng chi tiết] + : <Tên định danh của đối tượng> |
| 6 | action_date | datetime |  | x | Ngày giờ phát sinh thao tác |

## Bảng: SYSTEM_ERROR_LOG (7 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | error_log_id | number(10,0) |  |  | ID bản ghi lỗi |
| 2 | error_code | varchar(255) |  | x | Mã lỗi hiển thị cho người dùng |
| 3 | module_name | varchar(255) |  | x | Phân hệ xảy ra lỗi (VD: Quản lý đoàn ra, Điều ước quốc tế...) |
| 4 | action_name | varchar(255) |  | x | Hoạt động đang thực hiện khi có lỗi (VD: Lưu thông tin thêm mới) |
| 5 | error_message | varchar(2000) |  | x | Thông báo lỗi với người dùng |
| 6 | error_date | datetime |  |  | Thời gian hệ thống ghi nhận lỗi |
| 7 | sys_user_id | number(10,0) |  | x | ID tài khoản đang thao tác khi gặp lỗi (Tham chiếu bảng SYS_USER) |

## Bảng: LOG_POLICY (14 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | policy_id | number(10,0) |  |  | ID chính sách |
| 2 | policy_code | varchar(255) |  |  | Mã chính sách. |
| 3 | policy_name | varchar(255) |  |  | Tên chính sách |
| 4 | menu_id | number(10,0) |  |  | Phân hệ áp dụng.
 Tham chiếu đến trường MENU_CONFIG_ID của bảng MENU_CONFIG |
| 5 | action_type | varchar(2000) |  | x | Tài áp dụng
Nếu action_type CÓ giá trị (Ví dụ: "101, 102"): Chỉ bắt log đúng 2 hành động đó.
Nếu action_type IS NULL: Tự động hiểu là Bắt log TOÀN BỘ hành động thuộc menu_id đó. |
| 6 | retention_days | number(5,0) |  | x | Quy định ngày lưu giữ nhật ký |
| 7 | is_lock | number(1,0) |  | x | Trạng thái hoạt động: Khóa/Mở khóa chính sách (1: Khóa, 0: Không khóa/Đang hoạt động) |
| 8 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 9 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 10 | created_date | datetime |  | x | Ngày tạo |
| 11 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 12 | modified_date | datetime |  | x | Ngày được chỉnh sửa |
| 13 | org_id | number(10,0) |  | x | ID đơn vị tạo dữ liệu |
| 14 | manage_department | number(10,0) |  | x | ID đơn vị quản lý dữ liệu |

## Bảng: BACKUP_POLICYBACKUP_RESTORE_HIS (33 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | policy_id | number(10,0) |  |  | ID chính sách sao lưu |
| 2 | frequency_type | number(1,0) |  |  | Chu kỳ sao lưu:
1: Hàng ngày
2: Hàng tuần
3: Hàng tháng |
| 3 | backup_scope | number(1,0) |  |  | Phạm vi sao lưu:
1: Toàn bộ hệ thống
2: Tùy chọn phân hệ |
| 4 | retention_days | number(5,0) |  | x | Số ngày lưu trữ bản sao lưu |
| 5 | run_time | varchar(5) |  | x | Lưu giờ chạy tiến trình |
| 6 | run_day_of_week | number(1,0) |  | x | Lưu Thứ trong tuần 
2: thứ hai
3: thứ ba
4: thứ tư
5: thứ năm
6: thứ sáu
7: thứ bảy
8: chủ nhật |
| 7 | run_day_of_month | number(2,0) |  | x | Lưu Ngày trong tháng (Từ 1 đến 31). 
Nếu người dùng chọn 31, thì mặc định tiến trình chạy ngày 28-29 đối với tháng 2, ngày 30 với tháng không có 31 ngày |
| 8 | module_ids | varchar(2000) |  | x | Lưu chuỗi ID các phân hệ được chọn 
Nếu backup_scope = 2 (VD: "1,4,5"). 
Nếu backup_scope = 1 thì để Null. |
| 9 | is_running | number(1,0) |  | x | Trạng thái hoạt động :
1: Đang Bật
0: Đã Tắt |
| 10 | is_active | number(1,0) |  | x | Mặc định = 1. |
| 11 | created_by | varchar(255) |  | x | ID tài khoản người tạo cấu hình |
| 12 | created_date | datetime |  | x | Thời gian tạo |
| 13 | modified_by | varchar(255) |  | x | ID tài khoản người chỉnh sửa lần cuối |
| 14 | modified_date | datetime |  | x | Thời gian chỉnh sửa lần cuối |
| 15 | org_id | number(10,0) |  | x | ID đơn vị tạo dữ liệu |
| 16 | manage_department | number(10,0) |  | x | ID đơn vị quản lý dữ liệu |
| 17 | history_id | number(10,0) |  |  | ID bản ghi nhật ký (Khóa chính). |
| 18 | action_type | number(1,0) |  |  | Loại tiến trình: 
1-Tự động, 
2-Sao lưu ngay, 
3-Khôi phục. |
| 19 | backup_scope | number(1,0) |  | x | Phạm vi
1- toàn hệ thống
2 - phân hệ |
| 20 | module_names | varchar(2000) |  | x | Tên các phân hệ |
| 21 | file_name | varchar(255) |  | x | Tên tệp tin |
| 22 | file_path | varchar(1000) |  | x | Đường dẫn file |
| 23 | file_size | varchar(50) |  |  | Kích thước file |
| 24 | execution_status | number(1,0) |  | x | Trạng thái tiến trình:
0 - đang xử lý
1-Thành công
2-Lỗi |
| 25 | error_message | varchar(2000) |  | x | Mã lỗi khi execution_status = 2 |
| 26 | start_time | datetime |  | x | Thời gian kích hoạt tiến trình |
| 27 | end_time | datetime |  | x | Thời gian kết thúc tiến trình |
| 28 | created_by | varchar(255) |  | x | ID tài khoản người tạo cấu hình |
| 29 | created_date | datetime |  | x | Thời gian tạo |
| 30 | modified_by | varchar(255) |  | x | ID tài khoản người chỉnh sửa lần cuối |
| 31 | modified_date | datetime |  | x | Thời gian chỉnh sửa lần cuối |
| 32 | org_id | number(10,0) |  | x | ID đơn vị tạo dữ liệu |
| 33 | manage_department | number(10,0) |  | x | ID đơn vị quản lý dữ liệu |

## Bảng: ROLE (23 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | role_id | number(10,0) |  |  | ID vai trò |
| 2 | role_code | varchar (255) |  | x | Mã vai trò |
| 3 | role_name | varchar (255) |  | x | Tên vai trò |
| 4 | level | varchar(255) |  | x | Cấp vai trò
3 - Cấp Quận/Huyện
4 - Cấp Phường/Xã |
| 5 | description | varchar (500) |  | x | Mô tả |
| 6 | is_lock | number(1,0) |  | x | Trạng thái hoạt động
1: Khóa
0: Không khóa |
| 7 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 8 | org_id | number(10,0) |  | x | ID đơn vị tạo dữ liệu |
| 9 | manage_department | number(10,0) |  | x | ID đơn vị quản lý dữ liệu |
| 10 | created_by | varchar(255) |  | x | Người tạo bản ghi |
| 11 | created_date | datetime |  | x | Ngày tạo |
| 12 | modified_by | varchar(255) |  | x | Người chỉnh sửa |
| 13 | modified_date | datetime |  | x | Ngày sửa |
| 14 | is_superadmin | number(1,0) |  | x | = 1: là tài khoản superadmin |
| 15 | role_menu_id | number(10,0) |  |  | ID bảng tự tăng |
| 16 | role_id | number(10,0) |  | x | ID vai trò |
| 17 | menu_id | number(10,0) |  | x | ID menu |
| 18 | resource_id | number(10,0) |  | x | ID resource |
| 19 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 20 | created_by | varchar(255) |  | x | Người tạo bản ghi |
| 21 | created_date | datetime |  | x | Ngày tạo |
| 22 | modified_by | varchar(255) |  | x | Người chỉnh sửa |
| 23 | modified_date | datetime |  | x | Ngày sửa |

## Bảng: SYS_USER (72 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | sys_user_id | number(10,0) |  |  | ID người dùng |
| 2 | user_name | varchar (200) |  | x | Tên đăng nhập |
| 3 | full_name | varchar (200) |  | x | Họ và tên |
| 4 | password | varchar (255) |  | x | Mật khẩu |
| 5 | salt | varchar (200) |  | x | Salt mã hóa password |
| 6 | image_url | varchar (255) |  | x | Link ảnh đại diện của người dùng |
| 7 | gender | number(1,0) |  | x | Giới tính
1: Nam
2: Nữ |
| 8 | identity_card | varchar (50) |  | x | Số giấy tờ tùy thân (CMND/CCCD/ĐDCN/MST) |
| 9 | user_type | varchar (50) |  | x | Loại tài khoản
 Citizen: Công dân
 Business: Cơ quan tổ chức
 Agency: Cơ quan quản lý |
| 10 | manager_id | number(10,0) |  | x | ID đơn vị quản lý tài khoản
 Tham chiếu bảng ORG |
| 11 | public_info | number(1,0) |  | x | Đánh dấu việc có công khai SĐT của CCTP không?
 1: Yes
 0: No |
| 12 | phone_number | varchar (255) |  | x | Số điện thoại |
| 13 | email | varchar (255) |  | x | Email |
| 14 | title | varchar (200) |  | x | Chức vụ |
| 15 | is_manager | number (1,0) |  |  | Lãnh đạo đơn vị, người ký
 1: Yes
 0: No |
| 16 | description | varchar(2000) |  | x | Mô tả |
| 17 | is_default_ps | number(1,0) |  | x | Mật khẩu hiện tại có là mật khẩu mặc định do hệ thống sinh ra hay không?
 1: Là mật khẩu mặc định
 0: Không là mật khẩu mặc định |
| 18 | last_change_password | date |  | x | Lần thay đổi mật khẩu cuối cùng |
| 19 | login_failure_count | number(1,0) |  | x | Số lần đăng nhập fail |
| 20 | login_check | number(1,0) |  | x | Check đã đăng nhập
 1: Đã đăng nhập
 0: Chưa đăng nhập |
| 21 | reset_key | varchar (50) |  | x | Thông tin chuỗi mã hóa dùng trong luồng quên mật khẩu |
| 22 | reset_date | date |  | x | Thời gian thực hiện đổi lại mật khẩu bằng chức năng đổi mật khẩu |
| 23 | remind_change_password | number(1,0) |  | x | Cho phép đổi mật khẩu
 1: Yes
 0: No |
| 24 | MAX_LENGTH | Number(3,0) |  |  | Độ dài mật khẩu tối đa |
| 25 | MIN_LENGTH | Number(1,0) |  |  | Độ dài mật khẩu tối thiểu |
| 26 | upper_letter | Number(1,0) |  | x | Thành phần cấu thành mật khẩu có chứa ít nhất 1 chữ cái viết hoa
 1-  Có
 0 - Không |
| 27 | lower_letter | Number(1,0) |  | x | Thành phần cấu thành mật khẩu có chứa ít nhất 1 chữ cái viết thường
 1 - Có
 0 - Không |
| 28 | numbers | Number(1,0) |  | x | Thành phần cấu thành mật khẩu có chứa ít nhất 1 chữ số
 1- Có
 0- Không |
| 29 | symbol | Number(1,0) |  | x | Thành phần cấu thành mật khẩu có chứa ít nhất 1 ký tự đặc biệt
 1- Có
 0 - Không |
| 30 | IS_CHANGE_DEFAULT_PASS | Number(1,0) |  |  | Yêu cầu thay đổi mật khẩu mặc định (1 – Có, 0 - Không) |
| 31 | IS_CHANGE_RESET_PASS | Number(1,0) |  |  | Yêu cầu thay đổi mật khẩu vừa được cấp lại (1 – Có, 0 - Không) |
| 32 | method_send_pass_user_management | NVARCHAR(255) |  | x | Phương thức cung cấp mật khẩu cho người dùng khi thêm mới người dùng/cài lại mật khẩu tại màn Quản lý người dùng
1 - Hiển thị cửa sổ thông báo chi tiết mật khẩu
2 - Gửi email tới chủ tài khoản |
| 33 | remind_password_change_time | date |  | x | Thời gian bắt đầu nhắc đổi mật khẩu |
| 34 | password_expired_time | Number(5,0) |  | x | Thời gian hết hạn mật khẩu |
| 35 | period_remind_password | number(2,0) |  | x | Số ngày định kỳ lặp lại gửi thông báo đổi mật khẩu |
| 36 | time_require_change | Number(5,0) |  | x | Thời gian yêu cầu thay đổi mật khẩu trước hạn (Đơn vị: Ngày) |
| 37 | remind_password_type | varchar (255) |  | x | Hình thức gửi nhắc đổi mật khẩu tới chủ tài khoản
 1: Email
 2: SMS |
| 38 | PASSWORD_LOCK_TIME | Number(5,0) |  | x | Thời gian khóa tài khoản khi mật khẩu hết hạn (số) |
| 39 | PASSWORD_LOCK_TIME_UNIT | Number(1,0) |  | x | Đơn vị thời gian khóa tài khoản khi mật khẩu hết hạn:
 0 = Giây
 1 = Phút
 2 = Giờ |
| 40 | IS_OPEN_LOCK | Number(1,0) |  | x | Mở khóa tài khoản khi: Thay đổi mật khẩu hết hạn thành công (1 – Có, 0 - Không) |
| 41 | send_via_when_locked | NVARCHAR(255) |  | x | Phương thức gửi thông báo khi tài khoản bị khóa do mật khẩu hết hạn:
1 - Email
2 - SMS |
| 42 | LOCK_DATE | date |  | x | Thời gian khóa tài khoản
 Định dạng: dd/mm/yyyy hh:mm:ss |
| 43 | UNLOCK_DATE | date |  | x | Thời gian mở khóa tài khoản
 Định dạng: dd/mm/yyyy hh:mm:ss |
| 44 | LOCK_REASON | Number(1,0) |  |  | Lý do khóa tài khoản:
3 - Quản trị viên khóa tài khoản
2 – Khóa do đăng nhập sai nhiều lần
1 - Khóa tài khoản do hết hạn mật khẩu
0 - Không |
| 45 | INCORRECT_PASSWORD_TIMES | Number(2,0) |  |  | Số lần nhập sai mật khẩu bị khóa tài khoản |
| 46 | INCORRECT_CAPTCHA_TIMES | Number(2,0) |  |  | Số lần nhập sai mật khẩu hiển thị capcha |
| 47 | lock_wrong_pass_count | Number(2,0) |  | x | Số lần nhập sai mật khẩu sẽ bị khóa tài khoản (theo cấu hình) |
| 48 | captcha_wrong_pass_count | Number(2,0) |  | x | Số lần nhập sai mật khẩu hiển thị capcha (theo cấu hình) |
| 49 | wrong_pass_time | Number (2,0) |  | x | Thời gian tính nhập sai mật khẩu (đơn vị: Phút) |
| 50 | LOCK_TIME | Number(5,0) |  | x | Thời gian khóa tài khoản khi đăng nhập sai mật khẩu (phút) |
| 51 | lock_time_unit | Number(1,0) |  | x | Đơn vị thời gian khóa tài khoản khi đăng nhập sai mật khẩu:
 0 = Giây
 1 = Phút
 2 = Giờ |
| 52 | SEND_LOCK_TYPE | NVARCHAR(255) |  | x | Phương thức gửi thông báo khi tài khoản bị khóa do đăng nhập sai mật khẩu:
1 - Email
2 - SMS |
| 53 | Representative | varchar (200) |  | x | Tên người đại diện |
| 54 | Representative_title | varchar (200) |  | x | Chức danh người đại diện |
| 55 | Approved | number(1,0) |  | x | Trạng thái phê duyệt: (chỉ áp dụng với tài khoản tổ chức)
0: Chờ phê duyệt
1: Được phê duyệt
2: Từ chối phê duyệt |
| 56 | Birthday | date |  |  | Ngày sinh |
| 57 | Two_Step_Verify_config | number(1,0) |  | x | Thiết lập xác thực 2 bước
0: Không thiết lập
1: Có thiết lập |
| 58 | Two_Step_Send_Type | number(1,0) |  | x | Phương thức lấy mã khi cấu hình xác thực 2 bước
1 - Email
2 - Google Authenticator |
| 59 | SMS_Config | number(1,0) |  | x | Thiết lập gửi/nhận SMS
0: Không thiết lập
1: Có thiết lập |
| 60 | is_lock | number(1,0) |  | x | Trạng thái hoạt động
 1: Khóa
 0: Không khóa |
| 61 | is_active | number(1,0) |  | x | Trạng thái xóa
 1: Hoạt động
 0: Xóa |
| 62 | org_id | number(10,0) |  | x | ID đơn vị của người dùng Tham chiếu tới bảng ORG |
| 63 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 64 | created_date | date |  | x | Ngày tạo |
| 65 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 66 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 67 | multi_Step_Verify_config | number(10,0) |  | x | Xác thực đa nhân tố
1- Có
0- Không |
| 68 | multi_Step_Verify_question | varchar (1000) |  |  | Cẩu hỏi xác thực đa nhân tố |
| 69 | multi_Step_Verify_answer | varchar (1000) |  |  | Cẩu trả lời xác thực đa nhân tố |
| 70 | Mapping_Vneid | NVARCHAR(50) |  |  | Lưu UserId do hệ thống VNEID trả về |
| 71 | sys_user_id | number(10,0) |  |  | ID người dùng |
| 72 | role_id | number(10,0) |  |  | ID vai trò |

## Bảng: EXPERIENCE_REPORT (15 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | experience_report_id | number(10,0) |  |  | ID báo cáo |
| 2 | experience_report_name | varchar (255) |  | x | Tên báo cáo |
| 3 | experience_report_summary | varchar (2000) |  | x | Trích yếu |
| 4 | author_name | varchar (255) |  | x | Tác giả/người biên soạn |
| 5 | implementing_org_id | number(10,0) |  | x | Đơn vị thực hiện (Khóa ngoại bảng ORG) |
| 6 | execution_year | number(4,0) |  | x | Năm thực hiện |
| 7 | delegation_id | number(10,0) |  | x | Đoàn công tác (Khóa ngoại bảng DELEGATION) |
| 8 | data_type | number(1,0) |  | x | Loại dữ liệu
1: công khai
2: Nội bộ |
| 9 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 10 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 11 | created_date | date |  | x | Ngày tạo |
| 12 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 13 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 14 | experience_report_id | number(10,0) |  | x | ID báo cáo kinh nghiệm, tham chiếu khóa ngoại tới bảng EXPERIENCE_REPORT |
| 15 | country_id | number(10,0) |  | x | ID quốc gia, tham chiếu khóa ngoại tới trường category_id của bảng CATEGORY (với category_type = 1) |

## Bảng: ORG (27 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | org_id | number(10,0) |  |  | ID bản ghi đơn vị |
| 2 | org_name | varchar (255) |  | x | Tên đơn vị |
| 3 | org_code | varchar (255) |  | x | Mã đơn vị |
| 4 | address | varchar (255) |  | x | Tòa nhà, số nhà, tên đường |
| 5 | parent_org_id | number(10,0) |  | x | ID đơn vị cha |
| 6 | parent_code | varchar (255) |  | x | Mã đơn vị cha |
| 7 | parent_name | varchar (255) |  | x | Tên địa danh hành chính của đơn vị cha |
| 8 | city_code | varchar(5) |  | x | Mã tỉnh |
| 9 | ctiy_name | varchar (255) |  | x | Tên tỉnh |
| 10 | city_id | number(10,0) |  | x | ID Tỉnh/Thành phố (dict_item.dict_item_id) |
| 11 | levels | number(1,0) |  | x | Cấp bậc đơn vị
 Level của đơn vị
 Không có đơn vị cha => LEVEL = 1
 Đơn vị con có level = level cha + 1 |
| 12 | description | varchar (500) |  | x | Mô tả |
| 13 | full_name | varchar (255) |  | x | Tên đầy đủ của đơn vị |
| 14 | from_date | datetime |  | x | Ngày có hiệu lực |
| 15 | to_date | datetime |  | x | Ngày hết hiệu lực |
| 16 | id_new | number(10,0) |  | x | ID đơn vị thay thế (đơn vị mới thay thế đơn vị cũ) |
| 17 | is_lock | number(1,0) |  | x | Trạng thái hoạt động
 1: Khóa
 0: Không khóa |
| 18 | is_active | number(1,0) |  | x | Trạng thái xóa
 1: Hoạt động
 0: Xóa |
| 19 | org_type | number(1,0) |  | x | Loại đơn vị: 
1: Đơn vị trong Bộ
0: Đơn vị ngoài Bộ |
| 20 | manage_id | number(10,0) |  | x | ID đơn vị quản lý dữ liệu hiện tại |
| 21 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 22 | created_date | datetime |  | x | Ngày tạo |
| 23 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 24 | modified_date | datetime |  | x | Ngày được chỉnh sửa |
| 25 | order | number(20,0) |  |  | Thứ tự của đơn vị trong cây đơn vị |
| 26 | signer_config | varchar |  |  | cấu hình người ký |
| 27 | auto_caps_lock | number |  |  | tự động viết hoa địa danh nơi cư trú |

## Bảng: CATEGORYATTACHMENTAREA (36 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | category_id | number(10,0) |  |  | ID danh mục |
| 2 | code | varchar(255) |  | x | Mã |
| 3 | name | varchar(255) |  | x | Tên |
| 4 | category_type | number(1,0) |  | x | Phân loại danh mục: 
1. Quốc gia
2. Cấp ký
3. Loại văn bản
4. Lĩnh vực
5. Học hàm/học vị
6. Quốc tịch
7. Chức vụ
8. Loại tiền, tiền tệ
9. Cấp cho phép
10. Chủ dự án
11. Đối tác phối hợp tổ chức
12. Nhà tài trợ
13. Danh nghĩa ký
14. Hình thức hợp tác
15. Hình thức khen thưởng |
| 5 | description | varchar(2000) |  | x | Mô tả |
| 6 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 7 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 8 | created_date | date |  | x | Ngày tạo |
| 9 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 10 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 11 | attachment_id | number(10,0) |  |  | ID file |
| 12 | object_id | number(10,0) |  | x | ID bản ghi hiển thị file đính kèm |
| 13 | file_name | varchar(255) |  | x | Tên file đính kèm |
| 14 | file_path | varchar(1000) |  | x | Đường dẫn lưu file |
| 15 | file_type | number(1,0) |  | x | Loại file cho từng đối tượng:
1. INTERNATIONAL_AGREEMENT
2. EXPERT
3. EMULATION_COMMENDATION
4. DELEGATION
5. DOCUMENT
6. CONFERENCE
7. PROJECT_PROGRAM 
8. EXPERIENCE_REPORT
9. ANNUAL_PLAN
10. ACTIVITY_RESULT
11. LEGAL_SCHEME
12. COOPERATION_REPORT
13. OTHER_ACTIVITY |
| 16 | file_extension | varchar(10) |  | x | Đuôi file: 
1. pdf
2. doc
3. docx
4. xls
5. xlsx
6. jpg
7. jpeg |
| 17 | file_size | bignint |  | x | Kích thước file |
| 18 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 19 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 20 | created_date | date |  | x | Ngày tạo |
| 21 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 22 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 23 | area_id | number(10,0) |  |  | ID khu vực |
| 24 | code | varchar(255) |  | x | Mã khu vực |
| 25 | name | varchar(255) |  | x | Tên khu vực |
| 26 | parent_id | number(10,0) |  | x | ID khu vực cha |
| 27 | area_level | number(1,0) |  | x | Cấp khu vực: 
1 - Quốc gia
2 - Tỉnh/thành phố
3 - Xã/phường |
| 28 | area_name_level1 | varchar(255) |  | x | Tên khu vực cấp 1 |
| 29 | area_name_level2 | varchar(255) |  | x | Tên khu vực cấp 2 |
| 30 | area_name_level3 | varchar(255) |  | x | Tên khu vực cấp 3 |
| 31 | area_path | varchar(255) |  |  | Đường dẫn |
| 32 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 33 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 34 | created_date | date |  | x | Ngày tạo |
| 35 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 36 | modified_date | date |  | x | Ngày được chỉnh sửa |

## Bảng: INTERNATIONAL_AGREEMENT (22 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | international_agreement_id | number(10,0) |  |  | ID điều ước quốc tế |
| 2 | document_name | varchar(255) |  | x | Tên văn bản |
| 3 | document_type | number(1,0) |  | x | Loại văn bản: 
1: Điều ước quốc tế
2: Thỏa thuận quốc tế
3: Thỏa thuận khác |
| 4 | sign_place_id | number(10,0) |  | x | Nơi ký kết. ID danh mục với category_type = 1 |
| 5 | sign_level_id | number(10,0) |  | x | Cấp ký. ID danh mục với category_type = 2 |
| 6 | sign_date | datetime |  | x | Ngày ký kết |
| 7 | effective_date | datetime |  | x | Ngày có hiệu lực |
| 8 | expired_date | datetime |  |  | Ngày hết hiệu lực |
| 9 | sign_event | varchar (1000) |  | x | Thông tin sự kiện ký kết |
| 10 | signer_name | varchar(255) |  | x | Người ký |
| 11 | title_id | number(10,0) |  | x | Chức vụ người ký. ID danh mục với category_type = 7 |
| 12 | proposing_agency_id | number(10,0) |  | x | Cơ quan đề xuất ký:  khóa ngoại FK tham chiếu tới bảng ORG |
| 13 | signing_capacity_id | number(10,0) |  | x | Danh nghĩa ký:  khóa ngoại FK tham chiếu tới bảng CATEGORY |
| 14 | foreign_partner | varchar(255) |  | x | Đối tác nước ngoài |
| 15 | note | varchar(2000) |  |  | Ghi chú |
| 16 | data_type | number(1,0) |  | x | Loại dữ liệu 
1: PUBLIC 
0: INTERNAL |
| 17 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 18 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 19 | created_date | date |  | x | Ngày tạo |
| 20 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 21 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 22 | manage_id | number(10,0) |  | x | ID đơn vị quản lý tài khoản
 Tham chiếu bảng ORG |

## Bảng: EXPERT (31 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | expert_id | number(10,0) |  |  | ID chuyên gia |
| 2 | full_name | varchar (200) |  | x | Họ và tên chuyên gia |
| 3 | gender | number(1,0) |  | x | Giới tính
1: Nam
2: Nữ |
| 4 | date_of_birth | datetime |  | x | Ngày sinh |
| 5 | identity_no | varchar (50) |  | x | Số giấy tờ tùy thân (CMND/CCCD/ĐDCN/MST) |
| 6 | phone_number | varchar(20) |  | x | Số điện thoại |
| 7 | email | varchar(255) |  | x | Địa chỉ email |
| 8 | address | varchar (500) |  |  | Địa chỉ cá nhân |
| 9 | specialization | varchar (255) |  | x | Lĩnh vực chuyên sâu |
| 10 | academic_title_id | number(10,0) |  | x | Học hàm/học vị |
| 11 | years_of_experience | number(10,0) |  |  | Số năm kinh nghiệm |
| 12 | title | varchar (200) |  |  | Chức vụ |
| 13 | organization_name | varchar (500) |  |  | Cơ quan/Đơn vị công tác |
| 14 | is_current_organization | number(1,0) |  |  | Là đơn vị hiện tại: 
0: Không
1: Có |
| 15 | work_address | varchar(255) |  |  | Địa chỉ nơi làm việc |
| 16 | description | varchar(1000) |  |  | Mô tả |
| 17 | nationality_id | number(10,0) |  |  | Quốc tịch |
| 18 | country_id | number(10,0) |  |  | Quốc gia |
| 19 | work_place | varchar(255) |  |  | Nơi làm việc |
| 20 | working_in_vietnam | varchar(255) |  |  | Hoạt động ở Việt Nam |
| 21 | expert_type | number(1,0) |  | x | Loại chuyên gia:
1: Chuyên gia trong nước
2: Chuyên gia quốc tế
3: Chuyên gia Việt Nam ở nước ngoài |
| 22 | is_lock | number(1,0) |  | x | Trạng thái khóa
1: Khóa
0: Không khóa |
| 23 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 24 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 25 | created_date | date |  | x | Ngày tạo |
| 26 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 27 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 28 | manage_id | number(10,0) |  | x | ID đơn vị quản lý tài khoản
 Tham chiếu bảng ORG |
| 29 | expert_id | ID chuyên gia. Tham chiếu bảng EXPERT |  | x | ID chuyên gia. Tham chiếu bảng EXPERT |
| 30 | created_by | Người tạo bản ghi |  | x | Người tạo bản ghi |
| 31 | created_date | Ngày tạo |  | x | Ngày tạo |

## Bảng: EMULATION_COMMENDATION (25 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | emulation_commendation_id | number(10,0) |  |  | ID thi đua khen thưởng |
| 2 | commendation_type | number(1,0) |  | x | Loại khen thưởng
1. Phía Việt Nam trao
2. Phía Việt Nam nhận |
| 3 | title_name | varchar(255) |  | x | Tên danh hiệu |
| 4 | target_type | number(1,0) |  | x | Đối tượng nhận khen thưởng
1. Cá nhân
2. Tập thể |
| 5 | person_name | varchar (200) |  |  | Tên cá nhân |
| 6 | person_position | varchar(200) |  |  | Chức vụ cá nhân |
| 7 | nationality_id | number(10,0) |  |  | Quốc tịch |
| 8 | working_organization | varchar(255) |  |  | Cơ quan/đơn vị làm việc |
| 9 | organization_name | varchar(255) |  |  | Tên tập thể |
| 10 | country_id | number(10,0) |  |  | Quốc gia nhận khen thưởng |
| 11 | decision_by | varchar(255) |  |  | Cơ quan ban hành quyết định |
| 12 | decision_no | varchar (50) |  |  | Số quyết định |
| 13 | decision_date | datetime |  |  | Ngày ban hành quyết định |
| 14 | achievement | varchar(255) |  |  | Thành tích |
| 15 | awarding | varchar(255) |  |  | Bên trao |
| 16 | receiving | varchar(255) |  |  | Bên nhận |
| 17 | awarding_organization | varchar(255) |  |  | Tên cơ quan/tổ chức trao thưởng |
| 18 | received_year | datetime |  |  | Năm nhận |
| 19 | is_lock | number(1,0) |  | x | Trạng thái khóa
1: Khóa
0: Không khóa |
| 20 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 21 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 22 | created_date | date |  | x | Ngày tạo |
| 23 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 24 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 25 | manage_id | number(10,0) |  | x | ID đơn vị quản lý tài khoản
 Tham chiếu bảng ORG |

## Bảng: CONFERENCE (36 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | conference_id | number(10,0) |  | x | ID hội nghị, hội thảo |
| 2 | title | varchar(255) |  | x | Tiêu đề |
| 3 | content | varchar(255) |  | x | Nội dung |
| 4 | program_id | number(10,0) |  | x | Chương trình dự án |
| 5 | sponsor_id | varchar(255) |  | x | Nhà tài trợ. Tham chiếu tới bảng CATEGORY với CATEGORY_TYPE = 12 |
| 6 | organizing_unit_id | number(10,0) |  | x | Đơn vị của bộ tổ chức. Tham chiếu bảng ORG |
| 7 | cooperating_organization_id | number(10,0) |  | x | Đối tác phối hợp tổ chức. Tham chiếu tới bảng CATEGORY với CATEGORY_TYPE = 11 |
| 8 | approval_level_id | number(1,0) |  | x | Cấp cho phép. Tham chiếu tới bảng CATEGORY với CATEGORY_TYPE = 9 |
| 9 | quantity | number(3,0) |  | x | Số lượng hội nghị/hội thảo/tập huấn |
| 10 | approval_document_no | varchar(50) |  | x | VB phê duyệt |
| 11 | agreement_id | number(10,0) |  | x | ID Điều ước quốc tế/thỏa thuận. Tham chiếu tới bảng INTERNATIONAL_AGREEMENT |
| 12 | has_leader | number(1,0) |  | x | Có lãnh đạo bộ (1: Có, 0: Không) |
| 13 | participant_level | number(1,0) |  | x | Cấp tham gia: 
1 - Bộ trưởng
2 - Thứ trưởng |
| 14 | participant_role | number(1,0) |  | x | Vai trò tham gia: 
1 - Khai mạc
0 - Chủ trì |
| 15 | domestic_delegate_count | number(3,0) |  | x | Số lượng đại biểu trong nước |
| 16 | international_delegate_count | number(3,0) |  | x | Số lượng đại biểu quốc tế |
| 17 | has_opinion | number(1,0) |  | x | Có xin ý kiến (1: Có, 0: Không) |
| 18 | opinion_document_no | varchar(50) |  | x | Số công văn xin ý kiến |
| 19 | has_foreign_delegation | number(1,0) |  | x | Có báo cáo viên nước ngoài (1: Có, 0: Không) |
| 20 | expert_id | number(10,0) |  | x | Chuyên gia tham gia. Tham chiếu tới bảng EXPERT |
| 21 | budget | varchar(50) |  | x | Kinh phí |
| 22 | currency_id | number(10,0) |  | x | Loại tiền. Tham chiếu tới bảng CATEGORY với CATEGORY.CATEGORY_TYPE = 8 |
| 23 | description | varchar (255) |  | x | Mô tả |
| 24 | start_date | date |  | x | Thời gian thực hiện từ |
| 25 | end_date | date |  | x | Thời gian thực hiện đến |
| 26 | province_id | number(10,0) |  | x | Tỉnh/Thành phố. Tham chiếu tới bảng AREA với AREA_LEVEL = 2 |
| 27 | ward_id | number(10,0) |  | x | Tỉnh/Thành phố. Tham chiếu tới bảng AREA với AREA_LEVEL = 3 |
| 28 | address | varchar (255) |  | x | Địa điểm tổ chức |
| 29 | data_type | number(1,0) |  | x | Loại dữ liệu (1: Công khai, 2: Nội bộ) |
| 30 | is_lock | number(1,0) |  | x | Trạng thái khóa
1: Khóa
0: Không khóa |
| 31 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 32 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 33 | created_date | date |  | x | Ngày tạo |
| 34 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 35 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 36 | manage_id | number(10,0) |  | x | ID đơn vị quản lý tài khoản
 Tham chiếu bảng ORG |

## Bảng: DATA_SHARING_CONNECTION (14 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | connection_id | number(10,0) |  |  | ID bản ghi kết nối |
| 2 | receiving_system | varchar(255) |  |  | Tên hệ thống nhận |
| 3 | shared_data_type | number(10,0) |  |  | Loại dữ liệu chia sẻ
1: Đoàn ra, Đoàn vào
2: Điều ước quốc tế, Thỏa thuận quốc tế
3: Báo cáo hợp tác pháp luật
4: Văn bản quy phạm pháp luật / Văn bản pháp luật các nước
5:Chương trình, dự án, phi dự án
6: Đề án hợp tác quốc tế về pháp luật 
7: Kết quả triển khai hoạt động
8: Chuyên gia
9: Hội nghị, hội thảo
10: Báo cáo kinh nghiệm quốc tế
11: Đồng bộ thông tin người dùng (vneid) |
| 4 | connection_account | varchar(255) |  |  | Tài khoản kết nối |
| 5 | connection_password | varchar(255) |  |  | Mật khẩu kết nối (Lưu ý: Bắt buộc mã hóa trước khi lưu) |
| 6 | connection_status | number(1,0) |  | x | Trạng thái kết nối API (Vật lý):
0: Lỗi / Mất kết nối
1: Đang hoạt động / Kết nối thành công
2: Chờ kết nối (Khởi tạo)
3: Tạm dừng |
| 7 | is_sharing | number(1,0) |  | x | Trạng thái chia sẻ :
1: Bật (Cho phép đồng bộ)
0: Tắt (Chặn đồng bộ) |
| 8 | is_active | number(1,0) |  | x | Trạng thái hoạt động, gồm các giá trị:
1 - Hoạt động; 
0 - Xóa |
| 9 | org_id | number(1,0) |  | x | ID đơn vị tạo dữ liệu. Tham chiếu bảng ORG |
| 10 | manage_id | number(10,0) |  | x | ID đơn vị quản lý dữ liệu. Tham chiếu bảng ORG |
| 11 | created_by | number(10,0) |  | x | Lưu ID của user thực hiện thao tác insert |
| 12 | created_date | date |  | x | Thời gian tạo |
| 13 | modified_by | varchar(255) |  | x | Lưu ID của user thực hiện thao tác update |
| 14 | modified_date | date |  | x | Thời gian chỉnh sửa |

## Bảng: COOPERATION_REPORT (19 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | report_id | number(10,0) |  |  | ID bản ghi báo cáo |
| 2 | report_name | varchar(255) |  |  | Tên báo cáo |
| 3 | report_type | number(10,0) |  |  | Phân loại báo cáo:
1: Báo cáo thường niên, giai đoạn
2: bái cáo chuyên đề, đặc thù |
| 4 | start_date | Thời gian bắt đầu (Kỳ báo cáo) |  |  | Thời gian bắt đầu (Kỳ báo cáo) |
| 5 | end_date | Thời gian kết thúc (Kỳ báo cáo) |  |  | Thời gian kết thúc (Kỳ báo cáo) |
| 6 | document_no | Số/Ký hiệu báo cáo |  | x | Số/Ký hiệu báo cáo |
| 7 | report_summary | Trích yếu / Tóm tắt nội dung |  |  | Trích yếu / Tóm tắt nội dung |
| 8 | reporting_agency_id | Cơ quan/Đơn vị ban hành: Tham chiếu ID tới bảng ORG |  | x | Cơ quan/Đơn vị ban hành: Tham chiếu ID tới bảng ORG |
| 9 | signer_name | Người ký / Phê duyệt |  | x | Người ký / Phê duyệt |
| 10 | title_id | Chức vụ người ký: Tham chiếu tới bảng CATEGORY với CATEGORY_TYPE = 7 |  | x | Chức vụ người ký: Tham chiếu tới bảng CATEGORY với CATEGORY_TYPE = 7 |
| 11 | issue_date | Ngày ký báo cáo |  | x | Ngày ký báo cáo |
| 12 | data_type | Loại dữ liệu (1: Công khai, 2: Nội bộ) |  | x | Loại dữ liệu (1: Công khai, 2: Nội bộ) |
| 13 | is_active | Trạng thái xóa (1: Hoạt động, 0: Xóa) |  | x | Trạng thái xóa (1: Hoạt động, 0: Xóa) |
| 14 | created_by | Người tạo bản ghi |  | x | Người tạo bản ghi |
| 15 | created_date | Ngày tạo |  | x | Ngày tạo |
| 16 | modified_by | Người chỉnh sửa |  | x | Người chỉnh sửa |
| 17 | modified_date | Ngày được chỉnh sửa |  | x | Ngày được chỉnh sửa |
| 18 | org_id | ID đơn vị tạo dữ liệu
. Tham chiếu bảng ORG |  | x | ID đơn vị tạo dữ liệu
. Tham chiếu bảng ORG |
| 19 | manage_id | ID đơn vị quản lý tài khoản
. Tham chiếu bảng ORG |  | x | ID đơn vị quản lý tài khoản
. Tham chiếu bảng ORG |

## Bảng: PROJECT_PROGRAMANNUAL_PLANACTIV (105 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | project_program_id | number(10,0) |  | x | ID chương trình dự án |
| 2 | program_name | varchar(255) |  | x | Tên chương trình/dự án |
| 3 | sponsor_id | varchar(255) |  | x | Nhà tài trợ. Tham chiếu tới bảng CATEGORY với CATEGORY_TYPE = 12 |
| 4 | governing_agency_id | number(10,0) |  | x | Cơ quan chủ quản. Tham chiếu bảng ORG |
| 5 | implementing_agency_id | number(10,0) |  | x | Cơ quan/đơn vị thực hiện. Tham chiếu bảng ORG |
| 6 | project_owner_id | number(10,0) |  | x | Chủ dự án. Tham chiếu tới bảng CATEGORY với CATEGORY.CATEGORY_TYPE = 10 |
| 7 | start_date | date |  | x | Thời gian bắt đầu |
| 8 | end_date | date |  | x | Thời gian kết thúc |
| 9 | extended_date | date |  | x | Thời gian gia hạn |
| 10 | international_agreement_id | number(10,0) |  | x | Điều ước quốc tế/thỏa thuận. tham chiếu tới bảng INTERNATIONAL_AGREEMENT |
| 11 | location | varchar(255) |  | x | Địa điểm thực hiện |
| 12 | main_objective | varchar(255) |  | x | Mục tiêu chính |
| 13 | counterpart_funds | varchar(50) |  | x | Vốn đối ứng |
| 14 | counterpart_currency_id | number(3,0) |  | x | Đơn vị tiền tệ vốn đối ứng. Tham chiếu tới bảng CATEGORY với CATEGORY.CATEGORY_TYPE = 8 |
| 15 | counterpart_amount_vnd | varchar(50) |  | x | Quy ra tiền Việt |
| 16 | sponsor_funds | varchar(50) |  | x | Vốn tài trợ |
| 17 | sponsor_currency_id | number(10,0) |  | x | Đơn vị tiền tệ vốn tài trợ. Tham chiếu tới bảng CATEGORY với CATEGORY.CATEGORY_TYPE = 8 |
| 18 | sponsor_amount_vnd | varchar(50) |  | x | Quy ra tiền Việt |
| 19 | decision_no | varchar(50) |  | x | Số văn bản/quyết định |
| 20 | signer_name | varchar(255) |  | x | Người ký |
| 21 | approval_date | date |  | x | Ngày phê duyệt |
| 22 | effective_date | date |  | x | Ngày có hiệu lực |
| 23 | support_source | varchar(255) |  | x | Nguồn hỗ trợ |
| 24 | consultation_level | number(1,0) |  | x | Cấp cho ý kiến (1: Cấp bộ, 0: cấp vụ) |
| 25 | opinion_document_no | varchar(50) |  | x | Văn bản cho ý kiến |
| 26 | note | varchar(2000) |  | x | Ghi chú |
| 27 | data_type | number(1,0) |  | x | "Loại dữ liệu (1: Công khai, 2: Nội bộ)" |
| 28 | is_lock | number(1,0) |  | x | Trạng thái khóa
1: Khóa
0: Không khóa |
| 29 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 30 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 31 | created_date | date |  | x | Ngày tạo |
| 32 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 33 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 34 | manage_id | number(10,0) |  | x | ID đơn vị quản lý tài khoản
 Tham chiếu bảng ORG |
| 35 | project_component_id | number(10,0) |  | x | ID hợp phần |
| 36 | project_program_id | number(10,0) |  | x | ID chương trình/dự án. Tham chiếu tới PROJECT_PROGRAM.PROJECT_PROGRAM_ID |
| 37 | component_name | varchar(255) |  | x | Nội dung hợp phần |
| 38 | display_order | number(2,0) |  | x | Thứ tự hiển thị |
| 39 | created_by | varchar (255) |  | x | Người tạo |
| 40 | created_at | date |  | x | Thời gian tạo |
| 41 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 42 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 43 | project_main_result_id | number(10,0) |  | x | ID kết quả chính |
| 44 | project_component_id | number(10,0) |  | x | ID hợp phần. Tham chiếu tới PROJECT_COMPONENT.PROJECT_COMPONENT_ID |
| 45 | result_content | varchar(255) |  | x | Nội dung kết quả chính |
| 46 | display_order | number(2,0) |  | x | Thứ tự hiển thị |
| 47 | created_by | varchar (255) |  | x | Người tạo |
| 48 | created_at | date |  | x | Thời gian tạo |
| 49 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 50 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 51 | project_activity_id | number(10,0) |  |  | ID nội dung hoạt động |
| 52 | project_component_id | number(10,0) |  | x | ID hợp phần. Tham chiếu tới PROJECT_COMPONENT.PROJECT_COMPONENT_ID |
| 53 | project_main_result_id | number(10,0) |  | x | ID kết quả chính. Tham chiếu tới PROJECT_MAIN_RESULT.PROJECT_MAIN_RESULT_ID |
| 54 | annual_plan_id | number(10,0) |  | x | ID kế hoạch hàng năm. Tham chiếu tới ANNUAL_PLAN.annual_plan_id |
| 55 | activity_name | varchar(255) |  | x | Tên hoạt động |
| 56 | implementing_agency_id | number(10,0) |  | x | Cơ quan/đơn vị thực hiện. Tham chiếu bảng ORG |
| 57 | start_date | date |  | x | Thời gian bắt đầu |
| 58 | end_date | date |  | x | Thời gian kết thúc |
| 59 | actual_start_date | date |  | x | Thời gian bắt đầu thực tế |
| 60 | actual_end_date | date |  | x | Thời gian kết thúc thực tế |
| 61 | budget | varchar (50) |  | x | Kinh phí |
| 62 | used_budget | varchar (50) |  | x | Kinh phí đã sử dụng |
| 63 | location | varchar(255) |  | x | Địa điểm thực hiện |
| 64 | actual_location | varchar(255) |  | x | Địa điểm thực hiện |
| 65 | owner_name | date |  | x | Người ký/phụ trách |
| 66 | note | varchar(255) |  |  | Ghi chú |
| 67 | data_type | number(1,0) |  | x | Loại dữ liệu (1: Công khai, 2: Nội bộ) |
| 68 | display_order | number(2,0) |  | x | Thứ tự hiển thị |
| 69 | created_by | varchar (255) |  | x | Người tạo |
| 70 | created_at | date |  | x | Thời gian tạo |
| 71 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 72 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 73 | project_coordinating_unit_id | number(10,0) |  | x | ID mapping |
| 74 | coordinating_unit_id | number(10,0) |  | x | ID đơn vị quản lý dự án. Tham chiếu bảng ORG |
| 75 | project_program_id | number(10,0) |  | x | ID chương trình dự án. Tham chiếu bảng PROJECT_PROGRAM |
| 76 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 77 | created_date | date |  | x | Ngày tạo |
| 78 | annual_plan_id | number(10,0) |  |  | ID kế hoạch hàng năm |
| 79 | annual_plan_name | varchar(255) |  |  | Tên kế hoạch |
| 80 | project_program_id | number(10,0) |  |  | ID chương trìn, dự án. Tham chiếu bảng PROJECT_PROGRAM |
| 81 | plan_year | number(10,0) |  | x | Năm thực hiện |
| 82 | start_date | date |  | x | Thời gian bắt đầu |
| 83 | end_date | date |  | x | Thời gian kết thúc |
| 84 | main_object | varchar(255) |  | x | Mục tiêu chính của kết hoạch năm đó |
| 85 | data_type | number(1,0) |  | x | Loại dữ liệu:
1: Công khai
2: Nội bộ |
| 86 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 87 | created_by | varchar (255) |  | x | Người tạo |
| 88 | created_at | date |  | x | Thời gian tạo |
| 89 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 90 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 91 | manage_id | number(10,0) |  | x | ID đơn vị quản lý tài khoản
 Tham chiếu bảng ORG |
| 92 | activity_result_id | number(10,0) |  |  | ID kết quả triển khai |
| 93 | project_component_id | number(10,0) |  | x | Khóa ngoại tham chiếu đến bảng PROJECT_ACTIVITY (Để biết báo cáo này của hoạt động nào). |
| 94 | actual_start_date | date |  | x | Thời gian bắt đầu thực tế |
| 95 | actual_end_date | date |  | x | Thời gian kết thúc thực tế |
| 96 | actual_location | varchar (255) |  | x | Địa điểm thực hiện thực tế |
| 97 | used_budget | varchar (255) |  | x | Kinh phí đã sử dụng |
| 98 | result_content | varchar (2000) |  | x | Nội dung kết quả triển khai |
| 99 | note | varchar (2000) |  | x | Ghi chú |
| 100 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 101 | created_by | varchar (255) |  | x | Người tạo |
| 102 | created_at | date |  | x | Thời gian tạo |
| 103 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 104 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 105 | manage_id | number(10,0) |  | x | ID đơn vị quản lý tài khoản
 Tham chiếu bảng ORG |

## Bảng: LEGAL_SCHEMEOTHER_ACTIVITY (59 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | legal_scheme_id | number(10,0) |  |  | ID đề án hợp tác pháp luật (Khóa chính) |
| 2 | scheme_name | varchar(255) |  | x | Tên đề án |
| 3 | governing_agency_id | number(10,0) |  | x | Cơ quan chủ quản. Tham chiếu tới bảng ORG |
| 4 | implementing_agency_id | number(10,0) |  | x | Cơ quan/đơn vị thực hiện. Tham chiếu tới bảng ORG |
| 5 | sponsor_id | varchar (255) |  | x | Nhà tài trợ . Tham chiếu bảng CATEGORY với CATEGORY_TYPE = 12 |
| 6 | international_agreement_id | number(10,0) |  | x | Điều ước QT/thỏa thuận (Không bắt buộc). Tham chiếu INTERNATIONAL_AGREEMENT |
| 7 | start_date | date |  | x | Thời gian bắt đầu |
| 8 | end_date | date |  | x | Thời gian kết thúc |
| 9 | extended_date | date |  | x | Thời gian gia hạn |
| 10 | location | varchar(255) |  | x | Phạm vi/Địa bàn thực hiện |
| 11 | main_objective | varchar(255) |  | x | Mục tiêu chính |
| 12 | budget_source | varchar(255) |  | x | Nguồn kinh phí |
| 13 | decision_no | varchar(50) |  | x | Số văn bản/quyết định |
| 14 | signer_name | varchar(255) |  | x | Người ký |
| 15 | approval_date | date |  | x | Ngày phê duyệt |
| 16 | effective_date | date |  | x | Ngày có hiệu lực |
| 17 | data_type | date |  | x | Loại dữ liệu (1: Công khai, 2: Nội bộ) |
| 18 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 19 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 20 | created_date | date |  | x | Ngày tạo |
| 21 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 22 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 23 | manage_id | number(10,0) |  | x | ID đơn vị quản lý tài khoản
 Tham chiếu bảng ORG |
| 24 | legal_scheme_activity_id | number(10,0) |  |  | ID nội dung hoạt động (Khóa chính) |
| 25 | legal_scheme_id | number(10,0) |  |  | ID đề án cha. Tham chiếu tới bảng LEGAL_SCHEME |
| 26 | activity_name | varchar(255) |  |  | Tên hoạt động |
| 27 | implementing_agency_id | number(10,0) |  |  | Cơ quan/đơn vị thực hiện (Chủ trì). Tham chiếu bảng ORG |
| 28 | coordinating_agency_ids | varchar (255) |  | x | Đơn vị phối hợp (Lưu chuỗi ID cách nhau bằng dấu phẩy) |
| 29 | start_date | date |  |  | Thời gian bắt đầu |
| 30 | end_date | date |  |  | Thời gian kết thúc |
| 31 | budget | varchar(50) |  |  | Kinh phí dự kiến |
| 32 | location | varchar(255) |  | x | Địa điểm thực hiện |
| 33 | signer_name | varchar(255) |  | x | Người ký |
| 34 | note | varchar(2000) |  | x | Ghi chú thêm về hoạt động. |
| 35 | data_type | number(1,0) |  | x | Loại dữ liệu (1: Công khai, 2: Nội bộ) |
| 36 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 37 | created_by | varchar (255) |  | x | Người tạo |
| 38 | created_date | date |  | x | Thời gian tạo |
| 39 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 40 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 41 | manage_id | number(10,0) |  | x | ID đơn vị quản lý tài khoản
 Tham chiếu bảng ORG |
| 42 | other_activity_id | number(10,0) |  |  | ID bản ghi hoạt động khác |
| 43 | activity_name | varchar(255) |  | x | Tên hoạt động khác |
| 44 | sponsor_id | number(10,0) |  | x | Đối tác/Nhà tài trợ. Tham chiếu tới bảng CATEGORY với CATEGORY_TYPE = 12. |
| 45 | implementing_agency_id | number(10,0) |  | x | Cơ quan/đơn vị thực hiện. Tham chiếu tới bảng ORG. |
| 46 | start_date | date |  | x | Thời gian bắt đầu thực hiện. |
| 47 | end_date | date |  | x | Thời gian kết thúc thực hiện. |
| 48 | budget | varchar(50) |  | x | Kinh phí hỗ trợ/tài trợ. |
| 49 | currency_id | number(10,0) |  | x | Loại tiền tệ. Tham chiếu tới bảng CATEGORY với CATEGORY_TYPE = 8. |
| 50 | description | varchar(2000) |  | x | Nội dung hoạt động chính. |
| 51 | note | varchar(2000) |  | x | Ghi chú thêm về hoạt động. |
| 52 | data_type | number(1,0) |  | x | Loại dữ liệu (1: Công khai, 2: Nội bộ) |
| 53 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 54 | created_by | varchar (255) |  | x | Người tạo |
| 55 | created_date | date |  | x | Thời gian tạo |
| 56 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 57 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 58 | org_id | number(10,0) |  | x | ID đơn vị tạo dữ liệu. Tham chiếu bảng ORG. |
| 59 | manage_id | number(10,0) |  | x | ID đơn vị quản lý tài khoản
 Tham chiếu bảng ORG |

## Bảng: DOCUMENT (15 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | document_ id | number(10,0) |  |  | ID của văn bản |
| 2 | document_type | number(1,0) |  |  | Phân loại văn bản:
1: Văn bản quy phạm pháp luật
0: Văn bản pháp luật |
| 3 | document_name | varchar (255) |  |  | Tên văn bản |
| 4 | document_summary | varchar (2000) |  |  | Trích yếu |
| 5 | issuing_department | number(10,0) |  |  | Cơ quan ban hành |
| 6 | issue_date | date |  |  | Ngày ban hành |
| 7 | effective_date | date |  |  | Ngày có hiệu lực |
| 8 | lookup_link | varchar (500) |  | x | Link tra cứu văn bản. |
| 9 | country_id | number(10,0) |  |  | Quốc gia |
| 10 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 11 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 12 | created_date | date |  | x | Ngày tạo |
| 13 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 14 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 15 | manage_id | number(10,0) |  | x | ID đơn vị quản lý tài khoản
 Tham chiếu bảng ORG |

## Bảng: DELEGATION (42 cột)

| STT | Tên cột | Kiểu dữ liệu | Khóa | Not Null | Mô tả |
|---|---|---|---|---|---|
| 1 | delegation_id | number(10,0) |  |  | ID đoàn công tác |
| 2 | delegation_direction | number(1,0) |  |  | Phân loại hướng đoàn.
1: Đoàn vào
0: Đoàn ra |
| 3 | delegation_name | varchar(255) |  |  | Tên đoàn |
| 4 | delegation_type | number(1,0) |  | x | Loại đoàn:
1: Đoàn do Bộ tư pháp chủ trì
2: Đoàn tháp tùng
3: Đoàn khác |
| 5 | delegation_level | number(1,0) |  |  | Cấp đoàn:
1: Cấp Bộ
0: Cấp Vụ |
| 6 | start_date | date |  | x | Thời gian bắt đầu thực hiện |
| 7 | end_date | date |  | x | Thời gian kết thúc thực hiện |
| 8 | excution_year | smallint |  | x | Năm thực hiện |
| 9 | delegation_description | varchar(2000) |  | x | Nội dung |
| 10 | lead_org_id | number(10,0) |  | x | ID Cơ quan chủ trì, tham chiếu tới bảng ORG |
| 11 | excuting_org_id | number(10,0) |  | x | ID Đơn vị thực hiện, tham chiếu tới bảng ORG |
| 12 | delegation_partner | varchar(255) |  | x | Đối tác làm việc |
| 13 | delegation_budget_source | varchar(255) |  | x | Nguồn kinh phí |
| 14 | international_agreement_id | number(10,0) |  |  | Điều ước quốc tế/Thỏa thuận |
| 15 | delegation_header | varchar(255) |  | x | Trưởng đoàn |
| 16 | delegation_header_level | number(1,0) |  | x | Hình thức tham gia (đối với Đoàn ra) hoặc Cấp trưởng đoàn (đối với Đoàn vào):
1: Là lãnh đạo bộ
0: Là lãnh đạo vụ |
| 17 | delegation_transitiontime | number(1,0) |  | x | Có/không bao gồm thời gian đi về:
1: có
0: không |
| 18 | delegation_scope | number(1,0) |  | x | Loại dữ liệu:
1: công khai
0: nội bộ |
| 19 | decision_info | varchar(500) |  | x | Quyết định đoàn và báo cáo |
| 20 | is_in_plan | number(1,0) |  | x | Đoàn có nằm trong kế hoạch
1: có
0: không |
| 21 | note | varchar(2000) |  | x | Ghi chú |
| 22 | activity_format | number(1,0) |  | x | Loại hoạt động
1: Hoạt động ra nước ngoài
2: Hoạt động đối ngoại trực tuyến |
| 23 | delegation_header_title | varchar(255) |  | x | Chức vụ của trrưởng đoàn |
| 24 | delegation_max_days | smallint |  | x | Số ngày làm việc tối đa |
| 25 | delegation_max_members | smallint |  | x | Số người tối đa |
| 26 | receiving_members | varchar(255) |  | x | Người tiếp |
| 27 | is_ministry_header | number(1,0) |  | x | Là lãnh đạo Bộ?
1: có
0: không |
| 28 | is_active | number(1,0) |  | x | Trạng thái xóa
1: Hoạt động
0: Xóa |
| 29 | report_attachment_ids | varchar(255) |  | x | Danh sách file báo cáo Kết quả đoàn công tác |
| 30 | delegation_result | varchar(2000) |  | x | Tóm tắt kết quả đạt được |
| 31 | created_by | varchar (255) |  | x | Người tạo bản ghi |
| 32 | created_date | date |  | x | Ngày tạo |
| 33 | modified_by | varchar (255) |  | x | Người chỉnh sửa |
| 34 | modified_date | date |  | x | Ngày được chỉnh sửa |
| 35 | manage_id | number(10,0) |  | x | ID đơn vị quản lý tài khoản
 Tham chiếu bảng ORG |
| 36 | delegation_member_id | number(10,0) |  |  | ID thành viên đoàn công tác |
| 37 | delegation_id | number(10,0) |  |  | ID đoàn công tác, tham chiếu tới bảng DELEGATION |
| 38 | delegation_member_name | varchar(255) |  |  | Tên thành viên |
| 39 | delegation_member_title | varchar(255) |  |  | Chức vụ |
| 40 | member_department | number(1,0) |  | x | Cơ quan thành viên đoàn thuộc về:
1: Đoàn lãnh đạo Bộ
0: Đoàn lãnh đạo Vụ |
| 41 | delegation_id | number(10,0) |  |  | ID đoàn công tác, tham chiếu khóa ngoại tới bảng DEGATION |
| 42 | country_id | number(10,0) |  |  | ID đoàn công tác, tham chiếu khóa ngoại tới bảng CATEGORY |

