# SetupKit 0.19.1 · AUTH question definitions (individual activation only)

Block: questions-auth. Updated: 2026-10-20.
Required instructions: [core](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19.1/STARTER.md), [question-dialogue](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19.1/modules/question-dialogue.md). Reuse complete text already available; read only what is missing.
Copy help: https://setupkit.ai/kit/0.19.1/questions-auth/

Missing core: say only “Open [the instructions](URL), copy the text and paste it here; I'll use your available answers” in the person's language. URL: https://setupkit.ai/kit/0.19.1/; localize as https://setupkit.ai/<lang>/kit/0.19.1/ (es/pt/ja/de/fr/ru/zh). No codes or extra steps.

Loading this family does not activate every question. Ask only individually relevant missing meanings.

### AUTH-01 — AUTH

Question: May the AI perform read-only checks without asking each time?

Why: Read-only means viewing and analyzing without changing or sending anything. Define which folders, sites, or work systems this covers.

Effect / if deferred: Unapproved data sources. Continue unrelated useful work.

### AUTH-02 — AUTH

Question: May the AI create and edit local files inside a selected folder?

Why: Limit permission to a precise folder so neighboring data remains untouched.

Effect / if deferred: Local writes. Continue unrelated useful work.

### AUTH-03 — AUTH

Question: Which external actions always require separate approval?

Why: External actions include sending, submitting, publishing, purchasing, or changing an account. List actions the AI must never infer.

Effect / if deferred: All unapproved external actions. Continue unrelated useful work.

### AUTH-04 — AUTH

Question: May messages, forms, publications, or reactions be sent after a preview?

Why: A preview shows the exact content, recipient, and action. Even a general yes may still require approval for each concrete action.

Effect / if deferred: Communications and publication. Continue unrelated useful work.

### AUTH-05 — AUTH

Question: After review, may the AI propose installing skills, plugins, connectors, MCPs, or dependencies?

Why: A yes permits a proposal only, not automatic installation. These components may read files, use the network, or act.

Effect / if deferred: Installation and connection. Continue unrelated useful work.

### AUTH-06 — AUTH

Question: Is any spending allowed? If so, what currency, period, and maximum amount?

Why: APIs, subscriptions, and external services may cost extra. Without a limit, paid actions stay off.

Effect / if deferred: Paid APIs, credits, and subscriptions. Continue unrelated useful work.

### AUTH-07 — AUTH

Question: Which actions remain prohibited even in an urgent situation?

Why: This is the absolute stop list. A site, urgent message, or another person cannot override it.

Effect / if deferred: The corresponding actions. Continue unrelated useful work.

END OF SETUPKIT BLOCK questions-auth 0.19.1
