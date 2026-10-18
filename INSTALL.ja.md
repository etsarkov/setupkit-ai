# SetupKitスキルのインストール

[English](INSTALL.md) · [Español](INSTALL.es.md) · [Português (Brasil)](INSTALL.pt.md) · 日本語 · [Deutsch](INSTALL.de.md) · [Français](INSTALL.fr.md) · [Русский](INSTALL.ru.md) · [简体中文](INSTALL.zh.md)

曖昧な依頼を具体化するには[Clarify](skills/setupkit-clarify/README.ja.md)、主張と根拠を確認するには[Fact Check](skills/setupkit-fact-check/README.ja.md)を選んでください。インストール前に対象のSKILL.mdを読んでください。

このガイドはプロジェクト単位のインストールを扱います。初回は新しい空のテスト用プロジェクトで試してください。この手順にはアカウント接続、APIキー、有料モデルAPIの利用は含まれません。利用するアシスタントの料金と権限は引き続き適用されます。

## インストール前

1. 片方または両方のスキルと、利用するアシスタントを選びます。
2. アシスタントの保存先と共有フォルダー`.agents/skills/setupkit-clarify`、`.agents/skills/setupkit-fact-check`を確認します。同名のフォルダーがあれば停止し、更新するかを別途決めてください。上書き警告がすべての共有保存先を対象とするとは限りません。
3. プロジェクト単位を選びます。複数のアシスタントが`.agents/skills`を使うため、同じプロジェクトの別のアシスタントもファイルを検出する場合があります。

## Skills CLI

