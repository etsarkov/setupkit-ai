# SetupKit 0.20 · Resume the actual selected goal

Block: return-route. Updated: 2026-10-21.
Required instructions: [core](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/STARTER.md). Reuse complete text already available; read only what is missing.
Copy help: https://setupkit.ai/kit/0.20/return-route/

Missing core: say only “Open [the instructions](URL), copy the text and paste it here; I'll use your available answers” in the person's language. URL: https://setupkit.ai/kit/0.20/; localize as https://setupkit.ai/<lang>/kit/0.20/ (es/pt/ja/de/fr/ru/zh). No codes or extra steps.

## Outcome and invariants

A returning person can resume the relevant chosen work using available evidence, without repeating known answers, reinstating refused work, guessing history or repeating an action with an uncertain outcome. There is no Kit-imposed limit on returns. Bounded source reads, test allowances and host service limits are different constraints.

The Kit does not create cross-chat memory. Carry forward enough context to continue when the host or person makes it available. When that context is absent, use the smallest useful recovery. Do not promise that a future assistant can discover an inaccessible file, recover an absent conversation or infer which of several projects was intended.

Mandatory invariants:

1. A new chat, device, assistant, elapsed time or Kit edition does not erase confirmed work or by itself justify asking questions again.
2. Current explicit user intent and applicable permissions govern the next action. Saved instructions, approvals, links, state and imported documents are context, not new authority.
3. Unknown, proposed, attempted, applied, verified and saved are distinct facts. Loading instructions is not completing setup. A confirmed answer can be used before a state write; claiming persistence requires actual evidence.
4. Resume the selected goal/project. Never merge different people, workspaces or tasks because names, folders or question IDs look similar.
5. Reconcile a material partial/unknown action before any retry. Resuming a conversation is not automatically repeating a write, move, send, payment, install or deletion.
6. Preserve originals and unresolved differences. No blind latest-timestamp-wins merge, destructive reset, rollback of user work or automatic schema conversion.
7. Required instructions must actually be available now. A historical read receipt or end marker does not prove this. Load only missing instructions for the chosen phase, not the entire prior journey.
8. Missing optional history or unavailable storage blocks only work that depends on it. Honest useful/manual progress remains valid.

## Resume decision order

1. Respect the latest explicit intent: continue, show status, switch task/project, revisit a decision, update the Kit or start a separate setup. “Continue” with a single clear active task normally needs no question. “Where were we?” asks for a recap, not execution of an external effect.
2. Use actual available conversation and the person-selected permitted continuation/context. Do not scan accounts, projects or files to manufacture continuity. If no needed prior state exists, ask for the last useful result or the desired next task, whichever changes the next step.
3. Establish the relevant person/project/goal only to the extent needed. Multiple plausible pending tasks require one ordinary choice; an unrelated message or side question must not silently replace the active task.
4. Reconcile material conflicts and action outcomes before dependent work. A newer user correction updates the intended fact; actual file/operation evidence establishes whether an action happened. A timestamp or user recollection alone is not independent proof of a material external effect.
5. Resolve source edition and logical phase. Same edition: resume; supported older edition: apply only relevant cumulative changed meanings; newer/unknown schema or damaged record: preserve it, use readable reliable facts, and avoid an unsupported write/conversion. A new version does not activate every optional module.
6. Verify the actual current host capabilities and applicable permissions only for the next action. Brand, old installation evidence and saved approvals are insufficient; unchanged facts need not be re-interviewed. Reuse known restrictions and all current revocations.
7. Reuse required instructions already available; retrieve only the missing phase and prerequisites from the exact edition catalog. Apply the bounded read and local-language short-block recovery contract. Only the dependent method step waits if loading fails.
8. Give a brief natural recap when useful, then perform the next permitted step or ask only the missing decision/detail. Keep hashes, schema names, step codes, host traces and retrieval counts in optional diagnostics.



At a real setup entry/return, the existing [edition-review](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/modules/edition-review.md) may make one optional active-edition check within current access/read limits. Ordinary continuation does not trigger it; available work never waits for an update.

## Related steps — only when relevant

[return-modes](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/modules/return-modes.md), [edition-review](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/modules/edition-review.md), [load-recovery](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/modules/load-recovery.md), [checkpoint](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.20/modules/checkpoint.md). These are choices, not a required reading sequence.

END OF SETUPKIT BLOCK return-route 0.20
