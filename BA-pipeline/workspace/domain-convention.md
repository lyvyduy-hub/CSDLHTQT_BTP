# Quy Chuẩn Thiết Kế Kỹ Thuật (Domain Convention)

## 1. Chuẩn RESTful API & OpenAPI
- Phiên bản OpenAPI: 3.0.3
- Định dạng dữ liệu: JSON (UTF-8)
- Định dạng đường dẫn API: Kebab-case, ví dụ: /api/v1/international-agreements
- Cấu trúc Response chuẩn:
{
  "code": 200,
  "message": "Success",
  "data": { ... },
  "timestamp": "2026-10-03T18:00:00Z"
}

## 2. Chuẩn Đặt Tên Cơ Sở Dữ Liệu
- Tên bảng: SNAKE_CASE chữ hoa, số ít hoặc số nhiều ngắn gọn (SYS_USER, ROLE, INTERNATIONAL_AGREEMENT, EXPERT, CONFERENCE, DELEGATION).
- Tên cột: SNAKE_CASE chữ hoa (USER_ID, AGREEMENT_NAME, IS_ACTIVE, CREATED_AT).
