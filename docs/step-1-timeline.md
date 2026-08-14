
# Step 1 — Timeline & Revert nguyên lý

## Sản phẩm

**Perplexity**

**Nhóm sản phẩm:** AI-native
**Phạm vi phân tích:** Từ AI Answer Engine → Research → Action → Creation → AI Browser → Agentic Execution

---

## 1. Product Narrative

Perplexity khởi đầu với một proposition tương đối rõ:

> Thay vì đưa cho người dùng một danh sách đường link, hãy trực tiếp tổng hợp câu trả lời từ web và cho phép người dùng kiểm chứng thông tin qua citation.

Tuy nhiên, timeline sản phẩm cho thấy Perplexity không dừng lại ở việc cải thiện search.

Sản phẩm dần mở rộng phạm vi công việc mà người dùng có thể giao cho AI:

```text
SEARCH
"Find information for me"

        ↓

ANSWER
"Answer my question"

        ↓

RESEARCH
"Research this problem for me"

        ↓

CREATE
"Create the output for me"

        ↓

ACT
"Take action for me"

        ↓

BROWSE
"Work with me across the web"

        ↓

EXECUTE
"Take my goal and complete the work"
```

Vì vậy, working thesis của timeline là:

> **Perplexity đang tiến hóa từ một AI Answer Engine thành một agentic work platform, trong đó AI không chỉ tìm và tổng hợp thông tin mà ngày càng đảm nhận nhiều hơn toàn bộ workflow của người dùng.**

---

# 2. Timeline các quyết định sản phẩm lớn

