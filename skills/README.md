# SetupKit Skills

Author: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · License: **MIT**

English · [Español](README.es.md) · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Clarify the task before work. Review the evidence before publication.

## Choose a skill

| Your situation | Skill | What you get |
|---|---|---|
| A request has gaps that could change the task | [Clarify](setupkit-clarify/README.md) | Focused questions and a clearer account of the scope |
| A public text or a claim needs factual review | [Fact Check](setupkit-fact-check/README.md) | A claim ledger, evidence gaps and a review decision |

Each skill page includes the selected example scenarios and a link to its full SKILL.md.

## Installation

Read the skill instructions first. For a first try, use a new empty test project. Before running the command, check for existing skill folders in the target and shared project locations; decide any update separately. See the [common installation guide](../INSTALL.md).

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Choose the target assistant and project scope. Review preselected choices, destinations and the final summary before confirming. Some assistants share .agents/skills; other assistants in the project may discover files placed there.

npx downloads and executes the installer. See the common installation guide for the exact versions and modes tested, and for compatibility limits.

## Using the skills

After your assistant has loaded the skill, use the identifier setupkit-clarify or setupkit-fact-check. Discovery, invocation, source access and tool permissions depend on the host; installer target support does not establish identical behavior across assistants.

Fact Check can follow an editorial step such as a humanizer. A humanizer is not required, included or installed by this package.

The skills remain subject to your assistant's permissions and approval rules. They do not grant account access or authorize spending, sending, installation or publication.

Use only material you are entitled to share with your chosen assistant. Review its data-handling terms before supplying confidential or personal information.

## License and provenance

[MIT](LICENSE). Copyright (c) 2026 Eugene Tsarkov. Developed with assistance from OpenAI Codex.

See [provenance](PROVENANCE.md) for the development history and known related work. The author credit covers these maintained implementations; it does not claim invention of general questioning or fact-checking methods.

The author name, SetupKit link, MIT identifier and complete license text also remain inside each SKILL.md, so those notices accompany a standalone copy.

English is the source of truth. The README translations describe the same skills; each skill has one English SKILL.md.
