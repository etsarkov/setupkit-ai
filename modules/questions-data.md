# SetupKit 0.19.1 · DATA question definitions (individual activation only)

Block: questions-data. Updated: 2026-10-20.
Required instructions: [core](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19.1/STARTER.md), [question-dialogue](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19.1/modules/question-dialogue.md). Reuse complete text already available; read only what is missing.
Copy help: https://setupkit.ai/kit/0.19.1/questions-data/

Missing core: say only “Open [the instructions](URL), copy the text and paste it here; I'll use your available answers” in the person's language. URL: https://setupkit.ai/kit/0.19.1/; localize as https://setupkit.ai/<lang>/kit/0.19.1/ (es/pt/ja/de/fr/ru/zh). No codes or extra steps.

Loading this family does not activate every question. Ask only individually relevant missing meanings.

### DATA-01 — DATA

Question: Which data categories do you handle: public, internal, client, personal, medical, legal, financial, or secret?

Why: Name categories, not the secrets themselves. The category controls where data may be read, stored, or sent.

Effect / if deferred: Uploading and connecting sources. Continue unrelated useful work.

### DATA-02 — DATA

Question: Which data must never be sent to external models or services?

Why: Sending includes uploads, pasted text, and connector transfers. When uncertain, keep the data local.

Effect / if deferred: External data transfer. Continue unrelated useful work.

### DATA-03 — DATA

Question: May work preferences persist between sessions?

Why: Persistence avoids repeating the interview, but secrets and sensitive details still must not be stored.

Effect / if deferred: Durable profile and memory. Continue unrelated useful work.

### DATA-04 — DATA

Question: Where may the profile live: local only, private repository, managed company storage, or nowhere?

Why: Storage controls who may see the profile and whether sync or Git may include it. Show the exact path before writing.

Effect / if deferred: Profile creation. Continue unrelated useful work.

### DATA-05 — DATA

Question: How long should open questions and change history be retained?

Why: A shorter retention period reduces stale personal context. Examples include until answered, 90 days, or until manual removal.

Effect / if deferred: Retention policy. Continue unrelated useful work.

### DATA-06 — DATA

Question: Who besides you may read shared instructions?

Why: This affects which personal preferences are safe in a team-visible file.

Effect / if deferred: Shared placement. Continue unrelated useful work.

### DATA-07 — DATA

Question: Should there be a recurring review of stale context?

Why: A review may propose changes but must not delete information automatically.

Effect / if deferred: Review cadence. Continue unrelated useful work.

END OF SETUPKIT BLOCK questions-data 0.19.1