| Thời điểm      | Cập nhật                                                                                                                                                                                                                | Context lúc đó                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Nguyên lý                                                                                                                                                                                                                                                                                                                          | Nguồn                                                                                                                                                                                                                                                                                                                                                               |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **12/2022** | **Perplexity ra mắt Search / Answer Engine** với trải nghiệm hỏi đáp dựa trên web và citation.                                                                                                            | ChatGPT vừa được OpenAI đưa ra công chúng ngày 30/11/2022, chứng minh conversational interface có thể trở thành một cách tương tác mới với AI. Trong khi search truyền thống vẫn yêu cầu người dùng nhận danh sách link → mở nhiều trang → đọc → tự tổng hợp, Perplexity chọn một product contract khác: đưa thẳng câu trả lời nhưng vẫn giữ nguồn để kiểm chứng.                                                          | **x10 — Compress the workflow.** Giá trị không nằm ở việc làm search “tốt hơn 10%”, mà ở việc giảm mạnh chuỗi thao tác `search → mở link → đọc → tổng hợp` thành `question → answer + citations`.                                                                                             | [Perplexity Research — product progression](https://research.perplexity.ai/articles/how-ai-agents-reshape-knowledge-work) · [OpenAI — ChatGPT launch](https://openai.com/index/chatgpt/)                                                                                                                                                                            |
| **04/2024** | **Enterprise Pro** — Perplexity đưa Answer Engine vào môi trường doanh nghiệp, hỗ trợ research trên web kết hợp với nguồn thông tin nội bộ và các yêu cầu bảo mật doanh nghiệp.            | Sau giai đoạn tăng trưởng consumer, Perplexity bắt đầu cần chứng minh sản phẩm có thể tạo value trong workflow có willingness-to-pay cao hơn. Cùng thời điểm ra Enterprise Pro, công ty cũng công bố vòng vốn mới và mức định giá trên 1 tỷ USD. Enterprise research khác consumer search ở chỗ context nội bộ, privacy, security và organizational knowledge trở thành yếu tố cốt lõi.                                               | **Wrapper → Moat — Data & Workflow Moat.** Một answer engine chỉ dựa vào model có nguy cơ bị sao chép; khi đi vào dữ liệu nội bộ, security và workflow của tổ chức, sản phẩm bắt đầu tạo moat từ context và integration thay vì chỉ từ model.                                                   | [Perplexity — Enterprise Pro announcement](https://x.com/perplexity_ai/status/1782774382399557633) · [Axios — Enterprise Pro](https://www.axios.com/2024/04/23/perplexity-ai-enterprise-search-answer-engine)                                                                                                                                                       |
| **05/2024** | **Perplexity Pages** — biến kết quả research thành các page/article có cấu trúc và có thể chia sẻ.                                                                                                     | AI-generated answer bắt đầu trở nên phổ biến hơn; Google cũng bắt đầu rollout AI Overviews tại Mỹ trong tháng 5/2024. Khi việc “AI trả lời câu hỏi” dần trở thành capability có ở nhiều sản phẩm, Perplexity mở rộng downstream workflow: user không chỉ cần biết câu trả lời mà còn cần tổ chức, trình bày và chia sẻ knowledge.                                                                                                    | **Định nghĩa “tốt” — từ Answer Quality → Usable Output.** Một kết quả tốt không còn chỉ là “câu trả lời đúng”; nó phải giúp user biến research thành output có thể sử dụng hoặc chia sẻ ngay.                                                                                               | [Perplexity — Pages announcement](https://x.com/perplexity_ai/status/1796203499245506823) · [TechCrunch — Perplexity Pages](https://techcrunch.com/2024/05/30/perplexity-ais-new-feature-will-turn-your-searches-into-sharable-pages/) · [Google — AI Overviews](https://blog.google/products-and-platforms/products/search/generative-ai-google-search-may-2024/) |
| **01/2025** | **Perplexity Assistant trên Android** — mở rộng từ trả lời câu hỏi sang thực hiện action như đặt bàn, gọi xe, đặt reminder và tương tác với ứng dụng.                                      | Đầu 2025, AI industry bắt đầu chuyển trọng tâm từ chatbot sang agent. Đáng chú ý, cùng ngày 23/01/2025 OpenAI giới thiệu Operator, một agent có khả năng sử dụng browser để thực hiện tác vụ. Cuộc cạnh tranh bắt đầu chuyển từ “AI nào trả lời tốt?” sang “AI nào thực sự làm được việc?”.                                                                                                                                      | **x10 — Answer → Action.** Nếu AI đã biết người dùng nên làm gì nhưng user vẫn phải tự chuyển app và thao tác từng bước, phần lớn workflow chưa được loại bỏ. Assistant rút ngắn khoảng cách giữa insight và execution.                                                                    | [Reuters — Perplexity Assistant](https://www.reuters.com/technology/artificial-intelligence/perplexity-debuts-ai-assistant-android-challenge-alexa-chatgpt-2025-01-23/) · [OpenAI — Operator](https://openai.com/index/introducing-operator/)                                                                                                                       |
| **02/2025** | **Deep Research** — Perplexity có thể tự thực hiện hàng chục lượt search, đọc nhiều nguồn, reasoning và tạo research report.                                                                        | Cuộc cạnh tranh AI research chuyển nhanh từ single-query Q&A sang multi-step research. Google đã có Deep Research trong Gemini và OpenAI giới thiệu Deep Research đầu tháng 2/2025. Với một công ty định vị quanh research/search, chỉ trả lời từng query riêng lẻ không còn đủ khác biệt.                                                                                                                                                            | **x10 — Automate the whole job, not one step.** Thay vì user tự lặp `search → đọc → hỏi tiếp → search tiếp → tổng hợp`, AI nhận research objective và xử lý nhiều bước của job end-to-end.                                                                                                            | [Perplexity — Deep Research](https://www.perplexity.ai/hub/blog/introducing-perplexity-deep-research) · [OpenAI — Deep Research](https://openai.com/index/introducing-deep-research/)                                                                                                                                                                               |
| **05/2025** | **Perplexity Labs** — mở rộng từ research report sang tạo spreadsheet, dashboard, chart, file và mini web app; có thể sử dụng browser, code execution và các công cụ khác để hoàn thành project. | Deep Research đã giúp user có được analysis, nhưng knowledge workers thường không kết thúc công việc ở “một report”. Họ cần artifact thực tế như spreadsheet, dashboard, presentation hoặc ứng dụng. Perplexity tự mô tả tiến trình: Search dành cho người cần answer → Deep Research dành cho analysis sâu → Labs dành cho việc đưa cả project thành hiện thực.                                                                     | **Định nghĩa “tốt” — Outcome > Answer.** Thước đo value chuyển từ “AI tạo câu trả lời tốt không?” sang “AI có tạo được deliverable mà user thực sự cần không?”.                                                                                                                                | [Perplexity — Introducing Labs](https://www.perplexity.ai/hub/blog/introducing-perplexity-labs)                                                                                                                                                                                                                                                                      |
| **07/2025** | **Comet Browser** — Perplexity ra mắt browser tích hợp AI search và agent có khả năng hiểu context của trang web và thực hiện tác vụ trong quá trình browsing.                                     | Nếu Perplexity chỉ tồn tại ở`perplexity.ai`, sản phẩm vẫn phụ thuộc browser của người khác để distribution và thiếu context trên toàn bộ web workflow. Chrome vẫn thống trị browser market, trong khi các công ty AI bắt đầu coi browser là surface chiến lược cho agent. Reuters cũng đưa tin OpenAI đang chuẩn bị browser cạnh tranh Chrome ngay trong thời điểm Comet ra mắt.                                                       | **Wrapper → Moat — Own the Workflow Surface.** Thay vì chỉ là một AI wrapper nằm bên trong browser, Perplexity cố sở hữu luôn surface nơi user search, đọc và hành động. Browser mang lại distribution, context và khả năng action sâu hơn — những thứ khó tạo ra nếu AI chỉ là một website. | [Reuters — Comet launch](https://www.reuters.com/business/media-telecom/nvidia-backed-perplexity-launches-ai-powered-browser-take-google-chrome-2025-07-09/) · [Perplexity — Comet](https://www.perplexity.ai/comet)                                                                                                                                                |
| **02/2026** | **Perplexity Computer** — mở rộng sang general-purpose agent có khả năng phối hợp nhiều model và công cụ để research, design, code, deploy và xử lý project nhiều bước.                         | Sau Search, Deep Research, Labs và Comet, Perplexity đã có các mảnh capability riêng lẻ: information retrieval, reasoning, browser action, code và artifact creation. Bước tiếp theo là hợp nhất chúng thành một abstraction cao hơn: user giao**objective**, hệ thống tự lựa chọn capability và thực hiện công việc. Perplexity sau đó mô tả chính product progression của mình là `Search (2022) → Comet (2025) → Computer (2026)`. | **x10 — Copilot → Delegated Execution.** Thay vì user điều khiển AI ở từng bước, user giao outcome mong muốn và AI chịu trách nhiệm lập kế hoạch + execution. “Tốt” lúc này được đo ngày càng gần với mức độ hoàn thành công việc, không chỉ chất lượng câu trả lời.             | [Perplexity — Computer announcement](https://x.com/perplexity_ai/status/2026695550771540489) · [Perplexity Research — Search → Comet → Computer](https://research.perplexity.ai/articles/how-ai-agents-reshape-knowledge-work) · [Perplexity Changelog](https://www.perplexity.ai/changelog/what-we-shipped---february-27-2026)                                   |

---

# 3. Revert nguyên lý

Nếu bỏ tên feature và chỉ nhìn vào logic sản phẩm, 8 quyết định trên có thể được quy về một số nguyên lý chính.

## 3.1. x10 — Không tối ưu một bước, loại bỏ nhiều bước

Perplexity liên tục mở rộng scope của automation:

```text
Traditional Search

Search
→ Inspect links
→ Open pages
→ Read
→ Compare
→ Synthesize
```

### Answer Engine

```text
Question
→ Answer + Citations
```

### Deep Research

```text
Research Goal
→ Search
→ Read
→ Reason
→ Search Again
→ Compare
→ Synthesize
→ Report
```

### Computer

```text
Goal
→ Plan
→ Select tools/models
→ Execute
→ Create output
→ Complete work
```

Pattern chung:

> **Một AI product x10 không chỉ làm từng bước nhanh hơn; nó cố xóa cả chuỗi thao tác khỏi workflow của user.**

---

# 3.2. Wrapper → Moat

Một rủi ro của AI product là:

```text
LLM API
   +
UI
   =
Feature dễ copy
```

Perplexity dần bổ sung các lớp khó thay thế hơn:

```text
Search infrastructure
        +
Real-time web data
        +
Citations
        +
Enterprise private context
        +
Workflow
        +
Browser
        +
Agent execution
```

Hai mốc thể hiện rõ nhất:

### Enterprise Pro

```text
Generic Answer Engine
        ↓
Company Data + Security + Workflow
```

Moat bắt đầu đến từ **context và integration**, không chỉ model.

### Comet

```text
AI website
    ↓
AI owns browser surface
```

Moat chuyển thêm sang:

* distribution;
* workflow context;
* action surface;
* product habit.

---

# 3.3. Định nghĩa “tốt” thay đổi theo thời gian

### Giai đoạn 1 — Search

“Tốt” nghĩa là:

```text
Answer chính xác
+
Citation đáng tin cậy
```

### Giai đoạn 2 — Deep Research

“Tốt” nghĩa là:

```text
Research đầy đủ
+
Synthesis tốt
+
Report hữu ích
```

### Giai đoạn 3 — Labs

“Tốt” nghĩa là:

```text
Deliverable sử dụng được
```

### Giai đoạn 4 — Computer

“Tốt” ngày càng gần:

```text
Outcome được hoàn thành
```

Do đó:

> **Perplexity đang dịch chuyển definition of good từ answer quality sang task/outcome completion.**

---

# 4. Product Evolution

Toàn bộ timeline có thể nén thành 6 bước:

```text
2022
ANSWER
"Give me the answer."

        ↓

2024
WORKFLOW + ENTERPRISE
"Use more of my context."

        ↓

2025
RESEARCH
"Investigate this for me."

        ↓

2025
CREATE + ACT
"Create and do something for me."

        ↓

2025
BROWSER
"Work where I work."

        ↓

2026
AGENT
"Take the goal and finish the work."
```

Điểm đáng chú ý là Perplexity không pivot bằng cách bỏ hoàn toàn sản phẩm cũ.

Thay vào đó, công ty **mở rộng dần radius của job** mà AI có thể đảm nhận:

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

---

# 5. Vì sao chọn 8 mốc này?

Nhóm không lựa chọn milestone dựa trên việc feature đó nổi tiếng hay có nhiều coverage, mà dựa trên việc nó có thay đổi ít nhất một trong các yếu tố sau hay không:

1. **Core value proposition**
2. **JTBD**
3. **User segment**
4. **Product surface**
5. **Phạm vi công việc AI có thể đảm nhận**
6. **Moat / strategic position của sản phẩm**

8 milestone được giữ đều thể hiện ít nhất một thay đổi đáng kể ở các yếu tố trên.

Timeline vì vậy không nhằm trả lời:

> “Perplexity đã release những feature gì?”

Mà nhằm trả lời:

> **“Perplexity đã liên tục đưa ra những quyết định sản phẩm nào để mở rộng từ Answer Engine thành Agentic Platform?”**

---

# 6. Các mốc đã cân nhắc nhưng loại

## 6.1. iOS App — 04/2023

Perplexity ra mắt ứng dụng iOS là một milestone thực sự và quan trọng đối với distribution.

Tuy nhiên, nhóm loại mốc này khỏi timeline final vì:

```text
Web
→ Ask
→ Answer + Citation
```

sang:

```text
Mobile
→ Ask
→ Answer + Citation
```

Core JTBD hầu như không thay đổi.

Nó chủ yếu trả lời:

> “User truy cập Perplexity ở đâu?”

thay vì thay đổi:

> “Perplexity có thể làm job gì cho user?”

Trong khi timeline chỉ có 6–8 vị trí, nhóm ưu tiên các quyết định như Deep Research, Assistant, Labs, Comet và Computer vì chúng thay đổi trực tiếp phạm vi value mà sản phẩm cung cấp.

Nguồn:

[TechCrunch — Perplexity launches iOS app](https://techcrunch.com/2023/04/04/ai-powered-search-engine-perplexity-ai-lands-26m-launches-ios-app/)

---

## 6.2. Comet mở miễn phí — 10/2025

Việc mở Comet cho nhiều người dùng hơn là một quyết định distribution/pricing đáng chú ý.

Tuy nhiên, core product decision lớn hơn đã xảy ra ở **07/2025 khi Perplexity quyết định xây và ra mắt chính browser Comet**.

Do đó:

```text
Comet launch
=
Product strategy change
```

còn:

```text
Comet free rollout
=
Distribution / adoption strategy
```

Trong timeline giới hạn 8 mốc, nhóm giữ **Comet launch**.

Nguồn:

[The Verge — Comet available for free](https://www.theverge.com/news/790419/perplexity-comet-available-everyone-free)

---

# 7. Câu trả lời phản biện CP1

### Câu hỏi: Vì sao không đưa tất cả các feature vào timeline?

Vì mục tiêu của timeline không phải dựng lại changelog. Một feature chỉ được chọn khi nó phản ánh một **quyết định sản phẩm đủ lớn**, chẳng hạn thay đổi JTBD, segment, value proposition, product surface hoặc phạm vi công việc mà AI có thể thực hiện.

---

### Câu hỏi: Mốc nào nhóm đã cân nhắc nhưng cuối cùng loại?

Nhóm đã cân nhắc **iOS App 2023**. Đây là một milestone quan trọng về distribution nhưng không làm thay đổi đáng kể core JTBD: người dùng vẫn hỏi và nhận câu trả lời có citation. Vì timeline chỉ giới hạn 6–8 mốc, nhóm ưu tiên những mốc như Deep Research, Assistant, Comet và Computer vì chúng thay đổi trực tiếp loại công việc user có thể giao cho AI.

---

### Câu hỏi: Vì sao Comet đáng là một product milestone?

Comet không chỉ là thêm một feature cho Perplexity. Nó thay đổi **product surface** từ một website AI sang chính môi trường browsing của người dùng.

Điều này giúp Perplexity tiến gần hơn đến việc:

```text
see context
+
reason
+
take action
```

trong cùng workflow, đồng thời giảm phụ thuộc vào browser của bên thứ ba. Vì vậy đây là một bước **Wrapper → Moat / Workflow Ownership**, không chỉ là distribution.

---

### Câu hỏi: Vì sao Deep Research quan trọng hơn một feature search thông thường?

Deep Research thay đổi abstraction của sản phẩm.

Trước đó:

```text
User controls every query
```

Sau đó:

```text
User gives research objective
→ AI controls multiple research steps
```

Do đó, đây là bước chuyển từ **AI hỗ trợ task** sang **AI nhận một phần job hoàn chỉnh**, phù hợp nguyên lý **x10 — automate the whole job**.

---

### Câu hỏi: Vì sao Computer là mốc quan trọng nhất ở cuối timeline?

Computer tổng hợp hướng đi đã hình thành từ nhiều milestone trước:

```text
Search
+
Research
+
Reasoning
+
Browser
+
Code
+
Tools
+
Actions
```

thành một abstraction cao hơn:

```text
GOAL
 ↓
AUTONOMOUS EXECUTION
 ↓
OUTCOME
```

Điều này cho thấy Perplexity đang dịch chuyển từ **answer engine / copilot** sang **delegated agent**.

---

# 8. Kết luận Step 1

Timeline cho thấy Perplexity không đơn thuần thêm nhiều feature AI vào cùng một search product.

Có một hướng tiến hóa tương đối nhất quán:

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

Ba nguyên lý nổi bật nhất xuyên suốt timeline là:

### 1. **x10**

Loại bỏ nhiều bước trong workflow thay vì chỉ làm từng bước nhanh hơn.

### 2. **Wrapper → Moat**

Di chuyển từ capability dễ bị copy sang context, dữ liệu, workflow và surface khó thay thế hơn.

### 3. **Định nghĩa “tốt”**

Dịch chuyển từ:

```text
Good answer
```

sang:

```text
Good research
```

rồi:

```text
Useful deliverable
```

và cuối cùng:

```text
Completed outcome
```

Vì vậy, thesis của Step 1 là:

> **Perplexity đang mở rộng từ việc “giúp user biết” sang “giúp user hoàn thành công việc”, đồng thời từng bước xây moat quanh search infrastructure, workflow context và agentic execution.**

---

# 9. CP1 — Self-check

## Timeline

* [X] Có 8 milestone
* [X] Mỗi milestone là một quyết định sản phẩm lớn
* [X] Có thời điểm
* [X] Có cập nhật
* [X] Có context
* [X] Có nguyên lý được đặt tên
* [X] Có link nguồn gốc

## Revert nguyên lý

* [X] Có nguyên lý **x10**
* [X] Có nguyên lý **Wrapper → Moat**
* [X] Có nguyên lý **Định nghĩa "tốt"**
* [X] Nguyên lý gắn trực tiếp với product decision
* [X] Không sử dụng các nhãn chung chung như “tăng trưởng” hoặc “cải thiện UX”

## Phản biện

* [X] Có milestone đã cân nhắc nhưng loại
* [X] Giải thích được tại sao iOS App không đủ mạnh
* [X] Giải thích được tại sao Comet free rollout không bằng Comet launch
* [X] Giải thích được tại sao 8 milestone được giữ

---

# 10. CP1 Result

**Status: ✅ PASS — Ready for Step 2 / Memo integration**

### Final Timeline

```text
12/2022 — Answer Engine
        ↓
04/2024 — Enterprise Pro
        ↓
05/2024 — Pages
        ↓
01/2025 — Assistant
        ↓
02/2025 — Deep Research
        ↓
05/2025 — Labs
        ↓
07/2025 — Comet
        ↓
02/2026 — Computer
```

### Final Product Narrative

> **Answer Engine → Research Assistant → Creation & Action → AI Browser → Agentic Execution**

---

# References

1. **Perplexity Research — How AI Agents Reshape Knowledge Work**
   https://research.perplexity.ai/articles/how-ai-agents-reshape-knowledge-work
2. **OpenAI — Introducing ChatGPT**
   https://openai.com/index/chatgpt/
3. **Perplexity — Enterprise Pro Announcement**
   https://x.com/perplexity_ai/status/1782774382399557633
4. **Axios — Perplexity brings its Answer Engine to enterprises**
   https://www.axios.com/2024/04/23/perplexity-ai-enterprise-search-answer-engine
5. **Perplexity — Pages Announcement**
   https://x.com/perplexity_ai/status/1796203499245506823
6. **TechCrunch — Perplexity Pages**
   https://techcrunch.com/2024/05/30/perplexity-ais-new-feature-will-turn-your-searches-into-sharable-pages/
7. **Google — AI Overviews in Search**
   https://blog.google/products-and-platforms/products/search/generative-ai-google-search-may-2024/
8. **Reuters — Perplexity Assistant**
   https://www.reuters.com/technology/artificial-intelligence/perplexity-debuts-ai-assistant-android-challenge-alexa-chatgpt-2025-01-23/
9. **OpenAI — Operator**
   https://openai.com/index/introducing-operator/
10. **Perplexity — Deep Research**
    https://www.perplexity.ai/hub/blog/introducing-perplexity-deep-research
11. **OpenAI — Deep Research**
    https://openai.com/index/introducing-deep-research/
12. **Perplexity — Introducing Labs**
    https://www.perplexity.ai/hub/blog/introducing-perplexity-labs
13. **Reuters — Perplexity launches Comet**
    https://www.reuters.com/business/media-telecom/nvidia-backed-perplexity-launches-ai-powered-browser-take-google-chrome-2025-07-09/
14. **Perplexity — Comet**
    https://www.perplexity.ai/comet
15. **Perplexity — Computer Announcement**
    https://x.com/perplexity_ai/status/2026695550771540489
16. **Perplexity Changelog — Computer**
    https://www.perplexity.ai/changelog/what-we-shipped---february-27-2026
17. **TechCrunch — Perplexity iOS App**
    https://techcrunch.com/2023/04/04/ai-powered-search-engine-perplexity-ai-lands-26m-launches-ios-app/
18. **The Verge — Comet available for free**
    https://www.theverge.com/news/790419/perplexity-comet-available-everyone-free
