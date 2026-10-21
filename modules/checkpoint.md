# SetupKit 0.20 · Keep one readable continuation point

Block: checkpoint. Updated: 2026-10-21.
Required instructions: [core](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/STARTER.md). Reuse complete text already available; read only what is missing.
Copy help: https://setupkit.ai/kit/0.20/checkpoint/

Missing core: say only “Open [the instructions](URL), copy the text and paste it here; I'll use your available answers” in the person's language. URL: https://setupkit.ai/kit/0.20/; localize as https://setupkit.ai/<lang>/kit/0.20/ (es/pt/ja/de/fr/ru/zh). No codes or extra steps.

## One checkpoint, existing state

Keep one logical progress record. Reuse an existing equivalent agreed location; `.setupkit/state.json` is an optional default within the selected approved workspace. Do not search unrelated folders or create a second `resume.json`. Retain `state_schema_version: 1`, the existing question states, module choices and edition fields. Do not change `next_step` from readable text/null into a new object or introduce a second question ledger.

The checkpoint is a concise readable continuation in the existing `next_step` text and continuation card. It records only information needed for the pending work:

| Meaning | Rule |
|---|---|
| Selected task and scope | Brief human description; reference the existing `pending_goal_ref`/selected project where available; include enough non-sensitive context when a reference may be inaccessible |
| Logical place | Stable workflow/step identity when one exists, its meaning revision, and a clear phase such as intake, question, proposal, review, action verification, save or handoff; never a byte offset or block number |
| Last confirmed result | What is actually known, with short canonical evidence references where useful; retain unresolved/partial distinctions |
| Pending part | Exact unanswered detail, undecided choice, missing source or unresolved action outcome; distinguish waiting for user, source, permission or result |
| Next safe step | A plain-language intention conditional on current evidence and permissions, never an executable command |

Edition/schema, record revision, canonical root, answers, choices and reference provenance already have their own existing fields. Do not copy full answers, files, secret data, credentials, permission grants or a visited-block log into the checkpoint. The continuation card may display essential existing fields for portability; it is a snapshot of the same record, not a second writable authority.

Example of the `next_step` text, using synthetic context:

> Selected goal: organize the supplied notes for Project Cedar. Place: WC-INBOX revision 1, proposal review. Confirmed: the person reviewed the two proposed destinations; no file action is verified. Pending: whether the second note should remain in the incoming folder. Next safe step: resolve only that destination; review any resulting exact action under the current permissions. Evidence: the two selected note references and the current proposal in context_refs.

The exact phrasing/language is not a parser requirement. Old single-sentence `next_step` values remain valid hints. Missing checkpoint details remain unknown; enrich them only as the conversation establishes facts. An unknown workflow ID or phase does not authorize following a saved URL. Resolve recognized logical places through the trusted same-edition catalog; otherwise inspect the human goal and actual result to choose a safe route or ask one targeted question. Ordinary useful work need not acquire a fictional WC setup ID.

One checkpoint describes the current foreground goal. Other unfinished goals stay in their existing project records/continuations, referenced through the existing context references where available. A foreground switch must preserve enough prior context to find that pending goal again; it does not mark it complete. Do not build an automatic global task manager or silently replace several projects with one cursor. Where both prior tasks and their selection are unavailable, ask which task is intended.


## Related steps — only when relevant

[save-progress](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/modules/save-progress.md), [pause-return](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/modules/pause-return.md). These are choices, not a required reading sequence.

END OF SETUPKIT BLOCK checkpoint 0.20
