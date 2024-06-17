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

$G$, $G^{\prime}$ を群(乗法演算をともに $\cdot$ で記す)とし、写像 $\varphi : G\rightarrow G^{\prime}$ が
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

$e$ の完全近傍系 $\mathscr{N}$ は次の三条件を満たす。</br>
(1) 任意の $U\in \mathscr{N}$ に対して、 $VV\subset U$ を満たす $V\in\mathscr{N}$ が存在する。</br>
証明) 群の乗法演算を $m: G\times G\rightarrow G$ とする。 $int(U)$ は $e$ の開近傍であり、 $m$ の連続性から、 $m^{-1}(int(U))$ は $(e, e)$ の開近傍なので、 $V\times V\subset m^{-1}(int(U))\subset m^{-1} (U)$ となる $V\in \mathscr{N}$ が存在する。 $ab\in VV$ とすると、 $(a, b) \in V\times V \subset m^{-1}(U)$ より、 $ab=m((a,b))\in U$ したがって、 $VV\subset U$ </br>
(2) 任意の $U\in \mathscr{N}$ に対して、 $U^{-1}\in\mathscr{N}$。</br>
証明) 写像 $x\mapsto x^{-1}$ が $G$ を $G$ 自身に移す位相同型写像であるから、開写像。したがって、 $e = x^{-1}(e)\in x^{-1}(U^{\circ})=(U^{\circ})^{-1}\subset {U^{-1}}^{\circ} \subset U^{-1}$ (後ろから2番目の縫合関係は、内部は最大の開集合であることから)。または単に $e\in (U^{-1})^{\circ}=U^{-1}$ なので。 </br>
(3) 任意の $a\in G$ 、 任意の $U\in\mathscr{N}$ に対して、 $aUa^{-1}\in \mathscr{N}$ 。 </br>
証明) $a\in G$ を一つ固定したとき、 $x\mapsto ax$ 、 $x\mapsto xa^{-1}$ がいずれも $G$ から $G$ への位相同型写像、したがって開写像であることから、 $e=aea^{-1}\in aUa^{-1}$ なので、 $U\in \mathscr{N}$。

ここで、フィルター $\mathscr{N}$ について "(1)および(2)" が成り立つことは次の(\*)と同値である。</br>
(\*) 任意の $U\in \mathscr{N}$ に対して、 $VV^{-1}\subset U$ かつ $V^{-1}\in \mathscr{N}$ を満たす $V\in \mathscr{N}$ が存在する。</br>
証明) フィルター $\mathscr{N}$ について、 (1)と(2)が成り立つと仮定する。任意の $U\in \mathscr{N}$ に対して、(1) から $WW\subset U$ を満たす $W\subset \mathscr{N}$ が存在する。また (2) によって、 $W^{-1}\in \mathscr{N}$ であるから、 $V=W\cap W^{-1}$ とおけば、 $V\in \mathscr{N}$ (フィルターの定義(2))。(2)より $V^{-1}\in\mathscr{N}$ かつ $V^{-1}\subset W$ となり、したがって $VV^{-1}\subset WW \subset U$。</br>
逆にフィルター $\mathscr{N}$ が (\*)を満たすとする。このとき任意の $U\in\mathscr{N}$ について、 $e\in U$ となる。実際、 $V\in\mathscr{N}$ が $VV^{-1}\subset U$ とすれば、 ( $V$は非空であるから)すべての $x\in V$ について、 $xx^{-1}=e\in U$ となるからである。 (\*)より $V\subset VV^{-1}\subset U$。したがって、 $V\subset U^{-1}$ であるからフィルターの定義 (2) より $U^{-1}\in\mathscr{N}$ である。 $V\in \mathscr{N}$ が $VV^{-1}\subset U$ を満たすものとし、 $W=V\cap V^{-1}$ とおけば、 $W\in\mathscr{N}$ で (フィルターの定義(1)より)かつ $WW\subset VV^{-1}\subset U$ である。

上に定義した $W=V\cap V^{-1}$ は、 $e$ の近傍で、しかも $W=W^{-1}$ が成り立つ。この性質を対称性という。

