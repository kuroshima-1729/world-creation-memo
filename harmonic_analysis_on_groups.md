Book Title: 群上の調和解析

 # 第1章 位相群
 ## Section 1. 群
 **定義** </br>
 集合 $G$ 上に演算 $G\times G\rightarrow G$ が定まっており、 $\left(x,y\right)\in G\times G$ の値を $x\cdot y$ と書く。この演算が次の３条件を満たすとき $G$ はこの演算についての群であるという。</br>
 (G1) 任意の $x,y,z\in G$について、 $(x\cdot y)\cdot z = x\cdot (y\cdot z)$ （結合法則）</br>
 (G2) 任意の $x\in G$ に対して、 $e\cdot x = x\cdot e = x$ を満たす $e\in G$ が存在する。($e$は$x$に依存しない。) $e$ を $G$ の単位元という。</br>
 (G3) 任意の $x\in G$ に対して、 $y_x\cdot x = x\cdot y_x = e$ を満たす。 $y_x\in G$が存在する。( $y_x$ は $x$ に依存して決まる。)この $y_x$ を $x$ の逆元という。


任意の $x,y\in G$ について、 $x\cdot y = y\cdot x$ が成り立つとき、 $G$ は演算 $\cdot$ に関して可換群であるという。</br>


演算の記号として、+を用いる場合もあり、このとき $G$ は加群であるという。加群の単位元は零元とよび、 $0$ と記し、 $x$ の逆元は、 $-x$ と表す。

**定義** </br>
群 $G$ の部分集合 $H$ が $G$ と同じ演算の下にそれ自体がほとつの群をなすとき、 $H$ は $G$ の部分群であるという。

$H$ を $G$ の部分群であるとし、 $G$ 上の２項関係 ~ を
$$x\sim y \iff xH = yH$$
と定義すれば、 $\sim$ は同値関係である。ここで、 $xH = \lbrace xa| a\in H\rbrace$ である。この同値関係による $x\in G$ の同値類は $\xi_x$ は、
$$\xi_x =\lbrace y\in G\|xH=yH\rbrace$$
である。 $G$ の $\sim$ による商集合 $\lbrace\xi_x | x\in G\rbrace$ を $G/H$ で表す。同値類 $\xi_x$ を右-剰余類という。

$x, y\in G$ が同じ剰余類に属するためには、 $x^{-1}y\in H$ であることが必要充分である。このとき $x$ と $y$ とは $H$ を法として合同であると言い、
$$x\equiv y (\rm{mod} \ \ \  H)$$
と表記する。

同値関係 $\sim$ を
$$x\sim y \iff Hx=Hy$$
と定義した場合は、この $\sim$ による同値類は左-剰余類といい、その集合を $H\backslash G$ で表す。

**定義**</br>
$G$ の部分群 $N$ が 任意の $a\in G$ に対して、 $aNa^{-1} = N\,\,(\iff aN=Na)$ を満たすとき、 $N$ は $G$ の正規部分群であるという。

群 $G$ の正規部分群 $N$ について、 $G/N = G\backslash N$ は群をなす。 $x\in G$ の剰余類を $\xi_x$ と書くことにすれば、 $\xi_x = xN$ である。 $\xi_x, \xi_y\in G$ に対して、
$$(\xi_x)\cdot (\xi_y) = \xi_{x\cdot y}, \ \ \  (\xi_x)^{-1}=\xi_{x^{-1}}$$
すなわち、
$$(xN)\cdot (yN) = (x\cdot y)N, \,\,\, (xN)^{-1}=x^{-1}N$$
なる演算を定めれば、 $G/N$ はこの演算の下に群となり、これらの演算は、well-definedである。 $G/N$ を $G$ の $N$ に関する商群とよぶ。 $G/N$ の単位元は $N$、 $xN$ の逆元は、 $x^{-1}N$ である。  

$G$, $G^{\prime}$ を群(情報演算をともに $\cdot$ で記す)とし、写像 $\varphi : G\rightarrow G^{\prime}$ が
$$\varphi (x\cdot y) = \varphi (x)\cdot \varphi (y),  x,y \in G$$
を満たすとき、 $\phi$ は準同型写像であるという。特に、$\varphi$ が全単射でもある場合は、これを同型写像という。

$G$ と $G^{\prime}$ の間になにか同型写像が存在するとき、 $G$ と $G^{\prime}$ はこの写像を媒介として、同型であるといい、これを $G\simeq G^{\prime}$ という記号で表記する。

