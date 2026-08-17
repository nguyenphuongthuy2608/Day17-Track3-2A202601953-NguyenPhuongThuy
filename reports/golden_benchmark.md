# Lab 17 Golden Set Report

- Implementation: `student`
- Kind: `golden`
- Cases: **20**
- Passed: **19/20**
- Evidence hit rate: **95.0%**
- Average retrieval latency: **1043.5 ms**
- Average token reduction vs full source context: **4.2%**
- Golden bonus: **0/10** (100% required)

| Case | Layer | Pass | Latency ms | Retrieved tokens | Token reduction | Missing / Error |
| --- | --- | --- | ---: | ---: | ---: | --- |
| G01 | short_term | PASS | 0.2 | 227 | 0.0% |  |
| G02 | short_term | PASS | 0.0 | 133 | 0.0% |  |
| G06 | long_term | PASS | 1458.8 | 829 | 0.0% |  |
| G09 | semantic | PASS | 227.7 | 418 | 8.9% |  |
| G10 | semantic | PASS | 574.9 | 270 | 41.2% |  |
| G14 | mixed | PASS | 1639.9 | 581 | 0.0% |  |
| G03 | long_term | PASS | 1357.6 | 1442 | 0.0% |  |
| G04 | long_term | PASS | 1340.8 | 1448 | 0.0% |  |
| G07 | episodic | PASS | 218.9 | 834 | 0.0% |  |
| G08 | episodic | PASS | 244.6 | 852 | 0.0% |  |
| G11 | mixed | PASS | 1658.9 | 581 | 0.0% |  |
| G13 | mixed | PASS | 431.1 | 500 | 11.5% |  |
| G15 | mixed | PASS | 1886.8 | 831 | 0.0% |  |
| G16 | mixed | PASS | 1651.8 | 581 | 0.0% |  |
| G17 | mixed | PASS | 1650.5 | 581 | 0.0% |  |
| G18 | mixed | FAIL | 454.3 | 500 | 11.5% | missing=connection churn, BUDGET-10-4-3-3 |
| G19 | mixed | PASS | 1664.9 | 581 | 0.0% |  |
| G05 | long_term | PASS | 1327.0 | 1440 | 0.0% |  |
| G12 | mixed | PASS | 1450.5 | 560 | 11.4% |  |
| G20 | mixed | PASS | 1631.4 | 756 | 0.0% |  |

## Evidence excerpts

### G01 - short_term

`<SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. | assistant: Noted staging constraint. | user: Filler A about button padding. | assistant: Filler A. | user: Filler B about color tokens. | assistant: Filler B. | user: Filler C about copy tone. | assistant: Filler C. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. - user: Constraint HOLD-BETA-STAGING: writes go to staging DB only. - assistant: Noted staging constraint. </DURA`

### G02 - short_term

`<RECENT_TURNS> user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </RECENT_TURNS>`

### G06 - long_term

`<USER_SUMMARY> Lan is working on a project titled LOTUS-88.  Lan prefers using Java and Spring Boot for backend development.  The user has instructed that Python should not be used in backend examples. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-01 11:00:00     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Lan Tran" }: Toi la Lan. Du an cua toi la LOTUS-88. Toi uu tien Java va Spring Boot, va khong dung Python trong vi du backend.   - Created At: 2026-08-01 11:00:20     Source: message     Content: Lab Assistant (assistant): Da hi`

### G09 - semantic

`EPISODE: For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3. metadata= EPISODE: {"id":"kb-payment-retry","entity":"Payment API Retry Policy","summary":"For POST /payments, every retryable request MUST send the same Idempotency-Key. Retry only HTTP 429 or transient 5xx errors, use exponential-backoff, and stop after max-3-retries. Marker: PAYMENT-RULE-3.","source":"internal-api-guideline-v3","updated_at":"2026-08-10T00:00:00Z"} metadata= EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal `

### G10 - semantic

`EPISODE: {"id":"kb-memory-privacy","entity":"Agent Memory Privacy Rule","summary":"Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL.","source":"memory-governance-policy","updated_at":"2026-08-12T00:00:00Z"} metadata= EPISODE: Do not persist personal data without explicit opt-in. A deletion request must remove user-scoped memory and be verified across every store. Marker: DELETE-VERIFY-ALL. metadata= EPISODE: {"id":"kb-context-budget","entity":"Memory Context Budget","summary":"Reserve bounded context for memory. This lab uses short-term 10 percent, long-term 4 percent, episodi`

