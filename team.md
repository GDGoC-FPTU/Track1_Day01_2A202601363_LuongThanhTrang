# Phân công nhóm — Sản phẩm: Perplexity

Nguyên tắc: chạy song song ngay từ đầu, không đợi checkpoint trước xong mới bắt đầu. Dùng bản nháp chung làm input tạm, refine dần qua các điểm sync ngắn.

## Sprint 0 — Bản nháp chung (cả 3, ~30-45 phút, làm cùng lúc)
Mỗi người tự research nhanh song song rồi gộp:
- Rough list 8-10 mốc lịch sử ứng viên (chưa cần verify kỹ).
- Rough hypothesis 2 tệp user (ai dùng, khi nào đổi).
- Rough 2-3 hướng dự đoán (chưa cần lập luận chặt).

→ Kết quả: 1 bản nháp dùng chung (draft_timeline, draft_user, draft_predictions) để 3 người làm song song ngay, không phải chờ bản final của nhau.

## Người A — Timeline & Nguồn (CP0, CP1)
Làm song song từ Sprint 0, không chờ ai:
- Verify tối thiểu 3 nguồn thô (changelog, blog founder, Product Hunt...).
- Chốt bảng 6-8 mốc: Thời điểm · Cập nhật · Context · Nguyên lý + link nguồn.
- Chuẩn bị lý do chọn/loại 1 mốc (phản biện CP1).
- Đẩy bản cập nhật timeline cho B, C ngay khi có, không đợi hoàn thiện 100%.

## Người B — User & JTBD (CP2)
Làm song song từ Sprint 0, dùng draft_timeline tạm:
- Dựng bảng so sánh 2 tệp user (chân dung thật + JTBD "việc cần làm").
- Đánh giá 4 forces + switching cost.
- Nối segment-shift về mốc — dùng draft_timeline trước, update lại khi A gửi bản chốt (chỉ sửa phần liên kết mốc, không làm lại từ đầu).
- Xác định lực giữ chân mạnh nhất + kịch bản mất lực (phản biện CP2).

## Người C — Dự đoán & Khung Memo (CP3, CP4 khung, CP5 khung)
Làm song song từ Sprint 0, dùng draft_timeline + draft_user tạm:
- Viết 3 dự đoán (cấu trúc Dự đoán / Lập luận) dựa bản nháp — update lại lập luận khi A, B gửi bản chốt.
- Xác định dự đoán tự tin nhất + giả định cốt lõi nếu sai (phản biện CP3).
- Dựng khung memo.md 4 phần + khung slides ngay từ Sprint 0 (mục lục, chỗ trống chờ nội dung) — không đợi A, B xong mới bắt đầu khung.
- Giữ AI Log xuyên suốt: mỗi người tự ghi phần AI hỗ trợ của mình vào file chung, C tổng hợp cuối.

## Điểm Sync (thay cho việc chờ nhau)
- Sync 1 (sau ~1/3 thời gian): A/B/C đối chiếu bản nháp vs tiến độ thật, ai lệch thì chỉnh input cho người kia — không dừng việc đang làm.
- Sync 2 (sau ~2/3 thời gian): chốt timeline + user + predictions, C khoá bản để ghép memo.md.
- Sync 3 (cuối): review chéo toàn bài — mỗi người đọc và phải tự giải thích được cả 3 phần, không chỉ phần mình.

## Việc chung cả 3 (CP5)
- slides.pdf: A trình bày Timeline, B trình bày User & JTBD, C trình bày Dự đoán + Memo.
- Tick đủ self-checklist hệ thống.
- Chuẩn bị thuyết trình luồng logic: Timeline → Nguyên lý → Tệp User → 3 Dự đoán, sẵn sàng Q&A.

## Lưu ý
Sync ngắn (15-20 phút), không phải bàn giao chờ đợi. Mỗi người luôn có việc để làm — không có khoảng chờ "ngồi không đợi checkpoint trước".