$G$ と $G^{\prime}$ の単位元をそれぞれ $e$ と $e^{\prime}$ と書けば、準同型写像 $\varphi : G\rightarrow G^{\prime}$ に対して $\varphi (e) = e^{\prime}$ であり、 $\varphi (x^{-1})= \varphi(x)^{-1} (x\in G)$ である。また $\varphi$ の像 $\varphi (G)$ は $G^{\prime}$ の部分群である。

順同型写像 $\varphi: G\rightarrow G^{\prime}$ に対して、集合
$$Ker\varphi = \lbrace x\in G | \varphi (x)=e^{\prime} \rbrace$$
は正規部分群であり、これを $\phi$ の核と呼ぶ。
(任意の $x\in G$ に対して、 $y\in x Ker\varphi x^{-1}$ とすると、ある $a\in Ker\varphi$ が存在して、 $y=xax^{-1}$ 。このとき $\varphi (xax^{-1})=\varphi (x)\varphi (a)\varphi (x^{-1})=\varphi (x)e^{\prime}\varphi (x)^{-1}=e^{\prime}$ より、 $y\in Ker\varphi$ 。逆に $y\in Ker\varphi$ とすると、$y=xx^{-1}yxx^{-1}$ かつ $\varphi (xyx^{\prime}) = e^{\prime}$ なので、 $y\in xKer\varphi x^{-1}$ )

$1^{\circ}$　$G$, $G^{\prime}$ は群、 $\varphi : G\rightarrow G^{\prime}$ は準同型写像でかつ全射であるとする。 $N$ が $G$ の正規部分群ならば、 $\varphi (N)$ は $G^{\prime}$ の正規部分群である。</br>
証明) 任意の $y\in G^{\prime}$ に対して、 $y=\varphi (x)$ を満たす $x\in G$ が存在する。 $x^{-1}Nx\subset N$ であるから
$$y\varphi (N) y^{-1}=\varphi(x)\varphi(N)\varphi(x)^{-1}=\varphi(xNx^{-1})\subset \varphi (N)$$
ゆえに $\varphi(N)$ は $G$ の正規部分群である。 </br>
$2^{\circ}$ $G$ は群、 $N$ をその正規部分群とし、写像 $\pi : G\rightarrow G/N$ を $\pi : x\mapsto xN \ (x\in G)$ と定義する。これを自然な写像または標準的写像という。 $\pi$ は準同型写像で、 $\pi (N)$ は $G/N$ の正規部分群である。
証明) $\pi$ は全射で、 $N$ が $G$ の正規部分群なので $1^{\circ}$ から導かれる。

**定理 1.1** <br>
$G$, $G^{\prime}$ は群、 $\varphi : G\rightarrow G^{\prime}$ は準同型写像とする。このとき $G/Ker\varphi$ と $\varphi(G)$ とは群として同型である。同型写像は
$$\Phi : x\cdot Ker\varphi \mapsto \varphi(x), \ \ x\in G$$
によって与えられる。</br>
証明) 全射性: 任意の $y=\varphi (x)$ に対し、 $x\cdot Ker\varphi$ をとれば、 $\Phi(x\cdot Ker\varphi)=\varphi (x)$ より全射。</br>
単射性: $\Phi (x\cdot Ker\varphi)=\Phi (x^{\prime}\cdot Ker\varphi)$ とすると $\varphi(x)=\varphi(x^{\prime})$ で、 $e^{\prime}=\varphi(x)\varphi(x^{\prime})=\varphi(x {x^{\prime}}^{-1})$ なので、 $x {x^{\prime}}^{-1} \in Ker\varphi$ よって、 $xKer\varphi=x^{\prime}Ker\varphi$ である。
さらに、 $\Phi$ は準同型写像である。実際、 $x, x^{\prime}$ に対して、
$$\Phi(xKer\varphi\cdot x^{\prime}Ker\varphi)=\Phi(xx^{\prime}Ker\varphi)=\varphi(x\cdot x^{\prime})=\varphi(x)\varphi(x^{\prime})=\Phi(xKer\varphi)\cdot \Phi(x^{\prime}Ker\varphi)$$
であるから、 $\Phi$ は準同型写像である。したがって、
$$G/Ker\varphi \simeq \varphi(G)$$
 
