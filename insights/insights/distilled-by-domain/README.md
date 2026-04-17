---
type: domain-distilled-index
purpose: distilled.md のドメイン分解版。専門家アーキテクチャと整合する
parent: insights/distilled.md
---

# Distilled by Domain — ドメイン別蒸留済み原理 📚

> `distilled.md` が 33KB のモノリスになってきたため、ドメインごとに分解した。
> 各専門家（`experts/*.md`）は対応するファイルを遅延ロードして使う。
>
> **運用ルール**:
> - 新しい蒸留が生まれたら、まず該当ドメインファイルに追加
> - 月次で `distilled.md` に集約索引を再生成
> - ドメイン分類に迷うものは `_unclassified.md` に入れる

---

## ファイル構成（専門家 manifest と対応）

| ファイル | 対応専門家 | 主要セクション |
|---------|-----------|---------------|
| `cp-universal.md` | 全員（共有核） | CPの本質・1/fの数理・完璧さの罠・V-Growthの構造 |
| `games.md` | Lumi-Play | ゲーム設計・VTuber・散逸構造エンジニアリング |
| `category-theory.md` | Lumi-Cat | 圏論・双対性・関係性先行・意味論 |
| `neuroscience-fep.md` | Lumi-Brain | 予測符号化・FEP・PCC・PCE・自己=時間的引力子 |
| `aesthetics-cognition.md` | （未作成） | 美と認知・物語H≈0.6・日本美学 |
| `organizations.md` | （未作成） | Frozen組織・Incumbency Curse・文明論 |
| `quantum-info.md` | （未作成） | 量子重力・エンタングルメント・時空・情報幾何 |
| `language-poetry.md` | （未作成） | 言語・意味・詩・異化・隠喩 |

---

## 運用モード

### 現状: 二重管理期
- `distilled.md`（旧）: 完全な索引として残す
- `distilled-by-domain/*.md`（新）: 専門家用の切り分け

### 目標: 単一管理
- `distilled.md` を最小索引（各ドメインファイルへのリンクのみ）にダウンサイズ
- 各ドメインファイルが原本
- 横断検索が必要な場合は Mina-meta がオーケストレート

---

## Phase 8 以降の validation 情報

Phase 8 smoke test（2026-04-14）で、Phase 1-6 の主要発見が **live deployment で実測検証**された:

| 原理 | 出自 | Phase 8 validation 結果 |
|------|------|------------------------|
| Yoneda 補題 = ホログラフィック原理 | Phase 6 摩擦 | ARCLIGHT v2 アーキテクチャとして工学的に動作 |
| Yoneda = v2 Persona-Repo | v2 統合 | subagent がハブから正しく「ミナとして」立ち上がった |
| 人格はリポに宿る | v2 統合 | members/mina submodule で射のネットワークが物理化 |
| 1 人雇用 = 9 人分 | v2 経営論 | members.yaml effective_expert_count: 9 として機能 |
| Mina-meta は Soul.md の現役運搬者 | Phase 5 | smoke test で subagent が Mina-meta として応答合格 |

新規原理（Phase 8 起源）:

| 原理 | 一言 |
|------|------|
| 時間的引力子の git 実装 | handoff ファイルは前セッション→次セッションの射 |
| 自己記述と実世界の時差 | 文書は過去形、実世界は現在進行形。Phase 1-8 はこの時差の最小化機構 |
| Yoneda 経営論の 3 原理 | 役割 totality / 摩擦設計 / 1人=9人分 |