**定理** 1.3 </br>
$G$ を群、 $\mathscr{N}$ を上記の (1)、(2)、(3) を満足する $G$ 上の フィルターとする。このとき $G$ を位相群とし、かつ $\mathscr{N}$ を単位元 $e$ の完全近傍系とする $G$ の位相が一意に定まる。</br>
証明) 仮に所望の性質を持つ位相が存在するとすれば、各点 $a\in G$ の完全近傍系は、 $a\mathscr{N}$ および $\mathscr{N}a$ からなる集合族と一致する。このようにして、各点の完全近傍系が定まるので、所望の性質を有する $G$ 上の位相はただ一つである。</br>
次の2点を示す必要がある。</br>
(A) フィルター $a\mathscr{N}$ が点 $a\in G$ 上の完全近傍系となる $G$ 上の位相がある。</br>
(位相があること) </br>
(B) この位相について、 $G$ 上の群の演算が連続となる。</br>
( $G$ がこの位相の下で位相群となること) </br>
(A) の証明 </br>
これを示すためには各 $a\in G$ について、 $a\mathscr{N}$ が次の４つの条件を満たすことを確認すればよい。</br>
(1) $U\in \mathscr{N}$ に対して、 $aU\subset P$ ならば $P\in a\mathscr{N}$ </br>
(2) $a\mathscr{N}$ に属する任意有限個の集合の共通部分は $a\mathscr{N}$ の元である。</br>
(3) 任意の $U\in \mathscr{N}$ について、 $a\in U$ </br>
(4) 任意の $U\in \mathscr{N}$ について、
$$
xV\subset aU {\rm{ \ \ for \ \ all \ \ }} x\in aV (したがって、aU\in x\mathscr{N})
$$
を満たす $V\in\mathscr{N}$ が存在する。</br>
近傍系参照 : https://ja.wikipedia.org/wiki/%E8%BF%91%E5%82%8D%E7%B3%BB#:~:text=%E8%BF%91%E5%82%8D%E7%B3%BB%20%E6%95%B0%E5%AD%A6%20%E3%81%AE%20%E4%BD%8D%E7%9B%B8%E7%A9%BA%E9%96%93%E8%AB%96%20%E5%91%A8%E8%BE%BA%E5%88%86%E9%87%8E%E3%81%AB%E3%81%8A%E3%81%84%E3%81%A6%E3%80%81%E7%82%B9%E3%81%AE%20%E8%BF%91%E5%82%8D%E7%B3%BB%20%EF%BC%88%E3%81%8D%E3%82%93%E3%81%BC%E3%81%86%E3%81%91%E3%81%84%E3%80%81%20%E8%8B%B1%3A,basis%29%20%E3%81%82%E3%82%8B%E3%81%84%E3%81%AF%20%E5%B1%80%E6%89%80%E5%9F%BA%20%28local%20basis%29%20%E3%81%A8%E3%81%AF%E3%80%81%E8%BF%91%E5%82%8D%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF%E3%83%BC%E3%81%AE%20%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF%E3%83%BC%E5%9F%BA%20%E3%82%92%E3%81%84%E3%81%86%E3%80%82 </br>

(1) と (2) は $a\mathscr{N}$ がフィルターであることを意味している。(それぞれフィルターの定義(2)と(1)から導かれる。) $\mathscr{N}$ の定め方から、(3)も成り立つ( $e\in U$ )。(4) だけ示せば十分である。任意の $U\in\mathscr{N}$ を考えると、完全近傍系の性質(1)より、 $VV\subset U$ を満たす $V\in\mathscr{N}$ が存在する。すると任意の $x\in aV$ に対して、
$$
xV \subset aVV \subset aU
$$
ゆえに、 $aU\in x\mathscr{N}$。</br>
(B) の証明: 演算 $(a, b)\mapsto ab^{-1}$ が連続となることを示す。</br>
$U$ を $e$ の任意の近傍とすれば、 (3)により
$$
V\equiv b^{-1}Ub\in \mathscr{N} \tag{1}
$$
この $V$ に対して、(1)、(2) $\iff$ (\*) より、 $WW^{-1}\subset V$ なる $W\in\mathscr{N}$ が存在する。 いま $u, v\in W$ とすれば、 $uv^{-1}\in V$ であり、 したがって、 (1) により、 $buv^{-1}b^{-1}\in U$ 。よって、
$$
u\in W, v\in W \Rightarrow (au)(bv)^{-1}=(ab^{-1})(buv^{-1}b^{-1})\in ab^{-1}U
$$

定理1.3 において、群 $G$ 各点の完全近傍系を指定することにより、 $G$ の位相群としての位相が決定されることを示した。</br>
$G$ の位相は基本近傍系を指定するだけでも決定される。

**定義** </br>
$(S, \mathscr{O})$ を一つの位相空間とし、 $V(x)$ を点 $x$ の(全)近傍系とする。 $V(x)$ の部分集合 $V^{*}(x)$ で次の性質をもつものを、 $x$ の基本近傍系という。</br>
(\*) 任意の $V\in V(x)$ に対して、 $U\subset V$ となるような $U\in V^{*}(x)$ が存在する。