**定理 1.2** </br>
$G$, $G^{\prime}$ は群、 $\varphi: G\rightarrow G^{\prime}$ は準同型全射とする。 $H^{\prime}$ を $G^{\prime}$ の正規部分群とすれば、 $H=\varphi^{-1}(H^{\prime})$ は $G$ の正規部分群で
$$G/H\simeq G^{\prime}/H^{\prime}$$
証明) 写像 $\Phi: G\rightarrow G^{\prime}/H^{\prime}$ を
$$\Phi: x\mapsto \varphi(x)H^{\prime}$$
と定義すると、 $\Phi$ は全射の準同型である。( $yH^{\prime}\in G^{\prime}/H^{\prime}$ とすると、 $\varphi$ の全射性から $y=\varphi(x)$ となる $x\in G$ がある。この $x$ をとればよい。) </br>
$\Phi$ の核は、
$$Ker\Phi = \lbrace x\in G | \Phi(x)=H^{\prime} \rbrace = \lbrace x\in G | \varphi(x)H^{\prime} = H^{\prime} \rbrace \\ = \lbrace x\in G | \varphi(x)\in H^{\prime} \rbrace = \varphi^{-1}(H^{\prime}) = H$$
である。したがって、定理 1.1 により、
$$G/H\simeq G^{\prime}/H^{\prime}$$

**系 1.1** $G$ は群、 $H$ と $N$ は $G$ の正規部分群で、しかも $N\subset H$ とする。このとき
$$(G/N)/(H/N)\simeq G/H$$
証明) $G^{\prime} = G/N$ 、 $H^{\prime}=H/N$ とする。 $H^{\prime}$ は $G^{\prime}$ の正規部分群である。 $\pi: G\rightarrow G/N$ を自然な写像 $x\mapsto xN$ として、これを定理1.2の $\varphi$ に見立てれば、
$$\pi^{-1}(H^{\prime})=\lbrace g\in G | \pi(g)=H^{\prime} \rbrace = \lbrace g\in G | gN=H/N \rbrace$$
で、 $N\subset H$ より、
$$\pi^{-1}(H^{\prime})=\lbrace g\in G | g\in H \rbrace = H$$
よって、定理 1.2 より、
$$G/H\simeq G^{\prime}/H^{\prime} = (G/N)/(H/N)$$

## Section 2. 位相群の概念
**定義** 集合 $G$ が次の３条件を満たすとき、それは位相群であるという。</br>
(TG-1) $G$ は群である。</br>
(TG-2) $G$ は位相空間である。</br>
(TG-3) $G$ 上で定義されている群の演算が、与えられた位相に関して連続である。</br>

$G$ 上の群の演算を仮に </br>
乗法演算 : $(x,y)\mapsto x\cdot y \ \ [G\times G\rightarrow G]$ </br>
逆元の演算 : $x\mapsto x^{-1} \ \ [G\rightarrow G]$ </br>
とすれば、(TG-3) の意味するところは、この二つが連続であることである。これは演算
$$(x,y)\mapsto x\cdot y^{-1} \ \ [G\times G\rightarrow G]$$
が連続であることと同値である。</br>

例:</br>
$G=\mathbb{R}$ とし、その上に定まる位相はユークリッド位相であるとする。このとき $\mathbb{R}$ は加法についての位相群となる。</br>
$G=\mathbb{R}^l$ とし、その上にEuclid位相を定めれば、 $\mathbb{R}^l$ はベクトルの加法演算についての位相群( $l$ 次元ベクトル群 )となる。</br>
$G=\{z\in \mathbb{C} : |z|=1 \}$ は複素数の乗法と、 $\mathbb{C}$ から導入される相対位相について位相群となる。</br>
$(n\times n)$-型の実行列の全体は行列の和に関して可換群、またそのうち正則行列の全体 $GL$ は行列の積について非可換群を成し、いずれも ${\mathbb{R}}^{n^2}$ のEuclid位相の下に位相群となる。 $GL$ の元のうち行列式の値が $1$ に等しいものの全体 $SL$ は、行列の積についての群をなし、やはり位相群である。


## Section 3. 位相群の位相
位相群の特徴: 代数的な演算と、位相的な性質の間に密接な関係があり、その結果として、群の構造をもつ $G$ に位相群としての位相を導入するには、全空間にわたる基底を指定する必要はなく、単位元 $e$ の完全近傍系(すべての近傍の族)を指定すれば十分である。</br>
$A, B\subset G$ に対し、
$$
A\cdot B = \{x\cdot y\ | x\in A, y\in B\}, \ \ A^{-1} = \{x^{-1} | x \in A \}
$$
などと書く。</br>
**定義** </br>
集合 $X$ の部分集合の族 $\mathscr{F}$ が次の３条件を満たすとき、 $\mathscr{F}$ は $X$ 上の**フィルター**という。</br>
(1) $A, B\in \mathscr{F} \Rightarrow A\cap B \in \mathscr{F}$ </br>
(2) $A\in \mathscr{F}, A\subset B \Rightarrow B\in \mathscr{F}$ </br>
(3) $\empty \notin \mathscr{F}$ </br>

