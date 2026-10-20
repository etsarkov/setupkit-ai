# SetupKit 0.19.1 · CTX question definitions (individual activation only)

Block: questions-ctx. Updated: 2026-10-20.
Required instructions: [core](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19.1/STARTER.md), [question-dialogue](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19.1/modules/question-dialogue.md). Reuse complete text already available; read only what is missing.
Copy help: https://setupkit.ai/kit/0.19.1/questions-ctx/

Missing core: say only “Open [the instructions](URL), copy the text and paste it here; I'll use your available answers” in the person's language. URL: https://setupkit.ai/kit/0.19.1/; localize as https://setupkit.ai/<lang>/kit/0.19.1/ (es/pt/ja/de/fr/ru/zh). No codes or extra steps.

Loading this family does not activate every question. Ask only individually relevant missing meanings.

### CTX-01 — CTX

Question: For [chosen task], are you working on your own, with a team, alongside other responsibilities, or in another situation worth taking into account?

Why: Use the actual task and what is already known. For example, studying while working may change which suggestions are practical. One relevant detail is enough; private-life disclosure is optional.

Effect / if deferred: This adjusts advice to the person’s relevant circumstances without asking for a biography. If unsure or unwilling to answer, use only the confirmed context and leave the rest out; continue independent useful work.

Activate / reuse: The person wants useful personal context and a missing circumstance would materially change advice. Skip when known roles/current facts are sufficient or this depth is unwanted. Reuse confirmed applicable answers and selected sources first. Relevant IDs: CORE-03, ORG-01. Reuse actual circumstances in those answers, not role-to-biography inferences.

### CTX-02 — CTX

Question: What do you do well that the assistant should build on?

Why: For example, explaining ideas, spotting mistakes or coming up with options. One example is enough; this is not a test.

Effect / if deferred: This helps suggest a useful way to work together without unnecessarily taking over things you do well. If you do not want to name strengths or are unsure, leave this section out; do not assign traits or abilities.

Activate / reuse: The person wants strengths included and they would help divide or approach the chosen work; no confirmed description exists. Reuse confirmed applicable answers and selected sources first. Relevant IDs: CORE-03, ORG-01. Reuse a self-description if actually supplied; occupation is not proof of ability.

### CTX-03 — CTX

Question: What principles matter to you in your work and decisions, even when another option would be easier?

Why: For example, keeping commitments or leaving time for learning. Use your own example; the suggestions are not a list you have to agree with.

Effect / if deferred: These principles help compare options in a way that fits you. If you prefer to skip this, keep the existing confirmed rules and ask about a specific tradeoff only when it matters. Safety boundaries still apply.

Activate / reuse: Principles would affect a chosen decision/help style and are not already explicit in confirmed answers. Reuse confirmed applicable answers and selected sources first. Relevant IDs: GOAL-02, GOAL-04, AUTH-07. Actual stated principles can be reused; priorities, prohibited AI actions and minimum safety protections are not automatically the person's whole value system.

END OF SETUPKIT BLOCK questions-ctx 0.19.1
