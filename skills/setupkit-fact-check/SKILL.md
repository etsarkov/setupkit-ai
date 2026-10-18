---
name: setupkit-fact-check
description: Verify the final wording, evidence, dates, quotations, provenance, and boundaries of factual claims in public content. Use implicitly after humanizer for every external post, thread, article, newsletter, presentation, marketing asset, and photo, video, or audio script; also use when the user explicitly asks to fact-check. Re-run after any material factual edit.
license: MIT
metadata:
  author: "Eugene Tsarkov"
  project: SetupKit
  homepage: https://github.com/etsarkov/setupkit-ai
---

# SetupKit Fact Check

Author: **Eugene Tsarkov** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · License: **MIT**

Act as the final evidence gate, not as a second copywriter. Check the exact final wording that would be published.

## Workflow

1. Extract every material statement and classify it as:
   - externally verifiable fact;
   - first-person experience or result;
   - opinion or judgment;
   - hypothesis, estimate, prediction, or recommendation;
   - quotation or close paraphrase.
2. Mark which claims are load-bearing: if false or unsupported, they would materially change the post's thesis, trustworthiness, reputational risk, or reader decision.
3. Map each factual claim to the available claim ledger and source bundle. Do not treat the draft itself, another unsourced summary, or repeated web pages as evidence.
4. Verify time-sensitive claims live. Prefer primary and authoritative sources; use independent corroboration when incentives, methodology, or interpretation matter.
5. Check names, roles, dates, numbers, units, denominators, comparisons, causality, quotation fidelity, source date, and whether the source supports the exact strength of the wording.
6. Check personal claims against user-provided or canonical evidence. Label them `author confirmation required` when only the author can verify them.
7. Check media provenance, rights, consent, accessibility, and AI disclosure when a post includes an image, video, or audio asset. Never recommend removing provenance metadata to conceal AI origin.
8. Produce a compact claim ledger with: claim, type, status, source, and required correction.
9. Return one decision:
   - `PASS`: all load-bearing claims are supported and the remaining uncertainty is accurately disclosed;
   - `PASS WITH EDITS`: provide the minimum precise corrections and verify the corrected text;
   - `BLOCK`: one or more load-bearing claims remain unsupported, contradicted, misleading, or unverifiable.

## Guardrails

- Do not evaluate an opinion as though it were a fact; verify only any factual premises inside it.
- Do not convert absence of evidence into evidence of absence.
- Do not strengthen correlation into causation or possibility into certainty.
- Do not invent citations, sources, quotations, dates, or personal experience.
- Do not use the skill name as proof. State what was actually checked and what remains unresolved.
- Do not rewrite the author's voice except for the minimum change needed to correct or qualify a claim.
- If any fact, number, causal link, quotation, or provenance statement changes after the pass, verify the changed claims again.
- Passing this gate never authorizes publication, scheduling, account changes, or external messaging.


---

## License

```text
MIT License

Copyright (c) 2026 Eugene Tsarkov

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