### G14 - mixed

`<LONG_TERM> <USER_SUMMARY> Lan is working on a project titled LOTUS-88.  Lan prefers using Java and Spring Boot for backend development.  The user has instructed that Python should not be used in backend examples. </USER_SUMMARY>  <EPISODES> Episodes are source message or document excerpts shown in selection order.   - Created At: 2026-08-17 09:54:36     Source: message     Content: [user] {   "user_id": "lan-lab17",   "first_name": "Lan",   "last_name": "Tran",   "user_alias": "Evaluation User" }: Lan uu tien stack backend nao cho LOTUS-88?   - Created At: 2026-08-01 11:00:20     Source: message     Content: Lab Assistant (assistant): Da hieu: LOTUS-88, Java + Spring Boot cho backend exampl`

### G03 - long_term

`<USER_SUMMARY> Minh is working on a personal project named ORCHID-27, for which he prefers Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. He has a deadline to complete a benchmark report for LAB-REPORT-1600 before Friday at 16:00. He recently debugged async HTTP, increasing the timeout to 60s, but it still failed. He is also addressing a concurrency issue related to connection churn in ASYNC-FIX-20 by reusing an aiohttp ClientSession with concurrency set to 20.  Minh prefers Python and dislikes Java. He wants a demo of his personal project ORCHID-27. He is learning async/await and often confuses coroutines with Tasks. He wants explanatio`

### G04 - long_term

`<USER_SUMMARY> Minh is working on a personal project named ORCHID-27, for which he prefers Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. He has a deadline to complete a benchmark report for LAB-REPORT-1600 before Friday at 16:00. He recently debugged async HTTP, increasing the timeout to 60s, but it still failed. He is also addressing a concurrency issue related to connection churn in ASYNC-FIX-20 by reusing an aiohttp ClientSession with concurrency set to 20.  Minh prefers Python and dislikes Java. He wants a demo of his personal project ORCHID-27. He is learning async/await and often confuses coroutines with Tasks. He wants explanatio`

### G07 - episodic

`EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. metadata= EPISODE: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. metadata= EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. metadata= EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. metadata= EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. metadata= EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai timeout threshold. Ma su co ASYNC-FIX-20. m`

### G08 - episodic

`EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. metadata= EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. metadata= EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. metadata= EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. metadata= EPISODE: Hay kiem tra connection pool, lifecycle cua client va concurrency. metadata= EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection churn, khong phai t`

### G11 - mixed

`<LONG_TERM> <USER_SUMMARY> Minh is working on a personal project named ORCHID-27, for which he prefers Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. He has a deadline to complete a benchmark report for LAB-REPORT-1600 before Friday at 16:00. He recently debugged async HTTP, increasing the timeout to 60s, but it still failed. He is also addressing a concurrency issue related to connection churn in ASYNC-FIX-20 by reusing an aiohttp ClientSession with concurrency set to 20.  Minh prefers Python and dislikes Java. He wants a demo of his personal project ORCHID-27. He is learning async/await and often confuses coroutines with Tasks. He want`

### G13 - mixed

`<EPISODIC> EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. metadata= EPISODE: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. metadata= EPISODE: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. metadata= EPISODE: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. metadata= EPISODE: Hom nay toi debug async HTTP. Toi da thu tang timeout len 60s nhung van fail. metadata= EPISODE: Cach hieu qua la reuse aiohttp ClientSession va dat concurrency=20. Reflection: loi chinh la connection ch`

### G15 - mixed

`<LONG_TERM> <USER_SUMMARY> Minh is working on a personal project named ORCHID-27, for which he prefers Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. He has a deadline to complete a benchmark report for LAB-REPORT-1600 before Friday at 16:00. He recently debugged async HTTP, increasing the timeout to 60s, but it still failed. He is also addressing a concurrency issue related to connection churn in ASYNC-FIX-20 by reusing an aiohttp ClientSession with concurrency set to 20.  Minh prefers Python and dislikes Java. He wants a demo of his personal project ORCHID-27. He is learning async/await and often confuses coroutines with Tasks. He want`

### G16 - mixed

