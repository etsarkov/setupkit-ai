# SetupKit 0.20 · TOOLS question definitions (individual activation only)

Block: questions-tools. Updated: 2026-10-21.
Required instructions: [core](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/STARTER.md), [question-dialogue](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/modules/question-dialogue.md). Reuse complete text already available; read only what is missing.
Copy help: https://setupkit.ai/kit/0.20/questions-tools/

Missing core: say only “Open [the instructions](URL), copy the text and paste it here; I'll use your available answers” in the person's language. URL: https://setupkit.ai/kit/0.20/; localize as https://setupkit.ai/<lang>/kit/0.20/ (es/pt/ja/de/fr/ru/zh). No codes or extra steps.

Loading this family does not activate every question. Ask only individually relevant missing meanings.

### TOOLS-01 — TOOLS

Question: Which applications should be used: Drive, Notion, email, calendar, Slack, GitHub, Figma, a data store, or another system?

Why: Name the scenario, such as “find documents in Drive,” rather than just the service.

Effect / if deferred: Plugin recommendations. Continue unrelated useful work.

### TOOLS-02 — TOOLS

Question: Is read-only access enough, or are changes needed?

Why: Start with minimum access. Write access may send, edit, or create objects.

Effect / if deferred: Write permissions. Continue unrelated useful work.

### TOOLS-03 — TOOLS

Question: Which accounts and workspaces are allowed?

Why: Personal and work accounts may contain different data. Limit the connection precisely.

Effect / if deferred: Connections. Continue unrelated useful work.

### TOOLS-04 — TOOLS

Question: Which data categories may be sent to each service?

Why: External transfer is data egress. Name allowed categories without placing confidential material in the profile.

Effect / if deferred: External data transfer. Continue unrelated useful work.

### TOOLS-05 — TOOLS

Question: Who approves new integrations and permissions?

Why: Technical availability is not authorization.

Effect / if deferred: Installation and connection. Continue unrelated useful work.

END OF SETUPKIT BLOCK questions-tools 0.20