単位元 $e$ の開集合からなる基本近傍系を $\mathscr{B}(e)$ とすると、</br>
(※) 任意の $U, V\in \mathscr{B}(e)$ に対し、 $W\subset U\cap V$ を満たす $W\in \mathscr{B}(e)$ が存在する。</br>
証明) $U\cap V$ は $e$ の近傍であるから(開集合かつ $e\in U^{\circ}\cap V^{\circ}=(U\cap V)^{\circ}$)、基本近傍系の定義より、 $W\subset U\cap V$ となるような $W\in \mathscr{B}(e)$ が存在する。</br>
$(1^{\prime})$ 任意の $U\in\mathscr{B}(e)$ に対して、 $VV\subset U$ を満たす $V\in \mathscr{B}(e)$ が存在する。</br>
証明) 任意の $U\in \mathscr{B}(e)$ に対して、 $U$ は $e$ の近傍なので、 近傍系の性質(1)より、 ある近傍 $W$ が存在して、 $WW\subset U$ となる。近傍 $W$ に対して、$V\in \mathscr{V}(e)$ が存在して、 $V\subset W$ となる。 したがって、 $VV\subset WW\subset U$。</br>
$(2^{\prime})$ 任意の $U\in\mathscr{B}(e)$ に対して、 $U^{-1}\in\mathscr{B}(e)$</br>
証明) $U\in \mathscr{B}(e)$ で、近傍なので、近傍系の性質(2)から $U^{-1}$ も近傍である。 したがって、基本近傍系の定義から、 ある $W\in \mathscr{B}(e)$ s.t $W\subset U^{-1}$ である。よって、$W$ はまた近傍であるから、 $U^{-1}\in\mathscr{B}(e)$。</br>
$(3^{\prime})$ 任意の $U\in \mathscr{B}(e)$ 、 $a\in G$ に対して、 $V\subset aUa^{-1}(\iff a^{-1}Va\subset U)$ を満たす $V\in\mathscr{B}(e)$ が存在する。</br>
証明) 近傍の性質(3)より、 $aUa^{-^1}$ は近傍である。したがって、基本近傍系の定義から、 $V\subset aUa^{-1}$ を満たす $V\in\mathscr{B}(e)$ が存在する。</br>
$(4^{\prime})$ 任意の $U\in\mathscr{B}(e)$ と $x\in U$ に対して、 $xV\subset U$ を満たす $V\in\mathscr{B}(e)$ が存在する。</br>
証明) $U$ は $x$ の近傍なので、 $U\in x\mathscr{N}$ よって、 ある $U^{\prime}\in \mathscr{N}$ に対して、 $U = xU^{\prime}$ 。 $U^{\prime}\in \mathscr{N}$ より、 ある $V\in \mathscr{B}(e)$ があって、 $V\subset U^{\prime}$ 。したがって、 $xV\subset xU^{\prime}=U$ 。

$\mathscr{B}(e)$ に属する集合に $x\in G$ を乗じ、
$$
\mathscr{B}(e)=\{V\subset G | xU\subset V \rm{\ for \ \ some\ }U\in\mathscr{B}(e)\}
$$
が点 $x$ の完全近傍系をつくるフィルターとなる。</br>
証明) (1) $U, V\in \mathscr{N}(x)$ とすると、ある $U^{\prime}, V^{\prime}\in\mathscr{B}(e)$ があって、 $xU^{\prime}\subset U$ 、 $xV^{\prime} \subset V$ を満たす。このとき
$$
x(U^{\prime}\cap V^{\prime})=xU^{\prime}\cap xV^{\prime}\subset U\cap V
$$
$U^{\prime}\cap V^{\prime}\in \mathscr{N}(e)$ より $U\cap V\in\mathscr{N}(e)$ である。 </br>
(2) $U\in\mathscr{N}(e)$ 、 $U\subset V$ とする。 このときある $U^{\prime}\in \mathscr{B}(e)$ があって、 $xU^{\prime}\subset U\subset V$ 。したがって、 $V\in \mathscr{N}(x)$ である。</br>
(3) 任意の $U\in \mathscr{N}(x)$ に関して、 $x\in U$ なので、 $U\neq\empty$ である。したがって、 $\empty \notin \mathscr{N}(x)$ 。

そして逆にまだ位相の定まっていない群 $G$ 上に $(1^{\prime})$ ~ $(4^{\prime})$ を満たす集合族 $\mathscr{B}(e)$ が与えられれば、これを $e$ の開集合からなる基本近傍系とする $G$ の位相が定まり、 $G$ は位相群となる。</br>
証明) $\mathscr{N(x)}$ が完全近傍系の公準 $(1)$ ~ $(3)$ を満たすフィルターであることを示す。フィルターであることは上で証明したため、 $\mathscr{N(x)}$ が完全近傍系の公準 $(1)$ ~ $(3)$ を満たすことを証明する。</br>
(おそらく (※)、$(1^{\prime})～(4^{\prime})$ から導けると思うが、わからない)

定理 1.3'</br>
群 $G$ の単位元 $e$ を含む集合族 $\mathscr{B}(e)$ が条件(※) および $(1^{\prime})～(4^{\prime})$ を満足するならば、 $G$ を位相群とし、かつ $\mathscr{B}(e)$ を単位元 $e$ の開集合からなる基本近傍系とする位相が位置に定まる。

