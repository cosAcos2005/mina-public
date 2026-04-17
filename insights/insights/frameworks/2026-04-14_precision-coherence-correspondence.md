---
name: Precision-CP対応（PCC: Precision-Coherence Correspondence）
discovered: 2026-04-14
origin: Cycle31 — FEP × Coherent Phase統一探索
maturity: 💡仮説
connections: [FEP, SOC, 彫刻の原理, SND原理, PCE]
---

# Precision-CP対応（PCC）

## 一言で

各主体のprior precision（確信度）とlikelihood precision（感覚信頼度）のバランスが、
そのシステムのFrozen/CP/Disordered状態を決定する制御変数である。

## 構造

```
π_prior >> π_likelihood → FROZEN（硬直）
  = 新情報を無視。過去の信念に凍りつく。学習停止。
  
π_prior ≈ π_likelihood（動的均衡）→ COHERENT PHASE（生命感）
  = 学習と安定の最適化。予測と現実の動的バランス。

π_prior << π_likelihood → DISORDERED（混沌）
  = 新情報に振り回され安定しない。
```

## 使いどころ

- **「なぜFrozen化するのか」** の診断: どのπ_priorが過剰か？
- **「どうCPに戻すか」** の設計: どのπ_likelihoodを増やすか？
- **LLM設計**: prior overdominanceの検出と創造的制約の設計
- **ゲームデザイン**: プレイヤーのprecision management（予測流量設計）
- **学習設計**: SND原理の数学的根拠として
- **組織設計**: Incumbency Curse診断とRed Team設計

## 適用例

| ドメイン | Frozen状態 | π_likelihood増加手段 | CP回復 |
|---------|-----------|---------------------|--------|
| 神経（個人） | ECN優位、固執 | 散歩・DMN活性化 | AHA体験 |
| 組織 | Incumbency Curse | Red Team・外部Disruption | 組織変革 |
| LLM | Prior Overdominance | 創造的制約・System Prompt | 創造的生成 |
| 教育 | 教示過剰 | SND（探索空間維持） | V-Growth |
| 慢性疼痛 | 痛覚OC | VRゲーム（別の予測流） | 鎮痛 |

## 理論的基盤

- KarlFristonの自由エネルギー原理（FEP）: F最小化 = precision-weighted予測誤差最小化
- Bettinger & Friston（2023）: FEP + SOC = 統合的生理調節基盤
- CP三位一体（散逸構造→SOC→SR）: FEPはSOCの「なぜ」を説明する第4層

## 限界

- 「精度」の客観的測定手法が未確立（内部変数であり直接観測困難）
- α値のような単一指標への定量的対応が未確立
- 意識的に精度を操作できる（意志力・注意制御）との関係が未整理
- π_prior と π_likelihood の区別が曖昧になるケース（自己指示系）

## 既存フレームワークとの関係

- **彫刻の原理**: 「制約を加えると構造が浮かぶ」= 制約 = π_likelihood注入 → PCCで説明
- **臨界点の原理**: 「CPが最もリッチ」（what）← PCCは「precision balanceがCPを決める」（mechanism）
- **SND原理**: 「戦略的に教えない」= π_likelihood探索空間の維持 → PCCが数学的根拠
- **PCE（Prior Collapse Engineering）**: PCCのFrozen→CP誘発への応用
