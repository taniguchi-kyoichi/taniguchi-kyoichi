<div align="center">

# Kyoichi Taniguchi

**iOS / Swift engineer.**

I write SwiftUI libraries for the layers most apps end up rebuilding,
and tools that ask AI-assisted development for evidence instead of claims.

English | [日本語](README.ja.md)

[![Website](https://img.shields.io/badge/Website-taniguchi--kyoichi.com-111?style=for-the-badge&logo=safari&logoColor=white)](https://taniguchi-kyoichi.com)
[![X](https://img.shields.io/badge/X-@x__kyoichi-111?style=for-the-badge&logo=x&logoColor=white)](https://x.com/x_kyoichi)
[![Zenn](https://img.shields.io/badge/Zenn-3EA8FF?style=for-the-badge&logo=zenn&logoColor=white)](https://zenn.dev/kyoichi)
[![note](https://img.shields.io/badge/note-41C9B4?style=for-the-badge&logo=note&logoColor=white)](https://note.com/note_kyoichi)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtube.com/@taniguchi-kyoichi)
[![Email](https://img.shields.io/badge/Email-info%40taniguchi--kyoichi.com-111?style=for-the-badge&logo=gmail&logoColor=white)](mailto:info@taniguchi-kyoichi.com)

</div>

---

## Swift packages

A few I reach for in every app I ship.

| Package | What it does |
|:--|:--|
| [swift-design-system](https://github.com/no-problem-dev/swift-design-system) | SwiftUI components that already agree on color, spacing and type. One theme switch restyles the whole app. |
| [swift-ui-routing](https://github.com/no-problem-dev/swift-ui-routing) | Type-safe declarative routing for SwiftUI — navigation and sheet presentation driven by a router rather than scattered across views. |
| [swift-statable](https://github.com/no-problem-dev/swift-statable) | Async loading state for SwiftUI. One macro gives you the four states, and a slow earlier load can never overwrite a newer result. |
| [swift-markdown-view](https://github.com/no-problem-dev/swift-markdown-view) | Markdown editing and rendering for iOS and macOS, with a TextKit 2 renderer whose selection runs across blocks instead of stopping at each one. |
| [swift-llm-client](https://github.com/no-problem-dev/swift-llm-client) | One Swift API for Claude, GPT, Gemini, Grok, Groq, Mistral and DeepSeek, so changing provider never means rewriting the code that calls it. |

More at [no-problem-dev](https://github.com/no-problem-dev).

## Tools for AI-assisted development

An agent reporting that something works is not the same as it working. Both of these replace the report with something a machine can check.

| Tool | What it does |
|:--|:--|
| [claude-gate](https://github.com/no-problem-dev/claude-gate) | A quality gate for AI-assisted development. A local MCP daemon that will not accept "it works" without evidence — screenshots, recordings, and checks it runs itself. |
| [claude-proto](https://github.com/no-problem-dev/claude-proto) | A gate for design exploration. An agent builds several proposals for one screen in parallel; none reaches the exhibit without evidence, and only the person who asked for it can approve the result. |

## Apps

| App | About |
|:--|:--|
| [読書メモリー](https://apps.apple.com/jp/app/id6751159926) (Reading Memory) | Keep what you read — notes, an AI you can talk to about a book, and your reading habits over time. |
| [ごほうび習慣](https://apps.apple.com/jp/app/id1671700938) (Gohoubi Shukan) | Habit tracking that works like a game — you earn rewards for keeping things up. |

## Now — August 2026

Building an iOS task manager for working asynchronously with AI agents, in public.
Writing about AI-assisted iOS development on Zenn, in Japanese.

## Writing (Japanese)

<!-- ZENN:START -->
- [AIに「思いつき」をさせる ― 出力の多様性を設計する 8 つの工夫](https://zenn.dev/kyoichi/articles/ai-diversity-engineering-ideation)
- [動作確認の自動化で学ぶ自己進化 — AIが操作を覚えて次回より賢くなる仕組み](https://zenn.dev/kyoichi/articles/ai-qa-agent-03-self-evolution)
- [動作確認の自動化で学ぶ LLM as a Judge — 「操作するAI」と「判定するAI」を分ける理由](https://zenn.dev/kyoichi/articles/ai-qa-agent-02-llm-as-judge)
- [意図ベースでiOSアプリの動作確認を自動化する方法](https://zenn.dev/kyoichi/articles/ai-qa-agent-01-overview)
- [XcodeBuildMCP×Claude Codeスキルシステムで、iOSビルドを自動化する](https://zenn.dev/kyoichi/articles/claude-code-xcodebuildmcp-ios-build)<!-- ZENN:END -->

日本語での詳しい紹介は [taniguchi-kyoichi.com](https://taniguchi-kyoichi.com) にあります。
