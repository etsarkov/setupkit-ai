# Install SetupKit Skills

English · [Español](INSTALL.es.md) · [Português (Brasil)](INSTALL.pt.md) · [日本語](INSTALL.ja.md) · [Deutsch](INSTALL.de.md) · [Français](INSTALL.fr.md) · [Русский](INSTALL.ru.md) · [简体中文](INSTALL.zh.md)

Choose [Clarify](skills/setupkit-clarify/README.md) to turn an unclear request into a brief, or [Fact Check](skills/setupkit-fact-check/README.md) to review claims and evidence. Read the selected skill's SKILL.md before installation.

This guide covers project installation. For a first try, use a new empty test project. No account connection, API key or paid model API is part of these instructions. Your chosen assistant's existing costs and permissions still apply.

## Before installation

1. Choose one skill or both, and the assistant you want to use.
2. Check the assistant's destination folders and the shared project folders `.agents/skills/setupkit-clarify` and `.agents/skills/setupkit-fact-check`. If a matching folder already exists, stop and decide on that update separately. Installer overwrite warnings may not cover every shared destination.
3. Choose project scope. Several assistants use `.agents/skills`, so other assistants in the project may discover files placed there.

## Skills CLI

The upstream [Skills CLI](https://github.com/vercel-labs/skills/blob/13e4063a1cf913f5606d57d42ab83a86f5001e04/README.md) documents targets including Codex, Claude Code, Cursor, Gemini CLI, OpenCode, Windsurf and GitHub Copilot. The inspected repository manifest requires Node.js 22.20.0 or later. Use the runtime required by the version you choose.

Open a terminal in the intended project folder. `npx` downloads and executes the installer; review the upstream package before running it.

Both skills:

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Clarify only:

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-clarify
```

Fact Check only:

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-fact-check
```

Choose the target assistant and project scope. Review all preselected choices, paths and the final summary before confirming. Cancel if an existing skill would be replaced without a separately agreed update. The examples keep confirmation enabled.

To specify a target, append its identifier, for example `--agent cursor`, `--agent gemini-cli` or `--agent opencode`. The [upstream target table](https://github.com/vercel-labs/skills/blob/13e4063a1cf913f5606d57d42ab83a86f5001e04/README.md#supported-agents) lists other identifiers and destinations.

These are representative project destinations in the inspected installer source:

| Installer target | Project directory |
|---|---|
| Codex, Cursor, Gemini CLI, OpenCode, GitHub Copilot | `.agents/skills/` |
| Claude Code | `.claude/skills/` |
| Windsurf | `.windsurf/skills/` |

This is an installer routing table, not evidence that SetupKit was tested in each assistant. The commands above are unpinned; a later distributed installer version may differ from the inspected source.

## Codex alternative

If skill-installer is available in your Codex environment, open the intended project and send:

```text
$skill-installer Install SetupKit Clarify and SetupKit Fact Check from:
https://github.com/etsarkov/setupkit-ai/tree/main/skills/setupkit-clarify
https://github.com/etsarkov/setupkit-ai/tree/main/skills/setupkit-fact-check
Install for this project only. Keep existing skills unchanged. If project installation is unavailable, explain the limitation without changing files.
```

For one skill, include only its name and URL. The request expresses the intended scope; confirm the actual destination before allowing file changes. If the installer only offers user-wide installation, stop and choose a suitable project method. See [official Codex guidance](https://learn.chatgpt.com/docs/build-skills).

## Manual installation and Claude Code

Download the repository archive from GitHub and extract it outside your assistant's skill discovery folders. Read the selected SKILL.md files before copying anything. Copy only the selected folders from `skills/` into the project directory documented by your assistant, keeping their names and contents. Check both target and shared locations first; do not replace an existing folder without a separate update decision.

For project-scoped Codex skills:

```text
.agents/skills/setupkit-clarify/SKILL.md
.agents/skills/setupkit-fact-check/SKILL.md
```

For project-scoped Claude Code skills:

```text
.claude/skills/setupkit-clarify/SKILL.md
.claude/skills/setupkit-fact-check/SKILL.md
```

Only the chosen skill's folder is needed for a single-skill installation. Preserve any README translations that you copy, and retain all author and license notices in SKILL.md. In Claude Code, after discovery, start a message with `/setupkit-clarify` or `/setupkit-fact-check`. See [official Claude Code skill documentation](https://code.claude.com/docs/en/skills).

For another assistant, check its official skill discovery path and invocation method. Keep one copy of each skill's instructions; adapting a path does not require translating or rewriting SKILL.md.

## Check the result

1. Confirm in the assistant's skill list or discovery view that the chosen identifiers appear in project scope. Start a fresh task or restart the host if its discovery process requires it.
2. Try one of the selected examples in [Clarify](skills/setupkit-clarify/README.md#examples) or [Fact Check](skills/setupkit-fact-check/README.md#examples). Check that the intended skill was actually loaded.
3. Check the result against the example's purpose. Clarify should ask only about missing material information. Fact Check should show the evidence gaps and an appropriate review decision, including BLOCK where necessary.

## Compatibility and permissions

The common file layout and command patterns have been checked against captured upstream documentation and source. The exact-version test scope is described below; other listed assistant targets have no native SetupKit invocation evidence from these tests. Listing a target does not establish identical triggering, tools, source access, permissions or review quality.

Fact Check needs current source access for time-sensitive claims. If material evidence is unavailable, the claim remains unresolved. The package does not include or install a humanizer; Fact Check can run without one.

The assistant controls loading, execution and permissions. A skill or a PASS decision does not authorize publication, sending, spending, installation or account changes. Use only material you are entitled to share with the selected host and review its data-handling terms.

## Verified test mode

On 18 October 2026, project-copy installation through npm/npx 11.6.2 and Skills CLI 1.7.2 was checked in fresh macOS projects. Both skills were explicitly invoked in Codex 0.163.0-alpha.10.2 (gpt-6.1-sol) and OpenCode 2.0.22 (gpt-5.6-sol), using an existing ChatGPT subscription. The synthetic tests covered clarification with incomplete/complete briefs and fact checking with unsupported/correct claims.

The test environment disabled npm lifecycle scripts.

The tested noninteractive copy command for Codex was:

```bash
npx --yes skills@1.7.2 add etsarkov/setupkit-ai --skill setupkit-clarify --skill setupkit-fact-check --agent codex --copy --yes --json
```

For the tested OpenCode target, replace `codex` with `opencode`. Use this confirmation-skipping mode only after checking the selected skills, project scope and all destination folders yourself. The examples above keep confirmation enabled.

These tests do not verify interactive defaults, default symlink mode, global installation, automatic triggering, live web fact verification or other assistant versions. They are not a guarantee of output quality for every task.

## Author and license

Author and maintainer: [Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/). Part of [SetupKit](https://github.com/etsarkov/setupkit-ai), developed with assistance from OpenAI Codex. These two skills use the [MIT license](skills/LICENSE); see [provenance](skills/PROVENANCE.md). The main SetupKit guide has its own license, described in the [repository README](README.md#author-and-reuse).