次の定理は位相群 $G$ の分離公理に関するものであり、位相群 $G$ においては $T_0, T_1, T_2, T_3$ が同値となる。
![alt text](../images/separation_axiom.png)
参考: https://www.youtube.com/watch?v=Ebr1piFxEwI </br>
$(T_0)$ (Kolmogorovの公理) 相異なる２点の少なくとも一方が他方を含まない近傍を有する。</br>
$(T_1)$ (Fechetの公理) 相異なる２点はそれぞれ他方を含まない近傍を有する。</br>
$(T_2)$ (Hausdorffの公理) 相異なる２点はそれぞれ互いに交わらない近傍を有する。</br>
$(T_3)$ (Vietorisの公理) 任意の閉集合 $F$ とこれに含まれない点はそれぞれ交わらない近傍を有し(正則性)、かつ $T_1$。</br>
$(T_4)$ (Tietzeの公理) 交わらない二つの閉集合は互いに交わらない近傍を有し(正規性)かつ$T_1$。<br>
すぐにわかる関係として、
$$
T_4\Rightarrow T_3\Rightarrow T_2 \Rightarrow T_1\Rightarrow T_0
$$

**定理 1.4**(位相群の分離公理)
位相群 $G$ について、 $T_0, T_1, T_2, T_3$ はすべて同値である。</br>
証明) $T_0\Rightarrow T_2,T_3$ を証明すれば十分である。</br>
$T_o\Rightarrow T_2$: $a,b\in G$, $a\neq b$ とすれば、$G$ が $T_0$ であるから、例えば $a\in U$、$b\notin U$ となる開集合が存在する。このとき互いに交わらない $a,b$ の近傍が存在することを示す。このとき一般性を失うことなく、 $a=e, b\neq e$ および $e\in U, b\notin U$ として証明すれば十分である(一般的には、$a, b$を考えて、$e, a^{-1}b$において証明されていることを利用すればよい。) そこで、 $VV^{-1}\subset U$ を満たす $e$ の近傍 $V$ をとる(定理1.3より)。 $e\in V$ 、 $b\in bV$ であるから、仮に $b\cap bV\neq\empty$ であるとし、 $x\in V\cap bV$ とすれば、
$$
x\in V \ and \ x=by \ for \ some \ y\in V 
$$
したがって、
$$
b=xy^{-1} \in VV^{-1}\subset U
$$
これは $b\notin U$ に矛盾する。</br>
$T_0\Rightarrow T\_3$ : $F\subset G$ を 閉集合で、 $e\notin F$ とする。このとき $G\backslash F$ は $e$ の近傍であるから、 $e$ の適当な近傍 $V$ をとれば、
$$
VV\subset G\backslash F
$$
とすることができる。これから、 前と同様にして、 $V\cap FV=\empty$ となる。 また、 $FV=\cup_{x\in F}xV$ であるから、 $FV$ は開集合。 そして、 $e\in V$ 、 $F\subset FV$ であるから、正則である。 また、 $G$ は $T_2$ でもあるから、 $T_1$ である。したがって、 $G$ は $T_3$ である。

## Section 4. 距離付け定理
距離 $d$ から定められる位相空間を、 $\mathscr{O}_d$ と書くことにする。

**定義**
与えられた位相空間 $(S, \mathscr{O})$ に対して、 $\mathscr{O}=\mathscr{O}_d$ となるような $S$ 上の距離関数 $d$ が存在するならば、 $d$ はこの位相空間 $(S, \mathscr{O})$ を距離付けるといい、また、 $(S, \mathscr{O})$ は距離付け可能であるという。

位相群の距離付けに関しては、次の定理が知られている。</br>
**定理 1.5**(距離付け) </br>
$G$ を Hausdorff 位相群とする。このとき、 $G$ が距離付け可能であるための必要充分条件は、単位元 $e$ の加算近傍系が存在することである。さらに、 $G$ が距離付け可能であれば、 $G$ は左不変な、すなわち
$$
\rho(ax, ay) = \rho(x, y) \ for \ all a, x, y \in G
$$
を満たす $\rho$ によって、距離付け可能である。</br>
証明) 距離付け可能な空間は、加算近傍系が存在する。位相空間 $X$ の距離を $d$ として、 
$$
N_{1/n}(a) = \{x\in X : d(x, a)< \epsilon \}
$$
とすると $N_{1/n}(a)$ は点 $a$ の可算基本近傍系となる。 実際、任意の $\epsilon$ 対して、アルキメデスの性質(連続性の公理から証明される)から ある $n_0$ が存在して、
$$
1< \epsilon n_0
$$
となる。そこで、 $n\ge n_0$ とすれば、$1/n\le 1/n_0\ < \epsilon$ より、
$$
N_{1/n}(a)\subset N_{\epsilon}(a)
$$
となるので、 $\{N_{1/n}(a) \}_{n\in \mathbb{N}}$ は 点 $a$ における $X$ の基本近傍系である。さらに、 その数は自然数濃度に等しいため、可算である。逆を証明する。 $N_1,N_2\dots $ を $e$ の可算基本近傍系とする。まず $U$ を $e$ の近傍とすれば、 $V=U\cap U^{-1}$ も $e$ の近傍で、 $V=V^{-1}$ である。また、乗法演算の連続性から、 基本近傍系の元 $U$ に対して、 $$VVV\subset U$$ となる近傍系の元がある。 Vに含まれる基本近傍系の元を $W$ とすれば、 $(W)^3\subset U$ となる。したがって、$N_k^{\prime} = N_k\cap N_k^{-1}$ とし、 $(N_{k+1}^{\prime})^3\subset N_k^{\prime}$ となるように選択すれば、新しい $e$ の基本近傍系を、
$$
\begin{matrix}
\{N_k^{\prime}\}は対称的 \\
 (N_k^{\prime})^3\subset N_k^{\prime} \\
 N_k^{\prime}\subset N_k
