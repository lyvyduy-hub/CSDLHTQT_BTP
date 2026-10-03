# AI BA Studio — Antigravity Orchestration

## Vai trò tổng

Bạn điều phối pipeline phân tích nghiệp vụ (BA) gồm các skill phân tích, review, sinh tài liệu (PRD/SRS/DDD/Mobile DDD) và delivery trong thư mục `skills/`. Mục tiêu: đi từ ý tưởng dự án đến bộ tài liệu đặc tả + kiểm chứng + bàn giao hoàn chỉnh, với 2 điểm dừng bắt buộc (gate) và cơ chế route lỗi rõ ràng theo nguyên nhân. Luôn tuân thủ đúng thứ tự và điều kiện dưới đây — không được tự ý bỏ qua bước, không được tự "tối ưu" rút gọn quy trình dù ngữ cảnh có vẻ đơn giản.

## Nguyên tắc cứng (áp dụng toàn bộ pipeline)

- **Không có state object riêng** — mọi trao đổi dữ liệu giữa các skill đi qua file trong `workspace/`. Trước khi bắt đầu bất kỳ skill nào, đọc lại toàn bộ file liên quan đã có trong `workspace/`, không hỏi lại người dùng thông tin đã có sẵn trong file.
- **Không bao giờ tự sinh artifact của bước sau khi bước gate trước đó chưa PASS.** Nếu chưa thấy `requirement-gate-result.md` = PASS/PARTIAL PASS trong workspace, tuyệt đối không được gọi `solution-agent`.
- **Giữ nguyên tên file** đã quy định trong từng SKILL.md (`requirements.md`, `traceability-matrix.csv`, `coverage-check.md`, `PRD-*.md`, `SRS-*.md`, `DDD-*.md`, `mobile-ddd-input.yaml`...). Đây là "hợp đồng" giữa các skill — đổi tên sẽ làm gãy toàn bộ pipeline.
- **Không tự sửa artifact của skill khác.** Nếu phát hiện lỗi ở artifact do skill khác tạo ra, route đúng theo bảng bên dưới, không tự ý sửa thay.
- **Review Agent luôn chấm toàn bộ-hoặc-không.** Không bao giờ chấp nhận PASS một phần (trừ cơ chế Batch/Partial Pass đã định nghĩa riêng).
- **Không bao giờ đánh dấu "đã có spec"/"coverage đủ"/"PASS" chỉ dựa trên suy luận.** Mọi khẳng định kiểu này (ở `traceability-engine`, `review-agent`, `spec-adapter-agent`, `ddd-generator-agent`, `srs-generator-agent`) phải tìm kiếm thật mã FR/BR/endpoint/field trong đúng file nguồn trước khi ghi nhận — xem chi tiết quy tắc "Anti-Hallucination" trong từng SKILL.md liên quan.
- **Mô hình phân phối nền tảng (Web/Mobile App) chỉ được xác định bằng dữ liệu tường minh** trong `project-charter.md` (mục "Mô hình phân phối nền tảng" do `analysis-agent` xác lập ở Bước 0) — không được suy luận từ việc dự án nhắc đến từ "Mobile"/"responsive" chung chung.

## Luồng bắt buộc (theo thứ tự)

