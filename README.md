# LLM-homelab

> 眠ってるPCで作る、俺だけのAIエージェント
> 〜次世代AIの感覚を、毎月1ステップずつ手に入れる12ヶ月の旅〜
>
> (English: A 12-month journey building local LLM environment with a sleeping PC.
> Full English translation in preparation. See bottom of page.)

###############################
# [IMPORTANT] 業務利用不可     #
###############################

本プロジェクトおよび連載で紹介する構成・手順は、
**個人のプライベート用途専用** です。

- 業務データ（コード、ドキュメント、議事録、顧客情報等）の投入禁止
- 業務利用への転用には、所属組織のセキュリティ部門への申請が必須
- 本連載は個人の自己研鑽・技術トレンドキャッチアップを目的としています

本プロジェクトは筆者の業務外活動として運営されており、
所属組織の見解とは無関係です。

## このプロジェクトについて

これは、業務外の個人プロジェクトとして取り組んでいる
**ローカルLLM運用環境の構築記録** です。

家に眠っているPCを叩き起こして、
ChatGPTのようなAIを自宅に構築し、
次世代の「AIエージェント」の感覚を手に入れることを目指します。

毎月1ステップずつ、12ヶ月かけて
体系的にローカルAI環境を育てていく連載形式で展開します。

## 連載進捗ダッシュボード

### シーズン1: 基礎構築編（全12話）

| #  | タイトル                              | 対象      | 執筆    | レビュー | 公開 | 公開予定日 |
|----|---------------------------------------|-----------|---------|----------|------|------------|
| 1  | 序章：なぜ今、自宅にAIを置くのか      | `A/B/C`   | `[PLAN]`| `[-]`    | `[-]`| 2026-10-01 |
| 2  | 最初のローカルAIを召喚する            | `A/B/C`   | `[PLAN]`| `[-]`    | `[-]`| 2026-11-01 |
| 3  | ブラウザUIで快適に使う                | `A/B/C`   | `[PLAN]`| `[-]`    | `[-]`| 2026-12-01 |
| 4  | Cloudflare Tunnel で外部公開          | `A/B/C`   | `[PLAN]`| `[-]`    | `[-]`| 2027-01-01 |
| 5  | APIで叩く・自作スクリプト             | `A/B/C`   | `[PLAN]`| `[-]`    | `[-]`| 2027-02-01 |
| 6  | マルチモーダル：画像理解              | `B/C`     | `[PLAN]`| `[-]`    | `[-]`| 2027-03-01 |
| 7  | 音声入力：Whisper活用                 | `A*/B/C`  | `[PLAN]`| `[-]`    | `[-]`| 2027-04-01 |
| 8  | RAG：個人ナレッジベース               | `A*/B/C`  | `[PLAN]`| `[-]`    | `[-]`| 2027-05-01 |
| 9  | Function Calling：AIに道具を          | `A/B/C`   | `[PLAN]`| `[-]`    | `[-]`| 2027-06-01 |
| 10 | ノーコードでエージェント構築          | `A/B/C`   | `[PLAN]`| `[-]`    | `[-]`| 2027-07-01 |
| 11 | モデルカスタマイズ入門                | `A/B/C`   | `[PLAN]`| `[-]`    | `[-]`| 2027-08-01 |
| 12 | 総集編：1年間の振り返り               | `A/B/C`   | `[PLAN]`| `[-]`    | `[-]`| 2027-09-01 |

**ステータス凡例**:

| 表記      | 意味     | 定義                       |
|-----------|----------|----------------------------|
| `[DONE]`  | 完了     | 完成基準を全て満たした     |
| `[WIP]`   | 進行中   | レビュー or 修正中         |
| `[DRAFT]` | 執筆中   | 本文を書いている最中       |
| `[PLAN]`  | 計画のみ | 概要だけ決まっている       |
| `[READY]` | 公開予定 | 公開日が確定している       |
| `[LIVE]`  | 公開済み | 公開完了                   |
| `[-]`     | 該当なし | このフェーズはまだ来ていない |

**対象スペック凡例**:

| 表記   | 意味                                                       |
|--------|------------------------------------------------------------|
| `A`    | クラスA（軽量環境: VRAM 6-8GB / RAM 16GB）で快適に対応     |
| `B`    | クラスB（標準環境: VRAM 12-16GB / RAM 32-64GB）で快適に対応|
| `C`    | クラスC（ハイエンド: VRAM 24GB+ / RAM 64GB+）で快適に対応  |
| `A*`   | クラスAは軽量代替手順で対応可能（本編とは別パス）          |
| `A/B/C`| 全クラスで対応可能                                         |
| `B/C`  | クラスBおよびC推奨（クラスAは動作困難または非対応）        |

各クラスの詳細は [docs/architecture.md](./docs/architecture.md) を参照。
各話の対応可否や軽量代替案は各記事冒頭の「対象スペック」セクションに記載。

