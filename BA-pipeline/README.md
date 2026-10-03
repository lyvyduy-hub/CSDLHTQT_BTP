# Mobile BA Pipeline — Antigravity

Thả toàn bộ thư mục này vào project Antigravity của bạn (giữ nguyên cấu trúc AGENTS.md + skills/ + workspace/).

- `AGENTS.md` — orchestration chính, agent Antigravity đọc khi khởi động, chứa toàn bộ luật routing/gate.
- `skills/` — toàn bộ skill trong pipeline, chi tiết bên dưới.
- `workspace/` — nơi lưu toàn bộ artifact sinh ra trong quá trình chạy (`requirements.md`, `traceability-matrix.csv`, `erd.md`, `PRD-*.md`, `SRS-*.md`, `DDD-*.md`...). Để trống lúc đầu, agent sẽ tự tạo file khi chạy.

## Danh sách skill

| Skill | Vai trò | Chạy khi nào |
|---|---|---|
| `domain-agent` | Cấp domain knowledge/convention cho Analysis và Solution | Đầu dự án + trước Solution |
| `analysis-agent` | Input Ingestion & Assessment, Discovery, As-Is, Requirement (BR/FR/NFR) | Đầu pipeline, và lặp lại khi Requirement Gate FAIL hoặc re-submit Batch 2 |
| `review-agent` | Thẩm định Requirement Gate và Solution Gate (dùng chung 1 skill, 2 chế độ) | Sau analysis-agent, sau solution-agent |
| `prd-generator-agent` | Sinh Product Requirements Document (PRD) cho stakeholder kinh doanh | Ngay sau Requirement Gate PASS/PARTIAL PASS |
| `srs-generator-agent` | Sinh "Tài liệu Phân tích Yêu cầu Người sử dụng" theo template BM_01 | 2 lần: sau Requirement Gate (bản sơ bộ) và sau Solution Gate (bản cập nhật) |
| `solution-agent` | Solution design, Data Model, API Spec, Report Spec, Migration Mapping, UI/Workflow | Sau Requirement Gate PASS |
| `traceability-engine` | Duy trì traceability-matrix.csv liên tục, xác minh thật từng mã FR trong file nguồn | Chạy nền, sau mỗi lần có artifact mới |
| `ddd-generator-agent` | Sinh Detailed Design Document tổng quát theo template BM_04 (phần Web/chung) | Ngay sau Solution Gate PASS |
| `spec-adapter-agent` | Chuyển output của solution-agent sang INPUT SCHEMA cho Mobile DDD (chỉ FR thuộc Mobile App) | Sau Solution Gate PASS, chỉ khi dự án có deliverable Mobile App |
| `mobile-ddd-generator-agent` | Sinh Mobile DDD (`<project_code>_Mobile_DDD.docx`) từ `mobile-ddd-input.yaml` | Sau spec-adapter-agent, nếu không có mục "Chặn" |
| `validation-engine` | Chuyển AC thành test case | Sau Working Artifact |
| `delivery-agent` | SIT → UAT → Reconciliation → Go-Live, route lỗi theo nguyên nhân | Sau validation-engine |
| `hypercare-agent` | Giám sát sau go-live | Sau delivery-agent |
| `artifact-engine` | 2 chế độ: Working Artifact (gọi ddd-generator-agent, srs-generator-agent v2, spec-adapter-agent) và Final Artifact Engine (đóng gói bản lưu trữ chốt) | Sau Solution Gate PASS, và sau hypercare-status = closed |

## Tài liệu sinh ra trong 1 vòng chạy đầy đủ

1. `PRD-<mã dự án>.md` — sau Requirement Gate
2. `SRS-<mã dự án>.md` — bản sơ bộ sau Requirement Gate, bản cập nhật sau Solution Gate
3. `DDD-<mã dự án>.md` — sau Solution Gate (phần Web/chung)
4. `<project_code>_Mobile_DDD.docx` — sau Solution Gate, chỉ khi dự án có deliverable Mobile App riêng (qua `spec-adapter-agent`)
5. Bản export cuối (Word/PDF) — sau khi Hypercare đóng, do Final Artifact Engine đóng gói

## Lưu ý khi dùng

- Antigravity không có graph điều phối cứng — `AGENTS.md` đã viết routing dưới dạng luật bắt buộc, nhưng nên theo dõi vài lượt chạy đầu để chắc agent tuân thủ đúng thứ tự Gate, không "nhảy cóc".
- Không đổi tên file trong `workspace/` đã được quy định trong từng `SKILL.md` — đây là hợp đồng dữ liệu giữa các skill.
- Mô hình phân phối nền tảng (Web/Mobile App riêng) phải được xác lập tường minh trong `project-charter.md` ở Bước 0 của `analysis-agent` — đây là điều kiện duy nhất quyết định có chạy nhánh Mobile DDD hay không, không được suy luận từ các từ khóa chung chung như "responsive"/"đa nền tảng".
- Các skill sinh tài liệu (`prd-generator-agent`, `srs-generator-agent`, `ddd-generator-agent`, `spec-adapter-agent`) đều áp dụng nguyên tắc chống tự tin báo cáo sai (Anti-Hallucination): mọi mã FR/BR/endpoint/field đưa vào tài liệu phải được tìm thấy thật trong file nguồn, không được suy luận hoặc bịa để lấp đầy bảng.
