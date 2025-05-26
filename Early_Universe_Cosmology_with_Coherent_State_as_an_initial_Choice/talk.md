---
marp: true
theme: default
paginate: true
---

# Early Universe Cosmology with Coherent State as an Initial Choice
### 論文概要と物理的含意（arXiv:2410.04608）

著者: Suman Kundu, Supratik Pal  
解析形式: Schrödinger & Heisenberg  
視点: 宇宙初期の量子揺らぎの初期状態の再検討

---

## インフレーション宇宙論の基礎

- 急激な膨張期で量子揺らぎが拡大
- ゲージ不変変数: Mukhanov–Sasaki 変数 $v_k$
- 標準初期状態: **Bunch-Davies 真空**
  $$
    \hat{a}_k |0\rangle = 0
  $$

---

## 本研究の提案

- 初期状態に **コヒーレント状態** を導入:
  $$
    \hat{a}_k |\alpha_k\rangle 
    = \alpha_k |\alpha_k\rangle
  $$
- 特徴: 最小不確定性、非ゼロ平均
- 目的: CMBやLSSに現れる新たな量子効果を理論的に予測

---

## 宇宙論的摂動の作用と運動方程式

- 2次作用:
  $$
    S^{(2)} 
    = \frac{1}{2} 
    \int d\eta \, 
    d^3x 
    \left[ 
        (v')^2 - (\nabla v)^2 + \frac{z''}{z} v^2 
    \right]
  $$
- 運動方程式（モード関数）:
  $$
    v_k'' 
    + \left( k^2 - \frac{z''}{z} \right) v_k 
    = 0
  $$

---

## ハイゼンベルク描像：量子揺らぎの展開

- モード展開:
  $$
    \hat{v}_k 
    = v_k \hat{a}_k 
    + v_k^* \hat{a}_{-k}^\dagger
  $$
- コヒーレント状態での期待値:
  $$
    \langle \hat{v}_k \rangle 
    \ne 0
  $$
- パワースペクトルに修正項が入る

---

## Schrödinger描像：波動関数とエンタングルメント

- 2モードスクイーズド・コヒーレント状態:
  $$
    |\alpha, z\rangle 
    = \hat{S}(z)\hat{D}(\alpha)|0\rangle
  $$
- reduced density matrix より von Neumann エントロピー:
  $$
    S 
    = \cosh^2 r \ln(\cosh^2 r) 
    - \sinh^2 r \ln(\sinh^2 r)
  $$

---

## 量子非局所性の検出：ベル不等式の違反

- GKMR演算子による CHSH不等式
- コヒーレント成分を含むスクイーズド状態が不等式を破る可能性
- CMBの非ガウス性や非局所相関と関連

---

## 結論と今後の展望

- コヒーレント状態は有力な初期状態の候補
- 観測的に検証可能な量子特徴（エンタングルメント・ベル不等式）
- 拡張課題:
  - 重力波テンソルモード
  - thermal/coherent混合状態
  - 観測的 signature の詳細予測

---

## 謝辞・参考文献

- arXiv: [2410.04608](https://arxiv.org/abs/2410.04608)
- Mukhanov, *Physical Foundations of Cosmology*
- Birrell & Davies, *Quantum Fields in Curved Space*
- GKMR formalism
