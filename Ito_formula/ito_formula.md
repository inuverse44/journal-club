---
marp: true
theme: default
paginate: true
---

# Itô formula
**Tatsuki Kodama**  
*New Journal Club@Online*

---

## Table of contents
- Itô積分・Itô公式とは
- Random walk と Brown運動
- 確率微分方程式 (SDE)
- Itô積分・Itô公式の詳細
- 宇宙論への応用

---

## Itô積分・Itô公式とは
- 確率微分方程式 (SDE) を解くための枠組み
- 微積分学の**基本定理の確率版**
- **Itô積分**
$$
x(t) = x_0 + \int_0^t \left( f(x, w, t)\, \mathrm{d}t + g(x, w, t)\, \mathrm{d}w \right)
$$
- **Itô公式**
$$
\mathrm{d}h(x,t) = \left( 
\frac{\partial h}{\partial x} f + \frac{1}{2} \frac{\partial^2 h}{\partial x^2} g^2 \sigma^2 + \frac{\partial h}{\partial t} 
\right) \mathrm{d}t + \frac{\partial h}{\partial x} g\, \mathrm{d}w
$$
- **重要**：$\mathrm{d}w^2 = \sigma^2\, \mathrm{d}t$

---

## Random walk と Brown運動
- $\mathrm{d}w^2 = \sigma^2 \mathrm{d}t$ の感覚を理解する
- **Random walk** $\rightarrow$ **Brown運動** (Wiener過程)
    - 離散確率過程 $\rightarrow$ 連続確率過程

---

## Random walk
- 点 $P$：時刻 $t = 0$ で原点
- 1秒ごとに確率 $\frac{1}{2}$ で $\pm \sigma$ 移動
- $t$ 秒後の位置 $r(t)$
- $r(t)$：random walk

---

## Random walk
- $\Delta r(t) := r(t+1) - r(t)$
- $\mathbb{E}[\Delta r(t)] = 0$, $\operatorname{Var}[\Delta r(t)] = \sigma^2$
- $\mathbb{E}[r(t)] = 0$
- $\operatorname{Var}[r(t)] = \sigma^2 t$
    - ゆらぎ $\sim 1/\sqrt{t}$ に比例して増大

---

## Brown運動
- $w$: 確率変数
- 時間分割 $\Delta t = 1/n$
- $\Delta w\left(\frac{k}{n}\right) := w\left( \frac{k+1}{n} \right) - w\left( \frac{k}{n} \right)$
- $\operatorname{Var}[w(t)] = \sigma^2 t$ となるように極限
$$
\lim_{n \to \infty} w(t) \quad \text{を Brown運動 (Wiener過程) と定義}
$$
- **ここで** $\mathrm{d}w^2 = \sigma^2\, \mathrm{d}t$

---

## 確率微分方程式 (SDE)
- 現実のデータは基本的にノイズあり
    - 例）stochastic inflation, 株価, 制御工学
- 古典的微分方程式が直接適用できない
    - $\rightarrow$ トレンドとノイズを明示的に分離
- 一般形
$$
\mathrm{d}x = f(x, w, t)\, \mathrm{d}t + g(x, w, t)\, \mathrm{d}w
$$
- 特に ${\mathrm{d}x = a x\, \mathrm{d}t + b x\, \mathrm{d}w}$ は **ブラック＝ショールズ過程**

---

## SDEの統計的解釈
- 解 $x(t)$ は確率的に変動
    - 瞬間値はあまり有用でない
- 興味の対象は
    - 確率分布
    - 期待値
    - 分散
    - 相関関数などの統計量

---

## Itô積分
### 定義
$$
\int_\alpha^\beta f(x, w, t)\, \mathrm{d}t + g(x, w, t)\, \mathrm{d}w
$$
は次の極限として定義：
$$
\lim_{N \to \infty} \sum_{i} \left[ 
f(x(t_i), w(t_i), t_i) (t_{i+1} - t_i) + 
g(x(t_i), w(t_i), t_i) (w(t_{i+1}) - w(t_i))
\right]
$$
$\Rightarrow$ **Itô積分**

