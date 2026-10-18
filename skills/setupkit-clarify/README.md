# SetupKit Clarify

Author: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · License: **MIT**

English · [Español](README.es.md) · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Turn an unclear request into a workable brief.

## When to use it

Use Clarify when an unanswered question could change the scope, cost, risk or definition of success. It uses the context already available, asks only about material gaps and stops when there is enough information to continue.

The result identifies the resolved scope, accepted assumptions, deferred questions and next step.

## Installation

Read the skill instructions first. For a first try, use a new empty test project. Before running the command, check for existing skill folders in the target and shared project locations; decide any update separately. See the [common installation guide](../../INSTALL.md).

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-clarify
```

Choose the target assistant and project scope. Review preselected choices, destinations and the final summary before confirming. Some assistants share .agents/skills; other assistants in the project may discover files placed there.

npx downloads and executes the installer. See the common installation guide for the exact versions and modes tested, and for compatibility limits.

## Examples

Illustrations, not recorded runs. Questions apply only when the answers are missing from the context.

### Automate a weekly report

**Example request:**

```text
Use setupkit-clarify: I spend too much time on our weekly report. Help me decide what to automate.
```

**Possible questions:**

- Where does the report's data come from?
- Who uses the report, and what decision should it help them make?
- Which steps can run automatically, and which need your review?

**Illustrative result:** A bounded workflow: inputs, useful output, automated steps and human review points. This brief does not authorize implementation or sending the report.

### Brief a launch post

**Example request:**

```text
Use setupkit-clarify: I want to announce our product launch. Help me define the post before writing it.
```

**Possible questions:**

- Who should read it, and what should they understand?
- What is the one point you want to make?
- Which results or product claims can we support, and what response do you want?

**Illustrative result:** A content brief with the reader, authorial point, supported claims and intended response.

## Limits

The example questions are illustrative. Clarify does not impose a fixed questionnaire or ask again for answers already available. A simple, well-specified request can proceed without more questions.

The skills remain subject to your assistant's permissions and approval rules. They do not grant account access or authorize spending, sending, installation or publication.

Use only material you are entitled to share with your chosen assistant. Review its data-handling terms before supplying confidential or personal information.

[SKILL.md](SKILL.md) · [SetupKit Skills](../README.md)

## License and provenance

[MIT](../LICENSE). Copyright (c) 2026 Eugene Tsarkov. Developed with assistance from OpenAI Codex.

See [provenance](../PROVENANCE.md) for the development history and known related work. The author credit covers these maintained implementations; it does not claim invention of general questioning or fact-checking methods.

The author name, SetupKit link, MIT identifier and complete license text also remain inside each SKILL.md, so those notices accompany a standalone copy.

English is the source of truth. The README translations describe the same skills; each skill has one English SKILL.md.
