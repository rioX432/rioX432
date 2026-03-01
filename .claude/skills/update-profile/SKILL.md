---
description: "LAPRAS・GitHub 活動からキャリア情報を同期し、ブランディング改善も提案する"
user-invocable: true
allowed-tools:
  - Read
  - Edit
  - mcp__lapras__*
  - AskUserQuestion
  - Bash
---

## 概要

LAPRAS とGitHub 活動を分析し、以下の2つを行うスキル。

1. **データ同期** — LAPRAS → README.md / CAREER.md への差分適用
2. **ブランディング改善提案** — GitHub 活動・LAPRAS 内容をもとに README の見せ方を改善

対象ファイル：
- `/Users/rio/workspace/projects/rioX432/README.md`
- `/Users/rio/workspace/projects/rioX432/CAREER.md`

---

## Phase 1: データ収集（並行実行）

### 1-1. LAPRAS データ取得

以下を並行して取得する：

```
mcp__lapras__get_experiences   → 職歴一覧（担当内容含む）
mcp__lapras__get_tech_skill    → テックスキル・経験年数
mcp__lapras__get_job_summary   → 職務要約
```

> **Note**: LAPRAS MCP が未設定の場合はユーザーに設定を案内して終了。
> 設定方法: `~/.claude.json` の `mcpServers` に LAPRAS MCP を追加する。

### 1-2. GitHub 活動データ取得

以下を Bash で取得する：

```bash
# 最近の公開リポジトリ（言語・更新日順）
gh api /users/rioX432/repos --jq '[.[] | {name, language, updated_at, description, topics}] | sort_by(.updated_at) | reverse | .[0:10]'

# 最近のコントリビューション（イベント）
gh api /users/rioX432/events --jq '[.[] | {type, repo: .repo.name, created_at}] | .[0:30]'
```

### 1-3. 現状ファイル読み取り

```
Read: /Users/rio/workspace/projects/rioX432/README.md
Read: /Users/rio/workspace/projects/rioX432/CAREER.md
```

---

## Phase 2: ブランディング分析

収集データをもとに以下を分析し、改善提案を作成する。

### 2-1. 現状のポジショニング確認

README の冒頭テキスト・見出し・説明文から現在の自己ブランディングを把握する。

### 2-2. 分析観点

| 観点 | 確認内容 |
|---|---|
| 技術スタックの鮮度 | 最近の GitHub 活動で使っている言語・技術が README に反映されているか |
| 強みの可視化 | LAPRAS の職歴・スキルから「最も伝えるべき強み」が README に出ているか |
| キャリアフォーカス | 現在の役割（Android Tech Lead / KMP / AI活用など）が冒頭で明確か |
| 差別化ポイント | 他のモバイルエンジニアと差別化できる要素（AIエージェント活用、KMP設計など）が伝わるか |
| 一貫性 | README の肩書き・説明・Tech Stack・Career が矛盾なく一貫しているか |

### 2-3. 改善提案を提示

分析結果をもとに、具体的な改善案を提示する。提案例：

```
【ブランディング改善提案】

現状: "Android | iOS | Backend" → 改善案: "Android Lead · KMP · AI-Driven Dev"
理由: KMP と AI エージェント活用が差別化ポイントになっているが現状の説明に出ていない

提案1: [README.md] ヘッダーの typing animation テキスト更新
提案2: [README.md] 冒頭の説明文でAIエージェント活用・KMP設計を前面に出す
提案3: [CAREER.md] AnotherBall の担当内容に Claude Code 活用を追記
```

---

## Phase 3: 差分確認（データ同期）

### 3-1. 差分を洗い出す

LAPRAS データと現状ファイルを比較し、以下の観点で更新候補を特定する：

| チェック項目 | 確認内容 |
|---|---|
| 新しい職歴 | LAPRAS に存在するが CAREER.md に未記載の職歴 |
| 終了期間の修正 | `Present` のまま終了している職歴がないか |
| 各職歴の担当内容 | LAPRAS の `experience.description` と CAREER.md の bullet points の差異（新しい取り組み・技術・役割が追加されていないか） |
| スキル年数の更新 | LAPRAS のスキル年数と CAREER.md のスキルテーブルの差異 |
| 職務要約の更新 | LAPRAS の summary と CAREER.md/README.md の記述の差異 |
| README Career セクション | 現状の `code block` 内の職歴テキストと LAPRAS データの差異 |

### 3-2. ユーザーへ確認

ブランディング改善提案とデータ同期候補をまとめて AskUserQuestion で提示する。

```
「以下の更新候補が見つかりました。適用する項目を選択してください：

【ブランディング改善】
1. [README.md] ヘッダー説明文を更新（KMP・AIエージェント活用を前面に）
2. [README.md] typing animation テキストを更新

【データ同期（LAPRAS）】
3. [CAREER.md] AnotherBall 担当内容更新（Claude Code活用・採用参画など）
4. [CAREER.md] スキル年数更新: Spring Boot 2年 → 1〜2年
5. [CAREER.md] 職務要約更新

どれを適用しますか？（複数選択可）」
```

---

## Phase 4: Edit 適用ルール

確認を得た項目のみ Edit で更新する。

### 更新対象と形式

#### CAREER.md — Work Experience (English)

```markdown
#### 会社名 — *職位* (開始月 年 ~ 終了月 年 or Present)

- 担当内容 1
- 担当内容 2
```

#### CAREER.md — 職務経歴 (日本語)

```markdown
#### 会社名 — *職位*（開始年月〜終了年月 or 現在）

- 担当内容 1
- 担当内容 2
```

#### CAREER.md — スキルテーブル

```markdown
| Category | Skills |
|----------|--------|
| **Languages** | Kotlin/Java (X年) · Swift (X年) · ... |
```

#### README.md — Career セクション

````markdown
```
2025 ~         AnotherBall        ── Android Tech Lead (Android / iOS) / Avvy
2024 ~         MedicalNote (Side) ── Android / iOS (KMP)
...
```
````

### 禁止事項（変更しない）

以下は手動管理のため **絶対に変更しない**：

- README.md の **Tech Stack バッジ**（`img.shields.io` の画像リンク群）
- README.md の **Side Projects テーブル**
- README.md の **GitHub Stats / Snake アニメーション**
- README.md の **shields.io バッジのリンク先 URL**
- CAREER.md の **Education / 学歴** セクション
- CAREER.md の **Links / リンク** セクション

---

## 出力フォーマット

更新完了後、以下の形式でサマリーを表示する：

```
## 更新完了

### 変更内容

| ファイル | セクション | 内容 |
|---|---|---|
| CAREER.md | Work Experience (EN) | AnotherBall 担当内容更新 |
| CAREER.md | スキルテーブル | Spring Boot 2年→1〜2年 |
| README.md | ヘッダー | KMP・AI活用を前面に更新 |

### スキップ（手動管理）

- Tech Stack バッジ
- Side Projects テーブル

次のステップ: `git diff` で差分を確認してからコミットしてください。
```