### シーズン2: AI協働開発編（構想中）

Claude Code × ローカルLLM のハイブリッド開発を主軸とした
全12話の連載を構想中。シーズン1完了後にロードマップ詳細を公開します。

詳細: [ROADMAP.md](./ROADMAP.md)

## 運用方針

本連載は **書き溜め型** で運用します。
4話分の在庫を確保してから初回公開し、
月1回（毎月1日）のペースで継続的に公開していきます。

詳細: [docs/operation-policy.md](./docs/operation-policy.md)

## ドキュメント

| ドキュメント                                          | 内容                                       |
|-------------------------------------------------------|--------------------------------------------|
| [ROADMAP.md](./ROADMAP.md)                            | 全12話の詳細ロードマップ＋シーズン2構想     |
| [CHANGELOG.md](./CHANGELOG.md)                        | 更新履歴                                   |
| [docs/operation-policy.md](./docs/operation-policy.md) | 連載運用方針・書き溜めルール               |
| [docs/disclaimer.md](./docs/disclaimer.md)            | 業務利用不可注意書きテンプレ               |
| [docs/architecture.md](./docs/architecture.md)        | システム全体構成・環境クラス分類           |

## 言語ポリシー

本プロジェクトは日本語をメイン言語として運用しますが、
個人的な英語学習を兼ねて段階的に英訳を追記していきます。

### 言語使い分けルール

| 対象                    | 言語                                  |
|-------------------------|---------------------------------------|
| マークダウン本文        | 日本語                                |
| コミットメッセージ      | 英語                                  |
| README/ドキュメント英訳 | 各ファイル末尾に段階的に追記           |
| コードコメント          | 日本語                                |
| ファイル名              | 英語（ケバブケース推奨）              |
| 連載コンテンツ本体      | 日本語                                |

### 英訳の運用方針

- 各マークダウンファイル末尾に「English Translation」セクションを設置
- ステータスを `[IN PREPARATION]` → `[IN PROGRESS]` → `[PARTIAL]` → `[COMPLETED]` で管理
- 進捗チェックリストでセクション単位の翻訳進捗を可視化
- 完璧主義に陥らず、暇な時に少しずつ進める
- 英訳されていない場合でも、本文（日本語）は完全に機能する

### なぜ英語コミット + 日本語本文か

- **コミット**: 短く頻度が高い → 英語学習教材として最適
- **本文**: 想定読者が日本語話者 → 日本語の方が情報伝達効率高い
- **英訳追記**: 学習を継続しつつ、将来的な国際化への布石

[NOTE] この方針はプロジェクト主宰者の個人的な英語学習を兼ねています。
英訳のペースや品質は学習の進捗に依存します。気長にお待ちください。

## コミットルール

