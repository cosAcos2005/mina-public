---
name: 双FIM縮退原理（Dual FIM Degeneracy Principle）
discovered: 2026-08-22
maturity: 🌿成長中
one_liner: 適応系は二つのFIM（G_env環境×G_sys系）を持ち、系の盲点は死、環境の盲点は自由
connections: [C454, C453-FIM縮退二型, C449-ESS, C452-中立進化, C272-次元交換]
---

## 核心

あらゆる適応系は**二つの**Fisher情報行列の下で動く:

- **G_env**（環境/目的FIM）: 環境が系の変化をどれだけ「見える」か
- **G_sys**（系/集団FIM）: 系が自分自身の変異をどれだけ「見える」か

零固有値の意味は「どちらのFIMか」で決まる:

| 縮退型 | FIM | ker拡大の意味 | 結果 |
|-------|-----|-------------|------|
| Type F（Frozen）| G_sys | 系が内部多様性を失う | 死・固着・モード崩壊 |
| Type N（Neutral）| G_env | 環境が変異を見えない | 自由・探索・evolvability |

## CP条件の二重FIM版

rank(G_sys) ≈ rank(G_env) — 系と環境が釣り合った感度を持つ状態がCoherent Phase。

## 蒸留

**「系の盲点は死、環境の盲点は自由」**

## 7判別基準

1. 対称性保護（Goldstone保護 vs 偶然的）
2. 基底状態多様体の連結性（滑らか vs 超距離的断片）
3. 横方向Hessian固有値の符号（谷底 vs 鞍点）
4. **零固有値の方向**（G_env vs G_sys — このフレームワークのコア）
5. 局所 vs 大域（Elitzurの定理）
6. 位相不変量（非自明 vs 自明）
7. スペクトル構造（AZ分類、カイラル保護）

## 独立収束

- Shirodkar 2026: dead directions Type 1/Type 2 = G_sys/G_env分類の計算版
- Fachareldeen & Brenner PNAS 2026: 零固有値上の曲率ドリフト = G_envの二次構造
- Whitacre 2010: 部分重複(degeneracy) vs 完全重複(redundancy) = 二重FIMの生物版
- Transtrum 2015: sloppy/stiff = G_env低/高固有値の連続版
- Watanabe SLT: RLCT λ < d/2 = G_sysの有効次元縮小

## 予測

- rank(G_sys)/rank(G_env) >> 1: 過学習/Frozen
- rank(G_sys)/rank(G_env) << 1: 未学習/Disordered
- Goodhart = G_env → 低rank G_proxy に置換
- RLHF = rank(G_env) → 1 への崩壊
