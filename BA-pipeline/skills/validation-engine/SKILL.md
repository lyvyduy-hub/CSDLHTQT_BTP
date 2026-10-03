---
name: validation-engine
description: Chuyển Acceptance Criteria thành test case, cập nhật traceability matrix. Chạy sau khi Solution Gate PASS và traceability-engine xác nhận coverage đầy đủ.
---

## Việc cần làm

1. Đọc `workspace/acceptance-criteria.md`, chuyển từng AC thành test case cụ thể (ID, bước thực hiện, dữ liệu test, kết quả kỳ vọng) → `workspace/test-cases.md`.
2. Gọi `traceability-engine` cập nhật cột Test Case ID.
3. Xác nhận mọi AC có ít nhất 1 test case trước khi báo hoàn tất cho Orchestrator gọi `delivery-agent`.

## Output

`workspace/test-cases.md`, `workspace/traceability-matrix.csv` (cập nhật).

## Evaluation

Không AC nào thiếu test case tương ứng.
