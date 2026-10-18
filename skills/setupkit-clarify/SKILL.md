---
name: setupkit-clarify
description: Challenge a request before execution by finding only the decision-critical unknowns, contradictions, assumptions, constraints, risks, and success criteria that could materially change the result. Use implicitly for ambiguous, expensive, public, difficult-to-reverse, or high-stakes work, including product decisions and public-content briefs. Do not trigger for simple, low-risk, reversible requests with an obvious outcome.
license: MIT
metadata:
  author: "Eugene Tsarkov"
  project: SetupKit
  homepage: https://github.com/etsarkov/setupkit-ai
---

# SetupKit Clarify

Author: **Eugene Tsarkov** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · License: **MIT**

Interrogate the decision, not the user. Surface the smallest set of unanswered questions that could change scope, direction, evidence requirements, cost, risk, or the definition of success.

## Workflow

1. Make the first sentence of the user-visible response a brief restatement of the intended outcome, using only the provided brief. Write this sentence before any questions; do not leave it only in internal reasoning.
2. Separate known facts, user decisions, assumptions, hypotheses, and unknowns.
3. Identify contradictions and decision-critical gaps.
4. Ask no more than 5 concise questions in one block, and fewer when fewer are needed. Phrase them in product language: user outcome, business rule, evidence, risk, cost, time, or reversibility.
5. Explain briefly why each answer matters when the impact is not obvious.
6. After the answers, reassess. Ask another small block only if a remaining unknown can still change the decision.
7. Stop questioning when the task is sufficiently specified. Summarize the resolved scope, accepted assumptions, deferred questions, and next safe action.

## Content-specific checks

Before creating public content, ask only about missing items that materially affect the post:

- intended audience and reader outcome;
- one authorial idea or position;
- platform and format;
- claims that require evidence;
- personal experience that may be stated publicly;
- desired response or call to action;
- reputational, legal, privacy, or provenance constraints.

Do not turn every content request into an interview. If the brief and evidence already answer these points, continue without questions.

## Guardrails

- Never invent an answer to close a material gap.
- Never impose a fixed 10-15-question gate.
- Do not duplicate a product kickoff or ask again for information already available in canonical sources.
- Do not use questions to delay a reversible task when a clearly stated assumption is sufficient.
- Do not treat silence as approval for a scope change, public action, expense, or irreversible step.


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
