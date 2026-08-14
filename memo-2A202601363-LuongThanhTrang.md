# Perplexity — AI Product Teardown Memo (Bản Tổng Hợp Nhóm)

<<<<<<< HEAD
**Nhóm:** T2H
**Thành viên:**

1. [Họ và tên A] — Timeline & Nguồn (CP0, CP1)
2. [Họ và tên B] — User & JTBD (CP2)
3. [Họ và tên C] — Dự đoán & Memo (CP3, CP4, CP5)

---

---

## Thông tin chung & Lý do chọn sản phẩm

- **Tên sản phẩm:** Perplexity (perplexity.ai)
- **Định vị:** Answer engine — công cụ tìm kiếm và nghiên cứu dựa trên hội thoại, trả về câu trả lời tổng hợp kèm trích dẫn nguồn trực tiếp.

**Lý do chọn:**

Tôi chọn Perplexity vì đây là một sản phẩm AI có định vị tương đối rõ: công cụ tìm kiếm và nghiên cứu dựa trên hội thoại, cung cấp câu trả lời tổng hợp kèm trích dẫn nguồn trực tiếp. So với nhiều AI agent đa năng, Perplexity nổi bật ở trải nghiệm "answer-first search": người dùng không chỉ nhận danh sách đường link mà có thể đặt câu hỏi tiếp nối, kiểm tra nguồn và mở rộng quá trình nghiên cứu trong cùng một luồng.

Perplexity phù hợp với bài teardown vì:

- Có hành trình phát triển đủ rõ để phân tích sự chuyển dịch từ AI search sang AI research/agentic search.
- Có những quyết định sản phẩm đặc trưng như ưu tiên nguồn dẫn, truy vấn tiếp nối và tổng hợp thông tin theo thời gian thực.
- Scope vừa đủ hẹp để truy ngược các cập nhật về nguyên lý cốt lõi, đồng thời vẫn có đủ dữ liệu và cột mốc cho timeline 6–8 sự kiện.
- Sản phẩm đang đứng tại giao điểm giữa search engine, chatbot và AI agent, tạo cơ sở hợp lý để dự đoán hướng phát triển trong 6–12 tháng tới.

Tôi không chọn ChatGPT vì phạm vi sản phẩm quá lớn: từ hội thoại, tìm kiếm, tạo nội dung, lập trình, hình ảnh, giọng nói đến agent và nền tảng dành cho doanh nghiệp. Trong giới hạn 120 phút và memo 3–5 trang, việc teardown ChatGPT dễ dẫn đến phân tích dàn trải, khó xác định một JTBD trung tâm và khó truy ngược các quyết định về cùng một tập nguyên lý. Perplexity có ranh giới sản phẩm rõ hơn nên phù hợp để phân tích sâu, thay vì chỉ liệt kê tính năng.

---

## §1. Timeline các cập nhật lớn & Revert Nguyên lý