---

## Itô積分の例
### SDE: $\mathrm{d}x = b w\, \mathrm{d}w$
Itô積分より
$$
\begin{align}
x(t) &= x_0 + \int_0^t b w\, \mathrm{d}w \\
&= x_0 + \lim_N \sum_i b w(t_i) \left( w(t_{i+1}) - w(t_i) \right) \\
&= x_0 + \frac{1}{2} b w(t)^2 - \frac{1}{2} b \sigma^2 t
\end{align}
$$
- **$\boxed{ - \frac{1}{2} b \sigma^2 t }$** は Itô特有の項

---

## Itô公式
### 一般形
SDE:
$$
\mathrm{d}x = f\, \mathrm{d}t + g\, \mathrm{d}w
$$
に従う場合、関数 $h(x,t)$ に対して
$$
\mathrm{d}h(x,t) = \left( 
\frac{\partial h}{\partial x} f + \frac{1}{2} \frac{\partial^2 h}{\partial x^2} g^2 \sigma^2 + \frac{\partial h}{\partial t} 
\right) \mathrm{d}t + \frac{\partial h}{\partial x} g\, \mathrm{d}w
$$

---

## Itô公式の導出の流れ
$$
\begin{align}
\mathrm{d}h(x,t) 
&= \frac{\partial h}{\partial x} \mathrm{d}x + \frac{\partial h}{\partial t} \mathrm{d}t \\
&\quad + \frac{1}{2} \frac{\partial^2 h}{\partial x^2} (\mathrm{d}x)^2 + \cdots
\end{align}
$$
- $\mathrm{d}x = f\, \mathrm{d}t + g\, \mathrm{d}w$ 代入
- **$\mathrm{d}w^2 = \sigma^2 \mathrm{d}t$** 使用
- 一次の微少量のみ保持 $\Rightarrow$ Itô公式

---

## Itô公式 例
### $x = w$, $h = x^2 = w^2$
$$
\begin{align}
\mathrm{d}h 
&= \left( 2x \cdot 0 + 1 \cdot 1 \cdot \sigma^2 \right) \mathrm{d}t + 2x\, \mathrm{d}w \\
&= \sigma^2 \mathrm{d}t + 2x\, \mathrm{d}w
\end{align}
$$
Itô積分により
$$
x(t) = x_0 + \frac{1}{2} b w(t)^2 - \frac{1}{2} b \sigma^2 t
$$

---

## Itô公式 応用例
SDE:
$$
\mathrm{d}x = a x\, \mathrm{d}t + b x\, \mathrm{d}w
$$
$\Rightarrow \frac{\mathrm{d}x}{x} = a\, \mathrm{d}t + b\, \mathrm{d}w$
- $h = \log(x)$ に対して Itô公式
$$
\mathrm{d}h = \left( a - \frac{b^2 \sigma^2}{2} \right) \mathrm{d}t + b\, \mathrm{d}w
$$
- 積分すると
$$
x(t) = x_0 \exp\left[ \left( a - \frac{b^2 \sigma^2}{2} \right) t + b w(t) \right]
$$
- **$\sigma$ が大きいと減衰可能**

---

## Summary
- **Itô積分** $\rightarrow$ ノイズを含む積分
- **Itô公式** $\rightarrow$ 関数変換時のSDE
- **応用**：金融、宇宙論、制御工学など

----
## 宇宙論への応用
- Eemeli Tomberg, "Itô, Stratonovich, and zoom-in schemes in stochastic inflation", https://arxiv.org/pdf/2411.12465
- Jérôme Martin et al., "Cosmological inflation and the quantum measurement problem", https://journals.aps.org/prd/abstract/10.1103/PhysRevD.86.103524
