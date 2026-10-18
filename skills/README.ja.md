# SetupKit Skills

作者: **[Eugene Tsarkov](https://www.linkedin.com/in/etsarkov/)** · [SetupKit](https://github.com/etsarkov/setupkit-ai) · ライセンス: **MIT**

[English](README.md) · [Español](README.es.md) · [Português (Brasil)](README.pt.md) · 日本語 · [Deutsch](README.de.md) · [Français](README.fr.md) · [Русский](README.ru.md) · [简体中文](README.zh.md)

作業前に依頼を明確に。公開前に根拠を確認。

## スキルを選ぶ

| 状況 | スキル | 得られるもの |
|---|---|---|
| 依頼の不足点によって作業内容が変わり得る | [Clarify](setupkit-clarify/README.ja.md) | 要点を絞った質問と、より明確な範囲 |
| 公開用の文章や主張に事実確認が必要 | [Fact Check](setupkit-fact-check/README.ja.md) | 主張一覧、根拠の不足点、確認の判定 |

各スキルのページには、選択済みの使用例とSKILL.md全文へのリンクがあります。

## インストール

まずスキルの指示を読んでください。初回は新しい空のテスト用プロジェクトを使います。コマンドを実行する前に、対象の場所とプロジェクト内の共有先に同名のスキルフォルダーがないか確認し、更新は別途判断してください。詳しくは[共通インストールガイド](../INSTALL.ja.md)を参照してください。

```bash
npx skills add etsarkov/setupkit-ai \
  --skill setupkit-clarify \
  --skill setupkit-fact-check
```

対象のアシスタントとプロジェクト単位の範囲を選びます。確定する前に、事前選択された項目、配置先、最終確認画面を確認してください。一部のアシスタントは.agents/skillsを共有するため、同じプロジェクトの別のアシスタントも、そこに置いたファイルを検出する場合があります。

npxはインストーラーをダウンロードして実行します。検証したバージョンと方式、および互換性の制限は共通のインストールガイドを参照してください。

## スキルの使い方

アシスタントがスキルを読み込んだら、setupkit-clarifyまたはsetupkit-fact-checkという識別子を使います。検出、呼び出し、情報源へのアクセス、ツールの権限は実行環境に依存します。インストーラーが対象に対応していることは、各アシスタントで同じ動作になる証拠ではありません。

Fact Checkはhumanizerなどの文章編集の後にも使えます。このパッケージはhumanizerを必須とせず、同梱もインストールもしません。

スキルには、利用するアシスタントの権限と承認ルールが引き続き適用されます。アカウントへのアクセスを付与したり、支出、送信、インストール、公開を許可したりするものではありません。

選んだアシスタントと共有する権利のある素材だけを使ってください。機密情報や個人情報を渡す前に、その環境のデータ取り扱い条件を確認してください。

## ライセンスと来歴

[MIT](LICENSE). Copyright (c) 2026 Eugene Tsarkov. OpenAI Codexの支援を受けて開発しました。

開発の経緯と確認されている関連作品は[来歴](PROVENANCE.md)を参照してください。作者表記はこれらの保守対象の実装についてのものであり、質問や事実確認という一般的な手法の発明を主張するものではありません。

作者名、SetupKitへのリンク、MITの識別子、ライセンス全文は各SKILL.mdにも含まれるため、ファイルを単独でコピーしても表記が残ります。

英語版が原文です。READMEの翻訳は同じスキルを説明しており、各スキルには英語のSKILL.mdが1つだけあります。
