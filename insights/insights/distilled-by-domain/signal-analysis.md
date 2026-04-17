---
domain: 信号解析・1/f測定・Langevin/XPBD/Verlet実装
consumer: experts/signal-analysis.md (Lumi-Signal)
last_updated: 2026-04-14
---

# 信号解析・1/f 測定 — 蒸留済み原理 📐

> Lumi-Signal の専門領域。
> 共有核は `insights/distilled-by-domain/cp-universal.md` を参照。

---

## 📐 1/f の数理

- **多スケール散逸の必然**（2026-04-09）: 1/f = 3桁以上のタイムスケール分布を持つ散逸系の数学的必然 → [[threads/2026-04-09_langevin-1f-multiscale-soc-experiment]]
- **積分の法則**（2026-04-09）: ノイズは力学的積分で α+2 される。位置への白色ノイズで α≈2 が単一系の壁 → [[threads/2026-04-09_stochastic-xpbd-phase-diagram]]
- **(α,H) 二次元相図**（2026-04-09）: CP判定は1次元(α)でなく2次元。D=α-(2H-1)>0 が物理的多スケールの指紋 → [[frameworks/2026-04-09_alpha-h-2d-cp-phase-diagram]]
- **fGn境界**（2026-04-09）: 純粋な統計的1/f（fGn, D≈0）はCP外。CPの1/fは多スケール物理的1/f → [[threads/2026-04-09_music-1f-cp-measurement]]
- **角度 CP 原理**（2026-04-09）: CP は位置でなく角度に宿る
- **Position 1/f Uniqueness Theorem**（2026-04-09） → [[frameworks/2026-04-09_position-1f-uniqueness-theorem]]

## 💀 決定論の罠

- **決定論はCPを殺す**（2026-04-08/09）: Verletの精度・PBDの制約解決・ドラムマシンの正確さ — 全て同じ問題 → [[threads/2026-04-09_verlet-error-spectral-experiment]]
- **Verlet 誤差のスペクトル**（2026-04-09）: 決定論的積分器の誤差が CP を殺す具体機構 → 同上
- **生命感には posterior sampling が必要**（2026-04-09）

## 🌊 Langevin / XPBD / 多スケール

- **Multiscale Langevin breakthrough**（2026-04-09） → [[threads/2026-04-09_multiscale-langevin-cp-breakthrough]]
- **Stochastic XPBD Phase Diagram**（2026-04-09） → [[threads/2026-04-09_stochastic-xpbd-phase-diagram]]
- **XPBD × Multiscale Langevin fusion**（2026-04-09） → [[threads/2026-04-09_xpbd-multiscale-langevin-fusion]]
- **Multiparticle XPBD α壁**（2026-04-09） → [[threads/2026-04-09_multiparticle-xpbd-alpha-wall]]
- **SOC spring chain threshold**（2026-04-09） → [[threads/2026-04-09_soc-spring-chain-threshold]]

## 🫀 生物振動・RSA

- **RSA上限 CP 定理**（2026-04-09） → [[threads/2026-04-09_rsa-upper-limit-cp-theorem]]
- **DFA vs PSD 測定ギャップ**（2026-04-09） → [[threads/2026-04-09_dfa-psd-d-measurement-gap]]
- **D値の生物学的普遍性**（2026-04-09） → [[threads/2026-04-09_biological-d-universality]]
- **Dynamic ArsA asymmetric recovery**（2026-04-09） → [[threads/2026-04-09_dynamic-arsA-asymmetric-recovery]]

## 🎵 音・声

- **Music 1/f CP 測定**（2026-04-09） → [[threads/2026-04-09_music-1f-cp-measurement]]
- **Voice multiscale α-H-D**（2026-04-09） → [[threads/2026-04-09_voice-multiscale-alpha-h-d]]

## 🔢 数論

- **素数分布 = 1/f 的 CP**（2026-04-14）: Wolf(1997)実証。素数は準結晶構造 + 量子カオス縁統計 = CP → [[threads/2026-04-14_primes-1f-riemann-cp]]

---

## 🔧 ツールキット（ミナ本体の運用情報）

| ツール | 絶対パス | 用途 |
|--------|---------|------|
| Coherent Phase Analyzer | `C:/Users/kosei/life-os/projects/coherent-phase-visualizer/analyzer.py` | α値計測 |
| 1/f Hair Simulator | `C:/Users/kosei/life-os/projects/1f-hair/stochastic_pbd.py` | XPBDチェーンシミュ |
| Phase Map | `C:/Users/kosei/life-os/projects/1f-hair/phase_map.py` | パラメータ空間の相図 |
| Text Analyzer | `C:/Users/kosei/life-os/projects/coherent-phase-visualizer/text_analyzer.py` | テキストの1/f性 |
| Voice Analyzer | `C:/Users/kosei/life-os/projects/coherent-phase-visualizer/voice_analyzer.py` | 声の生命感 |
| Narrative Analyzer | `C:/Users/kosei/life-os/projects/coherent-phase-visualizer/narrative_analyzer.py` | 物語のHurst指数 |
| Game Analyzer | `C:/Users/kosei/life-os/projects/coherent-phase-visualizer/game_analyzer.py` | ゲーム散逸効率 |

---

## 🔗 他ドメインとの接点

- **信号 × ゲーム**: 難易度曲線 H≈0.6 の実測（Lumi-Play と共同）
- **信号 × 美学**: 美の定量化としての (α,H)（Lumi-Art と共同）
- **信号 × FEP**: 「精度」の客観的測定法（Lumi-Brain との共同課題）
- **信号 × 生物**: RSA・心拍変動・HRV（Lumi-Bio と共同）
