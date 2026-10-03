---
name: traceability-engine
description: Duy trì traceability-matrix.csv liên tục từ sau analysis-agent, cập nhật sau mỗi thay đổi artifact. Không chờ đến cuối pipeline mới chạy. Mọi khẳng định "đã có spec" phải được xác minh bằng cách đọc thật nội dung file, không được suy luận.
---

## Vai trò

Đảm bảo mọi BR/FR đều trace được đến Solution/Spec/Test case, phát hiện sớm phần nào bị bỏ sót. Đây là skill không hội thoại — chỉ đọc/ghi file trong `workspace/`.

## Việc cần làm

1. Khởi tạo `workspace/traceability-matrix.csv` ngay khi `analysis-agent` có `requirements.md` — cột: `BR/FR ID | Batch | Mô tả | Solution ref | Use Case ID | Data/API/Report spec ID | Test Case ID | Trạng thái`.
2. Sau mỗi lần `solution-agent` hoặc `validation-engine` tạo/sửa artifact, quét lại và cập nhật các cột tương ứng.
3. Xuất `workspace/coverage-check.md` mỗi lần được gọi — liệt kê ID nào còn thiếu spec/test case.
4. Nếu Requirement Gate hoặc Solution Gate trả FAIL, đánh dấu trạng thái tương ứng trong matrix là `needs-rework`, không xóa dòng.

---

## QUY TẮC BẮT BUỘC — Chống tự tin báo cáo sai (Anti-Hallucination Verification)

**Đây là quy tắc có hiệu lực cao nhất của skill này, áp dụng cho mọi lần đánh dấu một FR/BR/NFR là "đã có spec".**

### Lý do quy tắc này tồn tại

Đã phát hiện trong thực tế: `coverage-check.md` từng báo "100% — 0 yêu cầu thiếu" cho một dự án mà 5 FR hoàn toàn không có dòng nào trong `erd.md`, `data-dictionary.md`, `openapi.yaml`, `api-spec.md`, `ui-spec.md`. Nguyên nhân: việc chấm "đã có spec" được suy luận dựa trên các FR cùng nhóm đã có spec, thay vì thực sự tìm kiếm mã FR đó trong từng file. Quy tắc dưới đây tồn tại để việc này không lặp lại.

### Bắt buộc thực hiện cho MỖI FR/BR/NFR, không có ngoại lệ

Trước khi điền bất kỳ ô nào trong cột `Solution ref`, `Use Case ID`, `Data/API/Report spec ID`, `Test Case ID` của `traceability-matrix.csv`, hoặc trước khi liệt kê một FR vào phần "đã đủ coverage" của `coverage-check.md`:

1. **Mở thật từng file đích** (`solution-design.md`, `use-cases.md`, `erd.md`, `data-dictionary.md`, `openapi.yaml`, `api-spec.md`, `report-catalog.md`, `report-spec.md`, `test-cases.md`) và **tìm kiếm chính xác mã FR/BR/NFR đó** (ví dụ tìm chuỗi `FR-UC-32`) trong nội dung file.
2. **Không được suy luận** "FR-UC-31 đến FR-UC-39 cùng nhóm nên chắc cũng có" — mỗi mã phải được tìm thấy độc lập, bằng chính mã đó, trong chính file đó.
3. Nếu tìm thấy → ghi lại **vị trí cụ thể** tìm thấy (tên mục/dòng/endpoint) vào ô tương ứng trong matrix, không ghi chung chung "đã có".
4. Nếu **không tìm thấy** mã đó trong một file bắt buộc phải có (ví dụ FR liên quan đến API nhưng không thấy mã trong `openapi.yaml`) → đánh dấu ngay `status: missing-spec` cho đúng cột đó, liệt kê vào `coverage-check.md` phần "THIẾU", **không được bỏ qua hoặc làm tròn thành "đã đủ"** dù các FR khác cùng nhóm đã đạt.
5. Khi một FR có AC và test case (`acceptance-criteria.md`, `test-cases.md`) nhưng KHÔNG có Data/API spec tương ứng — đây là tín hiệu cảnh báo đặc biệt (AC/test case không thể kiểm chứng được nếu chưa có backend/API thật). Luôn gắn cờ riêng các trường hợp này trong `coverage-check.md` dưới mục "⚠️ Có AC/Test Case nhưng thiếu Data/API Spec — cần rà lại ngay", vì đây là dấu hiệu dễ xảy ra việc tạo test case "khống" không gắn với spec thật.

### Định dạng `coverage-check.md` bắt buộc có thêm mục xác minh

```markdown
## Nhật ký xác minh (Verification Log)

Với mỗi FR/BR/NFR được đánh dấu "đã đủ", liệt kê bằng chứng cụ thể đã tìm thấy:

| Mã YC | Tìm thấy trong file nào | Vị trí/Tên mục cụ thể | Đã tìm kiếm trực tiếp mã này? |
|---|---|---|---|
| FR-UC-05 | openapi.yaml | /admin/app-groups (GET/POST) | Có |
| FR-UC-32 | — KHÔNG TÌM THẤY — | — | Có tìm, không thấy → status: missing-spec |
```

Nếu không thể điền cột "Vị trí/Tên mục cụ thể" bằng một giá trị thật lấy từ file, **không được đánh dấu FR đó là đã đủ coverage**.

## Output

`workspace/traceability-matrix.csv` (luôn ở trạng thái mới nhất), `workspace/coverage-check.md` (kèm Nhật ký xác minh như trên).

## Evaluation

Trước khi báo "matrix đầy đủ" hoặc "coverage 100%", quét toàn bộ hàng trong Nhật ký xác minh — nếu có bất kỳ dòng nào thiếu "Vị trí/Tên mục cụ thể" thật, KHÔNG được báo đầy đủ, bất kể các dòng khác đã đạt bao nhiêu phần trăm.
