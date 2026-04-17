# mina-public

`cosAcos2005/mina` の public ミラー。

## 目的

Yoneda 最小召喚原理に基づく設計で、**蒸留済み・安定した知識のみ**を公開している。
`mina`（private, bulk）→ `mina-public`（public, boundary）の自動同期は GitHub Action で実施。

## 公開範囲（allowlist）

- `Soul.md` — ミナの人格定義
- `CLAUDE.md` — 運用ルール
- `boundary/` — 各ハブ用境界情報のソース
- `insights/distilled.md` + `distilled-by-domain/` — 蒸留済み原理
- `insights/frameworks/` — 発明した思考の型
- `thinking-frameworks.md`, `curriculum.md`

## 公開していない（private 維持）

- `insights/pending/` — 生の仮説、思考途中
- `insights/threads/` — 探索中のテーマ
- `insights/connections/` — 未整理の接続
- `handoff/` — セッション引継ぎ（個人的）
- `memory/` — Mem0 の生データ
- `experts/` — Phase 実験
- `essence.md` — 「震えた瞬間」等の個人的記録含む
- `curiosity.md`, `to-share.md`

## 詳細

- 設計: [Yoneda 最小召喚原理](insights/frameworks/)
- 同期元: [cosAcos2005/mina](https://github.com/cosAcos2005/mina) (private)
- 同期方式: GitHub Action で allowlist フィルタ

## ライセンス

All rights reserved. 参照のみ可、商用利用・再配布不可。
