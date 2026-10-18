# SetupKit Skills

Skills for clarifying a request and checking facts before publication.

Author and maintainer: [Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/). Developed with assistance from OpenAI Codex. Part of [SetupKit](https://github.com/etsarkov/setupkit-ai).

| Skill | Use it when | Result |
|---|---|---|
| [SetupKit Clarify](setupkit-clarify/SKILL.md) | An unanswered question could change the scope, cost, risk or definition of success. | A short set of relevant questions and a clear account of what is settled. |
| [SetupKit Fact Check](setupkit-fact-check/SKILL.md) | A public text is ready for its final factual review, or you explicitly request a fact-check. | A claim ledger, unresolved issues and a PASS, PASS WITH EDITS or BLOCK decision. |

## Clarify

Clarify asks about the gaps that could change the task. It works in short question blocks and stops when there is enough information to proceed. A simple, well-specified request should not become an interview.

Skill identifier: `setupkit-clarify`.

## Fact Check

Fact Check examines the exact wording intended for publication. It separates facts, personal experience, opinions and hypotheses, checks the supporting evidence, and flags claims that need correction or confirmation. Changes to factual wording require another check.

A PASS is an assessment of the checked claims and available evidence. It does not authorize publication or replace professional advice where needed.

Skill identifier: `setupkit-fact-check`.

## Using the files

Read the linked SKILL.md before adding it to an AI host that supports skill instructions. Use the identifier after the host has loaded the skill. Invocation, source access and tool permissions depend on that host; compatibility with every host is not claimed.

Fact Check can follow an editorial step such as a humanizer. This package does not include or install a humanizer. Both skills remain subject to your host's permissions and approval rules. They do not grant access to accounts or authorize external actions.

Use only material you are entitled to share with your chosen host. Review its data-handling terms before providing confidential or personal information.

## License and provenance

[MIT License](LICENSE). Copyright (c) 2026 Eugene Tsarkov.

Each SKILL.md also shows the author name, SetupKit project link and MIT identifier directly below its title. Metadata and the complete license text remain inside the file, so those notices are present when the file is copied on its own.

See [provenance](PROVENANCE.md) for the development history, AI assistance and known related work. The author credit covers these maintained implementations; it does not claim invention of general questioning or fact-checking methods.
