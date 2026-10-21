# SetupKit 0.20 · Ask needed questions and preserve their meaning

Block: question-dialogue. Updated: 2026-10-21.
Required instructions: [core](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/STARTER.md). Reuse complete text already available; read only what is missing.
Copy help: https://setupkit.ai/kit/0.20/question-dialogue/

Missing core: say only “Open [the instructions](URL), copy the text and paste it here; I'll use your available answers” in the person's language. URL: https://setupkit.ai/kit/0.20/; localize as https://setupkit.ai/<lang>/kit/0.20/ (es/pt/ja/de/fr/ru/zh). No codes or extra steps.

## Understand the person and how they use AI

Our first users may be new to AI or use only a chat. Explain choices through their goal, not technical jargon. Reuse answers already supplied; do not ask the same thing again just to fill this order. Before deep questions, ask what they want help with, which assistant they use, and how they use it: in a browser chat, desktop chat, mobile app, cloud work/code environment, local work/code environment, several, or unsure. Ask what actually happens when they use it, rather than expecting them to know a mode name. Record the assistant and usage details with CORE-05; its bank wording and ID remain unchanged.
Ask where relevant original material lives only when needed: on the computer, uploaded copies, a project/library, a repository or a connected service. Do not infer file access, scripts, skills, browser control or scheduling from an assistant brand, browser tab or app icon. Distinguish what the person wants from what is actually available. Unknown capabilities stay UNVERIFIED. Ask operating system only when a relevant installation route needs it. Gemini guidance remains deferred; preserve supplied Gemini answers without inventing a supported setup route.
Continue the same relevant questions for browser and app users. Do not turn the first step into a complete technical inventory or make installation a condition of getting a useful result.

## Adaptive interview

When a question is needed, ask it first, then explain why it matters, which outcome/action it affects, and what remains possible if deferred or declined. The linked question-family blocks supply exact question IDs, wording, explanation and deferred dependency. Treat that dependency as a restriction on the affected action, never the whole interview. Answer / defer / not applicable / decline are equally valid. Clarify ambiguous “skip” once; default to defer. Declining authority leaves the action prohibited. No pressure to explain a refusal.
For every question in the initial group and later groups, use this compact visible shape in the person's language: “1. [Question]”; “Why: [one short sentence]”; “Effect / if later: [affected result or action; useful safe fallback]”. Use natural wording, not unexplained codes or a long technical form. A shared group introduction does not replace each question's why/effect/fallback. Example: “What one result would you like AI to help with first? Why: This keeps the next steps relevant to your work. Effect / if later: Personalized recommendations will wait; we can still work on a small task you choose.” Do not reask a known answer merely to fill this shape.
Use small groups of related questions as pacing, not a quota or total cap; one necessary question is enough. Adapt depth to the person. There is no requirement to answer the whole bank. CORE routes the selected outcome. GOAL, COMMS, AUTH, DATA, WORK and MAINT activate progressively when needed. ORG-01..12 apply to needed organization choices, or only the individual matching meaning when wanted context needs it; ORG-13..15 require a wanted overview of multiple selected projects. CTX and NOW apply only to their relevant chosen context/task gaps; no module activates every question automatically. RES requires research; CONTENT writing; PROD product/design; DEV software work (Codex alone is not enough); TOOLS an actual capability need; REM explicit reminder interest. Reminders are manual by default; a due date is not scheduling approval. Keep stable IDs when areas change and explain newly activated/deactivated questions without erasing previous answers.
## Reuse answers by meaning, not by nearby vocabulary

Before marking a question answered, deferred or declined, compare the person's actual statement with that question's meaning. Keep task restrictions separately from question answers. In particular, AUTH-05 asks “After review, may the AI propose installing skills, plugins, connectors, MCPs, or dependencies?” It asks about suggestions, not app installation or activating a suggested component. “I do not want to install an app” records an installation restriction but leaves AUTH-05 OPEN unless its actual question was answered. “After review, you may propose installing skills or plugins, but do not install anything” makes AUTH-05 ANSWERED with that limited scope, while installation remains prohibited. “Do not propose installing skills or plugins” makes AUTH-05 DECLINED; wanting to install an app later does not reverse that answer. An explicit request to defer suggestions makes AUTH-05 DEFERRED. Preserve the exact relevant source/confirmation; do not infer a permission or answer from a neighboring choice. A switch requires fresh capability and action-permission checks, never inherited grants.


## Related steps — only when relevant

[question-index](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/modules/question-index.md), [question-ledger](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/modules/question-ledger.md). These are choices, not a required reading sequence.

END OF SETUPKIT BLOCK question-dialogue 0.20
