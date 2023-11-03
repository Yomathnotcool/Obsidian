
# Tags
#ergodic-theory #dynamical-system #number-theory #measure-theory 


---

# References


---


# Other related files


---

## Dirichlet regions
### Def :: Properly discontinuous action

^6ee38f

Given a locally compact metric space $X$ with an action of countable group $\Gamma$ by homeomorphism, the action is properly discontinuous if for any compact subspace $K\subset X$, $$\{\gamma\in\Gamma|\gamma K\cap K\not=\emptyset\}$$ is finite.
	i.e. any compact subset of $X$ only intersects with finitely many orbit points of action. $\forall K$ compact, there exists $g\in G$, $\{ K\cap \{ g^{n}x\mid n\in\mathbb{N} \} \}\not=\emptyset$.


### Def :: fundamental domain
A measurable subset $F$ of $X$ is fundamental domain if $|\Gamma z\cap F|=1$ for any $z\in X$. 

i.e. it contains one and only one representative of each orbits.

### Def :: Open fundamental domain
A measurable subset $F\subset X$ is open fundamental domain if 
1. $g_{1}\not=g_{2}$ then $g_{1}F\cap g_{2}F=\emptyset$;
2. $X=\bigcup_{g\in G}g\overline{F}$.

### Thm :: An infinite subgroup $\Gamma\subset PSL_{2}(\mathbb{R})$ is Fuchsian if and only if its action is [[Ergodic theory towards number theory#^6ee38f|properly discontinuous]].

### Def :: Dirichlet region

^cea52d

Given infinite Fuchsian group $\Gamma$ and point $p\in\mathbb{H}$ that is not fixed by any element of $\Gamma$ other than the identity.
$$D(p)=\{z\in\mathbb{H}|d(z,p)<d(z,\gamma p)\ \text{for all}\ \gamma\in\Gamma\backslash\{Id\}\}$$
is called a Dirichlet region for $\Gamma$.

### Def :: connected Dirichlet region
A Dirichlet region is connected and convex if there exists hyperbolic geodesic path joining any two points in $D$ that lie entirely inside of $D$.

#### Def :: Geodesic in $\mathbb{H}$
$L_{\gamma}$ geodesic in $\mathbb{H}$ defined by $$\{z\in\mathbb{H}|\text{d}(z,p)=\text{d}(z,\gamma p)\}.$$
#### Rmk :
The point $p$ exists because $\Gamma$ is discrete. The fixed points of $\Gamma$ are just the solution of $\gamma z=z$. But since it's discrete, its solution can not cover the entire upper half plane.


### Thm :: The open set $D_{\gamma}$ is connected component of $\mathbb{H}\backslash L_{\gamma}$ containing $p.$ 
$$D_{\gamma}=\{z\in\mathbb{H}|\text{d}(z,p)<\text{d}(z,\gamma p)\}$$

#### Notation:
$\overline{\mathbb{H}}=\mathbb{H}\cup\partial\mathbb{H}$ in which $\partial\mathbb{H}=\mathbb{R}\cup\{\infty\}$.

### Thm :: A Dirichlet region for a lattice in $PSL_{2}(\mathbb{R})$ has finitely many sides, which is a convex hyperbolic polygon.



### Thm :: Gauss-Bonnet formula
Let $P$ be a hyperbolic $n$-sided convex polygon in $\mathbb{H}$ with $n\geq 3$ vertices in $\overline{\mathbb{H}}$, with angles $\alpha_{1},...,\alpha_{n}$ at the $n-$vertices. The hyperbolic area of $P$ is 
$$(n-2)\pi-(\sum\limits^{n}_{i=1}\alpha_{i}).$$