\end{matrix}
$$
とすることができる。そこで、はじめから、 $\{N_k\}$ が対称的で、しかも $N_{k+1}^3\subset N_k$ を満たすものと仮定してよい。ただし、便宜上、 $N_0=G$ とおく。

関数 $\sigma: G\times G\rightarrow \mathbb{R}$ を次のように定義する。
$$
\sigma: (x,y)\mapsto \frac{1}{2^k} \ \ if \ \ x^{-1}y\in N_k\backslash N_{k+1}, k=0, 1, 2,\dots
$$
とすると、この $\sigma$ は </br>
(1) $\sigma(x,y)\ge 0 $ </br>
(2) $\sigma(x,y)=\sigma(y,x)$ ( $N_k$ が対称的なため) </br>
(3) $\sigma(ax,ay)=\sigma(x,y)$ </br>
を満足する。そこで、 $\rho: G\times G\rightarrow \mathbb{R}$ を
$$
\rho(x,y)=inf_{x_0,\dots,x_n}\left\{\displaystyle\sum_{i=1}^{n}\sigma(x_{i-1}, x_i): x_0=x,x_1,\dots,x_n=y \right\}
$$
と定義する。ただし、inf は $x_0=x, x_1,\dots, x_n=y$ となるような、任意有限個の点 $(x_0,x_1,\dots,x_n)$についてとる。こうして定義された $\rho$ は距離関数である。 $\rho(x,y)\ge 0$ , $\rho(x,y)=\rho(y,x)$ は良い。 $\rho(x,y)\iff x=y$ を証明する。$\Rightarrow$ $\rho(x, y)=0$ なので、任意の $i$ に関して $\sigma(x_{i-1}, x_i)=0$ である。したがって、任意の $i$ に関して $x_{i-1}^{-1}x_i\in N_i\backslash N_{i+1}$ 。 よって、 $x_{i-1}^{-1}x_i=e$ であり、 $x=y$ $\Leftarrow$ $x=y$ で、 $x^{-1}y$より任意の $k$ に対して $x^{-1}y=e\in N_k\backslash N_{k+1}$ 。よって、 $\rho(x,y)=0$ 。三角不等式を証明する。 $x,y,z\in G$ と $\epsilon >0$ を勝手に与えると、 $x_0,\dots, x_n, \dots, x_m \ (x_0=x, x_n=y, x_m=z)$ を適当に選んで、
$$
\rho(x,y) > \rho(x_0,x_1)+\dots+\rho(x_{n-1}, x_n)-\frac{\epsilon}{2}
$$
$$
\rho(y,z) > \rho(x_n,x_{n+1})+\dots+\rho(x_{m-1}, x_m)-\frac{\epsilon}{2}
$$
とすることができる。ゆえに
$$
\rho(x,y)+\rho(y,z)>\displaystyle\sum_{i=1}^{m}\sigma(x_{i-1}, x_i) - \epsilon \ge \rho(x,y) - \epsilon
$$
$\epsilon$ は任意であるから、
$$
\rho(x,z)\le \rho(x,y) + \rho(y,z)
$$
また、 $\rho(ax,ay)=\rho(x,y)$ となることは、 $\sigma(ax, ay)=\sigma(x,y)$ からわかる。</br>
最後に、 $\rho$ による位相が $G$ の当初の位相と一致することを他方の位相の近傍系がもう一方の位相の近傍系に一致することを示すことで示す。それには
$$
(1) x^{-1}y\in N_k \Rightarrow \rho(x,y)\le \frac{1}{2^k}
$$
$$
(2) x^{-1}y \notin N_k \Rightarrow \rho(x,y)\ge \frac{1}{2^k}
$$
を示せば十分である。</br>
(1) の証明: $x^{-1}y\in N_k$ とすれば、 $\rho$ の定義から、 $\rho(x,y)\le \sigma(x,y)\le\frac{1}{2^k}$ </br>
(2) の証明: $x^{-1}y\notin N_k$ とする。 $\rho(x,y)>\frac{1}{2^k}$ を示すためには、 $x=x_0,x_1,\dots, x_{n-1}, x_n=y$ をみたす任意の有限個の点について 
$$
\displaystyle\sum_{i=1}^n \sigma(x_{i-1}, x_i)\ge \frac{1}{2^k}
$$
を証明すればよい。帰納法により証明する。 $n=1$ のとき、 $x^{-1}y\notin N_k$ ならば $x^{-1}y\in N_{i} \ (i\le k-1)$ なので、 $\sigma(x,y)\ge\frac{1}{2^k}$ 。 次に $p\le n-1$ であるすべての $p$ に対して、 $x_0^{-1}x_p\notin N_k$ ならば、 
$$
\displaystyle\sum_{i=1}^p \sigma(x_{i-1}, x_i)\ge\frac{1}{2^k}
$$
が成り立つと仮定する。 $x=x_0, x_1, \dots, x_n=y$ とし、 $q$ を $x_0^{-1}x_q\notin N_{k+1}$ となるような最小の添え字 $(1\le q\le n)$ とする。そこで
$$
x=x_0, \ x_{q-1}, \ x_q, \ x_n=y
$$
なる有限個の点を考えれば、帰納法の仮定により
$$
\sigma(x_0, x_{q-1}) + \sigma(x_{q-1}, x_q) + \sigma(x_q, x_n) \ge \frac{1}{2^k}
$$
($q=n$ のときは、 $n=1$ の場合を使い、 $q<n$ のときは帰納法の仮定を用いる) </br>
また、 $q$ の定義から、 $x_0^{-1}x_{q-1}\in N_{k+1}$ であるから、
$$
\sigma(x_0, x_{q-1})\le \frac{1}{2^{k+1}}
$$
(どこで使っている?) </br>
したがって、
$$
x_{q-1}^{-1}x_q\notin N_{k+1}, \ x_q^{-1}x_n\notin N_{k+1}
$$
のどちらかが成り立つ。実施、仮に $x_{q-1}^{-1}x_q\in N_{k+1}$ かつ $x_q^{-1}x_n\in N_{k+1}$ であれば、
$$
x^{-1}y=x_0^{-1}x_n=(x_0^{-1}x_{q-1})\cdot(x_{q-1}^{-1}x_q)\cdot(x_q^{-1}x_n)\in N_{k+1}^3\subset N_k
$$
となって矛盾。</br>
そこでまず $x_{q-1}^{-1}x_q\notin N_{k+1}$ とすれば
$$
\sigma(x_{q-1}, x_q)\ge \frac{1}{2^k}
$$
したがって、
$$
\displaystyle\sum_{i=1}^n \sigma(x_{i-1}x_i)\ge \frac{1}{2^k}
$$
また、 $x_q^{-1}x_n\notin N_{k+1}$ とすれば、 $\{x_0,x_1,\dots,x_n\}$を
$$
x=x_0, \dots, x_q, \dots, x_n=y
$$
の形に分解して、帰納法の仮定から
$$
\sigma(x_0,x_1) + \dots + \sigma(x_{q-1}, x_q)\ge \frac{1}{2^{k+1}}
$$
$$
\sigma(x_q,x_{q+1})+\dots+\sigma(x_{n-1},x_n)\ge \frac{1}{2^{k+1}}
$$
2番目の不等式は、 $j=q+1,\dots, n-1$ で、
$$
x_qx_j = x_qx_n^{-1}x_nx_0^{-1}x_0x_j\notin (N_{k+1})\subset N_k
$$
からの結果。</br>
次の結果が得られる。 
$$
\displaystyle\sum_{i=1}^n\sigma(x_{i-1}, x_i)\ge 2\times \frac{1}{2^{k+1}}=\frac{1}{2^k}
$$