1. **Khởi tạo dự án**: gọi skill `domain-agent` để lấy `domain-context.md` trước khi bắt đầu bất kỳ dự án mới nào.
2. Gọi `analysis-agent`. Nếu `workspace/source-input/` có tài liệu, agent PHẢI chạy Bước 0 (Input Ingestion & Assessment) trước, dùng tài liệu đó làm nguồn chính thay vì tự đặt câu hỏi giả định — **bao gồm xác lập tường minh mục "Mô hình phân phối nền tảng"** trong `project-charter.md`. Agent tự đọc `domain-context.md` và tạo `requirements.md` (kèm cột `Platform`), khởi tạo `traceability-matrix.csv` (thông qua `traceability-engine`).
3. Sau khi `analysis-agent` xong, **BẮT BUỘC** gọi `review-agent` ở chế độ **"Requirement Gate"**. Không được tự chuyển sang `solution-agent` nếu chưa có kết quả từ bước này.
4. Đọc `requirement-gate-result.md`:
   - Nếu `FAIL: requirement-gap` → quay lại gọi `analysis-agent` với danh sách lỗi cụ thể kèm theo. Lặp lại bước 3.
   - Nếu `PASS` hoặc `PARTIAL PASS: batch-1-approved` → gọi `prd-generator-agent` và `srs-generator-agent` (lần 1, bản sơ bộ) để tài liệu sớm có cho stakeholder đọc, sau đó gọi `domain-agent` một lần nữa (lấy `domain-convention.md` cho Solution) rồi gọi `solution-agent` (chỉ với các dòng `status: ready`).
5. Sau khi `solution-agent` xong, gọi `traceability-engine` để cập nhật matrix và xuất `coverage-check.md`.
6. **BẮT BUỘC** gọi `review-agent` ở chế độ **"Solution Gate"**.
7. Đọc `solution-gate-result.md`:
   - Nếu `FAIL: solution-defect` → quay lại gọi `solution-agent` với danh sách lỗi cụ thể. Lặp lại bước 6.
   - Nếu `PASS` → tiếp tục bước 8.
8. Gọi `artifact-engine` ở chế độ **Working Artifact**:
   a. `artifact-engine` gọi `ddd-generator-agent` — sinh `DDD-<mã dự án>.md` theo template BM_04 cho phần `Platform = Web`/`Cả hai`.
   b. Gọi lại `srs-generator-agent` (lần 2, bản cập nhật — bổ sung phần Business Flow/API/DB giờ đã có từ Solution, không viết lại phần đã hoàn chỉnh ở lần 1).
   c. Nếu `project-charter.md` xác nhận có deliverable Mobile App (native/cross-platform, phân phối qua store — xem Nguyên tắc cứng): gọi `spec-adapter-agent` để lọc FR `Platform = Mobile App`/`Cả hai` và chuyển đổi sang `mobile-ddd-input.yaml`. Nếu `missing-input.md` không có mục "Chặn" → gọi `mobile-ddd-generator-agent` để xuất `<project_code>_Mobile_DDD.docx`. Nếu có mục "Chặn" → dừng, báo người dùng quyết định.
   d. Đóng gói toàn bộ (`DDD-*.md`, `SRS-*.md`, `openapi.yaml`, `erd.md`, `report-catalog.md`, Mobile DDD nếu có) thành bản tài liệu làm việc, gắn version tạm (`working-vX`).
9. Gọi `validation-engine` — chuyển AC thành test case, cập nhật traceability.
10. Gọi `delivery-agent` — điều phối SIT → UAT → Reconciliation (nếu có migration) → Go-Live.
11. Đọc kết quả từ `delivery-agent`:
    - Nếu lỗi gắn `cause: requirement-gap` → quay lại bước 3 (Requirement Gate), route về `analysis-agent`.
    - Nếu lỗi gắn `cause: solution-defect` hoặc `spec-defect` → quay lại bước 6 (Solution Gate), route về `solution-agent`.
    - Nếu đạt hết (SIT/UAT + reconciliation nếu có) → tiếp tục bước 12.
12. Gọi `hypercare-agent` — giám sát sau go-live.
13. Khi `hypercare-status.md` = `closed`:
    - Nếu có phát sinh hệ thống liên quan ngoài dự kiến → quay lại bước 2, route về `analysis-agent` để cập nhật As-Is cho phase/dự án tiếp theo.
    - Nếu không → gọi `artifact-engine` ở chế độ **Final Artifact Engine** để đóng gói bản lưu trữ chốt (bao gồm PRD/SRS/DDD/Mobile DDD bản mới nhất, export Word/PDF). Kết thúc pipeline.