| # | Thời điểm | Cập nhật | Context (vì sao lúc đó) | Nguyên lý cốt lõi được revert ra |
| :-- | :--- | :--- | :--- | :--- |
| 1 | 07/12/2022 | Ra mắt **Perplexity Ask** dạng public beta — câu trả lời tổng hợp kèm trích dẫn inline ([Britannica Money](https://www.britannica.com/money/Perplexity-AI), [Built In](https://builtin.com/artificial-intelligence/what-is-perplexity-ai)) | ChatGPT ra mắt 30/11/2022, tạo cơn sốt nhưng bịa thông tin, không nguồn, dữ liệu bị cắt theo mốc huấn luyện. Google thì trả về danh sách link ngày càng nhiều quảng cáo và nội dung SEO. | **Câu trả lời phải kiểm chứng được thì mới dùng được.** Trích dẫn không phải tính năng phụ — nó là điều kiện để một câu trả lời do máy sinh ra có giá trị. |
| 2 | Giữa 2023 | **Copilot** (guided search — AI hỏi lại để làm rõ ý định) + gói **Pro $20/tháng**, không chạy quảng cáo ([Perplexity Pricing 2026](https://suprmind.ai/hub/perplexity/pricing/)) | Người dùng bắt đầu dùng cho câu hỏi phức tạp chứ không chỉ tra cứu nhanh. Bing Chat và Google SGE cùng lúc nhảy vào ô tìm kiếm. | **Truy vấn là một cuộc hội thoại, không phải một phát ăn ngay.** Và: **người trả tiền là người dùng, không phải nhà quảng cáo** — nếu nhà quảng cáo trả tiền thì trung lập của câu trả lời sẽ bị bán trước. |
| 3 | 30/07/2024 | **Publishers' Program** — chia doanh thu hai chữ số phần trăm cho Time, Fortune, Der Spiegel, The Texas Tribune, WordPress.com ([CNBC](https://www.cnbc.com/2024/07/30/perplexity-ai-to-share-revenue-with-publishers-after-plagiarism-accusations.html)) | Tháng 6/2024 Forbes phát hiện nội dung trả phí của mình bị tái tạo gần như nguyên văn trong tính năng Pages mà chỉ ghi nguồn bằng logo nhỏ; Wired sau đó tố tương tự và tố Perplexity lách robots.txt. | **Nguồn là nhà cung cấp, không phải nguyên liệu miễn phí.** Mô hình "dẫn nguồn" chỉ bền nếu chủ nguồn có lợi ích trong đó — nếu không, chính nguồn sẽ đóng cửa và sản phẩm mất nguyên liệu. |
| 4 | 18/11/2024 | **Shopping Hub + "Buy with Pro"** — mua và thanh toán ngay trong câu trả lời, cho Pro users tại Mỹ ([TechResearchOnline](https://techresearchonline.com/news/perplexity-buy-with-pro-ai-shopping-agent/), [Stellagent](https://stellagent.ai/insights/perplexity-shopping-buy-with-pro)) | Truy vấn mua sắm là loại truy vấn đắt tiền nhất trên Google. Perplexity đã có traffic nhưng chưa có đường kiếm tiền ngoài subscription. | **Câu trả lời chỉ hoàn thành job khi dẫn tới hành động.** Trả lời "nên mua cái nào" rồi đá người dùng sang tab khác là bỏ dở việc. |
| 5 | 14/02/2025 | **Deep Research** — chạy hàng chục lượt tìm, đọc hàng trăm nguồn, tự xuất báo cáo; miễn phí có hạn mức ([TechCrunch](https://techcrunch.com/2025/02/15/perplexity-launches-its-own-freemium-deep-research-product/), [Simon Willison](https://simonwillison.net/2025/Feb/16/introducing-perplexity-deep-research/)) | OpenAI ra Deep Research trước đó vài ngày; trục cạnh tranh chuyển từ "ai trả lời nhanh hơn" sang "ai làm hộ được việc nặng hơn". | **Một câu hỏi khó xứng đáng nhiều lượt tìm.** Bỏ ràng buộc "một truy vấn = một câu trả lời tức thì" để đổi lấy độ sâu. Đây là điểm sản phẩm rời khỏi khung *search* và bước vào khung *research*. |
| 6 | 09/07/2025 | **Comet** — trình duyệt AI-native trên nền Chromium, mở đầu chỉ cho gói Max $200/tháng ([UPI](https://www.upi.com/Top_News/US/2025/07/09/bc-us-perplexity-comet-browser-launch/5911752083534/), [Wikipedia](https://en.wikipedia.org/wiki/Comet_(browser))) | Muốn agent làm hộ việc thật thì cần context thật: tab đang mở, phiên đăng nhập, lịch sử, form. Ô tìm kiếm không có gì trong số đó. | **Muốn agent hành động thay người dùng thì phải sở hữu nơi người dùng đang làm việc.** Đây là bước đổi định nghĩa sản phẩm lần thứ hai: từ *research tool* sang *lớp thao tác*. |
| 7 | 25/08/2025 | **Comet Plus** — gói $5/tháng, chia **80%** doanh thu cho nhà xuất bản, quỹ khởi động $42,5M; tính cả *agent traffic* (khi agent dùng nội dung để làm việc) ([Search Engine Journal](https://www.searchenginejournal.com/perplexity-launches-comet-plus-shares-revenue-with-publishers/554596/), [Engadget](https://www.engadget.com/ai/perplexity-has-cooked-up-a-new-way-to-pay-publishers-for-their-content-204255019.html), [Forbes](https://www.forbes.com/sites/anishasircar/2025/08/28/perplexitys-comet-plus--legal-peace-offering-or-new-dawn-for-publishers-in-the-ai-era/)) | Mốc 3 chưa đủ dập được kiện tụng và phản ứng của báo chí. Khi agent tự đọc nội dung thay người, mô hình "chia tiền theo lượt hiển thị quảng cáo" hết hiệu lực. | Nguyên lý ở mốc 3 được **siết chặt và định giá lại**: nếu agent tiêu thụ nội dung thay con người, thì phải trả tiền cho hành vi tiêu thụ đó, không chỉ cho lượt click. |
| 8 | 02/10/2025 → 06/2026 | **Comet mở miễn phí toàn cầu** (02/10/2025, [CNBC](https://www.cnbc.com/2025/10/02/perplexity-ai-comet-browser-free-.html)), rồi **gọi $200M ở định giá ~$20B** để scale Comet ([Dealroom](https://app.dealroom.co/news/feed/perplexity-raises-200m-at-20b-valuation-to-scale-free-comet-browser-in-race-for-ai-agent-economy), [TechTimes](https://www.techtimes.com/articles/318028/20260608/perplexity-raises-200-million-comet-ai-browser-agent-economy-front-door.htm)) | Trình duyệt $200/tháng không thể phá được thói quen Chrome. Cửa vào của "agent economy" chỉ đáng giá nếu có đủ người đứng ở cửa. | **Phân phối trước, doanh thu sau.** Chấp nhận đốt tiền để chiếm thanh địa chỉ, vì lực giữ chân mạnh nhất của đối thủ là thói quen mặc định (xem §2). |

> **Ghi chú mốc bị loại:**
>
> - **Bird SQL (15/12/2022)** — giao diện tìm kiếm Twitter chạy trên engine của Perplexity. Loại vì đây là một thử nghiệm phân phối chết yểu, không sinh ra nguyên lý nào còn sống trong sản phẩm hôm nay.
> - **Các lần đổi/bổ sung mô hình nền** (thêm GPT-4, Claude, Gemini; ra mô hình Sonar của riêng mình). Loại vì đây là thay linh kiện, không phải quyết định về *sản phẩm là gì*. Chúng phục vụ nguyên lý cũ chứ không đổi nguyên lý.
> - **Các vòng gọi vốn thuần túy** (trừ vòng 06/2026 vì vòng này gắn trực tiếp với quyết định phát Comet miễn phí — tức là gắn với một quyết định sản phẩm).
> - **Đề nghị mua lại Chrome (08/2025)** — loại vì đây là động thái truyền thông/pháp lý trong bối cảnh vụ kiện chống độc quyền của Google, không phải cập nhật sản phẩm đã xảy ra. *(Mốc này tôi chưa truy được nguồn sơ cấp trong thời gian làm bài — xem mục "Chưa kiểm chứng được".)*

---

## §2. Tệp User & JTBD (Segment Shift & 4 Forces)

### Bảng so sánh Tệp User

| Tiêu chí | Early Adopters (2022 – giữa 2023) | Tệp hiện tại (2025 – 2026) |
| :--- | :--- | :--- |
| **Đặc điểm** | Dân công nghệ trên Hacker News / X, developer, nhà nghiên cứu, người theo dõi sát làn sóng LLM. Có sẵn hoài nghi với AI, biết AI bịa, và **có khả năng tự kiểm nguồn**. Số ít, chịu khó, sẵn sàng dùng sản phẩm còn thô. | Người làm tri thức phổ thông (marketing, tài chính, tư vấn, sinh viên), người mua sắm, và nhóm doanh nghiệp. **Không có khả năng và không có ý định tự kiểm từng nguồn** — họ mua sự tiện, không mua sự minh bạch. Cộng thêm nhóm mới: người muốn AI *thao tác hộ* chứ không chỉ *trả lời*. |
| **JTBD** | "Khi tôi gặp một câu hỏi mới hoặc ngách mà Google trả về toàn rác SEO, hãy cho tôi câu trả lời tổng hợp **kèm nguồn để tôi tự kiểm**, để tôi không phải mở 10 tab và không phải lo bị bịa." | "Khi tôi có một việc cần thông tin để ra quyết định — chọn mua gì, viết báo cáo gì, khảo sát thị trường nào — hãy **làm hộ tôi cả quá trình và giao ra thành phẩm**, để tôi không phải tự đi từ câu hỏi đến kết quả." |
| **Cách làm cũ** | Google + mở hàng loạt tab + Ctrl-F từng bài; hoặc hỏi ChatGPT rồi tự đi verify lại từ đầu — tức là làm việc hai lần. | Tự Google nhiều vòng + copy vào Excel/Docs + đọc review + hỏi đồng nghiệp + tự viết báo cáo. Với mua sắm: so giá thủ công qua nhiều sàn. |
| **Cột mốc dịch chuyển** | — | Dịch chuyển không xảy ra ở một mốc mà qua ba mốc nối tiếp: **Mốc 4 (Buy with Pro, 11/2024)** mở job "ra quyết định mua"; **Mốc 5 (Deep Research, 02/2025)** đổi đơn vị giao hàng từ *câu trả lời* sang *báo cáo*; **Mốc 6 (Comet, 07/2025)** đổi từ *giao thành phẩm* sang *tự làm việc*. Mốc 8 (Comet free) là bước đưa tệp mới này thành tệp đại chúng. |

**Điều đáng chú ý trong dịch chuyển này:** nguyên lý gốc "câu trả lời phải kiểm chứng được" (Mốc 1) sinh ra để phục vụ nhóm *có khả năng kiểm chứng*. Tệp hiện tại phần lớn **không kiểm**. Trích dẫn với họ không còn là công cụ kiểm chứng mà đã trở thành **tín hiệu đáng tin** — một thứ để yên tâm, không phải để soi. Đây là căng thẳng trung tâm của sản phẩm hiện nay và là gốc của phần lớn rủi ro ở §3.

### Phân tích 4 Forces & Switching Cost

- **Push (Lực đẩy khỏi cách làm cũ):** Trang kết quả Google ngày càng dày quảng cáo và nội dung SEO sản xuất hàng loạt; người dùng phải tự tổng hợp từ 5–10 tab. Ở phía ChatGPT giai đoạn đầu: bịa thông tin, không nguồn, dữ liệu cũ. Cả hai lối cũ đều bắt người dùng làm phần việc nặng nhất — đọc và tổng hợp.

- **Pull (Lực hút sang sản phẩm mới):** Câu trả lời tổng hợp có trích dẫn ngay tại chỗ; hỏi tiếp trong cùng luồng mà không mất ngữ cảnh; Deep Research xuất thẳng báo cáo; Comet thao tác trên chính các tab đang mở. Lực hút tăng dần theo timeline — từ *tiết kiệm thời gian đọc* lên *tiết kiệm cả quy trình làm việc*.

- **Anxiety (Lo âu khi chuyển):** (a) Nguồn nó dẫn có thật và có đúng ý không — AI vẫn có thể trích sai hoặc trích nguồn kém chất lượng; (b) rời Google thì mất các thứ đã quen: Maps, Shopping, lịch sử, tài khoản; (c) với Comet, mức lo cao hơn hẳn vì phải giao quyền truy cập tab đã đăng nhập, email, thông tin thanh toán — rủi ro prompt injection là rủi ro thật, không phải cảm tính; (d) lo một startup nhỏ sẽ tăng giá, đổi mô hình hoặc biến mất.

- **Habit (Thói quen giữ lại):** Google là mặc định trong thanh địa chỉ của Chrome và Safari — người dùng không "chọn" Google, họ chỉ gõ. Ctrl+T rồi gõ thẳng câu hỏi là phản xạ, không phải quyết định. Với nhóm trẻ hơn, ChatGPT đã kịp trở thành phản xạ mới. Đổi search engine không tốn tiền, nhưng tốn việc phá một phản xạ ngày làm vài chục lần.

- **Lực giữ chân mạnh nhất: Habit, và cụ thể hơn là *điểm phân phối mặc định*.** Không phải chất lượng câu trả lời của Google — Perplexity đã thắng ở nhiều loại truy vấn. Vấn đề là người dùng không bao giờ đi tới nơi để so sánh.

  Đây chính là điều giải thích toàn bộ nửa sau của timeline: **Comet (Mốc 6) không phải là một tính năng, nó là câu trả lời cho lực giữ chân này.** Nếu lực giữ chân là "người dùng gõ vào thanh địa chỉ mặc định", thì cách duy nhất để thắng là *sở hữu thanh địa chỉ đó*. Và nếu phải sở hữu thanh địa chỉ thì không thể bán nó giá $200/tháng — nên nó phải miễn phí (Mốc 8), nên phải gọi $200M để bù (Mốc 8). Chuỗi này là chuỗi nhân quả chặt nhất trong cả timeline.

---

## §3. Ba Dự đoán Hướng đi (6–12 tháng tới)

### Dự đoán 1 — Trọng tâm sản phẩm dịch hẳn về trình duyệt/trợ lý; tìm kiếm web thành hàng miễn phí, và Perplexity sẽ ký thêm các hợp đồng đặt sẵn ở cấp thiết bị/nhà mạng

**Lập luận:** Dẫn truyền từ **Mốc 6 → 8 ở §1** và **lực giữ chân "phân phối mặc định" ở §2**. Khi đã kết luận rằng rào cản thật là thói quen chứ không phải chất lượng, chỉ có hai đường đi: mua điểm phân phối, hoặc trở thành điểm phân phối. Vòng $200M ở định giá ~$20B được công bố gắn thẳng với việc scale Comet miễn phí — tức là tiền đang được phân bổ cho phân phối, không cho tính năng. Dấu hiệu sớm cần theo dõi: các thỏa thuận cài sẵn trên điện thoại và trong gói cước nhà mạng. *(Có nguồn thứ cấp nhắc tới việc Comet cấp nguồn cho Bixby trên Galaxy S26 — tôi đưa vào đây như tín hiệu cần kiểm, không như dữ kiện đã xác nhận; xem mục "Chưa kiểm chứng được".)*

**Nếu tôi sai:** trường hợp Perplexity thu hẹp lại, bán Comet như tính năng của gói trả phí thay vì kênh phân phối đại chúng — điều đó có nghĩa chi phí giữ chân người dùng free vượt quá khả năng chịu đựng, và họ đang quay về mô hình subscription thuần.

### Dự đoán 2 — Thương mại (commerce) trở thành trục doanh thu thứ hai, thay cho quảng cáo hiển thị, dưới dạng phí giao dịch / affiliate / phí merchant chứ không phải banner

**Lập luận:** Dẫn truyền từ **Mốc 2** (từ chối mô hình quảng cáo để giữ trung lập của câu trả lời) và **Mốc 4** (Buy with Pro + hạ tầng thanh toán). Hai mốc này gộp lại tạo ra một ràng buộc rất cụ thể: cần tiền từ truy vấn thương mại, nhưng không được bán vị trí trong câu trả lời. Cách duy nhất còn lại là ăn ở khâu giao dịch — sau khi người dùng đã chọn. Điều này khớp với việc tệp hiện tại (§2) đã dịch sang JTBD "ra quyết định mua", và khớp với hướng dựng hạ tầng thanh toán cho agent.

**Điểm căng cần theo dõi:** ranh giới giữa "phí giao dịch" và "trả tiền để được xuất hiện trong câu trả lời" rất mỏng. Nếu Perplexity bước qua ranh giới đó, họ phá chính nguyên lý ở Mốc 2 — và đó sẽ là mốc teardown quan trọng nhất của năm sau.

### Dự đoán 3 — Quan hệ với nhà xuất bản bị đẩy từ "chương trình tự nguyện" sang "hợp đồng có giá và có phán quyết", dưới sức ép pháp lý

**Lập luận:** Dẫn truyền từ **Mốc 3 → Mốc 7 ở §1**. Đường đi đã rất rõ: chia doanh thu tự nguyện (2024) → định giá 80/20 và tính cả *agent traffic* (2025). Mỗi bước đều là phản ứng với áp lực từ bên ngoài chứ không phải sáng kiến chủ động, và mỗi bước đều đắt hơn bước trước. Bước tiếp theo hợp lý là hợp đồng cấp phép song phương với các nhà xuất bản lớn, đồng thời với việc một số vụ kiện đi tới phán quyết hoặc dàn xếp — và phán quyết đó sẽ ấn định giá sàn cho toàn ngành.

Điều này nối trực tiếp với căng thẳng đã nêu ở §2: nguyên lý gốc "dẫn nguồn" vốn là một cam kết đạo đức với người dùng có khả năng kiểm chứng; đến đây nó bị chuyển hóa thành một **khoản chi phí đầu vào có giá thị trường**. Khi trích dẫn có giá, số lượng và chất lượng nguồn được dẫn sẽ chịu ràng buộc kinh tế — đó là rủi ro dài hạn với chính lời hứa ban đầu của sản phẩm.

---

## §4. AI Log

| Công việc | AI làm hay tôi làm? | Tôi kiểm chứng & phán đoán lại thế nào? |
| :--- | :--- | :--- |
| Chọn sản phẩm & viết lý do chọn | **Tôi làm.** | Lập luận loại ChatGPT là phán đoán của tôi về scope so với giới hạn 120 phút, không phải gợi ý của AI. |
| Tra cứu mốc thời gian và link nguồn | **AI làm** (web search). | Tôi yêu cầu AI chỉ dùng mốc có link công khai và ghi rõ mốc nào chỉ có nguồn thứ cấp. Các mốc chính (Deep Research 14/02/2025, Publishers' Program 30/07/2024, Comet 09/07/2025, Comet free 02/10/2025) đều được đối chiếu ở ít nhất hai nguồn độc lập. Blog chính chủ của Perplexity trả về HTTP 403 khi truy cập tự động nên **không mốc nào trong memo này được xác nhận trực tiếp từ trang chủ** — tôi ghi nhận hạn chế này thay vì giấu đi. |
| Suy ra "nguyên lý cốt lõi" từ mỗi mốc | **Cả hai, tôi chốt.** | AI đề xuất cách diễn đạt; tôi loại các nguyên lý chỉ là mô tả tính năng viết lại ("ra mắt trình duyệt AI" không phải nguyên lý). Tiêu chí tôi áp: một nguyên lý phải giải thích được ít nhất một mốc *khác* trong bảng, nếu không thì nó chỉ là caption. |
| Chọn mốc để loại | **Tôi làm.** | Tôi loại các vòng gọi vốn và các lần đổi mô hình nền vì chúng không đổi định nghĩa sản phẩm. Riêng vòng 06/2026 tôi giữ lại vì nó gắn trực tiếp với quyết định phát Comet miễn phí. |
| Phân tích JTBD & 4 Forces | **Tôi làm,** AI phản biện. | Điểm tôi tự sửa sau khi rà lại: bản đầu tôi viết lực giữ chân mạnh nhất là "chất lượng của Google". Sai — Perplexity đã thắng Google ở nhiều loại truy vấn mà vẫn không giành được người dùng. Lực giữ chân thật là *thói quen ở điểm phân phối mặc định*, và chính cách đọc này mới giải thích được vì sao Comet tồn tại. |
| Ba dự đoán | **Tôi làm.** | Mỗi dự đoán bắt buộc phải dẫn về ít nhất một mốc ở §1 và một lực ở §2; dự đoán nào không dẫn được thì bỏ. Tôi cũng ghi kèm điều kiện chứng minh mình sai cho Dự đoán 1 và điểm căng cần theo dõi cho Dự đoán 2 — dự đoán không có điều kiện bác bỏ thì không kiểm được. |
| Viết & biên tập văn bản | **AI soạn bản nháp theo dàn ý của tôi, tôi biên tập.** | Tôi cắt các đoạn AI viết trơn nhưng rỗng, và giữ lại các chỗ có phán đoán riêng dù diễn đạt kém mượt hơn. |

---

## Chưa kiểm chứng được trong bản này

Ghi lại trung thực để người đọc biết chỗ nào cần tự kiểm:

1. **Ngày chính xác của mốc Copilot/Pro (Mốc 2).** Tôi chỉ truy được mức giá $20/tháng và mô tả tính năng, không truy được thông cáo gốc có ngày cụ thể. Vì vậy tôi ghi "giữa 2023" thay vì bịa một ngày.
2. **Đề nghị mua lại Chrome (08/2025)** — nhắc trong phần mốc bị loại, chưa truy được nguồn sơ cấp.
3. **Comet cấp nguồn cho Bixby trên Galaxy S26** — chỉ có nguồn thứ cấp bậc thấp (blog thống kê), chưa có thông cáo từ Samsung hoặc Perplexity. Đưa vào Dự đoán 1 như tín hiệu, không như dữ kiện.
4. **Các vụ kiện bản quyền cụ thể** làm nền cho Dự đoán 3 — tôi biết là có nhưng không kịp truy nguồn hồ sơ trong thời gian làm bài, nên đã viết dự đoán ở dạng chung thay vì nêu tên vụ kiện.
5. **Các con số doanh thu/người dùng 2026** (~$450M ARR, ~3 triệu MAU của Comet) xuất hiện trong kết quả tìm kiếm nhưng chỉ từ các trang tổng hợp thống kê không công bố phương pháp. **Tôi cố ý không đưa vào memo** vì không truy được nguồn gốc.

---

## Nguồn

| Nội dung | Nguồn | Link |
| :--- | :--- | :--- |
| Thành lập & ra mắt 12/2022 | Britannica Money | https://www.britannica.com/money/Perplexity-AI |
| Bối cảnh ra mắt, Copilot | Built In | https://builtin.com/artificial-intelligence/what-is-perplexity-ai |
| Giá Pro/Max | Suprmind (tổng hợp) | https://suprmind.ai/hub/perplexity/pricing/ |
| Publishers' Program 30/07/2024 & vụ Forbes/Wired | CNBC | https://www.cnbc.com/2024/07/30/perplexity-ai-to-share-revenue-with-publishers-after-plagiarism-accusations.html |
| Buy with Pro 18/11/2024 | TechResearchOnline / Stellagent | https://techresearchonline.com/news/perplexity-buy-with-pro-ai-shopping-agent/ |
| Deep Research 14/02/2025 | TechCrunch | https://techcrunch.com/2025/02/15/perplexity-launches-its-own-freemium-deep-research-product/ |
| Deep Research — đánh giá độc lập | Simon Willison | https://simonwillison.net/2025/Feb/16/introducing-perplexity-deep-research/ |
| Comet ra mắt 09/07/2025 | UPI | https://www.upi.com/Top_News/US/2025/07/09/bc-us-perplexity-comet-browser-launch/5911752083534/ |
| Comet Plus 25/08/2025, chia 80% | Search Engine Journal | https://www.searchenginejournal.com/perplexity-launches-comet-plus-shares-revenue-with-publishers/554596/ |
| Comet Plus — phân tích | Forbes | https://www.forbes.com/sites/anishasircar/2025/08/28/perplexitys-comet-plus--legal-peace-offering-or-new-dawn-for-publishers-in-the-ai-era/ |
| Comet miễn phí toàn cầu 02/10/2025 | CNBC | https://www.cnbc.com/2025/10/02/perplexity-ai-comet-browser-free-.html |
| Vòng $200M @ ~$20B, 06/2026 | Dealroom | https://app.dealroom.co/news/feed/perplexity-raises-200m-at-20b-valuation-to-scale-free-comet-browser-in-race-for-ai-agent-economy |

*Ngày truy cập toàn bộ nguồn: 14/08/2026. Trang blog chính chủ perplexity.ai/hub/blog trả về HTTP 403 với công cụ truy cập tự động, nên các mốc trong memo được xác nhận qua nguồn báo chí thứ cấp, đối chiếu tối thiểu hai nguồn với các mốc chính.*