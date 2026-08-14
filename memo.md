# Memo: [Tên sản phẩm AI]

## Step 1 — Timeline & Nguyên lý

...

## Step 2 — Tệp User, JTBD & 4 Forces (Perplexity.ai)
*(Được tổng hợp và phân tích chuyên sâu dựa trên dữ liệu từ Step 0 — `docs/step-0-raw-sources.md`)*

---

### 1. Bảng So Sánh Tệp User: Early Adopters vs. Tệp Hiện Tại (2024 - 2026)

| Tiêu chí | Early Adopters (12/2022 - 2023) | Tệp User Hiện Tại (2024 - 2026) |
| :--- | :--- | :--- |
| **Chân dung cụ thể** *(Gọi tên người thật)* | **"Minh Tech"** — Full-stack Developer 27 tuổi tại startup AI (TP.HCM). Hằng ngày theo dõi X/Twitter, Reddit `r/LocalLLaMA`, săn tìm công cụ AI mới trên Product Hunt. | **"Hà Research"** — Senior Market Analyst & Knowledge Worker 32 tuổi tại tập đoàn tư vấn. Hằng ngày phải làm báo cáo phân tích thị trường, nghiên cứu đối thủ và lập kế hoạch chiến lược. |
| **JTBD (Việc cần làm)** | *"Khi tôi cần tra cứu thông tin/tài liệu công nghệ mới, tôi muốn nhận câu trả lời tổng hợp trực tiếp kèm citation trích dẫn link nguồn để kiểm chứng ngay, thay vì phải tự mở 10+ tab Google và đọc sàng lọc thủ công."* | *"Khi tôi được giao một đề tài nghiên cứu phức tạp hoặc workflow đa bước, tôi muốn AI tự động tìm kiếm, phân tích file (PDF/Excel), làm Deep Research và tạo bài báo cáo/dashboard hoàn chỉnh (Pages/Labs/Computer) để bàn giao công việc mà không phải làm từng bước thủ công."* |
| **Cách làm cũ** *(Trước khi dùng Perplexity)* | Dùng Google Search (vất vả lọc link SEO rác) + Dùng ChatGPT 3.5 (bị giới hạn real-time web và hay bị bịa đặt/hallucination không nguồn). | Dùng Google Search mở 20+ tab + Notion + Excel + ChatGPT chat qua lại nhiều lần, tự đọc lướt và tự soạn báo cáo mất 4-5 tiếng/ngày; thao tác trình duyệt lặp đi lặp lại. |
| **Cột mốc dịch chuyển** *(Segment-Shift nối về Step 0)* | **M01 (12/2022):** Ra mắt **Perplexity Answer Engine** — Chuyển từ *Retrieve (Google)* sang *Answer with Citation*. | **M03 (04/2024):** Enterprise Pro & File Upload.<br>**M04 (05/2024):** Perplexity Pages (biến nghiên cứu thành báo cáo có thể chia sẻ).<br>**M06 (02/2025):** Deep Research (ủy quyền workflow nghiên cứu đa bước).<br>**M08 (07/2025):** Comet Browser & **M10 (02/2026):** Perplexity Computer (chuyển hẳn sang Agentic Execution). |

---

### 2. Phân Tích 4 Forces of Progress (Lực Đổi Công Cụ)

#### 1. Push of the Present (Lực đẩy từ công cụ cũ):
* **Sự suy giảm chất lượng của Google Search:** Google tràn ngập kết quả tài trợ (Sponsored links), trang web tối ưu SEO rác (content farm), buộc người dùng phải bấm vào từng link tự tổng hợp.
* **Hạn chế của AI Chatbot truyền thống (ChatGPT đứng ngoài workflow):** ChatGPT chỉ trả lời hội thoại text tĩnh, không tự động chạy công việc đa bước, không tích hợp trực tiếp vào môi trường duyệt web (*surface*) của người dùng.