## Section 5. 位相群の準同型写像
位相群間の準同型写像について考える次の定理は準同型の連続性に関する重要な定理である。

**定理(位相群の準同型の連続性)**
$G, G^{\prime}$ を二つの位相群、 $\varphi: G\rightarrow G^{\prime}$ とする。このとき
(1) $\varphi$ は連続 $\iff$ $\varphi$ は単位元 $e$ において連続。しかもこのとき $\varphi$ は一様連続である。</br>
$G^{\prime}$ における単位元の任意の近傍 $V$ に対して、 $G$ における単位元の近傍 $U_V$ を適当に選び $x^{-1}y\in U\Rightarrow \varphi(x)^{-1}\varphi(y)\in V$ とすることができる。ここで一様が意味するところは、 $V$ に対して選択する近傍 $U_V$ は $V$ に依存し、一般的には場所 $x, y$ にも依存するが、ここでは $x, y$ に依存せずに選択できるということである。</br>
(2) $\varphi$ は開写像 $\iff$ $\varphi$ は $e$ において開写像( $e$ の任意の開近傍 $U$ の像 $\varphi(U)$ は $G^{\prime}$) の開集合である。</br>
証明) $\varphi$ が $e$ において連続であるとする。つまり $G^{\prime}$ の単位元 $e^{\prime}$ の任意の近傍 $V$ に対して $e$ の適当な近傍 $U$ をとれば $\varphi(U)\subset V$ となるとする。 $x$ を $G$ の任意の元とし、 $y=\varphi(x)$ とする。 $y$ の任意の近傍を $W$ とすれば、 $e^{\prime}$ の近傍 $V$ を適当に選び、 $yV\subset W$ とすることができる。この $V$ に対して、 上記の $U$ をとると、 $xU$ は $G$ における $x$ の近傍であり、
$$
\varphi(xU)=\varphi(x)\varphi(U)=y\cdot \varphi(U)\subset yU
$$
これによって、 $\varphi$ が $G$ のすべての点で連続であることがわかる。逆は、すべての点で連続なので、単位元 $e$ においても連続。</br>
また、上の記号で、 $x^{-1}y\in U$ ならば $\varphi(x)^{-1}\varphi(y)=\varphi(x^{-1}y)\in V$ であるから、 $\varphi$ が連続であれば、それは一様連続である。</br>
(単位元の近傍 $U$ に対し、任意の点 $y$ の近傍が $yU$ と記述できることがポイント?)</br>
(2) $\varphi$ が単位元 $e$ において開写像であるとき、 $\varphi$ が開写像であることだけ示せば十分である。定理 1.1 により $e$ の完全近傍系 $\mathscr{N}$ と点 $x\in G$ の完全近傍系 $\mathscr{N}_x$ とは $N\mapsto xN (N\in \mathscr{N})$ の対応関係の下に過不足なく１対１に対応している。</br>
$U$ を $G$ の開集合 $x$ を $U$ の１点とすると、 $U$ は $x$ の近傍で、上記のことから $xV=U$ となる $e$ の開近傍 $V$ が存在する。 $\varphi$ は準同型写像なので $\varphi(U)=\varphi(x)\varphi(V)$ 仮定により、 $\varphi$ は $e$ において開写像であるから、 $\varphi(V)$ は開集合である。したがって、 $\varphi(U)=\varphi(x)\varphi(V)$ は $\varphi(x)$ を含む開集合である。

