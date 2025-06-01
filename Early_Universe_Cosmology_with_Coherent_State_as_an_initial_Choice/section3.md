本記事では、初期宇宙におけるインフレーション期の摂動について、特にコヒーレント状態およびスクイーズドコヒーレント状態を初期状態として選択した場合に焦点を当てて議論が展開されています。背景宇宙モデルとして、空間的に平坦なFriedmann-Lemaître-Robertson-Walker (FLRW) メトリックが採用されています。

$$
    ds^{2}
    =
    a^{2} (
        -d\eta^{2} 
        + \delta_{ij}dx^{i}dx^{j}
    )
$$

ここで、$a(\eta)$ はスケールファクターであり、$\eta$ は共形時間です。メトリックシグネチャは $(- , + , + , +)$ が使用されています。
FLRWメトリックに対する時空依存のスカラー摂動は、${ \psi_{1},\psi_{2},B,E }$ で表されます。また、インフレーション場 ($\phi$) の摂動は、背景場 ($\bar{\phi}(t)$) と小さな摂動 ($\delta\phi(x^i, t)$) に分けられます。

$$ 
    \phi(x^{\mu})={}\bar{\phi}(t)+\delta\phi(x^{i},t)
$$
摂動の解析において、Mukhanov-Sasaki変数 $v(\eta)$ が重要な役割を果たします。この変数は、メトリック摂動と物質摂動のゲージ不変な組み合わせとして定義されます。

$$ 
    v
    = z
    \left(
        \psi_{2}
        + H \frac{\delta\phi}{\dot{\phi}}
    \right)
$$
ここで、$z$ は第1スローロールパラメータ $\epsilon_1$ に関連するパラメータであり、$H$ はハッブルパラメータです。インフレーションは $\epsilon_1 < 1$ の場合に発生し、スローロールとはインフレーション場がそのポテンシャル曲面に沿って非常にゆっくりと転がる状態を指し、数学的には $\dot{\phi}^2 \ll V(\phi)$ と表現されます。
系の量子化は、通常、実空間ではなくフーリエ空間で行われます。Mukhanov-Sasaki変数のフーリエ変換 $v_k$ は一般に実数ではありませんが、実空間での $v(x)$ が実数であるためには $v_k^* = v_{-k}$ という制約を満たす必要があります。摂動の2次までの作用はフーリエ空間で以下のように表現されます。

$$ 
    {}^{(2)}S
    =\frac{1}{2} \int d\eta d^{3}k
    \left[
        v^{\prime}{k}v^{\prime*}{k} 
        - \bigg(k^{2}-\frac{z^{\prime\prime}}{z}\bigg)v_{k}v^{*}_{k}
    \right] \quad 