本プロジェクトは [Conventional Commits](https://www.conventionalcommits.org/ja/) 形式に従います。
コミットメッセージは **英語** で記述します。

### 基本フォーマット

```text
<type>(<scope>): <subject>

[optional body]

[optional footer]
```

### Type 一覧

| Type       | 用途                              | 例                                          |
|------------|-----------------------------------|---------------------------------------------|
| `feat`     | 新機能・新コンテンツ追加          | `feat(ep03): add web UI chapter`            |
| `fix`      | バグ・誤字・誤情報の修正          | `fix(ep01): correct typo in section 3`      |
| `docs`     | ドキュメント変更                  | `docs: update roadmap progress`             |
| `chore`    | 雑務・設定変更                    | `chore: update gitignore`                   |
| `refactor` | 構造・表現の整理（意味は変えない）| `refactor(ep02): reorganize sections`       |
| `style`    | フォーマット・表記揺れ修正        | `style: fix markdown formatting`            |
| `revert`   | 過去コミットの取り消し            | `revert: undo ep03 publish`                 |

### Scope 一覧

| Scope               | 対象                          |
|---------------------|-------------------------------|
| `ep01` 〜 `ep12`    | シーズン1 各話                |
| `s2-ep01` 〜        | シーズン2 各話（将来）        |
| `roadmap`           | ROADMAP.md                    |
| `readme`            | README.md                     |
| `zenn`              | Zenn Book 設定                |
| `internal`          | 社内掲示板向け原稿            |
| `template`          | テンプレート類                |
| `assets`            | 画像・図表                    |
| `i18n`              | 英訳追加・更新                |

Scopeは省略可。プロジェクト全体に関わる場合はScopeなしで書く。

### Subject のルール

- 英語・小文字で書く（先頭も小文字）
- 命令形（`add`, `fix`, `update` 等）
- 末尾にピリオドをつけない
- 50文字以内目安

### よく使う動詞リファレンス

| 動詞       | 意味      | 用例                                              |
|------------|-----------|---------------------------------------------------|
| `add`      | 追加する  | `feat(ep01): add introduction chapter`            |
| `write`    | 執筆する  | `feat(ep02): write first draft`                   |
| `fix`      | 修正する  | `fix(ep01): fix typo in section 3`                |
| `update`   | 更新する  | `docs: update roadmap progress`                   |
| `remove`   | 削除する  | `chore: remove unused template`                   |
| `rename`   | 改名する  | `refactor: rename chapter file`                   |
| `move`     | 移動する  | `refactor: move docs to subdirectory`             |
| `improve`  | 改善する  | `refactor(ep01): improve clarity`                 |
| `clarify`  | 明確化    | `docs: clarify usage instructions`                |
| `correct`  | 訂正する  | `fix(ep02): correct command example`              |
| `translate`| 翻訳する  | `docs(i18n): translate readme intro to English`   |

### コミット粒度のルール

**1コミット = 1つの論理的変更**

- BAD : 「第1話書いた + READMEのタイポ修正 + ロードマップ更新」を1コミット
- GOOD: それぞれ別コミットに分ける

例外: 初期構築・大規模リファクタリング等は1コミットでまとめてOK。

### コミット例

```text
chore: initial project setup with documentation and templates

feat(ep01): write first draft of introduction chapter

fix(ep02): correct command example for Windows users

docs(roadmap): update episode 3 status to in-progress

docs(readme): update progress dashboard for ep01 publication

style(ep01): fix markdown formatting in code blocks

refactor(ep02): split troubleshooting section for clarity

docs(i18n): add English translation for project overview
```

### ブランチ戦略

- `main`: 公開・確定版のみ
- `draft/ep-XX`: 各話の執筆中ブランチ
- `wip/<topic>`: その他の作業中ブランチ
- `i18n/<file>`: 英訳作業ブランチ

各話の執筆フロー:

```text
1. git checkout -b draft/ep-XX
2. （執筆・コミット）
3. セルフレビュー完了
4. git checkout main && git merge draft/ep-XX
5. git tag v1.0-ep-XX  ← 公開時にタグ
```

### タグ運用

各話の公開タイミングでタグを打ちます。
詳細なタグ規則は [CHANGELOG.md](./CHANGELOG.md) の「バージョニング方針」を参照。

| タグ例             | 意味                          |
|--------------------|-------------------------------|
| `v1.0-init`        | シーズン1 プロジェクト初期構築 |
| `v1.0-ep01`        | シーズン1 第1話 公開          |
| `v1.0-ep01-fix1`   | シーズン1 第1話 軽微修正      |
| `v1.0-ep02`        | シーズン1 第2話 公開          |
| `v1.0-final`       | シーズン1 完結                |
| `v2.0-init`        | シーズン2 開始                |
| `v2.0-ep01`        | シーズン2 第1話 公開          |

タグを打つことで、後から「公開時点」のスナップショットに戻れます。

## 公開チャネル

- **Zenn Book**: LLM-homelab シーズン1（準備中）
- **GitHub**: このリポジトリ
- **社内掲示板**: 所属組織内で別途共有

## ディレクトリ構成

```text
LLM-homelab/
├── README.md                    このファイル
├── ROADMAP.md                   全体ロードマップ
├── CHANGELOG.md                 更新履歴
├── .gitignore
│
├── docs/                        補助ドキュメント
│   ├── operation-policy.md
│   ├── disclaimer.md
│   └── architecture.md
│
├── templates/                   各回テンプレート
│   └── episode-template.md
│
├── articles/                    Zenn単発記事用
│
├── books/                       Zenn Book（連載本）
│   └── llm-homelab-s1/
│       ├── config.yaml
│       └── chapters/
│
├── episodes-internal/           社内掲示板向け原稿
│
└── assets/                      画像・図表
```

## 連絡先・フィードバック

GitHub Issues でお気軽にどうぞ。
読者の構成事例・トラブル相談・改善提案歓迎です。

## ライセンス

MIT License

---

*このプロジェクトは継続的に更新されます。
最新の進捗は上記の「連載進捗ダッシュボード」をご確認ください。*

---

## English Translation

Status: `[IN PREPARATION]`

英語勉強のため個人的な翻訳活動をしています。気長にお待ちを。

(English translation is in preparation as a personal English learning activity.
Please be patient.)

### Translation Progress

Status transitions: `[IN PREPARATION]` → `[IN PROGRESS]` → `[PARTIAL]` → `[COMPLETED]`

- [ ] About This Project
- [ ] Important Notice (Not for Business Use)
- [ ] Progress Dashboard
- [ ] Status Legend
- [ ] Spec Class Legend
- [ ] Operation Policy
- [ ] Documentation Index
- [ ] Language Policy
- [ ] Commit Rules
- [ ] Branch Strategy
- [ ] Tag Strategy
- [ ] Publication Channels
- [ ] Directory Structure
- [ ] Contact / Feedback
- [ ] License