いま、位相群の単位元 $e$ の完全近傍系の作るフィルターを $\mathscr{N}$ とする。 $a$ を $G$ の任意の元とするとするとき、写像
$$
x\mapsto a\cdot x; \ \ x\mapsto x\cdot a
$$ 
は $G$ から $G$ への位相同型写像である。したがって、
$$
a\mathscr{N}=\{aV|V\in \mathscr{N}\}, \mathscr{N}a = \{Va| V\in\mathscr{N}\}
$$
は点 $a$ の完全近傍系になる。このようにして、単位元 $e$ の完全近傍系を知ることにより、ほかの任意の点における完全近傍系を知ることができる。

$e$ の完全近傍系 $\mathscr{N}$ は次の三条件を満たす。
(1) 任意の $U\in \mathscr{N}$ に対して、 $VV\subset U$ を満たす $N\in\mathscr{N}$ が存在する。</br>
証明) 群の乗法演算を $m: G\times G\rightarrow G$ とする。 $int(U)$ は $e$ の開近傍であり、 $m$ の連続性から、 $m^{-1}(int(U))$ は $(e, e)$ の開近傍なので、 $V\times V\subset m^{-1}(int(U))\subset m^{-1} (U)$ となる $V\in \mathscr{N}$ が存在する。 $ab\in VV$ とすると、 $(a, b) \in V\times V \subset m^{-1}(U)$ より、 $ab=m((a,b))\in U$ したがって、 $VV\subset U$ </br>
(2) 任意の $U\in \mathscr{N}$ に対して、 $U^{-1}\in\mathscr{N}$。</br>
証明) 写像 $x\mapsto x^{-1}$ が $G$ を $G$ 自身に移す位相同型写像であるから、開写像。したがって、 $e = x^{-1}(e)\in x^{-1}(U^{\circ})=(U^{\circ})^{-1}\subset {U^{-1}}^{\circ} \subset U^{-1}$ (後ろから2番目の縫合関係は、内部は最大の開集合であることから)。または単に $e\in (U^{-1})^{\circ}=U^{-1}$ なので。 </br>
(3) 任意の $a\in G$ 、 任意の $U\in\mathscr{N}$ に対して、 $aUa^{-1}\in \mathscr{N}$ 。 </br>
証明) $a\in G$ を一つ固定したとき、 $x\mapsto ax$ 、 $x\mapsto xa^{-1}$ がいずれも $G$ から $G$ への位相同型写像、したがって開写像であることから、 $e=aea^{-1}\in aUa^{-1}$ なので、 $U\in \mathscr{N}$。

ここで、フィルター $\mathscr{N}$ について "(1)および(2)" が成り立つことは次の(\*)と同値である。</br>
(\*) 任意の $U\in \mathscr{N}$ に対して、 $VV^{-1}\subset U$ かつ $V^{-1}\in \matscr{N} を満たす $V\in \mathscr{N}$$ が存在する。</br>
証明) フィルター $\mathscr{N}$ について、 (1)と(2)が成り立つと仮定する。任意の $U\in \mathscr{N}$ に対して、(1) から $WW\subset U$ を満たす $W\subset \mathscr{N}$ が存在する。また (2) によって、 $W^{-1}\in \mathscr{N}$ であるから、 $V=W\cap W^{-1}$ とおけば、 $V\in \mathscr{N}$ (フィルターの定義(2))。(2)より $V^{-1}\in\mathscr{N}$ かつ $V^{-1}\subset W$ となり、したがって $VV^{-1}\subset WW \subset U$。</br>
逆にフィルター $\mathscr{N}$ が (\*)を満たすとする。このとき任意の $U\in\mathscr{N}$ について、 $e\in U$ となる。実際、 $V\in\mathscr{N}$ が $VV^{-1}\subset U$ とすれば、 ( $V$は非空であるから)すべての $x\in V$ について、 $xx^{-1}=e\in U$ となるからである。 (\*)より $V\subset VV^{-1}\subset U$。したがって、 $V\subset U^{-1}$ であるからフィルターの定義 (2) より $U^{-1}\in\mathscr{N}$ である。 $V\in \mathscr{N}$ が $VV^{-1}\subset U$ を満たすものとし、 $W=V\cap V^{-1}$ とおけば、 $W\in\mathscr{N}$ で (フィルターの定義(1)より)かつ $WW\subset VV^{-1}\subset U$ である。

上に定義した $W=V\cap V^{-1}$ は、 $e$ の近傍で、しかも $W=W^{-1}$ が成り立つ。この性質を対称性という。

**定理** 1.3 </br>
$G$ を群、 $\mathscr{N}$ を上記の (1)、(2)、(3) を満足する $G$ 上の フィルターとする。このとき $G$ を位相群とし、かつ $\mathscr{N}$ を単位元 $e$ の完全近傍系とする $G$ の位相が一意に定まる。