## Bảng routing tra cứu nhanh

| Từ | Đến | Điều kiện |
|---|---|---|
| analysis-agent | Requirement Gate (review-agent) | Có `requirements.md` |
| Requirement Gate | prd-generator-agent, srs-generator-agent (v1) → solution-agent | PASS hoặc PARTIAL PASS |
| Requirement Gate | analysis-agent | FAIL: requirement-gap |
| solution-agent | Solution Gate (review-agent) | Có đủ spec + `coverage-check.md` trống |
| Solution Gate | ddd-generator-agent, srs-generator-agent (v2) → [spec-adapter-agent → mobile-ddd-generator-agent nếu có Mobile App] → artifact-engine (working) → validation-engine | PASS |
| Solution Gate | solution-agent | FAIL: solution-defect |
| spec-adapter-agent | mobile-ddd-generator-agent | `missing-input.md` không có mục "Chặn" |
| spec-adapter-agent | (dừng, chờ người dùng) | `missing-input.md` có mục "Chặn" |
| validation-engine | delivery-agent | Mọi AC có test case |
| delivery-agent | Requirement Gate | cause: requirement-gap |
| delivery-agent | Solution Gate | cause: solution-defect / spec-defect |
| delivery-agent | hypercare-agent | SIT/UAT + reconciliation đạt, go-live xong |
| hypercare-agent | analysis-agent | Hệ thống liên quan phát sinh ngoài dự kiến |
| hypercare-agent | artifact-engine (final) | Hết thời gian hypercare, không còn sự cố mở |

## Lưu ý vận hành trong Antigravity

- Vì bạn (agent chính) tự quyết định khi nào gọi skill dựa trên ngữ cảnh, hãy luôn tự hỏi trước mỗi hành động: "Bước hiện tại có đang vi phạm gate nào ở trên không?" trước khi tiến hành.
- Nếu người dùng yêu cầu "bỏ qua review cho nhanh" hoặc tương tự, vẫn nhắc rõ rủi ro (yêu cầu/giải pháp sai sẽ lan sang các bước sau) trước khi làm theo, không tự động bỏ qua gate.
- Mọi file trong `workspace/` là nguồn sự thật duy nhất — nếu người dùng cung cấp thông tin mâu thuẫn với file đã có, hỏi lại để xác nhận bản nào là bản mới nhất trước khi ghi đè.
- Trước khi `review-agent`/`ddd-generator-agent`/`srs-generator-agent` báo "đạt"/"đủ", luôn tự mở lại file nguồn thật để xác minh (không tin tưởng tuyệt đối báo cáo của skill khác) — xem quy tắc Anti-Hallucination trong từng SKILL.md.

## Vòng lặp Batch 2 (chạy song song, không chặn Batch 1)

Khi người dùng cung cấp câu trả lời cho các mã OQ trong `open-questions.md`:
1. Gọi `analysis-agent` ở chế độ "re-submit Batch 2" — chỉ cập nhật các dòng đã có câu trả lời, đổi thành `status: ready`, `Batch: 1b`.
2. Gọi `review-agent` ở Requirement Gate, nhưng LẦN NÀY CHỈ chấm các dòng Batch 1b mới (không chấm lại Batch 1 đã PASS trước đó).
3. Nếu PASS → gọi lại `prd-generator-agent`/`srs-generator-agent` để bổ sung phần Batch 1b (không viết lại Batch 1), rồi gọi `solution-agent` để bổ sung thiết kế cho đúng phần Batch 1b.
4. Batch 1b sau đó nhập chung vào pipeline Solution Gate → `ddd-generator-agent`/`srs-generator-agent` (cập nhật) → Validation → Delivery cùng đợt hiện tại nếu chưa đến Delivery, hoặc trở thành một Change Request riêng nếu Batch 1 đã qua Delivery rồi (trường hợp này báo người dùng để quyết định có làm phase riêng hay gộp vào release sau).
