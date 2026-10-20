# SetupKit 0.19 · Apply only supported actions and verify what happened

Block: inbox-apply. Updated: 2026-10-19.
Required instructions: [core](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19/STARTER.md), [inbox-review](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19/modules/inbox-review.md). Reuse complete text already available; read only what is missing.
Copy help: https://setupkit.ai/kit/0.19/inbox-apply/

Missing core: say only “Open [the instructions](URL), copy the text and paste it here; I'll use your available answers” in the person's language. URL: https://setupkit.ai/kit/0.19/; localize as https://setupkit.ai/<lang>/kit/0.19/ (es/pt/ja/de/fr/ru/zh). No codes or extra steps.

### Apply only supported actions and verify what happened

The guide supplies no filesystem executor or security boundary. For read-only intake, follow the existing read-only review rules: use an available permitted read tool on the exact selected sources within current host permissions and data restrictions. The ability to create or move files is not a prerequisite for reading and proposing a classification. Do not demand mutation-specific approval or proof of a write boundary before an otherwise permitted read. If a read is denied, out of scope, unsafe or unavailable, leave that source unread and use only permitted supplied material; do not broaden access or evade the restriction.

Before creating, editing, copying or moving files, or another data-changing or external action, require the actual host to enforce permitted source/target scope, safe argument handling and applicable action approval. Treat paths and model-produced arguments as untrusted data; do not interpolate untrusted text into executable commands or follow unapproved symlinks. If the host cannot demonstrate the required control for a proposed change, provide the useful analysis from permitted sources and a complete manual plan, explicitly not applied. Do not replace a denied operation with another tool, privilege increase, installation or new access route.

Use the accepted operation list as the batch limit. Re-read affected sources and targets immediately before acting. A changed file, changed destination, unexpected shared/public visibility, stale preview, out-of-scope path, traversal or unapproved symlink stops the affected action; show a fresh delta if needed. A new target collision must never cause an overwrite. Same names, similar content, byte-identical copies and different revisions need their actual evidence stated; retain originals and propose a distinct name or no change. Do not delete duplicates or choose a canonical version solely from its name.

An approved move in this procedure is a supported reversible local move between exact allowed locations, without overwrite, followed by verification. Cross-volume/provider moves requiring a copy-and-delete fallback are outside this procedure. No deletion, destructive overwrite or silent cleanup is included, including under the names archive, deduplicate, move or undo. The existing separate deletion gate remains intact for any future request. No publication, external transfer, message, installation, spending or recurring schedule is inferred.

Verify each affected result appropriate to its action: created text matches the accepted delta, moved content is preserved and at the agreed destination, source/target state matches the operation, and approved references resolve. Retrieve one representative original/result through the agreed reference; report the limits rather than claiming the entire workspace is checked. Distinguish an accepted no-change decision from a file operation. Do not claim saved, moved or verified from an intention, a tool request or a manual instruction alone.

After an error, partial batch or unknown outcome, stop affected dependent operations and preserve each row's actual result. There are no automatic retries. Inspect actual state through a permitted read before considering a new justified, authorized attempt; never repeat a potentially completed move/write blindly. If the person stops or withdraws permission, perform no further actions. To undo, inspect the current state and preview the exact safe restoration with applicable approval; do not automatically overwrite newer work or delete a created file. Keep the original failure evidence and continue only independent authorized work.


## Related steps — only when relevant

[inbox-return](https://raw.githubusercontent.com/etsarkov/setupkit-ai/setupkit-v0.19/modules/inbox-return.md). These are choices, not a required reading sequence.

END OF SETUPKIT BLOCK inbox-apply 0.19