#### 2. Pull of the New (Lực hút từ Perplexity):
* **Từ Answer sang Agentic Execution (Tiến hóa theo Step 0):**
  * **Answer Engine:** Trích dẫn nguồn `[1]`, `[2]` minh bạch để kiểm chứng tức thì.
  * **Deep Research & Pages/Labs:** Tự động đọc hàng trăm trang web, phân tích PDF/Excel và xuất ra bài báo cáo/dashboard hoàn thiện (*Outcome-driven*).
  * **Comet Browser & Perplexity Computer:** Đưa AI trực tiếp vào trình duyệt, cho phép AI thực hiện tác vụ thay mặt người dùng (*Delegated Execution*).

#### 3. Habit / Inertia of the Present (Thói quen cũ):
* **Thói quen "Google it":** Thói quen gõ từ khóa vào thanh địa chỉ Google Chrome và sự gắn chặt với hệ sinh thái Google (Workspace, Docs, Drive).
* **Thói quen tự điều khiển thủ công:** Thói quen tự bấm từng bước trên trình duyệt thay vì tin tưởng giao mục tiêu cho AI agent tự chạy.

#### 4. Anxiety of the New (Nỗi lo khi chuyển sang Perplexity):
* **Nỗi lo về độ chính xác của Agent:** Phân vân liệu AI Deep Research hay Computer Agent có thực hiện sai hành động hoặc bỏ sót số liệu quan trọng không.
* **Chi phí & Bảo mật:** Rào cản chi phí đăng ký gói Pro ($20/tháng) / Enterprise Pro và nỗi lo bảo mật dữ liệu doanh nghiệp khi upload file nội bộ.

---

### 3. Câu Hỏi Phản Biện CP2

> **Câu hỏi:** Trong 4 forces, lực nào đang giữ user của sản phẩm này mạnh nhất — và nếu lực đó biến mất thì chuyện gì xảy ra?

#### 💡 Trả lời chi tiết:

1. **Lực giữ chân mạnh nhất hiện tại:**
   * Đó là **Pull of the New** phát triển thành **Workflow & Browser Lock-in (Habit mới)**.
   * **Phân tích:** Perplexity đã mở rộng từ việc chỉ "trả lời câu hỏi" (*Answer Engine*) sang **ủy quyền toàn bộ quy trình công việc** (*Deep Research, Pages, Comet Browser và Perplexity Computer*). Người dùng không chỉ tra cứu thông tin mà đã biến Perplexity thành **môi trường làm việc hàng ngày (AI Work Environment)**. Việc lưu trữ tri thức qua *Spaces/Collections* và thói quen để AI tự động nghiên cứu/thao tác trình duyệt tạo ra rào cản từ bỏ rất lớn.

2. **Nếu lực đó biến mất (hoặc bị đối thủ triệt hạ) thì chuyện gì xảy ra?**
   * **Kịch bản:** Google (với hệ sinh thái Chrome + Gemini Deep Research + Gemini Agent tích hợp sẵn trong Android/Chrome OS) hoặc OpenAI (với ChatGPT Web Search + Operator Browser Extension) cung cấp tính năng Deep Research & Agentic Execution tương đương hoàn toàn miễn phí hoặc tích hợp sẵn trong trình duyệt mặc định.
   * **Hậu quả:** Perplexity sẽ đối mặt với **nguy cơ chảy máu người dùng (User Churn) vô cùng nghiêm trọng**. Lý do vì Switching Cost (chi phí chuyển đổi) về mặt dữ liệu lưu trữ thuần túy của Perplexity chưa đủ dày so với các gã khổng lồ sinh thái (Google Workspace, Microsoft 365). Nếu trải nghiệm Agentic & Research không còn độc quyền vượt trội, người dùng sẽ rút về hệ sinh thái gốc có sẵn của họ.


## Step 3 — 3 Dự đoán

1. ...
2. ...
3. ...

## Step 4 — Tổng hợp & Kết luận

...
