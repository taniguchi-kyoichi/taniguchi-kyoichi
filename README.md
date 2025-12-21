<div align="center">

# 谷口 恭一 / Kyoichi Taniguchi

**iOSエンジニア | Swift & SwiftUI**

[![Email](https://img.shields.io/badge/Email-info%40taniguchi--kyoichi.com-blue?style=for-the-badge&logo=gmail&logoColor=white)](mailto:info@taniguchi-kyoichi.com)
[![Website](https://img.shields.io/badge/Website-taniguchi--kyoichi.com-green?style=for-the-badge&logo=safari&logoColor=white)](https://taniguchi-kyoichi.com)
[![Zenn](https://img.shields.io/badge/Zenn-3EA8FF?style=for-the-badge&logo=zenn&logoColor=white)](https://zenn.dev/kyoichi)
[![YouTube](https://img.shields.io/badge/YouTube-@taniguchi--kyoichi-red?style=for-the-badge&logo=youtube&logoColor=white)](https://youtube.com/@taniguchi-kyoichi)

</div>

---

## 👨‍💻 自己紹介

- 🎓 **横浜国立大学** 卒業（2025年3月）
  - 理工学部 数物・電子情報系学科
- 🏢 東京のライフスタイルアプリ開発会社でiOSエンジニアとして勤務
- 📍 神奈川県横浜市在住
- 💡 **Swift & SwiftUI** を使ったネイティブiOSアプリ開発に情熱を注ぐ
- 🤖 モバイルアプリケーションへのAI統合技術を探求中

---

## 🚀 注力プロジェクト

<table>
<tr>
<td>

### 🧠 [swift-llm-structured-outputs](https://github.com/no-problem-dev/swift-llm-structured-outputs)

**Swift で LLM を使ったアプリ・エージェントを構築するためのライブラリ**

[![Swift](https://img.shields.io/badge/Swift-6.0-orange.svg)](https://github.com/no-problem-dev/swift-llm-structured-outputs)
[![iOS](https://img.shields.io/badge/iOS-17.0+-blue.svg)](https://github.com/no-problem-dev/swift-llm-structured-outputs)
[![macOS](https://img.shields.io/badge/macOS-14.0+-blue.svg)](https://github.com/no-problem-dev/swift-llm-structured-outputs)
[![Linux](https://img.shields.io/badge/Linux-compatible-green.svg)](https://github.com/no-problem-dev/swift-llm-structured-outputs)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/no-problem-dev/swift-llm-structured-outputs)

OpenAI・Anthropic・Gemini に対応した**マルチモーダル LLM クライアント**。
構造化出力・ツール定義・MCP統合・会話型エージェントを簡単に構築できます。

```swift
@Structured("リサーチ結果")
struct ResearchResult {
    @StructuredField("要約") var summary: String
    @StructuredField("主要な発見") var findings: [String]
}

@Tool("Webページの内容を取得")
struct FetchWebPage {
    @ToolArgument("URL") var url: String
    func call() async throws -> String { ... }
}

let tools = ToolSet {
    FetchWebPage()
    MCPServer(command: "npx", arguments: ["-y", "@anthropic/mcp-server-filesystem", "/docs"])
}

let systemPrompt = Prompt {
    PromptComponent.role("リサーチアシスタント")
    PromptComponent.objective("ドキュメントを調査してレポートを作成")
    PromptComponent.instruction("複数のソースから情報を収集する")
    PromptComponent.constraint("事実に基づいた情報のみを報告する")
}

let session = ConversationalAgentSession(
    client: AnthropicClient(apiKey: "..."),
    systemPrompt: systemPrompt,
    tools: tools
)

let image = try ImageContent.file(at: "/path/to/document.png")
let input = LLMInput("この資料を分析して最新トレンドをまとめて", images: [image])

let stream: AsyncThrowingStream<SessionPhase<ResearchResult>, Error> = session.run(input: input, model: .sonnet)
for try await phase in stream {
    if case .completed(let result) = phase { print(result.summary) }
}
```

📚 [ドキュメント](https://no-problem-dev.github.io/swift-llm-structured-outputs/documentation/llmstructuredoutputs/)

</td>
</tr>
</table>

---

## 📦 Swift Packages

Swift開発者向けに、アプリ開発を加速させるパッケージを公開しています。

| パッケージ | 説明 |
|:----------|:-----|
| [swift-llm-structured-outputs](https://github.com/no-problem-dev/swift-llm-structured-outputs) | マルチモーダル対応のLLMクライアント。会話型エージェントを簡単に構築 |
| [LLMCodable](https://github.com/no-problem-dev/LLMCodable) | LLMベースの構造化データ変換。自然言語からSwift型への変換を実現 |
| [swift-design-system](https://github.com/no-problem-dev/swift-design-system) | SwiftUI向け型安全デザインシステム。7種類のビルトインテーマ、ライト/ダークモード対応 |
| [swift-cached-remote-image](https://github.com/no-problem-dev/swift-cached-remote-image) | メモリ＆ディスク二層キャッシュのリモート画像ライブラリ |
| [swift-authentication](https://github.com/no-problem-dev/swift-authentication) | Firebase Auth / Google Sign-In / Apple Sign-In 統合。async/await対応 |
| [swift-subscription](https://github.com/no-problem-dev/swift-subscription) | RevenueCat統合のサブスクリプション管理。購入・復元・状態監視 |
| [swift-api-client](https://github.com/no-problem-dev/swift-api-client) | async/await対応の軽量HTTPクライアント。型安全なAPI通信 |
| [swift-firebase-server](https://github.com/no-problem-dev/swift-firebase-server) | Firestore REST APIクライアント。サーバーサイドSwift向け |

---

## 📱 公開アプリ

| App | Description | Platform |
|:---:|:------------|:---------|
| <a href="https://apps.apple.com/jp/app/id6751159926"><img src="assets/reading-memory-icon.png" width="100" alt="読書メモリー Icon"></a> <br> 読書メモリー | 本との出会いと対話を美しく記録するアプリ。AIチャットメモ・読書習慣トラッキング・本棚管理 <br> [![App Store](https://img.shields.io/badge/App_Store-0D96F6?style=for-the-badge&logo=app-store&logoColor=white)](https://apps.apple.com/jp/app/id6751159926) | iOS |

---

## 🤖 Claude Code プラグイン

Claude Code の機能を拡張するプラグインを開発・公開中。

| カテゴリ | プラグイン |
|:--------|:----------|
| **Development** | [ios-dev](https://github.com/no-problem-dev/claude-code-plugins/tree/main/plugins/ios-dev) ・ [go-backend](https://github.com/no-problem-dev/claude-code-plugins/tree/main/plugins/go-backend) ・ [firebase-emulator](https://github.com/no-problem-dev/claude-code-plugins/tree/main/plugins/firebase-emulator) |
| **Architecture** | [ios-architecture](https://github.com/no-problem-dev/claude-code-plugins/tree/main/plugins/ios-architecture) ・ [swift-design-system](https://github.com/no-problem-dev/claude-code-plugins/tree/main/plugins/swift-design-system) |
| **Utility** | [release-flow](https://github.com/no-problem-dev/claude-code-plugins/tree/main/plugins/release-flow) ・ [notify-on-stop](https://github.com/no-problem-dev/claude-code-plugins/tree/main/plugins/notify-on-stop) |

[![Marketplace](https://img.shields.io/badge/claude--code--plugins-blueviolet?style=for-the-badge&logo=github)](https://github.com/no-problem-dev/claude-code-plugins)

---

## 🛠 技術スタック

### 主要スタック（実務経験あり）

**iOS開発**
- **Swift** - ネイティブiOS開発の主要言語
- **SwiftUI** - モダンな宣言的UIフレームワーク
- **UIKit** - 従来のiOS UIフレームワーク
- **Combine** - リアクティブプログラミングフレームワーク
- **async/await** - モダンなSwift並行処理

**クラウド & バックエンド**
- **Firebase** - 認証、Firestore、Cloud Functions
- **Google Cloud Platform** - クラウドサービスとAPI

### サブスタック

![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

---

## 📝 Zenn 記事

<!-- ZENN:START -->
- [プロトコル指向でデザインシステムを抽象化する - Swift/SwiftUI実践](https://zenn.dev/kyoichi/articles/f3a3c6a9dfe14d)
- [なぜSwiftのSendableはデフォルトにならなかったのか](https://zenn.dev/kyoichi/articles/swift-sendable-not-default)
- [Swift Concurrency用語完全ガイド](https://zenn.dev/kyoichi/articles/swift-concurrency-terminology)
- [Codableの延長線で考える、Swift Foundation ModelsによるLLMデコード](https://zenn.dev/kyoichi/articles/llmcodable-introduction)
- [SwiftUI Environmentをジェネリックに拡張する](https://zenn.dev/kyoichi/articles/58495f1e979601)<!-- ZENN:END -->

---

## 💬 お問い合わせ

📧 **Email:** [info@taniguchi-kyoichi.com](mailto:info@taniguchi-kyoichi.com)

🌐 **Website:** [taniguchi-kyoichi.com](https://taniguchi-kyoichi.com)

📝 **Zenn:** [zenn.dev/kyoichi](https://zenn.dev/kyoichi)

🎥 **YouTube:** [@taniguchi-kyoichi](https://youtube.com/@taniguchi-kyoichi)
