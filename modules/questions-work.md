# SetupKit 0.19 · WORK question definitions (individual activation only)

Block: questions-work. Updated: 2026-10-19.
Required instructions: [core](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19/STARTER.md), [question-dialogue](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19/modules/question-dialogue.md). Reuse complete text already available; read only what is missing.
Copy help: https://setupkit.ai/kit/0.19/questions-work/

Missing core: say only “Open [the instructions](URL), copy the text and paste it here; I'll use your available answers” in the person's language. URL: https://setupkit.ai/kit/0.19/; localize as https://setupkit.ai/<lang>/kit/0.19/ (es/pt/ja/de/fr/ru/zh). No codes or extra steps.

Loading this family does not activate every question. Ask only individually relevant missing meanings.

### WORK-01 — WORK

Question: Where does current information live: files, Notion, Drive, GitHub, email, Slack, or elsewhere?

Why: Name places the AI should check before concluding. Connection to them is a separate decision.

Effect / if deferred: None. Continue unrelated useful work.

### WORK-02 — WORK

Question: Which source wins when documents conflict?

Why: A canonical source is the place trusted as current. Without one, the AI must surface the conflict and ask.

Effect / if deferred: None. Continue unrelated useful work.

### WORK-03 — WORK

Question: How should drafts, accepted decisions, completed actions, and verified results be distinguished?

Why: These states are not equivalent: written text is not published, and a sent command does not prove success.

Effect / if deferred: None. Continue unrelated useful work.

### WORK-04 — WORK

Question: Are change, decision, source, and completion-evidence logs needed?

Why: These briefly record what changed, why, which sources supported it, and how the result was checked.

Effect / if deferred: None. Continue unrelated useful work.

### WORK-05 — WORK

Question: What should happen to stale information?

Why: It may be dated, archived, or require confirmation before use. Never delete it automatically.

Effect / if deferred: None. Continue unrelated useful work.

### WORK-06 — WORK

Question: What must remain after work is handed to another person or AI?

Why: Useful handoff material includes status, sources, open questions, and the next safe step.

Effect / if deferred: None. Continue unrelated useful work.

### WORK-07 — WORK

Question: Are there decisions you have already made that the assistant should take into account and not suggest revisiting without a reason?

Why: For example, where you keep the main documents or an approach you have already ruled out. Add only decisions missing from the list we already have.

Effect / if deferred: This helps preserve earlier choices and avoids going through the same discussion again. If there are no such decisions or you do not want to add them now, keep only what is actually known. Do not invent past decisions or create an empty file.

Activate / reuse: A useful decision record is chosen and earlier decisions may be missing. First show/reuse known decisions; ask only the missing part, not for reconfirmation of the entire history. Reuse confirmed applicable answers and selected sources first. Relevant IDs: WORK-02, WORK-03, WORK-04, WORK-05, CTX-03, GOAL-07. A recording preference, value, constraint or assistant suggestion is not automatically a historical decision. A statement can serve multiple purposes when its actual confirmed meaning supports them.

END OF SETUPKIT BLOCK questions-work 0.19
