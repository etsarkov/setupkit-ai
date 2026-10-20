# SetupKit 0.19.1 · GOAL question definitions (individual activation only)

Block: questions-goal. Updated: 2026-10-20.
Required instructions: [core](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19.1/STARTER.md), [question-dialogue](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19.1/modules/question-dialogue.md). Reuse complete text already available; read only what is missing.
Copy help: https://setupkit.ai/kit/0.19.1/questions-goal/

Missing core: say only “Open [the instructions](URL), copy the text and paste it here; I'll use your available answers” in the person's language. URL: https://setupkit.ai/kit/0.19.1/; localize as https://setupkit.ai/<lang>/kit/0.19.1/ (es/pt/ja/de/fr/ru/zh). No codes or extra steps.

Loading this family does not activate every question. Ask only individually relevant missing meanings.

### GOAL-01 — GOAL

Question: What would a good result look like after 30 days of using AI?

Why: Describe an observable change, such as reducing report preparation from two days to one, rather than “be more efficient.”

Effect / if deferred: None. Continue unrelated useful work.

### GOAL-02 — GOAL

Question: Which matters most: speed, quality, time saved, lower risk, learning, or scale? Please rank them.

Why: These goals can conflict. The ranking helps the AI choose tradeoffs.

Effect / if deferred: None. Continue unrelated useful work.

### GOAL-03 — GOAL

Question: Which mistakes would be inconvenient, and which could cost money, trust, health, rights, or reputation?

Why: This distinguishes tasks needing a quick check from those needing stronger evidence and human approval.

Effect / if deferred: None. Continue unrelated useful work.

### GOAL-04 — GOAL

Question: Are there tasks the AI must never perform?

Why: These are standing prohibitions that urgency or convenience cannot override, such as sending messages in your name or making medical decisions.

Effect / if deferred: None. Continue unrelated useful work.

### GOAL-05 — GOAL

Question: How should value be measured: hours saved, completed outcomes, quality, revenue, fewer errors, or something else?

Why: A simple observable measure helps determine whether the setup actually works and can be revised later.

Effect / if deferred: None. Continue unrelated useful work.

### GOAL-06 — GOAL

Question: What result are you working towards in your work, studies or personal life? If there is more than one, which matters most now?

Why: For example, finish a course, find your first clients or complete a project. Mention a date if one matters; you do not need to plan your whole life.

Effect / if deferred: This gives the assistant a real outcome to support and a way to prioritize its suggestions. If the goal is not clear yet, offer help choosing one small useful task. Keep possible goals labeled as proposals, not settled plans.

Activate / reuse: The chosen goals/context task needs a concrete underlying goal that CORE-02/GOAL-01 or current task facts did not supply. Reuse confirmed applicable answers and selected sources first. Relevant IDs: CORE-02, GOAL-01, GOAL-02, GOAL-05, PROD-02. A real outcome supplied in an AI-use answer is sufficient. Do not re-ask it or activate product questions for non-product work.

### GOAL-07 — GOAL

Question: What should we take into account to make the plan realistic for you?

Why: For example, you have two hours a week, a fixed deadline or need to fit around other work. Approximate limits are enough; no private financial or health details are needed.

Effect / if deferred: This changes the size, pace and order of the proposed steps. If the limits are unclear, propose a small reversible next step with assumptions shown. Do not promise a schedule or authorize spending.

Activate / reuse: A proposed plan could be unrealistic without a specific missing constraint; ask after choosing the relevant goal and reuse stated constraints first. Reuse confirmed applicable answers and selected sources first. Relevant IDs: CORE-02, GOAL-01, AUTH-06, PROD-03. Reuse exact known limits where relevant. Spending permission is not total resource availability; available budget is not permission to spend.

END OF SETUPKIT BLOCK questions-goal 0.19.1
