# Changelog

本プロジェクトの主要な変更履歴を記録します。

書式は [Keep a Changelog](https://keepachangelog.com/ja/1.1.0/) に準拠します。
バージョニングは連載コンテンツ向けに独自規則を採用します（詳細は後述）。

###############################
# [IMPORTANT] 業務利用不可     #
###############################

本プロジェクトで扱う全ての構成・手順は **個人のプライベート用途専用** です。
詳細は [README.md](./README.md) を参照してください。

---

## バージョニング方針

本プロジェクトは連載コンテンツを扱うため、
ソフトウェア向けの SemVer ではなく、独自のタグ規則を採用します。

### タグ命名規則

| タグ形式 | 意味 | 例 |
|---|---|---|
| `v<season>.0-init` | シーズン開始時点 | `v1.0-init` |
| `v<season>.0-ep<NN>` | 各話の公開 | `v1.0-ep01`, `v1.0-ep02` |
| `v<season>.0-ep<NN>-fix<N>` | 各話の修正版 | `v1.0-ep01-fix1` |
| `v<season>.0-final` | シーズン完結時点 | `v1.0-final` |

### タグ運用例

```text
v1.0-init        シーズン1 プロジェクト初期構築
v1.0-ep01        シーズン1 第1話 公開
v1.0-ep01-fix1   シーズン1 第1話 軽微修正
v1.0-ep02        シーズン1 第2話 公開
v1.0-ep02-fix1   シーズン1 第2話 軽微修正
v1.0-ep02-fix2   シーズン1 第2話 さらなる修正
...
v1.0-final       シーズン1 完結
v2.0-init        シーズン2 プロジェクト開始
v2.0-ep01        シーズン2 第1話 公開
```

### この規則を採用する理由

- **直感的**: タグ名から「シーズン何の第何話か」が一目でわかる
- **拡張性**: 修正版を `-fix<N>` で柔軟に表現可能
- **可読性**: SemVer の `v1.1.1` より読み手に優しい
- **連載特化**: 各話=独立した公開単位という連載の本質に合致

---

## 変更カテゴリ

[Keep a Changelog](https://keepachangelog.com/ja/1.1.0/) に従い、以下のカテゴリで分類します。

| カテゴリ | 用途 |
|---|---|
| `Added` | 新機能・新コンテンツの追加 |
| `Changed` | 既存機能・コンテンツの変更 |
| `Deprecated` | 将来削除予定の機能・コンテンツ |
| `Removed` | 削除された機能・コンテンツ |
| `Fixed` | バグ・誤字・誤情報の修正 |
| `Security` | セキュリティ関連の修正 |

### コミット type との対応

| コミット type | CHANGELOG カテゴリ |
|---|---|
| `feat` | Added |
| `fix` | Fixed |
| `refactor` | Changed |
| `docs` | 変更内容次第（基本記載しない軽微なものは省略可） |
| `chore` | 基本記載しない |
| `style` | 基本記載しない |

---

## [Unreleased]

### Added

- プロジェクト初期構成
- README.md（プロジェクト概要・進捗ダッシュボード・コミットルール）
- ROADMAP.md（シーズン1全12話の詳細計画・シーズン2構想）
- CHANGELOG.md（このファイル）
- .gitignore（個人メモ・認証情報・Bridge情報の混入防止）
- docs/operation-policy.md（書き溜め型運用ルール）
- docs/disclaimer.md（業務利用不可テンプレート）
- docs/architecture.md（システム全体構成）
- templates/episode-template.md（各話の共通テンプレート）
- books/llm-homelab-s1/config.yaml（Zenn Book 設定）

### Changed

- なし

### Fixed

- なし

---

## [v1.0-init] - 2026-XX-XX

### Added

- プロジェクト発足
- 連載構成の検討
- シーズン1 全12話の構成決定
- シーズン2 構想開始（Claude Code × ローカルLLM ハイブリッド）
- 言語ポリシー策定（マークダウン本文：日本語 / コミット：英語）
- 英訳運用ルール策定（段階的追記）
- タグ命名規則策定

---

## 記入ルール

### いつ更新するか

- 各話の公開時（必須）
- 大きな構成変更時（必須）
- 運用方針の変更時（必須）
- 軽微な修正は `[Unreleased]` に蓄積し、まとめてリリース時に確定版へ

### どう書くか

- 過去形・体言止めで簡潔に
- 読者にとっての変更点を書く（内部リファクタは省略可）
- リンクは積極的に貼る（該当話、該当ドキュメント等）

### 記入例

```text
## [v1.0-ep01] - 2026-10-01

### Added
- 第1話「序章：なぜ今、自宅にAIを置くのか」公開
  - 連載全体の見取り図
  - PCスペック分類（クラスA/B/C）
  - 業務利用不可ポリシーの宣言

## [v1.0-ep01-fix1] - 2026-10-05

### Fixed
- 第1話 クラスBのRAM記載を「32GB」から「32-64GB」に修正
- 第1話 Ollama公式リンクが切れていたため更新
```

---

## English Translation

Status: `[IN PREPARATION]`

英語勉強のため個人的な翻訳活動をしています。気長にお待ちを。

(English translation is in preparation as a personal English learning activity.
Please be patient.)

### Translation Progress

Status transitions: `[IN PREPARATION]` → `[IN PROGRESS]` → `[PARTIAL]` → `[COMPLETED]`

- [ ] Versioning Policy
- [ ] Tag Naming Convention
- [ ] Change Categories
- [ ] Unreleased Section
- [ ] Initial Release Notes
- [ ] Update Rules