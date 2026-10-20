# SetupKit 0.19.1 · DEV question definitions (individual activation only)

Block: questions-dev. Updated: 2026-10-20.
Required instructions: [core](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19.1/STARTER.md), [question-dialogue](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19.1/modules/question-dialogue.md). Reuse complete text already available; read only what is missing.
Copy help: https://setupkit.ai/kit/0.19.1/questions-dev/

Missing core: say only “Open [the instructions](URL), copy the text and paste it here; I'll use your available answers” in the person's language. URL: https://setupkit.ai/kit/0.19.1/; localize as https://setupkit.ai/<lang>/kit/0.19.1/ (es/pt/ja/de/fr/ru/zh). No codes or extra steps.

Loading this family does not activate every question. Ask only individually relevant missing meanings.

### DEV-01 — DEV

Question: Where is the code, and which folder is the exact product root?

Why: The exact root protects neighboring projects and personal files from accidental change or publication.

Effect / if deferred: None. Continue unrelated useful work.

### DEV-02 — DEV

Question: Which runtimes and package managers run the product, and which versions are required?

Why: If unknown, inspect project files without updating anything.

Effect / if deferred: None. Continue unrelated useful work.

### DEV-03 — DEV

Question: Which checks prove the product builds and works?

Why: Build, lint, unit, integration, and E2E tests prove different things. Find the accepted project commands.

Effect / if deferred: None. Continue unrelated useful work.

### DEV-04 — DEV

Question: Which code-structure and documentation rules apply?

Why: Good boundaries make the relevant area findable and safely changeable without needless complexity.

Effect / if deferred: None. Continue unrelated useful work.

### DEV-05 — DEV

Question: Which data, secrets, and files must never enter version history?

Why: A secret committed to Git may remain in history even after the current file is removed.

Effect / if deferred: None. Continue unrelated useful work.

### DEV-06 — DEV

Question: Which security, dependency, license, and repository checks are required before handoff or release?

Why: A successful build does not replace these independent checks.

Effect / if deferred: None. Continue unrelated useful work.

### DEV-07 — DEV

Question: May the AI commit, push, open a pull request, deploy, or change production?

Why: Each release or external action requires its own exact approval by default.

Effect / if deferred: None. Continue unrelated useful work.

END OF SETUPKIT BLOCK questions-dev 0.19.1
