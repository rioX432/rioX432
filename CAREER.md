# Career Detail

[English](#english) | [日本語](#日本語)

---

## English

### Summary

Senior Mobile Engineer and Android Tech Lead with 8+ years of professional experience, primarily in Android development, with hands-on experience in iOS, Kotlin/Spring Boot backend development, Kotlin Multiplatform, Compose Multiplatform, real-time systems, and technical leadership.

Currently leading the Android domain for Avvy at AnotherBall. I own Android architecture, feature delivery, quality, releases, performance, and production issue resolution while contributing directly to iOS and shared KMP layers. I also design AI-agent development infrastructure for production Android engineering, including structured context, specialized subagents, automated verification, performance analysis, human approval gates, and safety guardrails.

I work in both Japanese and English. Source code, pull requests, and code reviews are written in English, while meetings, specifications, and day-to-day communication use both languages.

### Professional Experience

#### AnotherBall Pte. Ltd. — Android Tech Lead / Mobile Engineer, Avvy

**Jul 2025 – Present · Tokyo, Japan**

Avvy is a global avatar-based live-streaming and social entertainment platform with more than 100,000 downloads.

- Lead Android development across a production codebase of approximately 40 modules, 1,300 Kotlin files, and 160,000 lines of Kotlin, with a biweekly release cadence.
- Own Android feature delivery, architecture, codebase modernization, quality, performance, release operations, and production issue resolution.
- Contribute directly to iOS development and design shared UseCase and Repository layers with Kotlin Multiplatform.
- Develop core experiences across live streaming, gifts, gift combos, events, gacha, avatar customization, and community features.
- Led the gift-combo feature from competitive research and UX design through architecture, implementation, release, and KPI dashboard development. The feature achieved sustained adoption and materially increased daily gift volume.
- Designed reliability mechanisms for high-frequency gift interactions, including optimistic UI, coin-balance reconciliation, unsent-state recovery, duplicate-send prevention, offline guards, animation queues, and Firestore-based synchronization.
- Work on RTC, camera and audio processing, face tracking, Unity integration, and real-time state synchronization.
- Evaluate WebSocket and WebRTC-based architecture options for future product-specific synchronization needs.
- Support engineering hiring through candidate sourcing, outreach, casual interviews, and selection coordination.

##### AI-Agent Development Infrastructure

- Designed and maintain an AI-agent development harness covering investigation, ambiguity resolution, decomposition, implementation, verification, review, and pull-request preparation.
- Established centralized architecture guidance, engineering rules, testing documentation, and a maintained production bug-pattern catalog for Claude Code, Codex, Gemini, and other agents.
- Built specialized investigator, build, Android-review, and performance-review agents, with cross-model checks and explicit human approval gates.
- Integrated Gradle tests, Detekt, Android Studio inspections, Compose Preview rendering, emulator journeys, screenshot comparison, Maestro flows, and evidence-based acceptance-criteria verification.
- Built agent-operable performance workflows using Perfetto, Macrobenchmark, Baseline Profiles, gfxinfo, meminfo, and trace SQL analysis.
- Added safeguards for destructive commands, secret access, generated code, repeated failures, and scenarios that require manual QA.

**Primary technologies:** Kotlin, Jetpack Compose, Swift, SwiftUI, Kotlin Multiplatform, Coroutines, Flow, Cloud Firestore, Firebase, Agora, MediaPipe, Unity, Maestro, Arbigent, Perfetto, Claude Code, Codex, Gemini

#### LY Corporation — Android Engineer / Feature Lead, Yahoo! Shopping

**Apr 2022 – Oct 2025 · Tokyo, Japan**

- Led three major redesigns of the Yahoo! Shopping Android top screen.
- Owned requirements alignment, technical design, implementation, testing, release, maintenance, and production issue resolution for the Android workstream.
- Introduced Jetpack Compose incrementally by replacing RecyclerView ViewHolders before migrating the full Fragment and screen structure.
- Migrated the top-screen architecture from MVP to MVVM and consolidated shared behavior used across multiple components.
- Contributed to multi-module architecture and engineering working groups.
- Developed Kotlin/Spring Boot proxy APIs between mobile clients and the Yahoo! Shopping backend.
- Built an internal iOS validation application from scratch with SwiftUI.

**Primary technologies:** Kotlin, Java, Jetpack Compose, Android Views, RecyclerView, ViewModel, Coroutines, Flow, Spring Boot, SwiftUI, CircleCI

#### Topcon Corporation — Android Engineer / Project Lead

**Apr 2018 – Mar 2022 · Tokyo, Japan**

- Built an Android field application used by civil-engineering surveyors to communicate with total stations and record surveying results through Bluetooth Low Energy.
- Designed offline-first workflows for fully offline field operation, with administrative work performed online later from the office.
- Led a nine-person delivery team consisting of six contract engineers, two QA engineers, and myself.
- Managed implementation, task allocation, schedules, technical decisions, specification alignment with the product manager, and QA execution.
- Collaborated with a Russian engineering team for four years, including a three-month on-site assignment.
- Helped transfer technical knowledge and development ownership from the outsourced Russian team to Japan, establishing the foundation for Japan-led in-house development.

**Primary technologies:** Kotlin, Java, Android SDK, Bluetooth Low Energy, Room, SQLite, C++, offline-first architecture, hardware integration

### Concurrent Contract Experience

#### MedicalNote Inc. — Android / iOS Engineer

**Apr 2024 – Present · Remote**

- Work as the sole mobile engineer for the MedicalNote consumer application across Android and iOS.
- Own delivery from specification review and technical design through implementation, testing, release preparation, and maintenance.
- Designed an incremental migration from existing native applications to Compose Multiplatform while preserving legacy screens.
- Built shared login, onboarding, and post-login top-screen experiences.
- Implemented a shared WebView layer and customized unsupported behavior such as Basic Authentication handling.
- Advanced the migration to a production-ready stage; the rollout was later discontinued for business reasons unrelated to technical feasibility.

#### Zaico Inc. — Android Engineer

**Aug 2022 – Feb 2024 · Remote**

- Developed inventory registration using barcode and QR-code scanning with CameraX.
- Developed inventory quantity-management features and contributed to an application-wide UI redesign.
- Owned assigned features from requirements clarification through testing and release.
- Incrementally replaced legacy state-management code with ViewModel-based implementations.

### Selected Open-Source Projects

#### [CivitDeck](https://github.com/rioX432/CivitDeck)

A full-featured Kotlin Multiplatform application for Android, iOS, and Desktop.

- Shares networking, persistence, domain logic, use cases, and approximately 49 ViewModels across three platforms.
- Uses Jetpack Compose, SwiftUI, and Compose Desktop for platform-native UIs.
- Integrates CivitAI, Hugging Face, TensorArt, ComfyUI, Stable Diffusion WebUI, and custom image servers.
- Includes REST/WebSocket generation workflows, on-device SigLIP-2 search, Room KMP persistence, modular Clean Architecture, testing, CI, and automated releases.

#### [agent-witness](https://github.com/rioX432/agent-witness)

A Rust-based observability and audit tool for AI coding agents.

- Records Claude Code sessions using hooks and preserves normalized and raw JSONL evidence.
- Provides TUI timelines, Markdown/JSON reports, delegation summaries, and MCP/skill usage inventories.
- Includes destructive-command flagging, token aggregation, deterministic core logic, and golden TUI tests.

#### [ai-dev-templates](https://github.com/rioX432/ai-dev-templates)

Reusable workflows and guardrails for reliable AI-agent-driven development.

### Education

- **Doshisha University Graduate School of Science and Engineering** — M.S., Mathematical Sciences and Environment, 2016–2018
- **Doshisha University, Faculty of Science and Engineering** — B.S., Environmental Systems, 2012–2016

### Languages

- Japanese: Native
- English: Professional working proficiency

### Links

- [GitHub](https://github.com/rioX432)
- [SpeakerDeck](https://speakerdeck.com/rio432)
- [Avvy](https://avvy.live/)
- [AnotherBall Tech Blog](https://tech.anotherball.com/)

---

## 日本語

### 職務要約

Androidを中心に8年以上の実務経験を持つ、Senior Mobile Engineer / Android Tech Leadです。iOS、Kotlin/Spring Bootによるバックエンド、Kotlin Multiplatform、Compose Multiplatform、リアルタイムシステム、技術リードの経験があります。

現在はAnotherBallでAvvyのAndroid領域を担当し、アーキテクチャ、機能開発、品質、リリース、パフォーマンス、障害対応までを主導しています。iOS実装やKMP共通層にも直接貢献しています。

また、本番Android開発向けのAIエージェント基盤を設計・運用しています。共通コンテキスト、専門サブエージェント、自動検証、パフォーマンス解析、人間の承認ゲート、安全ガードレールまで含む開発ハーネスを整備しています。

### 職務経歴

#### AnotherBall Pte. Ltd. — Android Tech Lead / Mobile Engineer, Avvy

**2025年7月 – 現在 · 東京**

- 約40モジュール、Kotlin約1,300ファイル・16万行規模のAndroidコードベースを、隔週リリースで担当。
- Androidの機能開発、アーキテクチャ、モダナイズ、品質、パフォーマンス、リリース、障害対応を主導。
- iOS開発にも直接参加し、Kotlin MultiplatformでUseCase・Repository層を共通化。
- 配信、ギフト、コンボ、イベント、ガチャ、アバター、コミュニティ機能を開発。
- ギフトコンボ機能を競合調査、UX設計、技術設計、実装、リリース、KPIダッシュボード作成まで一貫して主導。継続利用され、日次ギフト量を大きく向上。
- 楽観的UI、コイン残高整合、未送信状態復旧、二重送信防止、オフライン制御、アニメーションキュー、Firestore同期などを設計。
- RTC、カメラ・音声処理、フェイストラッキング、Unity連携、リアルタイム状態同期を担当。
- 採用候補者の探索、スカウト、カジュアル面談、選考調整にも参加。

##### AIエージェント開発基盤

- 調査、曖昧性解消、分解、実装、検証、レビュー、PR作成までを統合した開発ハーネスを設計・運用。
- Claude Code、Codex、Gemini等に共通で参照されるアーキテクチャ、規約、テスト資料、バグパターン集を整備。
- 調査、ビルド、Androidレビュー、性能レビューの専門サブエージェントと、別モデルによるクロスチェックを導入。
- Gradleテスト、Detekt、Android Studio Inspection、Compose Preview、エミュレーター操作、スクリーンショット比較、Maestro、AC証跡確認を統合。
- Perfetto、Macrobenchmark、Baseline Profile、gfxinfo、meminfo、SQL解析によるエージェント実行可能な性能計測チェーンを整備。
- 破壊的コマンド、シークレット参照、自動生成コード、連続失敗、手動QA境界に対するガードレールを導入。

#### LY Corporation — Android Engineer / Feature Lead, Yahoo!ショッピング

**2022年4月 – 2025年10月 · 東京**

- Yahoo!ショッピングAndroidアプリのTOP画面刷新を3回担当。
- PdMとの要件調整、技術設計、実装、テスト、リリース、保守までを担当。
- RecyclerViewのViewHolder単位からJetpack Composeへ段階移行し、最終的にFragment・画面全体をCompose化。
- MVPからMVVMへ移行し、複数コンポーネントから利用される共通処理を整理。
- マルチモジュール化、アーキテクチャ・Androidワーキンググループに参加。
- Kotlin/Spring BootでモバイルクライアントとショッピングBE間のプロキシAPIを開発。
- SwiftUIで社内Web表示検証用iOSアプリをフルスクラッチ開発。

#### Topcon Corporation — Android Engineer / Project Lead

**2018年4月 – 2022年3月 · 東京**

- 土木測量で使用するトータルステーションとBLE通信し、測量結果を記録するAndroidアプリを新規開発。
- 現場では完全オフライン、事務所でオンライン作業を行うオフラインファースト設計。
- 業務委託エンジニア6名、QA2名、自身を含む9名チームをリード。
- 実装、タスク管理、スケジュール調整、技術選定、PdMとの仕様調整、QA管理を担当。
- ロシア開発チームと4年間協働し、3か月の現地出張を経験。
- ロシア側から技術スタックと開発手法を獲得し、日本主導の内製開発へ移行するための基盤を構築。

### 業務委託

#### MedicalNote Inc. — Android / iOS Engineer

**2024年4月 – 現在 · リモート**

- MedicalNoteアプリのAndroid/iOSを単独で担当し、仕様受領から開発、テスト、リリース準備、保守まで実施。
- 既存ネイティブ画面を維持しながら、Compose Multiplatformへ段階移行する構成を設計。
- ログイン、オンボーディング、ログイン後TOP画面を共通化。
- CMP WebViewを導入し、Basic認証などライブラリ未対応部分をカスタム実装。
- 本番導入可能な段階まで進めた後、技術的理由ではなく会社都合で展開中止。

#### Zaico Inc. — Android Engineer

**2022年8月 – 2024年2月 · リモート**

- CameraXによるバーコード・QRコード読み取りを利用した在庫登録機能を開発。
- 在庫数量管理、アプリ全体のUI刷新を担当。
- 要件確認からテスト・リリースまでを担当。
- 既存状態管理をViewModelベースへ段階的に置き換え。

### 主なOSS

- **[CivitDeck](https://github.com/rioX432/CivitDeck)** — Android / iOS / Desktop対応のKotlin Multiplatformアプリ。共有ViewModel、ComfyUI連携、オンデバイスML検索、Room KMP、CIを実装。
- **[agent-witness](https://github.com/rioX432/agent-witness)** — AIコーディングエージェントのセッション記録・監査・可観測性を提供するRust製CLI/TUI。
- **[ai-dev-templates](https://github.com/rioX432/ai-dev-templates)** — AIエージェント開発向けの再利用可能なワークフローと安全ガードレール。

### 学歴

- **同志社大学大学院 理工学研究科** 数理環境科学専攻 修士課程（2016–2018）
- **同志社大学 理工学部** 環境システム学科（2012–2016）

### 言語

- 日本語: ネイティブ
- 英語: ビジネス実務レベル

### リンク

- [GitHub](https://github.com/rioX432)
- [SpeakerDeck](https://speakerdeck.com/rio432)
- [Avvy](https://avvy.live/)
- [AnotherBall Tech Blog](https://tech.anotherball.com/)
