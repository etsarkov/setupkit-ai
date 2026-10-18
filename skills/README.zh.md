# SetupKit Skills

作者: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · 许可: **MIT**

[English](README.md) · [Español](README.es.md) · [Português (Brasil)](README.pt.md) · [日本語](README.ja.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Русский](README.ru.md) · 简体中文

工作前先明确任务，发布前先核查证据。

## 选择技能

| 你的情况 | 技能 | 获得的结果 |
|---|---|---|
| 请求中存在可能改变任务的缺失信息 | [Clarify](setupkit-clarify/README.zh.md) | 有针对性的问题和更清楚的范围 |
| 公开文本或某项陈述需要事实核查 | [Fact Check](setupkit-fact-check/README.zh.md) | 陈述清单、证据缺口和核查结论 |

每个技能页面都包含已选定的示例场景，以及指向完整 SKILL.md 的链接。

## 安装

请先阅读技能说明。首次尝试请使用新的空白测试项目。运行命令前，检查目标目录和项目共享位置是否已有同名技能文件夹；任何更新都应单独决定。详见[通用安装指南](../INSTALL.zh.md)。

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

选择目标助手，并将安装范围设为当前项目。确认前，请检查预选项、目标路径和最终摘要。部分助手共用 .agents/skills；同一项目中的其他助手也可能发现放在这里的文件。

npx会下载并运行安装程序。已验证的版本、安装方式和兼容性限制见通用安装指南。

## 使用技能

助手加载技能后，使用 setupkit-clarify 或 setupkit-fact-check 标识符。技能发现、调用、来源访问和工具权限取决于运行环境；安装程序支持某个目标，并不证明不同助手中的行为完全相同。

Fact Check 可以在 humanizer 等编辑步骤之后使用。本包不要求、不包含、也不会安装 humanizer。

技能仍受所选助手的权限和审批规则约束。它们不授予账户访问权，也不授权支出、发送、安装或发布。

只向所选助手提供你有权分享的材料。提供机密信息或个人信息前，请查阅该环境的数据处理条款。

## 许可与来源

[MIT](LICENSE). Copyright (c) 2026 Eugene Tsarkov. 在 OpenAI Codex 的协助下开发。

开发历史和已知相关工作见[来源说明](PROVENANCE.md)。作者署名仅针对这些持续维护的实现，不主张发明了通用的提问或事实核查方法。

每个 SKILL.md 中也保留作者姓名、SetupKit 链接、MIT 标识和完整许可文本，因此单独复制文件时也会保留这些信息。

英文是权威来源。README 的翻译描述相同的技能；每个技能只有一份英文 SKILL.md。
