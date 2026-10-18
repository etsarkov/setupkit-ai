# SetupKit Fact Check

Author: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · License: **MIT**

English · [Español](README.es.md) · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Review claims and supporting evidence before publication.

## When to use it

Use Fact Check for a public text ready for factual review, or when you explicitly want to verify a claim. It separates facts, personal experience, opinions and hypotheses, checks available evidence and returns a compact claim ledger.

The decision is PASS, PASS WITH EDITS or BLOCK. Unsupported load-bearing claims or unresolved material media requirements lead to BLOCK.

## Installation

Read the skill instructions first. For a first try, use a new empty test project. Before running the command, check for existing skill folders in the target and shared project locations; decide any update separately. See the [common installation guide](../../INSTALL.md).

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-fact-check
```

Choose the target assistant and project scope. Review preselected choices, destinations and the final summary before confirming. Some assistants share .agents/skills; other assistants in the project may discover files placed there.

npx downloads and executes the installer. See the common installation guide for the exact versions and modes tested, and for compatibility limits.

## Examples

Fictional source fragments and data, not claims about real companies, measured results or image rights.

### Preserve the meaning of a quotation

**Material to check:**

```text
Use setupkit-fact-check. Fictional source excerpt: "We are considering a launch in June." Draft: "The company has launched the product."
```

**Illustrative result:** Identify that a possible future launch became a completed event. Replace the assertion with a faithful attributed statement such as "The company says it is considering a launch in June." Check any final quotation against the supplied source.

### Check percentages

**Material to check:**

```text
Use setupkit-fact-check. Fictional supplied data: 10 conversions out of 100 visits before, 12 out of 100 after. Draft: "Conversion rose by 20 percentage points."
```

**Illustrative result:** Correct to "Conversion rose from 10% to 12%: 2 percentage points, or 20% relative." PASS WITH EDITS for this arithmetic fixture after checking the correction; the figures do not establish a real measurement, statistical significance or causality.

### Check a photo's provenance

**Material to check:**

```text
Use setupkit-fact-check. A post includes a photo found online. Its author, original source and permission for this use are unknown.
```

**Illustrative result:** Record the missing provenance and permission. BLOCK the post while applicable material media requirements remain unresolved. Request the source and permission, or replace the asset with one whose intended use is supported.

## Limits

The review depends on the sources and tools available to your assistant. Time-sensitive facts need current verification. PASS is an assessment of the checked wording and evidence; it does not authorize publication or replace professional advice where needed.

The skills remain subject to your assistant's permissions and approval rules. They do not grant account access or authorize spending, sending, installation or publication.

Use only material you are entitled to share with your chosen assistant. Review its data-handling terms before supplying confidential or personal information.

[SKILL.md](SKILL.md) · [SetupKit Skills](../README.md)

## License and provenance

[MIT](../LICENSE). Copyright (c) 2026 Eugene Tsarkov. Developed with assistance from OpenAI Codex.

See [provenance](../PROVENANCE.md) for the development history and known related work. The author credit covers these maintained implementations; it does not claim invention of general questioning or fact-checking methods.

The author name, SetupKit link, MIT identifier and complete license text also remain inside each SKILL.md, so those notices accompany a standalone copy.

English is the source of truth. The README translations describe the same skills; each skill has one English SKILL.md.