$$
ここでプライム(')は共形時間 $\eta$ に関する微分を表し、ドット(.)は宇宙時間 $t$ に関する微分を表します。全微分項を作用に加えても運動方程式には影響しません。
量子力学の形式として、Heisenberg描像が採用されています。この描像では状態ベクトルは時間によらず一定であり、物理量に対応する線形演算子がHeisenbergの運動方程式に従って時間発展します。これはSchrödinger描像とは逆の振る舞いです。
論文では、初期状態としてコヒーレント状態 $|\alpha\rangle$ およびスクイーズドコヒーレント状態 $|r, \alpha\rangle$ を考え、これらの状態に対するMukhanov変数の相関関数を計算しています。
コヒーレント状態 $|\alpha\rangle$ に関するMukhanov変数の1点および2点相関関数は以下のようになります。
$$ 
    \braket{\alpha | \hat{v}{k} | \alpha} 
    = \frac{1}{2}\bigg[
        \alpha_{k}\mathcal{F}^\ast_{k}
        + \alpha^\dag_{-k}\mathcal{F}_{k}
    \bigg]
$$

$$ \innerproduct{\alpha}{\hat{v}{k{1}}\hat{v}{k{2}}|\alpha} = \frac{1}{4}\bigg{[}\mathcal{F}^{}{1}}\mathcal{F}^{}{k{2}}\alpha_{k_{1}}\alpha_{k_{2}}+\mathcal{F}{k{1}}\mathcal{F}{k{2}}\alpha^{}{1}}\alpha^{}{-k{2}}-\mathcal{F}^{}{1}}\mathcal{F}{2}}\alpha_{k_{1}}\alpha^{}{-k{2}} - \mathcal{F}{k{1}}\mathcal{F}^{}{2}}\alpha^{}{-k{1}}\alpha_{k_{2}} + \mathcal{F}^{*}{k{1}}\mathcal{F}{k{2}}(2\pi)^{3}\delta^{3}(k_{1}+k_{2})\bigg{]} \quad $$
ここで $\mathcal{F}_k(\eta)$ はMukhanov変数のモード関数です。パワースペクトル $\mathcal{P}_v(k)$ は2点相関関数から導出されます。
$$ \mathcal{P}{v}(k) = \innerproduct{\alpha}{\hat{v}{k_{1}}\hat{v}{k{2}} | \alpha} = \frac{1}{4}\bigg{[}\Re{\mathcal{F}^{}{1}}\mathcal{F}^{}{k{2}}\alpha_{k_{1}}\alpha_{k_{2}}}-\Re{\mathcal{F}^{}{1}}\mathcal{F}{2}}\alpha_{k_{1}}\alpha^{}{k{2}}}+\mathcal{F}^{*}{k{1}}\mathcal{F}{k{2}}(2\pi)^{3}\delta^{3}(k_{1}+k_{2})\bigg{]} \quad $$
スクイーズドコヒーレント状態 $|r, \alpha\rangle$ は、真空状態 $|0_k, 0_{-k}\rangle$ にユニタリー演算子 $\hat{U}(r, \theta, \phi)$ と変位演算子 $\hat{D}(\alpha_k), \hat{D}(\alpha_{-k})$ を作用させることで得られます。あるいは、スクイーズド真空 $|r, 0\rangle$ に変位演算子 $\hat{D}(\beta_k)$ を作用させても得られます。$\hat{U}(r, \theta, \phi)$ はスクイージング演算子 $\hat{S}(r, \phi)$ と回転演算子 $\hat{R}(\theta)$ で構成されます。
スクイーズドコヒーレント状態に対するMukhanov変数の2点相関関数は以下の形式で与えられます。
$$ \mathcal{P}{v}(k) = \innerproduct{r,\alpha}{\hat{v}{k_{1}}\hat{v}{k{2}}|r,\alpha} = \frac{1}{4}\bigg{[}\hskip 1.13791pt\mathbf{I_{1}(k_{1},k_{2})}+\hskip 1.13791pt\mathbf{I_{2}(k_{1},k_{2})}+\hskip 1.13791pt\mathbf{I_{3}(k_{1},k_{2})}+\hskip 1.13791pt\mathbf{I_{4}(k_{1},k_{2})} + \bigg{{}\bigg{(}\absolutevalue{\lambda_{1}}^{2}+\absolutevalue{\lambda_{2}}^{2}\bigg{)}-\bigg{(}\lambda_{1}\lambda_{2}+\lambda^{}_{1}\lambda^{}{2}\bigg{)}\bigg{}}(2\pi)^{3}\delta^{3}\big{(}k{1}+k_{2}\big{)}\bigg{]} \quad $$
ここで $I_1, I_2, I_3, I_4$ は補助的な関数であり、$\lambda_1, \lambda_2$ はモード関数に関連するパラメータです。これらの相関関数には、真空状態では見られないデルタ関数を含まない項が存在するという興味深い特徴があります。これは、初期状態の識別可能な特性と見なすことができます。リアルスペースでの2点相関関数も計算されています。
量子情報に関連して、系のエントロピーについても議論されています。リデュースド密度演算子 ($\hat{\rho}b$) のエントロピーは $S(\rho_b)=-\Tr{\hat{\rho}{b}\log_{2}{\hat{\rho}_{b}}}$ で定義されます。連続変数系の密度演算子の対角化は困難なため、代替手法として数演算子の期待値を用いる方法が示されています。
変位ガウス状態のエントロピーは、数演算子の期待値 ($\overline{N}k = \left\langle r,\alpha\right|\hat{N}{k}\left|r,\alpha\right\rangle$) と変位演算子の引数 ($\beta_k$) の絶対値の二乗 ($\absolutevalue{\beta_{k}}^{2}$) を用いて以下の形式で表されます。
$$ S(\rho_{k})=(\overline{M}{k}+1)\log{2}{(\overline{M}{k}+1)}-\overline{M}{k}\log_{2}{\overline{M}_{k}} \quad $$
ここで $\overline{M}k = \big{(}\overline{N}{k}-\absolutevalue{\beta_{k}}^{2}\big{)}$ です。スクイーズドコヒーレント状態のエントロピーは、スクイージングパラメータ $r$ のみで表現される場合もあります。
$$ S(\rho_{k})=\big{[}\cosh^{2}{r}\log_{2}\big{(}\cosh^{2}{r}\big{)}-\sinh^{2}{r}\log_{2}\big{(}\sinh^{2}{r}\big{)}\big{]} \quad $$
Spin-xx相関関数の積分を解析的に評価するために、いくつかの特殊関数が使用されています。これらには、Owen's T関数 ($\operatorname{OwnT}(h, a)$)、Error関数 ($\operatorname{Erf}(x)$)、およびSignum関数が含まれます。それぞれの定義は積分形式で与えられています。
$$ \operatorname{OwnT}{\big{(}h,a\big{)}}\hskip 2.84544pt=\hskip 2.84544pt\frac{1}{2\pi}\int^{a}_{0}dx\hskip 2.84544pt\frac{e^{-h^{2}(1+x^{2})/2}}{(1+x^{2})} \quad $$
$$ \operatorname{Erf}{(x)}=\frac{2}{\sqrt{\pi}}\int^{x}_{0}dz\hskip 2.84544pte^{-z^{2}} \quad $$
Error関数はガウス関数を有限区間で積分する際に必要となり、$\operatorname{Erf}(-x) = -\operatorname{Erf}(x)$ という奇関数としての性質を持ちます。
特殊関数を用いずにSpin-xx相関関数の積分を近似的に解く方法も示されています。これは、コヒーレント状態パラメータの寄与が小さいという近似のもと、積分内の指数関数をTaylor展開することで行われます。この近似計算の結果、いくつかの基本的な積分 $J_i$ が定義され、その解析解が与えられています。例えば、$J_0$ は以下のようになります。
$$ J_{0} = \int^{\infty}{0} dx \hspace{0.06cm} e^{-g{1}x^{2}} \Erf{\big{\sqrt{g_{2}}x \big}} \hspace{0.1cm} = \hspace{0.1cm} \frac{1}{\sqrt{\pi g_{1}}} \tan^{-1}{\sqrt{\frac{g_{2}}{g_{1}}}} \quad $$
論文中では、これらの積分 $J_i$ を用いて近似的な積分結果 $I_0, I_1, I_2, I_3$ を表現しています。
Bell不等式の破れを定量化するBell演算子の期待値も計算されています。この期待値は、スクイージングパラメータ $r$ や角度 $\phi$、コヒーレント状態パラメータ $\alpha_k$ の関数として振る舞いが示されています。Bell演算子の期待値は、Spin-xx相関関数の期待値に関連しており、ある角度 $\theta_2$ の関数として以下のように表すことができます。
$$ \left\langle r,\alpha \right| \hat{\mathcal{B}} \left| r,\alpha \right\rangle = 2 \big[\cos{\theta_{2}} \hspace{0.1cm} \boldsymbol{J_{0}(r,\alpha)} + \sin{\theta_{2}} \hspace{0.1cm} \boldsymbol{J_{1}(r,\alpha)} \big] \quad $$
また、時間の発展を記述するユニタリー演算子 $\hat{U}(\zeta)$ の形式とその導出についても触れられており、BCH公式などが用いられています。