---
name: artifact-engine
description: Hai chế độ - Working Artifact (ngay sau Solution Gate PASS, cho dev/DBA/QA dùng ngay) và Final Artifact Engine (sau hypercare-agent, đóng gói bản lưu trữ chốt).
---

## Chế độ 1 — Working Artifact (Orchestrator gọi ngay sau Solution Gate PASS)

1. Gọi `ddd-generator-agent` — sinh `DDD-<mã dự án>.md` theo template BM_04 cho phần Web/chung (không bao gồm FR thuộc riêng Mobile App).
2. Đóng gói `DDD-<mã dự án>.md` cùng `openapi.yaml`, `erd.md`, `report-catalog.md` thành bản tài liệu làm việc để dev/DBA/QA dùng ngay. Lưu vào `workspace/`, gắn version tạm (`working-vX`).

Lưu ý: `srs-generator-agent` chạy riêng, SỚM HƠN — ngay sau Requirement Gate PASS (không chờ đến Working Artifact), rồi chạy lại lần 2 ở bước này để bổ sung phần còn thiếu (xem "Cơ chế SRS bản cập nhật" trong `srs-generator-agent/SKILL.md`).

### Điều kiện gọi thêm `mobile-ddd-generator-agent` (dựa trên dữ liệu tường minh, không suy luận)

Đọc mục **"Mô hình phân phối nền tảng"** trong `workspace/project-charter.md` (do `analysis-agent` xác lập ở Bước 0 — xem `analysis-agent/SKILL.md`). Chỉ gọi `mobile-ddd-generator-agent` khi bảng đó có dòng `Deliverable: Mobile app` với `Loại: Native / Cross-platform` và `Phân phối qua: App Store / Google Play`.

**KHÔNG được tự suy luận** từ việc `project-charter.md` nhắc đến từ "Mobile" trong yêu cầu responsive UI — một web app responsive chạy tốt trên màn hình điện thoại KHÔNG đồng nghĩa có app mobile riêng. Nếu mục "Mô hình phân phối nền tảng" không tồn tại hoặc không rõ ràng trong `project-charter.md`, **KHÔNG được tự quyết định gọi hay không gọi** — báo lại cho Orchestrator/người dùng để xác nhận trước, ghi rõ vào `version-log.md` rằng quyết định đang chờ xác nhận.

Khi dự án có CẢ Web app và Mobile app riêng (2 dòng trong bảng Mô hình phân phối nền tảng):
1. Gọi skill `spec-adapter-agent` TRƯỚC — skill này lọc đúng các FR có `Platform = Mobile App`/`Cả hai` từ `requirements.md`/`traceability-matrix.csv`, đọc lại `use-cases.md`/`ui-spec.md`/`erd.md`/`openapi.yaml`/`api-spec.md` và chuyển đổi thành `workspace/mobile-ddd-input.yaml` đúng INPUT SCHEMA.
2. Chỉ sau khi `spec-adapter-agent` báo không còn mục "Chặn" trong `missing-input.md` (hoặc người dùng đã quyết định chấp nhận sinh thiếu), mới gọi `mobile-ddd-generator-agent` với `workspace/mobile-ddd-input.yaml` làm input — không tự đọc trực tiếp output thô của `solution-agent` để đưa vào `mobile-ddd-generator-agent`.

## Chế độ 2 — Final Artifact Engine (Orchestrator gọi sau khi hypercare-agent báo closed)

Đóng gói toàn bộ artifact cuối cùng (đã qua go-live, đã fix theo `hypercare-log.md` nếu có) thành bản lưu trữ chốt — export Word/Excel/PDF, gắn version chính thức (`final-v1.0`), lưu vào `workspace/` cùng `traceability-matrix.csv` bản cuối.

## Output

Bộ file export (docx/xlsx/pdf), `workspace/version-log.md`.

## Lưu ý khi xác định chế độ nào đang được gọi

Nếu chưa có `hypercare-status.md` = closed trong workspace → đang ở Chế độ 1 (Working). Nếu đã có → Chế độ 2 (Final).
