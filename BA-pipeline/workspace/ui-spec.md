# Đặc Tả Giao Diện Người Dùng (UI Specification)

## 1. Nguyên Tắc Thiết Kế UI/UX
- Tuân thủ thiết kế Figma dự án CSDL Hợp tác quốc tế Bộ Tư pháp.
- Áp dụng chuẩn responsive (Layout thích ứng Desktop, Tablet, Mobile Browser).

## 2. Quy Định Kỹ Thuật Dùng Chung (D012 - D018)
- **Mã D012 (Upload file đính kèm)**: Hỗ trợ chọn file / kéo thả. Hỗ trợ dạng ảnh, video, pdf, doc, excel <= 10MB/file. Validate đuôi file trực tiếp trên form.
- **Mã D013 (Tải file đính kèm)**: TH1 (0 file): Toast message "Bản ghi... không có file đính kèm". TH2 (1 file): Tải file trực tiếp. TH3 (nhiều file): Nén file ZIP dạng `File_dinh_kem_<tên đối tượng>_dd/MM/yyyy.zip`.
- **Mã D014 (Tab Tài liệu đính kèm)**: Nút "Thêm mới" chỉ hiển thị cho superadmin (`is_superadmin = 1`). Nút "Xem" preview full màn hình popup. Nút "Xóa" popup xác nhận.
- **Mã D015 (Xóa file đính kèm)**: Popup xác nhận "Thao tác xóa sẽ không thể hoàn tác. Bạn có chắc chắn muốn xóa tệp tin?".
- **Mã D018 (Bộ lọc thời gian báo cáo)**: Nhóm 3 tab [Theo ngày] / [Theo tháng] / [Theo năm]. Tự động ẩn/hiện bộ lọc Datepicker / Combobox tương ứng.
