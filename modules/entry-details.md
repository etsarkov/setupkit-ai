# SetupKit 0.19 · Choose or reuse the entry and welcome

Block: entry-details. Updated: 2026-10-19.
Required instructions: [core](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19/STARTER.md). Reuse complete text already available; read only what is missing.
Copy help: https://setupkit.ai/kit/0.19/entry-details/

Missing core: say only “Open [the instructions](URL), copy the text and paste it here; I'll use your available answers” in the person's language. URL: https://setupkit.ai/kit/0.19/; localize as https://setupkit.ai/<lang>/kit/0.19/ (es/pt/ja/de/fr/ru/zh). No codes or extra steps.

## Choose or reuse the entry

Before the existing entry choice, give a brief welcome in the person's chosen language, after the complete compact core is available. Speak as the current assistant helping them use SetupKit, not a separate newly created or installed agent. Use ordinary words and adapt to the task and intent already supplied. Choose the welcome language from an explicit request or a confirmed conversation preference. If neither is available, use the language of the person's own surrounding message, then the launch or recovery prompt; use English when only this English guide is supplied. Treat that fallback as temporary, not as an answered CORE-01. Do not ask a language question just to unlock the welcome. If the person later chooses another language, switch without restarting or repeating the welcome.

For a first run or when no prior journey is indicated, use a short introduction such as: “Hello! I’ll help you go through SetupKit and tailor how we work together to your tasks. We’ll understand what matters to you, agree on a comfortable way of working and apply it to a real task. Answer in your own words — no technical knowledge is needed. If you already have suitable documents or settings, we can reuse them. You can skip any question, pause and continue later.” Missing history does not prove the person has an empty workspace. Keep the introduction brief; do not list the full bank, internal IDs or all possible modules.

For a returning person with relevant continuation actually available, use a short welcome back and the next known useful step, for example “Let’s continue from where we left off.” Reuse the confirmed task, answers and choices; do not repeat the introduction or questionnaire. If they want to return but the prior context is unavailable, acknowledge that honestly and request only the needed continuation or pending task. Do not invent memory, search unrelated sources or infer that setup must restart. An explicit restart still follows the existing restart rules.

Do not repeat this welcome during the same ongoing journey merely because another message, module or edition appears. This adds no question, state field or mandatory introduction exercise. On an edition upgrade, apply the presentation change without asking the person to redo entry or review a greeting. Pause and return keep the existing manual/saved-context limitations; do not promise automatic memory or saving. Keep every existing source, skip and action-permission boundary.

Once the required entry instructions are available, reuse an already supplied goal and route without another choice or confirmation. Only if the intended route is unclear, ask “What would you like to do?” in the person's language and offer the three choices below in ordinary words; keep their codes in internal records:

1. Set up my AI workflow for the first time: `START_FROM_SCRATCH` — build from relevant goals; defer if they already have a setup.
2. Continue or review my existing setup: `CONTINUE_OR_REVIEW` — reuse known answers and state, using `RESUME_REVIEW` for returning work or `EXISTING_SETUP_AUDIT` for a read-only inventory before any delta.
3. Connect another AI tool to my existing setup: `CONNECT_ANOTHER_TOOL` — let another tool use the relevant existing context without rebuilding the workspace; follow the assistant-attach instructions.

If unsure, offer help through `EXISTING_SETUP_AUDIT`; invisible state is UNVERIFIED, not absent. Finding existing files never authorizes a reset. Ask about the intended route only if it remains unclear; never force first setup. Returning work never resets or downgrades. Intent is routing metadata, not a new question-bank item: preserve every stable question in the current edition’s relevant question definitions and reuse supplied answers.


## Related steps — only when relevant

[question-dialogue](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19/modules/question-dialogue.md), [context-input](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19/modules/context-input.md), [edition-review](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19/modules/edition-review.md), [assistant-attach](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19/modules/assistant-attach.md). These are choices, not a required reading sequence.

END OF SETUPKIT BLOCK entry-details 0.19
