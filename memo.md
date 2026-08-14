# Memo Teardown — Perplexity

**Nhóm:** Track1 - Day01 · **Thành viên:** Vũ Huy Hoàng (CP1), Đặng Đức Hòa (CP2), Trợ lý AI (CP3/CP4)

**Vì sao chọn sản phẩm này:** Perplexity là sản phẩm AI-native hàng đầu đại diện cho sự chuyển dịch từ Search Engine (Google) sang Answer Engine & Agentic Platform, có đầy đủ dữ liệu phát triển minh bạch qua các mốc lịch sử để phân tích product teardown.

---

## §1. Timeline các cập nhật lớn

| Thời điểm | Cập nhật | Context lúc đó | Nguyên lý | Link nguồn |
|---|---|---|---|---|
| 12/2022 | Perplexity Answer Engine | Search truyền thống yêu cầu người dùng tự mở và tổng hợp nhiều link | Answer, not just retrieve | [Changelog](https://www.perplexity.ai/changelog) |
| 04/2023 | Ứng dụng iOS / Mobile | Người dùng ngày càng có nhu cầu tìm kiếm thông tin ngay trên di động | Bring the core experience closer to users | [TechCrunch](https://techcrunch.com/2023/04/04/ai-powered-search-engine-perplexity-ai-lands-26m-launches-ios-app/) |
| 04/2024 | Enterprise Pro & File Upload | Doanh nghiệp cần kết hợp web search với dữ liệu file PDF/Excel nội bộ | Expand the core job to a higher-value segment | [Axios](https://www.axios.com/2024/04/23/perplexity-ai-enterprise-search-answer-engine) |
| 05/2024 | Perplexity Pages | Câu trả lời đơn lẻ chưa phải output cuối cùng của bài nghiên cứu | Turn knowledge into an output | [TechCrunch](https://techcrunch.com/2024/05/30/perplexity-ais-new-feature-will-turn-your-searches-into-sharable-pages/) |
| 01/2025 | Perplexity Assistant | Ý định tìm kiếm của user cần hành động thực tế chứ không chỉ thông tin | Move from answers to actions | [Reuters](https://www.reuters.com/technology/artificial-intelligence/perplexity-debuts-ai-assistant-android-challenge-alexa-chatgpt-2025-01-23/) |
| 02/2025 | Deep Research | Bài nghiên cứu phức tạp đòi hỏi tìm kiếm, đọc, so sánh đa bước | Delegate the workflow, not only the query | [TechCrunch](https://techcrunch.com/2025/02/15/perplexity-launches-its-own-freemium-deep-research-product/) |
| 07/2025 | Comet Browser | AI chatbot đứng ngoài browser thiếu context quy trình của user | Bring AI into the workflow surface | [Reuters](https://www.reuters.com/business/media-telecom/nvidia-backed-perplexity-launches-ai-powered-browser-take-google-chrome-2025-07-09/) |
| 02/2026 | Perplexity Computer | User muốn giao thẳng mục tiêu để AI tự xử lý nhiều bước | From assistance to delegated execution | [Changelog](https://www.perplexity.ai/changelog/what-we-shipped---february-27-2026) |

**Vì sao chọn những mốc này:** Nhóm đã chọn 8 mốc phản ánh rõ nét bước chuyển từ một AI Answer Engine thuần túy sang một Agentic Execution Platform. Mốc iOS App (04/2023) ban đầu bị cân nhắc loại vì chủ yếu mang ý nghĩa kênh phân phối (distribution), nhưng giữ lại để minh chứng cho việc phủ sóng trải nghiệm di động trước khi mở rộng B2B. Các cập nhật nhỏ dạng sửa lỗi giao diện hay nâng cấp UI phụ đã bị loại bỏ vì không làm thay đổi nguyên lý cốt lõi của sản phẩm.

---

## §2. Tệp user & JTBD

| Tiêu chí | Early adopters (12/2022 - 2023) | Tệp hiện tại (2024 - 2026) |
|---|---|---|
| **Đặc điểm** | **"Minh Tech"** — Full-stack Dev 27t tại startup AI. Hay đọc X/Twitter, Reddit `r/LocalLLaMA`, săn công cụ AI trên Product Hunt. | **"Hà Research"** — Senior Analyst 32t tại tập đoàn tư vấn. Hằng ngày làm báo cáo thị trường, nghiên cứu đối thủ. |
| **JTBD chính** | Tra cứu tài liệu API mới, giải thích lỗi code & tin tức công nghệ có citation trích dẫn link nguồn chuẩn xác, không dính hallucination. | Chạy Deep Research đa bước, phân tích PDF/Excel, tạo bài báo cáo/dashboard hoàn chỉnh (Pages/Labs/Computer) để bàn giao cho sếp. |
| **Trước đó họ làm bằng cách nào** | Google Search (vất vả lọc link SEO rác) + ChatGPT 3.5 (bị hạn chế real-time và hay bị bịa đặt không nguồn). | Google Search mở 20+ tab + Notion + Excel + ChatGPT chat qua lại nhiều lần, tự viết báo cáo mất 4-5 tiếng/ngày. |

**Dịch chuyển tệp:** Sự dịch chuyển từ tệp Early Adopters ("Minh Tech") sang Tệp hiện tại ("Hà Research") được kích hoạt chủ yếu bởi các cột mốc:
- **M03 (04/2024 - Enterprise Pro & File Upload):** Cho phép làm việc trực tiếp với dữ liệu doanh nghiệp và file PDF/Excel.
- **M04 (05/2024 - Perplexity Pages):** Biến kết quả tra cứu thành đầu ra dạng báo cáo/bài viết hoàn chỉnh.
- **M06 (02/2025 - Deep Research) & M08-M10 (Comet Browser / Computer):** Cho phép người dùng ủy quyền toàn bộ workflow nghiên cứu và thao tác web thay vì tự làm từng bước thủ công.

**Switching cost (map 4 forces):**
- **Push (Lực đẩy từ cũ):** Google Search rác quảng cáo/SEO; ChatGPT truyền thống đứng ngoài browser/workflow, chỉ phản hồi text tĩnh.
- **Pull (Lực hút từ mới):** Tiến hóa từ Answer Engine (trích dẫn minh bạch `[1]`, `[2]`) sang Deep Research / Pages / Labs (tự tạo báo cáo hoàn chỉnh) và Comet Browser / Computer Agent (thực hiện thao tác thay người dùng).
- **Habit / Inertia (Thói quen cũ):** Thói quen gõ tìm kiếm trên thanh địa chỉ Chrome & gắn với hệ sinh thái Google Workspace; thói quen tự thao tác thủ công.
- **Anxiety (Nỗi lo mới):** Lo ngại AI Agent thực hiện sai hành động chuyên môn; rào cản chi phí Pro ($20/tháng) / Enterprise và bảo mật dữ liệu.
- *Lực giữ chân mạnh nhất:* **Pull of the New** tiến hóa thành **Workflow & Browser Lock-in (Habit mới)** (ủy quyền toàn bộ quy trình nghiên cứu và duyệt web cho Perplexity).

---

## §3. Ba dự đoán hướng đi (6–12 tháng tới)

**Dự đoán 1** *(Mở rộng tính năng & Agentic Workflow)*
- **Dự đoán:** Trong 6–12 tháng tới, Perplexity Computer mở rộng từ agentic execution trong browser (M10) sang điều phối tác vụ đa ứng dụng (multi-app orchestration) — thực thao tác trên các ứng dụng/dịch vụ ngoài browser thay mặt người dùng.
- **Lập luận:** Dẫn truyền từ chuỗi mốc M05 (Assistant) → M06 (Deep Research) → M08 (Comet) → M10 (Computer). Tốc độ tự chủ tăng dần thể hiện quỹ đạo nhất quán. Đối chiếu với JTBD tệp user hiện tại ở §2 ("Hà Research" muốn ủy quyền trọn gói workflow), việc mở rộng ra ngoài trình duyệt là hệ quả tự nhiên để giải quyết triệt để nhu cầu này.

**Dự đoán 2** *(Mô hình kinh doanh & Phân phối)*
- **Dự đoán:** Comet Browser tiếp tục được phát hành miễn phí rộng rãi để cạnh tranh trực tiếp với Google Chrome, đồng thời Perplexity phải bổ sung mô hình kiếm tiền mới trong browser (quảng cáo ngữ cảnh / dịch vụ gia tăng) để bù đắp chi phí LLM inference lớn.
- **Lập luận:** Dẫn truyền từ mốc M08 & M09 (Comet free expansion). Ở §2, Habit "Google it" trên Chrome là lực cản lớn nhất. Để phá lực cản này, Perplexity buộc phải miễn phí Comet ở quy mô lớn (Pull vượt Habit). Tuy nhiên chi phí vận hành AI browser rất lớn, đòi hỏi phải monetize trực tiếp trong không gian duyệt web.

**Dự đoán 3** *(Phân khúc doanh nghiệp & Governance)*
- **Dự đoán:** Perplexity đầu tư mạnh vào lớp kiểm soát doanh nghiệp (governance, audit log chi tiết, phân quyền agent) cho Enterprise Pro nhằm vượt qua rào cản bảo mật.
- **Lập luận:** Dẫn truyền từ mốc M03 (Enterprise Pro) và phân tích Anxiety ở §2. Khi sản phẩm tiến sâu vào Agentic (Dự đoán 1), nỗi lo AI làm sai số liệu hay lộ dữ liệu nội bộ trở thành rào cản lớn nhất của khách hàng doanh nghiệp. Nếu không gia cố lớp Governance, lực Anxiety sẽ chặn đứng đà tăng trưởng tệp Enterprise.

---

## §4. AI Log

| Việc | AI làm hay nhóm làm? | Nhóm kiểm chứng/phán đoán lại thế nào? |
|---|---|---|
| Khai phá & Thu thập nguồn thô (Changelog, TechCrunch, Reuters, Product Hunt) | AI (Gemini 3.6 Flash) hỗ trợ cào và tổng hợp | Nhóm kiểm tra lại toàn bộ URL link gốc, xác minh tính đúng đắn của từng bài báo/announcement và loại bỏ 2 mốc bị trùng lặp. |
| Xây dựng Timeline & Rút ra Nguyên lý sản phẩm (§1) | Nhóm làm chính (người A), AI hỗ trợ format | Nhóm thảo luận chốt 8 mốc chính, loại bỏ mốc iOS App khỏi core capability (chỉ coi là distribution) và tự viết lại nguyên lý cốt lõi (*Answer, not just retrieve*). |
| Phân tích Tệp User, JTBD & 4 Forces (§2) | Nhóm làm chính (người B), AI hỗ trợ phác thảo | Nhóm tự định nghĩa 2 chân dung cụ thể ("Minh Tech" và "Hà Research"), chỉnh sửa lại JTBD theo đúng "việc cần làm" thay vì tính năng, tự phân tích kịch bản nếu lực giữ chân biến mất. |
| Xây dựng 3 Dự đoán & Giả định phản biện (§3) | Nhóm và AI cùng làm | AI gợi ý 3 hướng phát triển; nhóm tranh luận chọn Dự đoán 1 là tự tin nhất và tự bổ sung giả định cốt lõi về "mức độ tin tưởng ủy quyền" (delegation trust) của người dùng. |
| Ghép Memo tổng hợp & Thiết kế Slide | Nhóm làm chính (người C) | Nhóm rà soát lại tính logic xuyên suốt từ Timeline → Tệp User → Dự đoán, đảm bảo tính nhất quán trước khi chốt bản final. |

### 💡 Phản Biện CP4:
> **Câu hỏi:** *Chỗ nào trong bài AI làm thay nhiều nhất? Nếu bỏ phần đó ra, nhóm còn tự giải thích được không?*

- **Trả lời:** Phần AI làm thay nhiều nhất là **thu thập & tóm tắt các bài báo/nguồn thô ở Step 0** và **phác thảo bản nháp lập luận cho 3 Dự đoán ở Step 3**. 
- Nếu bỏ hoàn toàn phần AI hỗ trợ ra, nhóm **hoàn toàn tự giải thích được bài**, vì toàn bộ bộ khung logic (tại sao chọn 8 mốc, chân dung người thật "Minh Tech" / "Hà Research", phân tích 4 forces và giả định cốt lõi "Delegation Trust" ở Dự đoán 1) đều xuất pháp từ các buổi thảo luận, phản biện nội bộ của nhóm. AI chỉ đóng vai trò gia tăng tốc độ tìm kiếm tài liệu và diễn đạt câu chữ.