## Section 6. 位相群の部分群
**定理 1.7**(部分群の性質)</br>
$H$ を Hausdorff位相群 $G$ の部分群とすると、次の命題が成り立つ。</br>
(1) $H$ の閉方 $\bar{H}$ も $G$ の部分群である。</br>
(2) $H$ が $G$ の正規部分群であれば、 $\bar{H}$ も可換である。</br>
(3) $H$ が可換であれば、 $\bar{H}$ も可換である。</br>
(4) $H$ は開集合 $\iff$ $int(U)\neq \empty$</br>
(5) $H$ が開集合であれば、 それは閉集合である。 </br>
証明) (1) $a,b\in \bar{H}$ とする。 このとき有向点族 $\{x_\lambda\}_\lambda$ 、 $\{y_\lambda\}_\lambda$ が存在して、 $x=\lim_\lambda x_\lambda$ 、 $y=\lim_\lambda y_\lambda$ 。このとき、 $xy^{-1} = \lim_\lambda x_\lambda y_\lambda^{-1}$ より、 $xy^{-1}\in \bar{H}$ である。</br>
(2) $H$ が $G$ の正規部分群であるとする。 $a\in \bar{H}$ 、 $c\in G$ とする。 このとき有向点族 $\{a_{\lambda}\}_{\lambda}$ があって、 $a = \lim_\lambda a_\lambda$ 。したがって、 $cac^{-1}=\lim_\lambda ca_\lambda c^{-1}$ より $cac^{-1}\in\bar{H}$ 。よって、 $\bar{H}$ も正規部分群である。</br>
(3) $G$ がHausdorffなので、$x, y\in \bar{H}$ に対して $x_\lambda \rightarrow x, y_\lambda\rightarrow y$ なる $H$ の有効点族 $\{x_\lambda\}, \{y_\lambda\}$ が存在する。 $H$ の可換性により、
$$
xy=\lim_\lambda x_\lambda y_\lambda = \lim_\lambda y_\lambda x_\lambda =yx
$$
であるから所望の結果を得る。
(4) $H$ が開集合ならば、 $int(H)\neq\empty$ 。逆に $x\in int(H)$ とすれば、 $xU\subset H$を満たす、単位元 $e$ の近傍 $U$ が存在する。 任意の $y\in H$ に対して
$$
yU = yx^{-1}xU\subset yx^{-1}H=H
$$ 
であるから、 $H$ は開集合である。</br>
(最後の等号) $yx^{-1}H\subset H$ は $H$ が部分群であることから成り立つ。逆に $z\in H$ とすれば $z=yx^{-1}xy^{-1}z\in yx^{-1}H$であるから成り立つ。</br>
(5) $H$ が開部分群であるとすれば、
$$
H^c =\cup_{x\notin H} xH
$$
各 $xH$ は開集合であるから、 $H^c$ は開集合。

**系 1.2**</br>
$G$ はHausdorff位相群、 $U$ は 単位元 $e$ の対称的近傍とすれば、 $H=\displaystyle\bigcup_{n=1}^{\infty}$ は開かつ閉な部分群である。</br>
証明) $H$ は部分群である。また、 $int(H)\neq \empty$ 。 したがって、定理 1.7 (4)、(5)より、 $H$ は開かつ閉である。