A not good understanding to show why we need [[Ergodic theory towards number theory#^cea52d|Dirichlet region]]:
### Thm :: A lattice $\Gamma\subset PSL_{2}(\mathbb{R})$ is [[Ergodic theory towards number theory#^6d290e|uniform]] if and only if every vertex of any Dirichlet region for $\Gamma$ lies in $\mathbb{H}$.
It has compact closure.


### Def :: Cusps
$D$ Dirichlet domain for a lattice $\Gamma$ in $PSL_{2}(\mathbb{R})$, points of the closure of $D$ taken in $\overline{H}$ that belong to $\partial\mathbb{H}$ are called cusps.

### Thm :: A lattice of $PSL_{2}(\mathbb{R})$ is finitely generated.





## Examples of lattices

## Unitary representation, Mautner phenomenon, and ergodicity

For any discrete subgroup $\Gamma\leq SL_{2}(\mathbb{R})$, we have the quotient space $X=\Gamma\backslash SL_{2}(\mathbb{R})$.
### Def :: Geodesic flow
$$R_{a_{t}}(x)=xa^{-1}_{t}=x\begin{pmatrix}e^{t/2} & 0\\ 0 & e^{-t/2}\end{pmatrix}$$
in which $x\in X, t\in\mathbb{R}$.

### Def :: stable(unstable) horocycle flow
$$R_{u^{-}(s)}(x)=xu^{-}(-s)=\begin{pmatrix}1 & -s\\ 0 & 1\end{pmatrix}$$
in which $x\in X$ and $x\in\mathbb{R}$.


Based on those two definitions, there are two subgroups that are defined as following:
$$U^{-}=\bigg\{\begin{pmatrix}1 & -s\\ 0 & 1\end{pmatrix}|s\in\mathbb{R}\bigg\},$$
$$A=\bigg\{\begin{pmatrix}e^{t/2} & 0\\ 0 & e^{-t/2}\end{pmatrix}|t\in\mathbb{R}\bigg\}.$$




### Thm :: Rigidity of horocycle flow
$\Gamma\subset SL_{{2}}(\mathbb{R})$, $X=\Gamma\backslash SL_{{2}}(\mathbb{R})$
$\mu$ probability measure and ergodic under $h(s)$ horocycle flow, $s\in \mathbb{R}$ 
Then $\mu=m_{{X}}$ or $\mu$ is unique invariant measure supported on periodic orbit for $U^{-}$. 
If $X$ is compact, the only choice is $\mu=m_{{X}}$ since there is no periodic orbit.



To prove the theorem, we need the following proposition:
#### Thm :: Asymptotic formula of horocycle flow
Let $K\subset X$ a compact subset, then there exists some constant $\eta$ with the following property: 
	suppose that $(t_{{n}})$ is a sequence in $\mathbb{R}$ with $t_{n}\rightarrow\infty$ and with $R_{a_{t_{n}}}\in K$ for all $n$, then
	$$
\frac{1}{\eta e^{t_{n}}}\int ^{e^{t_{n}}}_{0}f(h(s)\cdot x_{0}) \, ds \rightarrow \int _{X}f(x)\ d m_{X}
$$
as $n\rightarrow\infty$ for all $f\in C_{c}(X)$.

In order to prove this theorem, we need to break the measure of $G$ into measure of $ST$.

#### Thm :: $G$ a $\sigma$-compact unimodular group, $S,T\leq G$ and $S\cap T=\{ e \}$ and $ST$ contains a neighborhood of $e\in G$. Let $\phi:S\times T \rightarrow G$ be the product map $\phi(s,t)=st \in ST\subset G.$ 


Then by the Haar measure $m_{G}$ restricted to $ST$ is proportional to the pushforward $\phi_{*}(m^{l}_{S}\times m^{r}_{T})$ where $m_{S}^{l}$ is the left Haar measure on $S$ and $m^{r}_{T}$ is right Haar measure on $T.$

We want to use this lemma on $G=PSL_{2}(\mathbb{R})$, $S=U^{-}$ and $T=U^{+}A$. 
1. $S\cap T=\{ e \}$;
2. $S, T\leq G$
3. $ST$ contains a neighborhood of $\{ e \}$.

###### Proof: 
Considering the Lie algebra of $S$ and $T$, 
$$
\mathfrak{s}=\{\begin{pmatrix}0 & a \\
0 & 0 
\end{pmatrix}|a\in\mathbb{R}  \}
$$
$$
\mathfrak{t}=\{ \begin{pmatrix}
a &  \\
c & -a
\end{pmatrix}|a,c\in\mathbb{R} \}
$$
$$
\begin{array}
\ \phi:\mathfrak{s}\times \mathfrak{t}\rightarrow \mathfrak{g}\\
(v,w)\mapsto \log(\exp(v)\exp(w))=v+w+\frac{1}{2}[v,w]+\frac{1}{12}([v,[v,w]]-[w,[v,w]])+\dots
\end{array}
$$


So now we can define $m^{l}_{S}$ as the one-dimensional Lebesgue measure on $\mathbb{R}$ and $m^{r}_{T}$ as the right measure such that  $m_{G}$ restricted to $U^{-}T$ coincides with product measure of $m^{l}_{S}$ and $m^{r}_{T}$.

Based the theorem about [[Chapter 9 Geodesic Flow on Quotients of the Hyperbolic Plane#^132adb|injective radius]], there exists a constant $\eta=\eta(K)>0$, then there is an embedding $u^{-}([0,\eta])B^{T}_{\eta}\hookrightarrow K$ for any $x\in K$. 

$f\in C_{c}^{X}$, with loss of generality $f\geq 0$ and it's uniformly continuous on compact subset $K$: $\forall \epsilon$, there exists some $\delta$, $d(x,y)<\delta$  such that $\mid f(x)-f(y)\mid<\epsilon$. Fixed $\epsilon$, there exists some the uniform continuous condition holds.

Now denote $$
\begin{equation}
Q_{\delta}=u^{-}(-[0,\eta])\cdot B^{T}_{\delta}=\{\begin{pmatrix}
1 & s \\  & 1
\end{pmatrix}\mid s\in -[0,\eta]  \}\cdot \{ g\in T=U^{+}A \mid d_{G}(g,e)<\delta \}
\end{equation}
$$
then for $\delta<\eta$, there is the embedding $Q_{\delta}\hookrightarrow K$, we want to prove the integral on the interval $[0,e^{t_{n}}\cdot\eta]$, which is $$
\begin{pmatrix}
e^{-t_{n}/2 } & \\ & e^{t_{n}/2}
\end{pmatrix}\begin{pmatrix}
1 & s\\  & 1 
\end{pmatrix}\begin{pmatrix}
e^{-t_{n}/2 } & \\ & e^{t_{n}/2}
\end{pmatrix}=\begin{pmatrix}
e^{-t_{n}/2 } & \\ & e^{t_{n}/2}
\end{pmatrix}\begin{pmatrix}
e^{-t_{n}/2} & s\cdot e^{t_{n}/2}\\ & e^{-t_{n}/2}
\end{pmatrix}=\begin{pmatrix}
1 & s\cdot e^{t_{n}}\\ & 1
\end{pmatrix}
$$
So the integral interval is $a^{-1}_{t_{n}}u^{-}(-[0,\eta])a_{t_{n}}$. We want to make the integral "larger" to make the geodesic $R_{a_{t_{n}}}$-orbit  more clear to study, which is why we need to add the ball $B_{\eta}^{T}$ in $Q_{\delta}$.


Now we fixed a point $x_{o}$, then denote $B_{n}=\{  R_{a_{t_{n}}}^{-1}(R_{a_{t_{n}}}(x_{0}Q_{\delta})) \}=x_{0}(a^{-1}_{t_{n}}Q_{\delta}a_{t_{n}})\subset x_{0}u^{-}(-[0,e^{t_{n}}\eta])B^{T}_{\eta}$.

We need to study the integral over $B_{n}$:
$$
\begin{align}
\frac{1}{m_{G}(B_{n})} \int_{B_{n}}f(x) \, dm_{X}
&=\int_{x_{0}(a_{t_{n}}Q_{\delta}a_{t_{n}})}f(x) \, dm_{X} \\
&= \frac{1}{m_{G}(B_{n})}\int_{a^{-1}_{t_{n}}Q_{\delta}a_{t_{n}}}f(x_{0}g) \, dm_{G}(g) \\
&= \frac{1}{m_{G}(B_{n})}\int_{a^{-1}_{t_{n}}Q_{\delta}B^{T}_{\eta}a_{t_{n}}}f(x_{0}g) \, dm_{G}(g) \\
&= \frac{1}{m_{G}(B_{n})}\int_{a^{-1}Q_{\delta}a_{t_{n}}a^{-1}_{t_{n}}B^{T}_{\eta}} f(x_{0}g) \, dm_{G}(g) \\
\text{By the decomposition of the measure}\ m_{G}\ \text{the lemma above} \\
&=\frac{1}{\eta e^{t_{n}}} \frac{1}{m_{G}(a^{-1}_{t_{n}})a_{t_{n}}}\int_{0}^{\eta e^{t_{n}}}\int_{a^{-1}_{t_{n}}B^{T}_{\eta}a_{t_{n}}}f(x_{0}u^{-}(-s)g) \, dm^{r}_{T}(g)  \, ds 
\end{align}
$$



Now we want to know how the uniform continuous work on $x_{0}u^{-}(-[0,e_{t_{n}}\eta])B^{T}_{\eta}$: $$
\begin{equation}
d_{X}(x_{0}u^{-}(-s),x_{0}u^{-}(-s)h)\leq d_{X}(e,h)<\delta
\end{equation}
$$
And this,
$$
\mid \frac{1}{\eta e^{t_{n}}} \frac{1}{m_{G}(a^{-1}_{t_{n}})a_{t_{n}}}\int_{0}^{\eta e^{t_{n}}}\int_{a^{-1}_{t_{n}}B^{T}_{\eta}a_{t_{n}}}f(x_{0}u^{-}(-s)g) \, dm^{r}_{T}(g)  \, ds - \frac{1}{\eta e^{t_{n}}}\int^{\eta e^{t_{n}}}_{0}f(x_{0}u^{-}(-s))  \, ds\mid<\epsilon
$$

	*_Now we want to construct subsets that mixing property can be applied easily_*

And since $K$ is compact, then there are finite many balls $B^{X}_{\kappa}$ with $\kappa$ sufficiently small that covers $K=\bigcup^{n}_{i}y_{i}B^{T}_{\kappa}$ .
By the regularity of  measure, there exists a compact subset $P_{\delta}\subset Q^{0}_{\delta}$ and a compact subset $R_{\delta}$ containing $\overline{Q_{\delta}}$, so that $$
\frac{m_{G}(R_{\delta}\backslash P_{\delta})}{m_{G}(Q_{\delta})}<\epsilon.
$$
and $B^{G}_{\kappa}P_{\delta}\subset Q_{\delta}$ and $B^{G}_{\kappa}Q_{\delta}\subset R_{\delta}$, which is well-defined since for any $g_{1}\in B^{G}_{\kappa}$ and $x \in P_{\delta}$, it satisfies $$
d_{G}(x,gx)=d_{G}(e,g)<\kappa,
$$
as the same reason above.

	Now we are ready to use the "mixing" property.

$$
\begin{align}
<f, \frac{1}{m_{G}(Q_{\delta})}\chi_{y_{i}P_{\delta}}\circ R_{a_{t_{n}}}>
&= \frac{1}{m_{G}}\int_{X}f(x)\cdot\chi_{y_{i}P_{\delta}}\circ R_{a_{t_{n}}}\,dm_{X}\\
&\longrightarrow \text{By the mixing of horocycle flow}\\
& \frac{1}{m_{G}}\int_{X}f(x)\,dm_{X}\int_{X}\chi_{y_{i}P_{\delta}}(x)\,dm_{X}\\
& =\frac{m_{G}(P_{\delta})}{m_{G}(Q_{\delta})}\int_{X}f(x)\,dm_{X} 
\end{align}
$$
Similarly, there is the asymptotic formula for $<f(x), \frac{1}{m_{G}(Q_{\delta})}\chi_{y_{i}R_{\delta}}\circ R_{a_{t_{n}}}>$.

Then if $x=R_{a_{t_{n}}}(x_{0})\in y_{i}B^{X}_{\eta}\subset K$, then $y_{i}P_{\delta}\subseteq xQ_{\delta}\subseteq y_{i}R_{\delta}$.

This gives us that 
$$
\begin{align}
<f, \frac{1}{m_{G}(Q_{\delta})}\chi_{y_{i}P_{\delta}}\circ R_{a_{t_{n}}}>
\leq \\ <f(x), \frac{1}{m_{G}(Q_{\delta})}\chi_{B_{n}}>
\leq \\<f(x), \frac{1}{m_{G}(Q_{\delta})}\chi_{y_{i}R_{\delta}}\circ R_{a_{t_{n}}}>,
\end{align}
$$
in which
$$
\begin{align}
<f(x), \frac{1}{m_{G}(Q_{\delta})}\chi_{B_{n}}> &=\frac{1}{m_{G}(Q_{\delta})}\int_{X}f(x)\chi_{B_{n}}(x)\,dm_{X}\\
&=\frac{1}{m_{G}(Q_{\delta})}\int_{X}f(x)\chi_{R_{a_{t_{n}}}^{-1}(x_{0}a^{-1}_{t_{n}}Q_{\delta})}(x)\,dm_{X}\\
& = \frac{1}{m_{G}(Q_{\delta})}\int_{X}f(x)\chi_{x_{0}a_{t_{n}}^{-1}Q_{\delta}}(R_{a_{t_{n}}}(x))\,dm_{X}\\
&\longrightarrow \text{By the property of mixing of geodesic flow}\\
&= \frac{1}{m_{G}(Q_{\delta})}\int_{X}f(x)\,dm_{X}\int_{X}\chi_{x_{0}a^{-1}_{t_{n}}Q_{\delta}}(x)\,dm_{X}\\
&=\int_{X}f(x)\,dm_{X} .
\end{align}
$$
### Thm :: Non-divergence theorem refined by Dani
For any lattice $L\subset SL_{2}(\mathbb{R})$, every compact subset $K$ in $X=\Gamma \backslash SL_{2}(\mathbb{R})$, and $\forall\epsilon$, there exists a compact subset $L=L(K,\epsilon)$ of $X$, such that 
$$
\frac{1}{T}m_{\mathbb{R}}(\{ t\in[0,T]\mid h(t)\cdot x\not\in L \})\leq\epsilon
$$
for $\forall\epsilon$ and $\forall x \in K.$
Moreover, there is a compact set $L=L(\varepsilon) \subseteq X$ (independent of $K$ and of $x$ ) such that for any $x \in X$ either $x$ is periodic or there exists some $T_x>0$ such that 
$$
\frac{1}{T}m_{\mathbb{R}}(\{ t\in[0,T]\mid h(t)\cdot x\not\in L \})\leq\epsilon
$$
holds for all $T \geqslant T_x$.
#### Remark ::

So this theorem gives a uniform control for all points in $X$. 


In the proof of this theorem, an important idea is to transfer the points in the quotient space to a different way of understanding: [[Moduli space|moduli]]of lattice, which requires the identification:
$$
\begin{array}
\ X_{2} = SL_{2}(\mathbb{Z})\backslash SL_{2}(\mathbb{R})= \{ SL_{2}(\mathbb{Z})g\mid g\in SL_{2}(\mathbb{R})\}\cong& X_{2}=\{\text{All lattices in}\ SL_{2}(\mathbb{R})\}\\
SL_{2}(\mathbb{Z})g \longleftrightarrow g^{-1}\mathbb{Z}^{2}
\end{array}
$$
The benefit of using lattice is by the following [[Chapter 11 More Dynamics on Quotients of the Hyperbolic Plane#^99ae84|Mahler compactness criterion]].
### Thm :: Proof of the identity
The following are equivalent:
1. $x$ is periodic under $U^{-}.$
2. $x \in \mathbb{Z}^{2}AU^{-}.$
3. $x\cdot a_{s}\to \infty$ as $s \to \infty$. 





### Thm :: Mahler compactness criterion

A set $K \subset X_{d}$ has compact closure if and only if  there is a $s>0$, such that $$
\forall \Lambda \in K, \Lambda \cap B_{S}(0)=\{0\}.
$$

^d946ab


$K\subseteq \Omega_{\delta}=\{\Lambda \in X_{2}\mid \Lambda \cap B_{\delta}(0)=\{0\}\}$, in which $\delta \in(0,1)$. by the [[Chapter 11 More Dynamics on Quotients of the Hyperbolic Plane#^d946ab| Mahler compactness criterion]], this makes sure that $K$ is compact.
Our goal is to choose a constant $\eta \in\left( 0,\frac{\delta}{4} \right)$ such that $L=\Omega_{\delta}$ satisfies  $$\frac{1}{T}m_{\mathbb{R}}(\{t\in[0,T]\mid h(t)\cdot x\not\in L\})\leq\epsilon, \text{for any}\ T>0, x \in K.$$Here we want to use  [[Chapter 11 More Dynamics on Quotients of the Hyperbolic Plane#^d946ab| Mahler compactness criterion]] for lattice, this depends on the lemma before [[Chapter 11 More Dynamics on Quotients of the Hyperbolic Plane#^d946ab|Identity between quotient space and moduli of lattice.]]
The corresponding elements under horocycle flow: 
$$ 
\begin{array}
\ h(t)\cdot x=U^{-}(-t)x\\
x=\Gamma g \longleftrightarrow g^{-1}\mathbb{Z}^{2}=\Lambda\\
u^{-}(-t)x\longleftrightarrow u^{-}(t)\Lambda
\end{array}
$$
Consider the maximal set of mutually non-proportional primitive elements of $\Lambda$, which is denoted as $\Pi = \{v_{1},\dots\}$. 
	if $v=u^{-}(t)v_{i}\in U^{-}(t)\Lambda \backslash\{0\}$ and the norm $\mid v\mid<\eta \iff u^{-}(t)v=u^{-}nv_{i}$, which gives $\mid u^{-}(t)v_{i}\mid<\eta$. So the set $\Pi$ is the only collection of vectors that we need to consider.
Pick $\Lambda \in K\subseteq \Omega_{\delta}$, so for any $v_{i}\in\Lambda$, $\mid v_{i}\mid \geq \delta$.
Fix $T>0$, for any $i\geq 1$,
$$
B_{i}=\{t\in[0,T]\mid u^{-}(t)v_{i}\in B^{\mathbb{R}^{2}}_{\delta}(0)\},\ \ \ \text{the bad time}
$$
and $$
P_{i}=\{t\in[0,T]\mid u^{-}(t)v_{i}\in B^{\mathbb{R}^{2}}_{\delta}(0)\},\ \ \ \text{the protected time that holds compactness.}
$$
it satisfies the properties below:
1. $B_{i}\subseteq P_{i}$;
2. $\forall i\not=j, P_{i}\cap P_{j}=\emptyset$. 

The first is trivial, and the second is proved by contradiction to the unimodular condition. 

##### Claim : $m_{\mathbb{R}}(B_{i})\leq \frac{4\eta}{\delta}m_{\mathbb{R}}(P_{i})$.
Proof: 

For the vector $v_{i}=\begin{pmatrix}\alpha_{1} \\ \alpha_{2}\end{pmatrix}$, then the vector under horocycle flow is $u^{-}(t)=\begin{pmatrix}\alpha_{1}+t\alpha_{2}\\ \alpha_{2}\end{pmatrix}$. 
Then the $\alpha_{2}$ is the moving speed under horocycle flow, so if $\alpha_{2}=0$, then $v_{i}$ under horocycle flow, which gives the $B_{i}=\emptyset$.

If $\alpha_{2}\geq \frac{\delta}{4}>\eta$, $\mid v_{i}\mid >\eta$. So $B_{i}=\emptyset$.

So the only interval that we need to consider is $\alpha_{2}<\eta \leq \frac{\delta}{4}$:
	Since the horocycle flow is continuous flow, denote the set $P_{i}=[T_{1},T_{2}]$, there exists $T'$, $\alpha_{1}+T'\alpha_{2}<\eta \leq \frac{\delta}{4}$, and for the time $T_{1}$, $\mid U^{-}(T_{1})v_{i}\mid=\delta=\mid \begin{pmatrix}\alpha_{1}+T_{1}\alpha_{2}\\ \alpha_{2}\end{pmatrix}\leq \mid \alpha_{1}+T_{1}\alpha_{2}\mid+\mid \alpha_{2}\mid$, as $\mid\alpha_{2}\mid< \frac{\delta}{4}$, $\mid \alpha_{1}+T_{1}\alpha_{2}\geq \frac{3\delta}{4}$. 
	SO $m_{\mathbb{R}}(P_{i})=T_{2}-T_{1}>T'-T_{1}> \frac{\delta}{2}\cdot \mid \alpha_{2}\mid^{-1}$ (distance divides speed = time). 
	And similarly, $m_{\mathbb{R}}(B_{i})=T_{3}-T_{4}\geq \frac{2\eta}{\alpha_{2}}$.
	$$
m_{\mathbb{R}}(B_{i})\leq \frac{4\eta}{\delta}m_{\mathbb{R}}(P_{i}).
$$
And $$
\begin{array}
m_{\mathbb{R}}(\{\Lambda\mid u^{-}(t)\Lambda \not\in \Omega_{\eta}\})\\
= m_{\mathbb{R}}(\{t\in[0,T]\mid h(t)\cdot x\not\in L\})\\
=\sum_{i}m_{\mathbb{R}}(B_{i})\\
\leq \frac{4\eta}{\delta}\sum_{i}m_{\mathbb{R}}(P_{i})\\
\leq \frac{4\eta}{\delta}T.
\end{array}
$$
So choose $\eta \leq \frac{\epsilon\delta}{4}.$

A set $K \subset X_{d}$ has compact closure if and only if  there is a $s>0$, such that 


































At the end of the chapter 11, our main goal is
### Thm :: equidistribution of orbits of horocycle flow
$\forall x \in X=SL_{2}(\mathbb{Z})\backslash SL_{2}(\mathbb{R}),$ which is not periodic under $h(t)$, for any $f \in C_{c}(X)$,
$$
\frac{1}{T}\int^{T}_{0}f(x\cdot u(t))\,dt \to \int_{X}f\,dm_{X}
$$
in which $m_{X}$ is the [[Haar measure]].

Recall [[Riesz representation theory]] and [[Functional Analysis#^1f9d81|Banach-Alaogulu theorem]].

Define $Y=X \bigsqcup\{\infty\}$ as the one-point compactification of $X$. Then for the time average of horocycle flow, it can be realized as a linear functional:
$$
M_{T}(f)=\frac{1}{T}\int^{T}_{0}f(x\cdot u(t))\,dt,
$$
And $M_{T}(f)\in M(Y)$ is a the space of continuous linear map from $C_{c}(Y)$ to $\mathbb{R}$. 

By the [[Functional Analysis#^1f9d81|Banach-Alaogulu theorem]], the sequence $M_{T_{i}}$ has convergent subsequence, so we can assume that it's convergent: $M_{T_{i}}\to M$.

##### Claim :: it's invariant under horocycle flow.

$$
\begin{array}
\mid M(f\circ u(s))-M(f)\mid&=\lim\limits_{ T_{i} \to \infty } \frac{1}{T_{i}}\mid \int^{T_{i}}_{0}f(x u(t+s))\,dt-\int^{T_{i}}_{0}f(xu(t))\,dt\mid \\
&\leq \lim\limits_{ T_{i} \to \infty } 2s\cdot \frac{max(f)}{T_{i}}=0
\end{array}
$$
