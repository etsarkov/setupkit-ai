# SetupKit 0.20 · Relevant optional skills with existing restrictions

Block: optional-skills. Updated: 2026-10-21.
Required instructions: [core](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/STARTER.md). Reuse complete text already available; read only what is missing.
Copy help: https://setupkit.ai/kit/0.20/optional-skills/

Missing core: say only “Open [the instructions](URL), copy the text and paste it here; I'll use your available answers” in the person's language. URL: https://setupkit.ai/kit/0.20/; localize as https://setupkit.ai/<lang>/kit/0.20/ (es/pt/ja/de/fr/ru/zh). No codes or extra steps.

## Offer a skill only when useful

Offer only a relevant missing skill capability when a concrete task makes it useful or the person asks; credit verified existing equivalents and preserve refusals/deferrals. Do not routinely offer both skills at the end of a chosen journey. Reuse known AUTH-05, restrictions, choices and equivalent available skills. An unknown preference does not require a question solely to close setup; silence grants neither preference nor installation authority. Never infer installation/support from an assistant brand.

| Skill | Plain-language benefit | Later task-specific trigger |
|---|---|---|
| SetupKit Clarify (`setupkit-clarify`) | Helps clarify a consequential task's outcome, constraints and decision-critical gaps before execution | Material ambiguity, contradiction or missing success/context information; already known answers are reused and simple clear requests need no extra interview |
| SetupKit Fact Check (`setupkit-fact-check`) | Helps verify final factual claims, dates, quotations and provenance, and show what remains unverified | Actual public content or an explicit fact-checking request; final text is checked after any material factual edit, including optional humanizer editing |

Both are maintained by Eugene Tsarkov and separately licensed under MIT. Reviewed distribution: package 0.1.0, repository etsarkov/setupkit-ai, immutable commit `f83d6e35dbf3d07b55fe4a1245db843035c3b854`:
- Clarify: https://github.com/etsarkov/setupkit-ai/blob/f83d6e35dbf3d07b55fe4a1245db843035c3b854/skills/setupkit-clarify/SKILL.md
- Fact Check: https://github.com/etsarkov/setupkit-ai/blob/f83d6e35dbf3d07b55fe4a1245db843035c3b854/skills/setupkit-fact-check/SKILL.md

These are exact source references, not permission to follow links, download, execute or install. They do not add startup reads. Public distribution is not recipient-host compatibility or safety certification. Before describing an installation as actionable, establish the actual host's supported mechanism and review the exact package, provenance/license, scripts/resources/dependencies, permissions, filesystem/network/data exposure and relevant cost within allowed scope. Keep unverified candidates outside auto-discovery and do not run their code. If that cannot be done here, say what is unavailable and continue manually; never guess commands, tags or installer links, create accounts, request paid API access or require a desktop switch.

Use one contextual offer in the person's language: “[Clarify / Fact Check] may help with [specific need]: [brief benefit]. I can tell you more.” Do not stack this with another unsolicited next-task or upgrade offer. Explain material access/cost limits and the no-install alternative. A choice to learn more permits only the proposal/review. Only an explicit action approval for the exact reviewed package, host and destination permits installation/activation; recheck current scope and verify the actual result. Stored preferences never carry installation grants. Installing a skill does not mean running it on every task. Neither skill is required to finish the chosen Kit journey.

If installation is declined now, continue the task and retain that decision separately from AUTH-05. “Not now” or “do not install” never grants installation permission and does not by itself prohibit future suggestions. During later user-initiated work, a new concrete suitable problem can justify one short offer of the relevant missing skill, with a reason tied to that task, provided suggestions remain permitted. Do not repeat an offer for the same unresolved need after refusal. An explicit “do not suggest this again” suppresses that skill; a ban on skill suggestions suppresses both until the person changes it. Do not ask for a reason or repeatedly seek to reverse a refusal. Passage of a week, reopening a chat or upgrading the Kit is not a new need.

With separate save approval, put the reviewed recommendation rule in the person's canonical working instructions (for example AI_WORKING_PROFILE.md or an existing equivalent); keep the per-skill choices and last offered need in the same logical progress record. Reference the rule rather than creating conflicting copies. Retain: whether a relevant offer was made, suggestion preference/scope, each skill's choice and actual installed evidence, contextual follow-up preference, last offered need/reason and the next step. Avoid personal task bodies or sensitive details in these records. In a fresh supported session verify the host reads the rule and applies a relevant choice before promising durable behavior; otherwise give an explicitly unsaved/manual continuation. This is reactive help during the person's work, not background monitoring, activity collection, scheduled reminders or an automatic install campaign.


## Related steps — only when relevant

[question-index](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/modules/question-index.md), [save-progress](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/modules/save-progress.md). These are choices, not a required reading sequence.

END OF SETUPKIT BLOCK optional-skills 0.20
