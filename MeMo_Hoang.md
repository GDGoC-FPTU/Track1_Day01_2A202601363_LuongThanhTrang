# Memo Teardown — Perplexity

**Nhóm:** T2H
**Thành viên:** Đặng Đức Hòa - 2A202601351

    Vũ Huy Hoàng - 2A202601057

    Lương Thanh Trang -2A202601363

## Vì sao chọn sản phẩm này?

Perplexity là một sản phẩm **AI-native** trong đó AI nằm ở trung tâm của trải nghiệm thay vì chỉ là một tính năng bổ sung. Sản phẩm cũng có một trajectory tương đối rõ từ **Answer Engine → Research → Creation → Browser → Agentic Execution**, đủ dữ liệu công khai để phân tích các quyết định sản phẩm, sự dịch chuyển JTBD và hướng phát triển trong tương lai.

---

# §1. Timeline các cập nhật lớn

| Thời điểm      | Cập nhật                                                                                                                                                                     | Context lúc đó                                                                                                                                                                                                                                    | Nguyên lý                                                                                                                                                                                                                                                                                                                                   |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **12/2022** | **Perplexity ra mắt Answer Engine** — thay vì chỉ trả danh sách link, hệ thống tổng hợp câu trả lời từ web và đi kèm citation.                          | ChatGPT vừa tạo ra làn sóng conversational AI. Trong khi search truyền thống vẫn yêu cầu user`search → mở nhiều link → đọc → tự tổng hợp`, Perplexity chọn cách nén workflow thành `question → answer + sources`.        | **x10 — Compress the workflow.** Giá trị không chỉ nằm ở search tốt hơn mà ở việc loại bỏ nhiều bước thủ công từ câu hỏi đến insight. [Nguồn](https://x.com/perplexity_ai/status/1732831676525650356)                                                                                                           |
| **04/2024** | **Enterprise Pro** — mở rộng Perplexity sang môi trường doanh nghiệp, kết hợp web research với knowledge nội bộ và yêu cầu privacy/security.              | Perplexity bắt đầu chuyển từ một consumer research tool sang các workflow có willingness-to-pay cao hơn. Với doanh nghiệp, generic web knowledge chưa đủ; internal context và security trở thành một phần của value proposition. | **Wrapper → Moat — Data & Workflow Moat.** Khi AI đi vào dữ liệu, permission và workflow riêng của tổ chức, moat bắt đầu đến từ context/integration chứ không chỉ model. [Nguồn](https://www.axios.com/2024/04/23/perplexity-ai-enterprise-search-answer-engine)                                                    |
| **05/2024** | **Perplexity Pages** — biến kết quả research thành article/page có cấu trúc và có thể chia sẻ.                                                               | AI trả lời câu hỏi ngày càng trở nên phổ biến. User sau research thường vẫn phải tự tổ chức lại kiến thức thành bài viết, brief hoặc output có thể chia sẻ.                                                               | **Định nghĩa “tốt” — Answer Quality → Usable Output.** Một câu trả lời tốt chưa đủ; sản phẩm bắt đầu tối ưu cho việc biến knowledge thành output sử dụng được. [Nguồn](https://techcrunch.com/2024/05/30/perplexity-ais-new-feature-will-turn-your-searches-into-sharable-pages/)                        |
| **01/2025** | **Perplexity Assistant** trên Android — không chỉ trả lời mà có thể hỗ trợ action như đặt bàn, gọi xe, tạo reminder hoặc tương tác với ứng dụng. | Cuộc cạnh tranh AI bắt đầu chuyển từ chatbot sang agent. Nhiều user intent không kết thúc ở việc “biết phải làm gì”, mà cần thực sự hoàn thành hành động tiếp theo.                                                     | **x10 — Answer → Action.** Xóa khoảng cách giữa insight và execution thay vì để user tự chuyển ứng dụng và thao tác tiếp. [Nguồn](https://www.reuters.com/technology/artificial-intelligence/perplexity-debuts-ai-assistant-android-challenge-alexa-chatgpt-2025-01-23/)                                               |
| **02/2025** | **Deep Research** — AI tự thực hiện nhiều vòng search, đọc, reasoning và tổng hợp thành research report.                                                     | Các câu hỏi chuyên sâu không thể xử lý tốt bằng single-query Q&A. User vẫn phải lặp`search → đọc → hỏi tiếp → search tiếp → tổng hợp`.                                                                                    | **x10 — Automate the whole job, not one step.** User giao research objective thay vì phải điều khiển từng query. [Nguồn](https://www.perplexity.ai/hub/blog/introducing-perplexity-deep-research)                                                                                                                                |
| **05/2025** | **Perplexity Labs** — mở rộng từ research sang tạo spreadsheet, dashboard, chart, file và các deliverable khác.                                                  | Knowledge worker thường không kết thúc workflow ở một report; họ còn phải biến insight thành artifact để sử dụng trong công việc.                                                                                                  | **Định nghĩa “tốt” — Outcome > Answer.** Value chuyển từ “AI trả lời tốt” sang “AI tạo được deliverable mà user thực sự cần”. [Nguồn](https://www.perplexity.ai/hub/blog/introducing-perplexity-labs)                                                                                                           |
| **07/2025** | **Comet Browser** — Perplexity đưa AI trực tiếp vào browser và browsing workflow.                                                                                 | Nếu AI chỉ tồn tại ở`perplexity.ai`, sản phẩm phụ thuộc browser của bên thứ ba và thiếu context của toàn bộ workflow trên web. Browser trở thành một strategic surface cho AI agent.                                          | **Wrapper → Moat — Own the Workflow Surface.** Perplexity cố sở hữu chính nơi user search, đọc và hành động để có distribution, context và khả năng execution sâu hơn. [Nguồn](https://www.reuters.com/business/media-telecom/nvidia-backed-perplexity-launches-ai-powered-browser-take-google-chrome-2025-07-09/) |
| **02/2026** | **Perplexity Computer** — hợp nhất research, reasoning, browser, code và tools để xử lý các project nhiều bước.                                              | Sau Search, Deep Research, Labs và Comet, Perplexity đã có nhiều capability riêng. Bước tiếp theo là cho user giao một**goal**, còn AI tự lựa chọn model/tool và xử lý workflow.                                             | **x10 — Copilot → Delegated Execution.** User không còn phải hướng dẫn từng bước; abstraction chuyển từ “giúp tôi” sang “hãy hoàn thành mục tiêu này”. [Nguồn](https://www.perplexity.ai/changelog/what-we-shipped---february-27-2026)                                                                         |

## Vì sao chọn những mốc này?

Nhóm ưu tiên các mốc làm thay đổi ít nhất một trong các yếu tố: **core value proposition, JTBD, user segment, product surface, moat hoặc phạm vi công việc mà AI có thể đảm nhận**. Vì vậy timeline không nhằm liệt kê changelog mà nhằm đọc Perplexity như một chuỗi quyết định sản phẩm.

Nhóm từng cân nhắc **iOS App 2023** nhưng loại khỏi timeline final. Đây là một mốc distribution quan trọng, nhưng core JTBD vẫn gần như giữ nguyên: user hỏi và nhận câu trả lời có citation. Trong khi Deep Research, Labs, Comet hay Computer thay đổi trực tiếp loại công việc user có thể giao cho AI.

Nhóm cũng loại mốc **Comet được mở miễn phí** vì đây chủ yếu là pricing/distribution decision; quyết định sản phẩm lớn hơn đã xảy ra khi Perplexity chọn xây chính một AI browser.

### Product evolution rút ra từ timeline

```text
ANSWER
   ↓
RESEARCH
   ↓
CREATE
   ↓
ACT
   ↓
OWN WORKFLOW SURFACE
   ↓
EXECUTE
```

Ba nguyên lý nổi bật xuyên suốt timeline là:

* **x10:** loại bỏ cả chuỗi thao tác thay vì chỉ tăng tốc một bước.
* **Wrapper → Moat:** chuyển từ AI capability dễ copy sang data, context, workflow và distribution surface khó thay thế hơn.
* **Định nghĩa “tốt”:** dịch từ `good answer → good research → usable deliverable → completed outcome`.

---

# §2. Tệp User & JTBD

|                                                   | **Early adopters**                                                                                                                                                                                                  | **Tệp hiện tại**                                                                                                                                                                                                                       |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Đặc điểm**                            | Student, researcher, developer hoặc tech-savvy knowledge worker thường xuyên research online, đã thử GenAI từ sớm và đặc biệt quan tâm citation/source verification.                                        | Analyst, consultant, marketer, researcher, founder hoặc enterprise knowledge worker cần research và tạo output cho công việc thực tế.                                                                                                   |
| **JTBD chính**                             | **Khi tôi cần tìm hiểu hoặc kiểm chứng một vấn đề, tôi muốn nhanh chóng nhận được câu trả lời tổng hợp từ nhiều nguồn và có citation để không phải tự đọc hàng loạt webpage.** | **Khi tôi có một vấn đề hoặc project phức tạp, tôi muốn AI tự research, phân tích, tổng hợp và tạo output ban đầu để tôi tập trung vào judgment, decision-making và phần công việc có giá trị cao hơn.** |
| **Trước đó họ làm bằng cách nào?** | Google Search/Google Scholar → mở nhiều tab → đọc → so sánh → ghi chú → tự tổng hợp; hoặc ChatGPT nhưng phải tự verify lại nguồn.                                                                     | Google + Chrome tabs + ChatGPT + Docs + Sheets + nhiều SaaS tool; user phải copy/paste và chuyển context giữa nhiều công cụ.                                                                                                            |

## Dịch chuyển tệp

Sự dịch chuyển của Perplexity không đơn giản là:

```text
Tech user
   ↓
Everyone
```

Mà chính xác hơn là:

```text
Information Seeker
        ↓
Researcher
        ↓
Knowledge Worker
        ↓
Workflow Delegator
```

**Enterprise Pro** là mốc rõ nhất làm thay đổi **ai sử dụng sản phẩm**:

```text
Individual research
        ↓
Professional / Enterprise research
```

Trong khi đó, **Deep Research → Labs → Comet → Computer** làm thay đổi mạnh **họ thuê sản phẩm để làm việc gì**:

```text
"Giúp tôi tìm câu trả lời"
        ↓
"Làm research này cho tôi"
        ↓
"Tạo output này cho tôi"
        ↓
"Giúp tôi thực hiện workflow"
        ↓
"Hãy hoàn thành mục tiêu này"
```

Vì vậy có thể tóm tắt:

> **Enterprise Pro thay đổi segment; Deep Research, Labs, Comet và Computer mở rộng JTBD.**

---

## Switching Cost — Map 4 Forces

### 1. Push — điều gì đẩy user khỏi giải pháp cũ?

Workflow truyền thống:

```text
Search
→ Scroll
→ Open tabs
→ Read
→ Compare
→ Synthesize
```

Pain point chính:

* information overload;
* nhiều SEO content/noise;
* mất thời gian mở và đọc nhiều nguồn;
* context switching giữa nhiều tool;
* generic chatbot có thể trả lời nhưng khó verify nguồn.

**Push: HIGH**

---

### 2. Pull — điều gì kéo user sang Perplexity?

Core pull ban đầu:

```text
Real-time Search
+
AI Synthesis
+
Citation
```

Sau đó được mở rộng bằng:

```text
Deep Research
+
Labs
+
Comet
+
Computer
```

User không chỉ được:

> “Tìm nhanh hơn”

mà ngày càng có thể:

> **“Giao nhiều phần của công việc cho AI.”**

**Pull: VERY HIGH**

Đây là lực mạnh nhất hiện tại.

---

### 3. Anxiety — điều gì khiến user e ngại?

Các rủi ro chính:

* hallucination;
* citation không thực sự support claim;
* source quality;
* agent action sai;
* enterprise privacy/security;
* high-stakes research vẫn cần human verification.

Khi sản phẩm chuyển:

```text
Answer
   ↓
Action
```

failure cost tăng đáng kể.

Một answer sai có thể chỉ khiến user bỏ qua.

Một agent thực hiện sai hành động có thể tạo hậu quả thực tế.

**Anxiety: MEDIUM–HIGH**

---

### 4. Habit — điều gì giữ user ở giải pháp cũ?

Perplexity phải cạnh tranh với các habit rất mạnh:

```text
"Google it"
```

và:

```text
"Ask ChatGPT"
```

Google/Chrome có:

* default position;
* bookmarks;
* passwords;
* history;
* extensions;
* ecosystem.

ChatGPT cũng đã trở thành default AI assistant của nhiều user.

**Habit: HIGH**

---

## Điều gì giữ user Perplexity ở lại mạnh nhất?

> **Pull từ trải nghiệm search + synthesis + citation vẫn là lực mạnh nhất.**

Consumer switching cost của Perplexity chưa phải hard lock-in. User vẫn có thể chuyển sang Google, ChatGPT, Gemini hoặc Claude khá dễ.

Vì vậy strategic risk lớn nhất là:

> Nếu các đối thủ cung cấp search + synthesis + citation + Deep Research tốt ngang hoặc tốt hơn, lợi thế ban đầu của Perplexity có thể bị commoditize.

Đây cũng giải thích tại sao sản phẩm liên tục mở rộng moat sang:

```text
Enterprise Context
+
Workflow
+
Comet
+
Computer
+
Agentic Execution
```

---

# §3. Ba dự đoán hướng đi trong 6–12 tháng tới

## Dự đoán 1 *(Loại: Mở rộng tính năng)*

* **Dự đoán:** Perplexity sẽ đẩy **Computer** thành một lớp workflow automation thường trực hơn, với reusable Skills/workflows, scheduling, background execution, multi-agent orchestration và tích hợp sâu hơn vào các công cụ doanh nghiệp.
* **Lập luận:** Step 1 cho thấy trajectory `Answer → Deep Research → Labs → Comet → Computer`; Step 2 cho thấy current user đang dịch sang knowledge worker muốn giao cả workflow cho AI. Do đó bước tiếp theo hợp lý không phải thêm một chatbot feature mới mà là làm cho Computer có thể chạy các workflow lặp lại và ngày càng autonomous.

Nguồn hỗ trợ:
https://www.perplexity.ai/help-center/en/articles/13901210/computer-for-enterprise

---

## Dự đoán 2 *(Loại: Thay đổi mô hình kiếm tiền)*

* **Dự đoán:** Perplexity sẽ tiếp tục chuyển từ subscription thuần túy sang mô hình **subscription + usage-based credits**, đặc biệt với các tác vụ Computer/agent có mức compute và complexity khác nhau.
* **Lập luận:** Step 1 cho thấy definition of good đang chuyển từ `answer quality → completed outcome`, tức AI đang thực hiện ngày càng nhiều “labor” thay cho user. Step 2 cũng cho thấy enterprise user có willingness-to-pay cao hơn khi AI tiết kiệm được thời gian thực tế; vì vậy monetization có xu hướng chuyển từ “trả tiền để truy cập AI” sang “trả tiền theo lượng công việc AI thực hiện”.

Nguồn hỗ trợ:
https://www.perplexity.ai/help-center/en/articles/13838041-how-credits-work-on-perplexity.html

---

## Dự đoán 3 *(Loại: Đe dọa từ Big Tech)*

* **Dự đoán:** Khi AI Search và Deep Research ngày càng bị commoditize bởi Google, OpenAI và các platform lớn, Perplexity sẽ giảm phụ thuộc vào định vị **“AI search tốt hơn”** và tiếp tục xây moat bằng **Comet + Computer + enterprise context + connectors + workflow ownership**.
* **Lập luận:** Step 1 cho thấy Perplexity đã chủ động đi từ Answer Engine sang browser và agent execution; Step 2 cho thấy consumer switching cost còn thấp. Nếu các đối thủ đạt parity về search/citation/research, Perplexity chỉ có thể giữ lợi thế bằng cách sở hữu nhiều hơn context và workflow của người dùng.

Nguồn hỗ trợ:
https://www.perplexity.ai/comet

---

## Dự đoán nhóm tự tin nhất

Nhóm tự tin nhất với **Dự đoán 1 — Computer tiếp tục tiến thành workflow/agent platform**, vì đây không phải một hướng đi hoàn toàn mới mà là continuation trực tiếp của product trajectory:

```text
Search
   ↓
Deep Research
   ↓
Labs
   ↓
Comet
   ↓
Computer
   ↓
Persistent / Automated Workflows
```

### Giả định có thể làm dự đoán này gãy

Giả định quan trọng nhất là:

> **Knowledge workers thực sự muốn giao nhiều phần workflow cho AI và giá trị tiết kiệm được lớn hơn chi phí, rủi ro và friction của agent.**

Nếu:

```text
Agent reliability thấp
+
Compute cost cao
+
Security / Compliance khó
+
User không tin AI action
        ↓
ROI không đủ tốt
```

thì enterprise user có thể chỉ sử dụng AI cho:

```text
Search
+
Research
+
Drafting
```

thay vì giao quyền thực thi workflow. Khi đó hướng `Computer → Autonomous Worker` sẽ phát triển chậm hơn và sản phẩm có thể phải giữ human-in-the-loop nhiều hơn.

---

# §4. AI Log

| Việc                                                                    | AI làm hay nhóm làm?                                                          | Nhóm kiểm chứng/phán đoán lại thế nào?                                                                                                                                                         |
| ------------------------------------------------------------------------ | -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Thu thập nguồn về Perplexity                                          | **Nhóm làm chính, AI hỗ trợ gợi ý từ khóa và nguồn tham khảo** | Nhóm trực tiếp mở Perplexity Changelog, blog chính thức, Reuters, TechCrunch, Axios và Product Hunt; chỉ giữ các nguồn có thể kiểm chứng được.                                        |
| Lập danh sách 8–10 milestone ứng viên                               | **Nhóm tổng hợp, AI hỗ trợ hệ thống hóa**                          | Từ các nguồn đã đọc, nhóm tự ghi lại các mốc ứng viên; AI hỗ trợ gom các mốc trùng và chuẩn hóa cách trình bày.                                                                |
| Chọn 8 milestone cho timeline cuối                                     | **Nhóm quyết định**                                                    | Cả nhóm so sánh mức độ ảnh hưởng của từng mốc đến JTBD, segment và value proposition; loại iOS App và Comet Free vì chủ yếu là thay đổi distribution.                            |
| Phân tích context của từng milestone                                 | **Nhóm research chính, AI hỗ trợ tóm tắt**                           | Thành viên phụ trách từng mốc đọc nguồn và xác định bối cảnh thị trường; AI chỉ hỗ trợ rút gọn và đặt lại câu cho dễ hiểu.                                                |
| Revert nguyên lý`x10`, `Wrapper → Moat`, `Định nghĩa "tốt"` | **Nhóm phân tích và map nguyên lý, AI hỗ trợ phản biện**         | Nhóm dựa trên nội dung đã học để chọn nguyên lý; sau đó kiểm tra xem nguyên lý có giải thích được quyết định sản phẩm hay không.                                           |
| Xác định Early adopters và Current users                             | **Nhóm làm chính**                                                      | Nhóm đọc review, community và positioning của Perplexity Enterprise để mô tả user cụ thể; AI hỗ trợ gom các insight tương đồng.                                                       |
| Viết JTBD                                                               | **Nhóm tự xây dựng, AI hỗ trợ chỉnh câu chữ**                     | Nhóm xác định job thực tế của từng tệp user và viết lại theo cấu trúc “khi... tôi muốn... để...”, tránh mô tả JTBD bằng tên tính năng.                                       |
| Phân tích Switching Cost và 4 Forces                                  | **Nhóm thảo luận và kết luận**                                       | Cả nhóm cùng phân tích Push, Pull, Anxiety và Habit; thống nhất Pull là lực mạnh nhất và consumer switching cost hiện chưa cao.                                                          |
| Đưa ra 3 dự đoán cho 6–12 tháng tới                              | **Mỗi thành viên tự đề xuất, cả nhóm chọn**                      | Mỗi người đưa ít nhất một dự đoán; nhóm chất vấn xem dự đoán dựa vào milestone và user/JTBD nào rồi chọn 3 nhận định có lập luận mạnh nhất. AI hỗ trợ kiểm tra logic. |
| Ghép và hoàn thiện memo                                              | **Nhóm làm chính, AI hỗ trợ diễn đạt và format**                  | Nhóm tự chọn nội dung đưa vào bản cuối, rút gọn các phần nghiên cứu, kiểm tra lại nguồn và đọc chéo toàn bộ memo trước khi nộp.                                              |

---

# Kết luận

Phân tích timeline cho thấy Perplexity không đơn thuần phát triển theo hướng “thêm nhiều AI feature hơn”.

Sản phẩm liên tục mở rộng **radius của job** mà AI có thể đảm nhận:

```text
Information
    ↓
Knowledge
    ↓
Research
    ↓
Artifact
    ↓
Action
    ↓
Workflow
    ↓
Outcome
```

Early adopters ban đầu chủ yếu thuê Perplexity để:

> **“Giúp tôi tìm và hiểu thông tin nhanh nhưng vẫn kiểm chứng được nguồn.”**

Trong khi current knowledge worker ngày càng có thể thuê sản phẩm để:

> **“Research, tạo output và thực hiện nhiều phần của workflow cho tôi.”**

Vì vậy thesis cuối cùng của nhóm là:

> **Perplexity đang dịch chuyển từ một AI Answer Engine sang một Agentic Work Platform; đồng thời moat phải dịch từ khả năng trả lời/search sang việc sở hữu context, workflow và execution của người dùng.**

---

# References

1. Perplexity Changelog
   https://www.perplexity.ai/changelog
2. Perplexity launch / first anniversary
   https://x.com/perplexity_ai/status/1732831676525650356
3. Axios — Enterprise Pro
   https://www.axios.com/2024/04/23/perplexity-ai-enterprise-search-answer-engine
4. TechCrunch — Perplexity Pages
   https://techcrunch.com/2024/05/30/perplexity-ais-new-feature-will-turn-your-searches-into-sharable-pages/
5. Reuters — Perplexity Assistant
   https://www.reuters.com/technology/artificial-intelligence/perplexity-debuts-ai-assistant-android-challenge-alexa-chatgpt-2025-01-23/
6. Perplexity — Deep Research
   https://www.perplexity.ai/hub/blog/introducing-perplexity-deep-research
7. Perplexity — Labs
   https://www.perplexity.ai/hub/blog/introducing-perplexity-labs
8. Reuters — Comet Browser
   https://www.reuters.com/business/media-telecom/nvidia-backed-perplexity-launches-ai-powered-browser-take-google-chrome-2025-07-09/
9. Perplexity — Comet
   https://www.perplexity.ai/comet
10. Perplexity — Computer
    https://www.perplexity.ai/changelog/what-we-shipped---february-27-2026
11. Perplexity Enterprise
    https://www.perplexity.ai/enterprise
12. Perplexity Enterprise Customer Stories
    https://www.perplexity.ai/enterprise/customers
13. Perplexity — Computer for Enterprise
    https://www.perplexity.ai/help-center/en/articles/13901210/computer-for-enterprise
14. Perplexity — Credits
    https://www.perplexity.ai/help-center/en/articles/13838041-how-credits-work-on-perplexity.html