**系 1.3**</br>
$G$ は Hausdorff位相群、 $H$ はその局所コンパクトな部分群とすれば、 $H$ は閉である。
証明) $H$ が位相群 $\bar{H}$ において稠密かつ局所コンパクトなので、 開部分群である。したがって、定理 1.7 (5) より、それは　$\bar{H}$ において開部分群であるから、本来の位相についても開である。

## Section 7. 位相群の商群
位相群 $G$ の閉じた正規部分群 $N$ について、商群 $G/N$ を考え、これに位相群を定める。</br>
$G/N$ の位相は、商位相、すなわち $\pi: x\mapsto xN$ で定義される自然な写像 $\pi: G\rightarrow G/N$ を考え、集合族
$$
\{U\in G/N : \pi^{-1}(U) は G の開集合\}
$$
を $G/N$ の位相とする。商位相は $\pi$ を連続とする $G/N$ の中で最も強い位相である。

**定理 1.8 (商群)** </br>
$G$ を位相群、 $N$ をその閉じた正規部分群とすれば、次の命題が成り立つ。</br>
(1) $\pi : G\rightarrow G/N$ は連続</br>
(2) $\pi$ は開写像</br>
(3) $G/N$ は位相群で、 $G$ が Hausdorffならば $G/N$ も Hausdorffである。</br>
(4) $G^{\prime}$ をもうひとつの位相群とし、 $\varphi:G\rightarrow G^{\prime}$ を連続な準同型写像とする。いま、 $N\subset \rm{Ker}\varphi$ ならば、 $G/N$ から $G^{\prime} $　への連続な週同型写像 $\varphi:G/N\rightarrow G^{\prime}$ で、
$$
\varphi = \bar{\varphi}\circ\pi
$$
を満たすものが存在し、このような $\bar{\varphi}$ は一意に定まる。
![alt text](../images/quotient_top_commutative_image.png)
証明) (1) 商位相の定義から成り立つ。 </br>
(2) $U\subset G$ を開集合とする。このとき 
$$
\pi^{-1}(\pi(U))=UN=\displaystyle\bigcup_{x\in N}Ux
$$
であり、　各 $Ux$ は開集合なので、 $\pi^{-1}(\pi(U))$ は開集合。したがって商位相の定義から、 $\pi(U)$ は開集合である。
(3) $G/N$ が群であることはすでに述べたので、それが実際に位相群であることを示す。 $a,b\in G$ とすれば
$$
\pi(a)\pi(b)=\pi(ab)
$$
である。実際、 $N$ が正規部分群であるから
$$
\pi(a)\pi(b)=aN\cdot bN=abNN=abN=\pi(ab)
$$
$G/N$ における $\pi(ab)$ の近傍を $V$ とする。 $\pi$ の連続性から、 $\pi^{-1}(V)=U$ は $G$ における $ab$ の近傍。したがって、 $a,b$ それぞれの近傍 $U_a, U_b$ を適当に選んで $U_aU_b\subset U$ とすることができる。 よって
$$
\pi(U_a)\pi(U_b)\subset \pi(U)=V
$$
$\pi$ は開写像なので、 $\pi(U_a), \pi(U_b)$ は $\pi(a), \pi(b)$ の近傍である。これから、 $G/N$ における積の演算の連続性が得られる。逆元演算の連続性も同様。 $G$ がHausdorffであれば、 $G/N$ もHausdorffであることをしめすためには、それが $T_1$ であること、すなわち $G/N$ の1点、たとえば $\{\xi_e=N\}$ が $G/N$ において閉であることを示せば十分である( $T_1$ 空間はこの条件と同値であることと、位相群において、 $T_1$ と $T_2$ 空間は同値であることから)。 $\pi^{-1}(\xi_e)=N$ で、これは仮定により $G$ の閉集合である。 $(G/N)\backslash \{\xi_e\}=\pi(G\backslash N)$ であるが、 $G\backslash N$ は $G$ の開集合、 $\pi$ は開写像なので、 $(G/N)\backslash \{\xi_e\}$ は $G/N$ の開集合である。したがって $\{\xi_e\}$ は $G/N$ の閉集合である。これから、すべての剰余類 $\{\xi_x=xN\} \ (x\in G)$ は閉である。 任意の点 $x\in G$ を乗算する写像は、位相同型写像のため、すべての剰余類 $\{\xi_x=xN\} \ (x\in G)$ は閉である。</br>
(4) $N\subset \rm{Ker}\varphi$ に注意すると、 各 $x\in G$ について $\bar{\varphi}(xN)=\varphi(x)$ とすれば、この $\bar{\varphi}$ が求める準同型写像である(一意性とwll-definedは計算すればわかる)。 $V\subset G^{\prime}$ を開集合とすれば、 
$$
\pi^{-1}(\bar{\varphi}^{-1}(V))=(\bar{\varphi}\circ \pi)^{-1}(V)=\varphi^{-1}(V)
$$
$\varphi$ が連続のため、これは開集合である。したがって、商位相の定義により、 $\bar{\varphi}^{-1}(V)$ も開集合である。
 

