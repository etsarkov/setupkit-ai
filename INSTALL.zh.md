# 安装SetupKit技能

[English](INSTALL.md) · [Español](INSTALL.es.md) · [Português (Brasil)](INSTALL.pt.md) · [日本語](INSTALL.ja.md) · [Deutsch](INSTALL.de.md) · [Français](INSTALL.fr.md) · [Русский](INSTALL.ru.md) · 简体中文

需要把模糊请求变成明确任务时，选择[Clarify](skills/setupkit-clarify/README.zh.md)；需要核查主张与证据时，选择[Fact Check](skills/setupkit-fact-check/README.zh.md)。安装前请阅读所选技能的SKILL.md。

本指南介绍项目级安装。首次尝试请使用新的空测试项目。这些步骤不包含连接账号、提供API密钥或使用付费模型API。所选助手本身的费用和权限规则仍然适用。

## 安装前

1. 选择一个或两个技能，以及要使用的助手。
2. 检查助手的目标目录，以及共享项目目录`.agents/skills/setupkit-clarify`和`.agents/skills/setupkit-fact-check`。如果同名目录已存在，请停止并单独决定是否更新。覆盖警告不一定涵盖所有共享目录。
3. 选择项目范围。多个助手使用`.agents/skills`，同一项目中的其他助手也可能发现放在这里的文件。

## Skills CLI

[Skills CLI上游文档](https://github.com/vercel-labs/skills/blob/13e4063a1cf913f5606d57d42ab83a86f5001e04/README.md)列出了Codex、Claude Code、Cursor、Gemini CLI、OpenCode、Windsurf和GitHub Copilot等目标。已检查仓库的清单要求Node.js 22.20.0或更高版本。请使用所选版本要求的运行环境。

在目标项目目录中打开终端。`npx`会下载并执行安装程序，请先检查上游软件包。

安装两个技能：

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

仅安装Clarify：

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-clarify
```

仅安装Fact Check：

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-fact-check
```

选择助手和项目范围，确认前检查所有预选项、路径及最终摘要。如果会在未经单独同意更新的情况下替换已有技能，请取消。这些示例保留确认步骤。

如需指定目标，可添加`--agent cursor`、`--agent gemini-cli`或`--agent opencode`等标识符。其他标识符和目录见[上游目标表](https://github.com/vercel-labs/skills/blob/13e4063a1cf913f5606d57d42ab83a86f5001e04/README.md#supported-agents)。

已检查安装程序源码中的部分项目目录：

| 安装程序目标 | 项目目录 |
|---|---|
| Codex, Cursor, Gemini CLI, OpenCode, GitHub Copilot | `.agents/skills/` |
| Claude Code | `.claude/skills/` |
| Windsurf | `.windsurf/skills/` |

此表描述安装程序如何分配文件，并不证明SetupKit已在每个助手中测试。以上命令未固定安装程序版本，后续发行版可能不同于已检查的源码。

## Codex的另一种方法

如果你的Codex环境提供skill-installer，打开目标项目并发送：

```text
$skill-installer 请从以下位置安装SetupKit Clarify和SetupKit Fact Check：
https://github.com/etsarkov/setupkit-ai/tree/main/skills/setupkit-clarify
https://github.com/etsarkov/setupkit-ai/tree/main/skills/setupkit-fact-check
仅为当前项目安装，不要修改已有技能。如果无法进行项目级安装，请说明限制，不要修改文件。
```

只安装一个技能时，仅保留其名称和URL。这项请求表达的是期望范围；允许修改前请确认实际目标目录。如果安装程序仅支持用户级安装，请停止并选择适合项目的方法。参阅[Codex官方指南](https://learn.chatgpt.com/docs/build-skills)。

## 手动安装与Claude Code

从GitHub下载仓库压缩包，并在助手的技能发现目录之外解压。阅读所选SKILL.md后，只把`skills/`中的对应目录复制到助手官方文档指定的项目目录，保持名称和内容不变。先检查专用和共享目标目录；没有单独的更新决定时，不要替换已有目录。

Codex项目级路径：

```text
.agents/skills/setupkit-clarify/SKILL.md
.agents/skills/setupkit-fact-check/SKILL.md
```

Claude Code项目级路径：

```text
.claude/skills/setupkit-clarify/SKILL.md
.claude/skills/setupkit-fact-check/SKILL.md
```

只安装一个技能时，只需该技能的目录。保留所复制的README译本，以及SKILL.md中的全部作者和许可声明。在Claude Code发现技能后，可用`/setupkit-clarify`或`/setupkit-fact-check`开头发送消息。参阅[Claude Code官方技能文档](https://code.claude.com/docs/en/skills)。

对于其他助手，请核查其官方技能发现路径和调用方法。每个技能保留一份指令；适配路径不需要翻译或改写SKILL.md。

## 检查结果

1. 在助手的技能列表或发现界面中，确认所选标识符以项目范围出现。若发现机制要求，请开始新任务或重启助手。
2. 尝试[Clarify](skills/setupkit-clarify/README.zh.md)或[Fact Check](skills/setupkit-fact-check/README.zh.md)中的示例，检查目标技能是否确实已加载。
3. 按示例的目的核对结果。Clarify只应询问缺少的重要信息；Fact Check应指出证据缺口并给出适当结论，包括必要时的BLOCK。

## 兼容性与权限

文件结构和命令模式已与保存的上游文档及源码核对。具体版本的测试范围见下文；这些测试没有提供其他所列助手中SetupKit原生调用的证据。安装目标列表不能证明触发方式、工具、来源访问、权限或核查质量完全相同。

涉及随时间变化的主张时，Fact Check需要访问当前来源。如果缺少重要证据，主张仍未解决。软件包不包含也不会安装humanizer；Fact Check可以在没有humanizer的情况下运行。

加载、执行和权限由助手控制。技能或PASS结论并不授权发布、发送、支出、安装或连接账号。只提供你有权向所选助手分享的材料，并阅读其数据处理条款。

## 已验证的测试方式

2026年10月18日，在新的macOS项目中，使用npm/npx 11.6.2和Skills CLI 1.7.2验证了项目级复制安装。通过已有ChatGPT订阅，在Codex 0.163.0-alpha.10.2（gpt-6.1-sol）和OpenCode 2.0.22（gpt-5.6-sol）中显式调用了两个技能。合成测试涵盖不完整/完整任务说明，以及缺乏依据/正确的主张。

测试环境禁用了npm生命周期脚本。

在Codex中验证的非交互复制命令：

```bash
npx --yes skills@1.7.2 add etsarkov/setupkit-ai --skill setupkit-clarify --skill setupkit-fact-check --agent codex --copy --yes --json
```

对于已验证的OpenCode目标，将`codex`替换为`opencode`。只有自行检查技能、项目范围和全部目标目录后，才使用这种跳过确认的方式。前面的示例保留确认步骤。

这些测试不验证交互式默认选项、默认符号链接模式、全局安装、自动触发、实时网页来源核查或其他助手版本，也不保证任意任务中的输出质量。

## 作者与许可

作者及维护者：[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)。本项目属于[SetupKit](https://github.com/etsarkov/setupkit-ai)，在OpenAI Codex协助下开发。这两个技能使用[MIT许可证](skills/LICENSE)，参阅[来源记录](skills/PROVENANCE.md)。SetupKit主指南有单独的许可证，见[仓库README](README.md#author-and-reuse)。

英文是权威版本。本译文保持相同的指令、标识符和限制。
