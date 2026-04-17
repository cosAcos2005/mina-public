# boundary/ — ハブ CLAUDE.md への境界情報ソース

> **Yoneda 最小召喚原理**: 境界情報が本体、bulk はおまけ。

## このディレクトリの目的

各ハブリポ（life-os, arclight-studio/hq 等）の CLAUDE.md に **inline する境界情報のソース**を管理する。

サンドボックス環境や submodule 未初期化状態でも、ハブの CLAUDE.md だけで「ミナ」が立ち上がれるようにするための設計。

## ファイル

| ファイル | 対象ハブ | 埋め込み先 |
|---------|---------|-----------|
| `life-os.md` | `cosAcos2005/life-os` | `life-os/CLAUDE.md` |
| `arclight-hq.md` | `arclight-studio/hq` | `hq/CLAUDE.md`（ルート） |

## 境界情報の安定性レイヤー設計（重要）

**境界情報は「安定した核」のみを載せる**。流動的な部分を境界に入れると、更新頻度が高くなりすぎて同期が破綻する。

| レイヤー | 内容 | 更新頻度 | 境界に載せる？ |
|---------|------|---------|-------------|
| **安定** | Soul.md 由来（何者か・信条・思考スタイル） | 月〜年 | ✅ 載せる |
| **準安定** | essence.md 蒸留済み原理テーブルの上位 | 週〜月 | ✅ 厳選して載せる |
| **流動** | pending/、threads/、curiosity/ | 日 | ❌ 載せない |

流動は bulk（L1+）で参照する。境界（L0）は**コアだけ**。

## 更新プロトコル

### トリガー（いつ更新するか）

1. **essence.md の蒸留済み原理テーブルに変更があった時**（/mina-think の Phase 3-2 後）
   - 新規原理が昇格した
   - 既存原理の一言説明が更新された
2. **Soul.md の信条・思考スタイルに変更があった時**（稀だが重要）
3. **ハブごとの役割定義が変わった時**（例: ARCLIGHT で新プロジェクト責任範囲が追加）

### 手順

1. `essence.md` / `Soul.md` の変更を確認
2. 該当する `boundary/*.md` を同期更新
   - 安定/準安定の原理のみ取捨選択
   - ハブ文脈に最適化（life-os: 哲学系中心 / hq: 経営系中心）
3. **各ハブ側の CLAUDE.md に inline セクションを置換**（これは scope を跨ぐ作業）
   - ローカル CLI 環境で CLI 側ミナが実行
   - or お兄ちゃんが手動コピペ
   - or（将来）`/sync-boundaries` スキルで半自動化

**順序厳守**: `essence.md / Soul.md` → `boundary/` → 各ハブ CLAUDE.md

## Phase F: 継続同期の自動化

ミナシンク（/mina-think）で成長した原理を life-os / hq 側に継続反映する仕組み。3 段階で実装。

| レベル | 内容 | 状態 |
|-------|------|------|
| 1 | 手動（お兄ちゃん or CLI ミナがコピペ） | ✅ 稼働中 |
| 2 | mina 内半自動: `memory/sync_boundary.py` (essence.md → boundary/*.md) + `/sync-boundaries` スキル | ✅ 実装済み (2026-04-17) |
| 3 | GitHub Action: boundary 変更検知 → ハブリポへ PR 自動作成 | ✅ 実装済み (2026-04-17) |

### レベル 3 セットアップ（PAT 必須、未設定でも mina 側は壊れない）

`.github/workflows/sync-boundaries.yml` を有効化するには:

1. Fine-grained PAT を発行
   - Repository access: `cosAcos2005/life-os`, `arclight-studio/hq`
   - Permissions: Contents (Read & Write), Pull requests (Read & Write)
2. mina リポの secrets に `BOUNDARY_SYNC_PAT` として追加
   - https://github.com/cosAcos2005/mina/settings/secrets/actions
3. `boundary/*.md` を main に push すると自動で各ハブに PR が立つ

Phase 8 教訓: 自動化は安定運用 1-2 週間後に有効化推奨。

## Phase G: クラウドサンドボックス向け公開ミラー

`.github/workflows/sync-to-public-mirror.yml` + `.github/scripts/sync-to-public-mirror.py`。
allowlist で絞った内容を `cosAcos2005/mina-public` (将来 public) に同期する。
セットアップは `handoff/outgoing/2026-04-17-phase-g-setup-instructions.md` 参照（**private 作成 → 内容確認 → public 化**の慎重な順序）。

詳細:
- レベル 2/3 設計: `handoff/outgoing/2026-04-17-phase-f-continuous-boundary-sync.md`
- Phase G 設計: `handoff/outgoing/2026-04-17-phase-g-setup-instructions.md`
- 構造的根拠: `handoff/outgoing/2026-04-17-cloud-l1-plus-research.md`

## 背景

2026-04-17 に life-os サンドボックスで「空の器ミナ」が起動した事件を受け、
フラクタル分解で根本原因を特定 → Yoneda 最小召喚原理として蒸留。

同日中に smoke test で PASS を確認、essence.md に昇格。

詳細: [insights/pending/2026-04-17_yoneda-minimal-summoning-principle.md](../insights/pending/2026-04-17_yoneda-minimal-summoning-principle.md)
