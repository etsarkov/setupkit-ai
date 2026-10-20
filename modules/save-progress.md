# SetupKit 0.19.2 · Save approved state and verify the result

Block: save-progress. Updated: 2026-10-20.
Required instructions: [core](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19.2/STARTER.md), [question-ledger](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19.2/modules/question-ledger.md), [checkpoint](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19.2/modules/checkpoint.md). Reuse complete text already available; read only what is missing.
Copy help: https://setupkit.ai/kit/0.19.2/save-progress/

Missing core: say only “Open [the instructions](URL), copy the text and paste it here; I'll use your available answers” in the person's language. URL: https://setupkit.ai/kit/0.19.2/; localize as https://setupkit.ai/<lang>/kit/0.19.2/ (es/pt/ja/de/fr/ru/zh). No codes or extra steps.

## Save progress only with permission

Keep one logical question/progress record, referring to canonical answers and files. Optional `.setupkit/state.json` is a progress container, not a replacement personal profile or an executable configuration. `state_schema_version` is separate from any older `profile_schema_version`; this edition does not overwrite or silently convert an older profile. Existing equivalent progress storage can be retained with a reviewed mapping. No file is created merely because this method was read.

A minimal shape, with unknown values represented by null and arrays populated only from observed/reviewed facts:

```json
{
  "state_schema_version": 1,
  "state_revision": 0,
  "last_seen_edition": null,
  "started_edition": null,
  "last_completed_edition": null,
  "completion_evidence": null,
  "canonical_root_ref": null,
  "layout_revision": null,
  "module_choices": {},
  "question_records": [],
  "context_refs": [],
  "skill_recommendations": [],
  "pending_goal_ref": null,
  "unresolved_conflicts": [],
  "next_step": null,
  "review_provenance": null
}
```

Each question record retains stable ID, meaning revision if known, active flag, exactly one existing question-state enum, known answer/reference, missing detail, source and confirmation. Module records use stable step ID/revision plus choice (`not_offered`, `accepted`, `deferred` or `declined`), source/confirmation and separate proposed/applied/saved/verified evidence. These are workflow choices, not extra question states. Context references identify canonical location, purpose, source revision/date where known and access/freshness limits; no full personal file bodies or secrets. Skill records follow optional-skills and never store action grants. A pointer or stored status is a claim to check, not a permission or proof of access.

Before saving, review the exact record/delta, privacy and destination under the existing save rules. Re-read the target and retain the previous revision; count a state revision as committed only after the authorized write/readback succeeds. A failed/unknown write leaves persisted state unverified and does not advance confirmed saved progress. Save/readback evidence is reported after the operation, not invented inside a pre-write preview. No file is deleted or overwritten destructively to recover. Stop the dependent action if the actual environment cannot enforce path scope, approval and safe parameter handling; use complete manual text instead of treating these instructions as a runtime security boundary.

At review, distinguish chosen, applied, saved and verified outcomes. Only set the current `last_completed_edition` when the existing COMPLETE conditions are met for the active chosen scope: all active questions terminal, dependent actions resolved or explicitly disabled, no material conflicts and the person's review. Declining an optional module leaves its unasked questions inactive; do not fabricate their answers or a completed module. Agreed active work deferred for later is still unfinished. A deliberately disabled optional branch can allow completion of the chosen scope without claiming it was performed. Preserve a supported earlier completed edition while a newer run is partial. Manual completion can be reviewed in the chat, explicitly unsaved, with no promise that a future assistant will remember it.

On pause or handoff, carry these facts and the pending next step in the existing continuation card/file, together with the exact full current method when that format is chosen. Preserve all source-boundary, visible-part and newline fidelity rules in transfer-assembly. No automatic transfer or permission inheritance follows from saved progress.



## Related steps — only when relevant

[optional-skills](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19.2/modules/optional-skills.md), [transfer-assembly](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19.2/modules/transfer-assembly.md). These are choices, not a required reading sequence.

END OF SETUPKIT BLOCK save-progress 0.19.2