`<LONG_TERM> <USER_SUMMARY> Minh is working on a personal project named ORCHID-27, for which he prefers Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. He has a deadline to complete a benchmark report for LAB-REPORT-1600 before Friday at 16:00. He recently debugged async HTTP, increasing the timeout to 60s, but it still failed. He is also addressing a concurrency issue related to connection churn in ASYNC-FIX-20 by reusing an aiohttp ClientSession with concurrency set to 20.  Minh prefers Python and dislikes Java. He wants a demo of his personal project ORCHID-27. He is learning async/await and often confuses coroutines with Tasks. He want`

### G17 - mixed

`<LONG_TERM> <USER_SUMMARY> Minh is working on a personal project named ORCHID-27, for which he prefers Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. He has a deadline to complete a benchmark report for LAB-REPORT-1600 before Friday at 16:00. He recently debugged async HTTP, increasing the timeout to 60s, but it still failed. He is also addressing a concurrency issue related to connection churn in ASYNC-FIX-20 by reusing an aiohttp ClientSession with concurrency set to 20.  Minh prefers Python and dislikes Java. He wants a demo of his personal project ORCHID-27. He is learning async/await and often confuses coroutines with Tasks. He want`

### G18 - mixed

`<EPISODIC> EPISODE: Minh sap viet script ca nhan de tai hien su co latency, muon code dung ngon ngu minh thich khi lam mot minh, dong thoi bam sat playbook incident cua lab chu dung vo tang timeout. Ghep hai manh: stack ca nhan cua Minh, va buoc bat buoc trong playbook truoc khi noi timeout. Dung lay stack cua ai khac. metadata= EPISODE: Minh con mot open-loop phai nop truoc deadline, dong thoi muon ghi chu retry payment dung so lan toi da theo policy. Nac lai ma task/deadline con dang do, va gioi han retry chinh thuc trong lab. metadata= EPISODE: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. metadata= EPISODE: Da hieu`

### G19 - mixed

`<LONG_TERM> <USER_SUMMARY> Minh is working on a personal project named ORCHID-27, for which he prefers Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. He has a deadline to complete a benchmark report for LAB-REPORT-1600 before Friday at 16:00. He recently debugged async HTTP, increasing the timeout to 60s, but it still failed. He is also addressing a concurrency issue related to connection churn in ASYNC-FIX-20 by reusing an aiohttp ClientSession with concurrency set to 20.  Minh prefers Python and dislikes Java. He wants a demo of his personal project ORCHID-27. He is learning async/await and often confuses coroutines with Tasks. He want`

### G05 - long_term

`<USER_SUMMARY> Minh is working on a personal project named ORCHID-27, for which he prefers Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. He has a deadline to complete a benchmark report for LAB-REPORT-1600 before Friday at 16:00. He recently debugged async HTTP, increasing the timeout to 60s, but it still failed. He is also addressing a concurrency issue related to connection churn in ASYNC-FIX-20 by reusing an aiohttp ClientSession with concurrency set to 20.  Minh prefers Python and dislikes Java. He wants a demo of his personal project ORCHID-27. He is learning async/await and often confuses coroutines with Tasks. He wants explanatio`

### G12 - mixed

`<LONG_TERM> <USER_SUMMARY> Minh is working on a personal project named ORCHID-27, for which he prefers Python. For the company project BLUEBIRD-42, the backend must use TypeScript with NestJS, not Python. He has a deadline to complete a benchmark report for LAB-REPORT-1600 before Friday at 16:00. He recently debugged async HTTP, increasing the timeout to 60s, but it still failed. He is also addressing a concurrency issue related to connection churn in ASYNC-FIX-20 by reusing an aiohttp ClientSession with concurrency set to 20.  Minh prefers Python and dislikes Java. He wants a demo of his personal project ORCHID-27. He is learning async/await and often confuses coroutines with Tasks. He want`

### G20 - mixed

`<SHORT_TERM> <SESSION_SUMMARY> user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. | assistant: Noted standup constraint. | user: Filler about dashboard widgets. | assistant: Filler. | user: Filler about CSS variables. | assistant: Filler. | user: Filler about copy review. | assistant: Filler. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint HOLD-ALPHA-0900: standup is 09:00 sharp and must not be forgotten. - assistant: Noted standup constraint. </DURABLE_NOTES> <RECENT_TURNS> user: Filler about empty charts. assistant: Filler. user: Filler about telemetry. assistant: Filler. user: Filler about a11y labels. assistant: Filler. </RECENT_TURNS> </SHORT_TERM>`
