# SetupKit

English · [Español](README.es.md) · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

Help your AI understand how you work. One free guide helps you create working rules and work on a real task in your own AI chat.

## How to start

1. Copy the [start prompt](prompts/en.txt).
2. Paste it into your AI chat and send it.
3. Answer the relevant questions and choose a task to work on together.

You can start in your current chat. Tell your assistant which tool you use and how you use it. If a task needs extra access, check what your chat can do first. You can work manually, leave the step for later or choose another work mode. Installing an app alone does not guarantee the tools you need.

## Current edition

[The complete guide](COMPLETE.md) is edition `0.20`, updated `2026-10-21`. Your assistant should ask relevant questions, explain why they matter and reuse answers you have already supplied.

If the source cannot be read, follow [the complete-text recovery steps](docs/getting-started.md#if-the-guide-cannot-be-read). Missing content must be requested, not invented. [Compatibility and limits](docs/compatibility.md) explain what has and has not been verified.

## Optional workspace and context

If useful, you can also organize your existing workspace and prepare a small set of reviewed files about you, your goals and your work. Start with material you already have, such as a CV or selected project notes. Choose which changes to make; you can skip questions or leave them for later.

When you return, bring your saved progress or continuation so your assistant can reuse confirmed answers and review relevant unfinished or new steps. Files are saved only with your approval and the access your assistant actually has; creating them does not guarantee automatic memory or synchronization.

## Sort selected materials — if useful

Ask your assistant to help sort selected files, links or notes. It can suggest which project each item belongs to, where to keep it and what is useful to summarize, while keeping references to the originals. Review the proposal and choose what to change or leave for later. Files are saved or moved only with your approval and suitable access; otherwise, you get a plan to follow manually. Bring the reviewed record when you return so the assistant can focus on new, changed or unfinished items.

## Skills

- [Clarify](skills/setupkit-clarify/README.md): asks focused questions to clarify a task before work starts.
- [Fact Check](skills/setupkit-fact-check/README.md): reviews claims, supporting evidence and media requirements before publication.

To install both, first read the [common installation guide](INSTALL.md) and check existing skill folders. For a first try, use a new empty test project.

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Choose the assistant and project scope; review the destinations before confirming. npx runs the installer. See [the skills overview](skills/README.md) for compatibility limits and individual installation instructions.

## Your work stays with you

No SetupKit account is needed. SetupKit does not receive the answers you give your assistant. Your assistant's costs, permissions and data rules apply. A request to draft is not approval to send, publish, install, connect an account or change files.

## Author and reuse

Created by [Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/). An independent, free project. The authored starter guide text is licensed under [CC BY 4.0](LICENSE.md), including commercial sharing and adaptations subject to the license conditions. Give credit, link to the original guide and license, and indicate changes as required. The seven supporting texts named in LICENSE.md use the same CC BY4.0 terms. Repository configuration remains outside the grant. No license for code, logos or third-party assets is implied.

## Feedback and language

See [contribution guidance](CONTRIBUTING.md) and [security reporting](SECURITY.md). Do not publish private chats, files or secrets in an Issue. English is the source of truth; the guided conversation can use your chosen language. Choose a README translation above to get started in that language. The canonical guide remains in English.
