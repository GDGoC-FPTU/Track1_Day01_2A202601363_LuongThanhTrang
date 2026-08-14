# Step 3 — 3 Dự đoán (Perplexity.ai)
(Dựa trên Step 0 — docs/step-0-raw-sources.md mốc M01-M10, và Step 2 — docs/step-2-user-jtbd.md tệp user & 4 forces. Sẽ cập nhật lập luận khi Step 1 (A) chốt bản timeline final.)

## Dự đoán 1

**Dự đoán:** Trong 6-12 tháng tới, Perplexity Computer mở rộng từ agentic execution trong browser (M10) sang điều phối tác vụ đa ứng dụng (multi-app orchestration) — không chỉ chạy trong Comet mà còn thao tác được trên các app/dịch vụ khác thay mặt user (đặt lịch, gửi mail, thao tác file cục bộ...).

**Lập luận:**
Chuỗi mốc M05 (Assistant, 01/2025) → M06 (Deep Research, 02/2025) → M08 (Comet Browser, 07/2025) → M10 (Computer, 02/2026) cho thấy một đường thẳng liên tục tăng dần mức độ tự chủ: từ trả lời (Answer) sang thực hiện hành động (Action) sang sở hữu cả bề mặt làm việc (Browser) sang thực thi công việc trọn gói (Execute). Khoảng cách giữa các lần ra mắt đang rút ngắn dần, cho thấy tốc độ đầu tư vào agentic tăng chứ không chững lại. Đối chiếu với JTBD tệp user hiện tại ở Step 2 ("Hà Research" muốn giao trọn workflow đa bước, không muốn tự làm từng bước) — nhu cầu "ủy quyền toàn phần" đã tồn tại, Perplexity chỉ cần mở rộng phạm vi ủy quyền ra ngoài browser để đáp ứng JTBD đó triệt để hơn.

---

## Dự đoán 2

**Dự đoán:** Comet Browser tiếp tục được đẩy miễn phí rộng rãi hơn (sau M09) để cạnh tranh trực tiếp thị phần với Chrome, đồng thời Perplexity phải tìm nguồn kiếm tiền mới gắn trong browser (quảng cáo ngữ cảnh, gói subscription nâng cấp trong luồng sử dụng) thay vì chỉ dựa vào Pro/Enterprise subscription.

**Lập luận:**
M08 (Comet ra mắt) và M09 (Comet mở rộng miễn phí, 10/2025) cho thấy chiến lược ưu tiên adoption hơn doanh thu trực tiếp từ browser. Theo phân tích 4 Forces ở Step 2, Habit "Google it" gắn với hệ sinh thái Chrome là lực cản lớn nhất (Habit/Inertia) — muốn phá lực này cần free-to-use ở quy mô lớn, không thể thu phí ngay từ đầu. Nhưng browser miễn phí quy mô lớn tạo áp lực chi phí vận hành (LLM inference cho mọi truy vấn duyệt web), nên cần một mô hình kiếm tiền mới trong chính browser để bù chi phí — đây là hệ quả tất yếu của việc Pull of the New (free Comet) đang được dùng để thắng Habit of the Present.

---

## Dự đoán 3

**Dự đoán:** Perplexity đầu tư mạnh hơn vào lớp kiểm soát doanh nghiệp (governance, audit log, quyền hạn chi tiết cho agent) cho Enterprise Pro, thay vì chỉ mở rộng tính năng agentic — nhằm giữ tệp user doanh nghiệp trước khi mất họ vì lo ngại bảo mật.

**Lập luận:**
M03 (Enterprise Pro, 04/2024) xác nhận doanh nghiệp là tệp user chiến lược. Step 2 chỉ ra Anxiety of the New mạnh nhất nằm ở "độ chính xác của Agent" và "bảo mật dữ liệu khi upload file nội bộ" — đây là lực cản trực tiếp lên chính hướng agentic (Dự đoán 1) khi áp dụng vào môi trường doanh nghiệp. Một sản phẩm càng agentic (tự hành động thay user) càng cần cơ chế kiểm soát/audit đi kèm để tệp user doanh nghiệp dám dùng, nếu không lực Anxiety sẽ thắng lực Pull of the New và làm chậm/mất tệp user giá trị cao này.

---

## Câu Hỏi Phản Biện CP3

**Câu hỏi:** Dự đoán nào bạn tự tin nhất — và giả định cốt lõi nào khiến nó sai nếu không đúng?

**Trả lời:**

Dự đoán tự tin nhất: **Dự đoán 1** (mở rộng agentic execution ra ngoài browser).

Lý do tự tin: đây là phần duy nhất được củng cố bởi *toàn bộ* 4 mốc liên tiếp gần nhất (M05 → M06 → M08 → M10), không phải suy diễn từ 1 mốc đơn lẻ như Dự đoán 2 và 3. Xu hướng đủ nhất quán và đủ dài để coi là quỹ đạo chính của sản phẩm, không phải một thử nghiệm nhánh phụ.

Giả định cốt lõi nếu sai: Dự đoán này đứng trên giả định rằng **user sẵn sàng tăng dần mức độ tin tưởng giao quyền (delegation trust)** cho agent theo thời gian. Nếu giả định này sai — tức là Deep Research/Computer gây ra đủ nhiều lỗi hành động hoặc sai số liệu đáng kể (đúng như Anxiety of the New đã nêu ở Step 2) — thì user sẽ rút lui về việc chỉ dùng Perplexity như công cụ *gợi ý* (suggest rồi user tự bấm xác nhận), chứ không cho agent tự thực thi (auto-execute). Khi đó quỹ đạo "Answer → Research → Act → Execute" sẽ dừng lại ở mức Assist thay vì tiến tới Execute hoàn toàn, và toàn bộ Dự đoán 1 (và phần nào Dự đoán 2, 3 phụ thuộc vào nó) sẽ không thành hiện thực như mô tả.
