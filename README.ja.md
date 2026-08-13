<div align="center">

# 谷口 恭一 / Kyoichi Taniguchi

**iOS / Swift エンジニア**

どのアプリでも作り直すことになる層を SwiftUI のライブラリにしています。
あわせて、AI に任せた開発から「できました」ではなく証拠を受け取るための道具を作っています。

[English](README.md) | 日本語

[![Website](https://img.shields.io/badge/Website-taniguchi--kyoichi.com-111?style=for-the-badge&logo=safari&logoColor=white)](https://taniguchi-kyoichi.com)
[![X](https://img.shields.io/badge/X-@x__kyoichi-111?style=for-the-badge&logo=x&logoColor=white)](https://x.com/x_kyoichi)
[![Zenn](https://img.shields.io/badge/Zenn-3EA8FF?style=for-the-badge&logo=zenn&logoColor=white)](https://zenn.dev/kyoichi)
[![note](https://img.shields.io/badge/note-41C9B4?style=for-the-badge&logo=note&logoColor=white)](https://note.com/note_kyoichi)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtube.com/@taniguchi-kyoichi)
[![Email](https://img.shields.io/badge/Email-info%40taniguchi--kyoichi.com-111?style=for-the-badge&logo=gmail&logoColor=white)](mailto:info@taniguchi-kyoichi.com)

</div>

---

## Swift パッケージ

自分がアプリを出すたびに使っているものです。

| パッケージ | 何をするか |
|:--|:--|
| [swift-design-system](https://github.com/no-problem-dev/swift-design-system) | 色・余白・書体が最初から揃っている SwiftUI の部品一式。テーマを1つ切り替えるとアプリ全体の見た目が変わります |
| [swift-ui-routing](https://github.com/no-problem-dev/swift-ui-routing) | SwiftUI の型安全な画面遷移。遷移とシート表示を各画面に散らさず、ルーターから駆動します |
| [swift-statable](https://github.com/no-problem-dev/swift-statable) | SwiftUI の非同期読み込み状態。マクロ1つで4つの状態が入り、遅れて返ってきた古い読み込みが新しい結果を上書きすることがありません |
| [swift-markdown-view](https://github.com/no-problem-dev/swift-markdown-view) | iOS / macOS の Markdown 編集と表示。TextKit 2 のレンダラで、選択がブロックごとに切れずにまたいで続きます |
| [swift-llm-client](https://github.com/no-problem-dev/swift-llm-client) | Claude / GPT / Gemini / Grok / Groq / Mistral / DeepSeek を1つの Swift API で。プロバイダを変えても呼び出し側を書き直しません |

ほかは [no-problem-dev](https://github.com/no-problem-dev) にあります。

## AI と作るための道具

エージェントが「動きました」と報告することと、実際に動くことは別です。どちらも報告を、機械が確かめられるものに置き換えます。

| 道具 | 何をするか |
|:--|:--|
| [claude-gate](https://github.com/no-problem-dev/claude-gate) | AI と作るときの品質のゲート。ローカルの MCP デーモンが、証拠（スクリーンショット・録画・自分で走らせる検査）の無い「動きました」を受け取りません |
| [claude-proto](https://github.com/no-problem-dev/claude-proto) | デザイン探索のゲート。1画面に対してエージェントが複数の案を並列で作り、証拠の無い案は展示に並ばず、承認できるのは依頼した人だけです |

## 公開しているアプリ

| アプリ | 内容 |
|:--|:--|
| [読書メモリー](https://apps.apple.com/jp/app/id6751159926) | 読んだ本を残すアプリ。メモ、本について話せる AI、読書習慣の記録 |
| [ごほうび習慣](https://apps.apple.com/jp/app/id1671700938) | ゲーム感覚で続ける習慣トラッキング。続けるとごほうびが手に入ります |

## いま — 2026年8月

AI エージェントと非同期で進めるための iOS タスク管理アプリを、build in public で作っています。
AI と作る iOS 開発について Zenn に書いています。

## 記事

<!-- ZENN:START -->
- [AIに「思いつき」をさせる ― 出力の多様性を設計する 8 つの工夫](https://zenn.dev/kyoichi/articles/ai-diversity-engineering-ideation)
- [動作確認の自動化で学ぶ自己進化 — AIが操作を覚えて次回より賢くなる仕組み](https://zenn.dev/kyoichi/articles/ai-qa-agent-03-self-evolution)
- [動作確認の自動化で学ぶ LLM as a Judge — 「操作するAI」と「判定するAI」を分ける理由](https://zenn.dev/kyoichi/articles/ai-qa-agent-02-llm-as-judge)
- [意図ベースでiOSアプリの動作確認を自動化する方法](https://zenn.dev/kyoichi/articles/ai-qa-agent-01-overview)
- [XcodeBuildMCP×Claude Codeスキルシステムで、iOSビルドを自動化する](https://zenn.dev/kyoichi/articles/claude-code-xcodebuildmcp-ios-build)<!-- ZENN:END -->

より詳しい紹介は [taniguchi-kyoichi.com](https://taniguchi-kyoichi.com) にあります。