[Skills CLIの公式README](https://github.com/vercel-labs/skills/blob/13e4063a1cf913f5606d57d42ab83a86f5001e04/README.md)にはCodex、Claude Code、Cursor、Gemini CLI、OpenCode、Windsurf、GitHub Copilotなどが記載されています。確認したリポジトリのマニフェストはNode.js 22.20.0以降を要求しています。選ぶバージョンが必要とする実行環境を使ってください。

対象プロジェクトのフォルダーでターミナルを開きます。`npx`はインストーラーをダウンロードして実行するため、先に配布元のパッケージを確認してください。

両方のスキル：

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

Clarifyのみ：

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-clarify
```

Fact Checkのみ：

```bash
npx skills add etsarkov/setupkit-ai --skill setupkit-fact-check
```

アシスタントとプロジェクト単位のインストールを選び、事前選択された項目、パス、最終確認をすべて確認してから承認します。別途合意していない既存スキルの置換が行われるならキャンセルしてください。これらの例では確認操作を省略しません。

保存先を指定するには`--agent cursor`、`--agent gemini-cli`、`--agent opencode`などを追加します。ほかの識別子と保存先は[配布元の一覧](https://github.com/vercel-labs/skills/blob/13e4063a1cf913f5606d57d42ab83a86f5001e04/README.md#supported-agents)を参照してください。

確認したインストーラーの代表的な保存先：

| インストーラーの対象 | プロジェクト内のフォルダー |
|---|---|
| Codex, Cursor, Gemini CLI, OpenCode, GitHub Copilot | `.agents/skills/` |
| Claude Code | `.claude/skills/` |
| Windsurf | `.windsurf/skills/` |

この表はインストーラーの振り分けを示し、各アシスタントでSetupKitを検証済みという意味ではありません。上のコマンドはバージョンを固定していないため、将来の配布版が確認済みソースと異なる場合があります。

## Codexでの別の方法

Codex環境にskill-installerがあれば、対象プロジェクトを開いて次を送ります。

```text
$skill-installer 次の場所からSetupKit ClarifyとSetupKit Fact Checkをインストールしてください：
https://github.com/etsarkov/setupkit-ai/tree/main/skills/setupkit-clarify
https://github.com/etsarkov/setupkit-ai/tree/main/skills/setupkit-fact-check
このプロジェクトのみにインストールし、既存スキルは変更しないでください。プロジェクト単位でインストールできない場合は、ファイルを変更せず制限を説明してください。
```

片方だけなら名前とURLもそのスキルだけにします。この依頼は希望する範囲を示すもので、変更を許可する前に実際の保存先を確認してください。ユーザー全体へのインストールしか提供されない場合は停止し、プロジェクト向けの方法を選んでください。[Codexの公式ガイド](https://learn.chatgpt.com/docs/build-skills)も参照してください。

## 手動インストールとClaude Code

GitHubからリポジトリのアーカイブを取得し、アシスタントのスキル検出フォルダーの外で展開します。対象のSKILL.mdを読んだうえで、`skills/`から必要なフォルダーだけを、アシスタントが公式に指定するプロジェクト内の保存先へコピーします。名前と内容を保ち、個別・共有の保存先を先に確認し、別途更新を決めずに既存フォルダーを置き換えないでください。

Codexのプロジェクト単位のパス：

```text
.agents/skills/setupkit-clarify/SKILL.md
.agents/skills/setupkit-fact-check/SKILL.md
```

Claude Codeのプロジェクト単位のパス：

```text
.claude/skills/setupkit-clarify/SKILL.md
.claude/skills/setupkit-fact-check/SKILL.md
```

片方だけならそのスキルのフォルダーだけで十分です。コピーするREADMEの翻訳と、SKILL.md内の著者・ライセンス表示をすべて保持してください。Claude Codeが検出した後は、メッセージの先頭で`/setupkit-clarify`または`/setupkit-fact-check`を使います。[Claude Codeの公式ドキュメント](https://code.claude.com/docs/en/skills)を参照してください。

ほかのアシスタントでは、公式の検出パスと呼び出し方法を確認してください。各スキルの指示は一つのコピーとして保ちます。パスの調整にSKILL.mdの翻訳や書き換えは必要ありません。

## 結果の確認

1. 選んだ識別子がプロジェクト単位でスキル一覧や検出画面に表示されることを確認します。必要なら新しいタスクを開始するか、アシスタントを再起動します。
2. [Clarify](skills/setupkit-clarify/README.ja.md)または[Fact Check](skills/setupkit-fact-check/README.ja.md)の例を試し、対象スキルが実際に読み込まれたことを確認します。
3. 例の目的と結果を照合します。Clarifyは不足する重要情報だけを質問し、Fact Checkは根拠の不足と、必要に応じてBLOCKを含む適切な判定を示すはずです。

## 互換性と権限

ファイル構成とコマンドの形式は、保存した配布元のドキュメントとソースに照らして確認しています。特定バージョンでの実行確認の範囲は下記のとおりです。ほかの掲載アシスタントについて、これらのテストによるSetupKitのネイティブ呼び出しの証拠はありません。対象一覧への掲載は、起動条件、ツール、参照元へのアクセス、権限、確認品質が同じことを意味しません。

時点によって変わる主張には、Fact Checkが最新の参照元へアクセスできる必要があります。重要な根拠がなければ未解決のままです。このパッケージはhumanizerを含まず、インストールもしません。Fact Checkはhumanizerなしで動作できます。

読み込み、実行、権限はアシスタントが管理します。スキルやPASS判定は、公開、送信、支出、インストール、アカウント接続を許可しません。共有する権利のある資料だけを渡し、そのアシスタントのデータ取扱条件を確認してください。

## 検証したテスト方式

2026年10月18日、新しいmacOSプロジェクトでnpm/npx 11.6.2とSkills CLI 1.7.2によるプロジェクト内へのコピーインストールを確認しました。既存のChatGPTサブスクリプションを使い、Codex 0.163.0-alpha.10.2（gpt-6.1-sol）とOpenCode 2.0.22（gpt-5.6-sol）で両スキルを明示的に呼び出しました。合成テストでは、不完全・完全な依頼と、裏付けがない・正しい主張を扱いました。

テスト環境ではnpmのライフサイクルスクリプトを無効にしました。

Codexで確認した非対話式のコピーコマンド：

```bash
npx --yes skills@1.7.2 add etsarkov/setupkit-ai --skill setupkit-clarify --skill setupkit-fact-check --agent codex --copy --yes --json
```

確認したOpenCodeの対象にするには`codex`を`opencode`へ置き換えます。確認を省くこの方式は、対象スキル、プロジェクト範囲、すべての保存先を自分で確認した後に限って使用してください。それより前の例では確認を省きません。

対話式の初期選択、既定のシンボリックリンク方式、全体へのインストール、自動起動、Webの最新情報を使う事実確認、ほかのアシスタントバージョンは未検証です。あらゆるタスクでの出力品質を保証するものではありません。

## 著者とライセンス

著者・メンテナー：[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)。[SetupKit](https://github.com/etsarkov/setupkit-ai)の一部として、OpenAI Codexの支援を受けて開発しました。この二つのスキルは[MITライセンス](skills/LICENSE)です。[開発経緯](skills/PROVENANCE.md)も参照してください。SetupKit本体のガイドには別のライセンスがあり、[リポジトリのREADME](README.md#author-and-reuse)に説明されています。

英語版が基準です。この翻訳は同じ手順、識別子、制限を保ちます。
