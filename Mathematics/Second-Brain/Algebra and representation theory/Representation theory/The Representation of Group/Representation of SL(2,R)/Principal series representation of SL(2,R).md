### Def :: Principal series representation

^62e5c4

Consider $G=SL_{2}(\mathbb{R})$, by [[Iwasawa decomposition of SL(2,R)|Iwasawa decomposition]], $G=KAU=KB$, in which $$
B=AU=\{\begin{pmatrix}
e^{x}  & t  \\
 & e^{-x}
\end{pmatrix}\mid x,t\in\mathbb{R}\}
$$
define the character of $B$: $\chi_{\xi}(a_{t}u_{x})=e^{i\xi t}$ for any $b=a_{t}u_{x}\in B$. 

The principal series representation of $SL_{2}(\mathbb{R})$ is defined as the induced representation $(\pi^{\xi},H_{\xi})=(Ind^{G}_{B}\chi_{\xi},Ind \mathbb{C}^{\times})$, in which 
$$
H_{\xi}=\{f:G\to \mathbb{C}^{\times} \mid f\ \text{is measurable}\ \ \text{with finite norm} \mid\mid f\mid_{K}\mid\mid<\infty\}
$$
and $f$ satisfies $f(gb)=\overline{\chi_{\xi}(b)}\Delta_{B}(b^{1/2})f(g)$ for any $b\in B$, which $\Delta_{B}$ as the modular function of $SL_{2}(\mathbb{R})$ is $e^{-2t}$.

And the norm $\mid\mid f\mid_{K}\mid\mid_{L^{2}(K)}^{2}$ is defined as $$
\int_{K}\mid\mid f(k)\mid\mid_{H_{B}}^{2}\,dm_{K}(k) 
$$
The representation $\pi^{\xi}_{g}$ acts as the [[Regular representation of SL(2,R)|left regular representation]]: $\pi^{\xi}_{g}(f)(x)=f(g^{-1}x)$.


#### Def :: even or odd representation

For a representation $\pi \in \widehat{SL_{2}(\mathbb{R})}$, it's called even representation if $\pi_{-I}f=f$, otherwise it's odd.

For the [[Principal series representation of SL(2,R)#^62e5c4|Principal series representaition]], its even part is 
$$
H^{even}_{\xi}=\{f\in H_{\xi}\mid f(g)=f(-g)\}=\{\pi_{-I}f=f\}=<F_{\xi,2n}\mid n \in \mathbb{Z}>
$$
on the other side, the odd part of the [[Principal series representation of SL(2,R)#^62e5c4|Principal series representaition]] is 
$$
H^{odd}_{\xi}=\{f\in H_{\xi}\mid f(g)=-f(-g)\}=\{\pi(f)=-f\}=<F_{\xi,2n+1}\mid n \in \mathbb{Z}>
$$

There is the proof of more explicit construction of this two spaces that will be provided later, in which $F_{\xi,n}(k_{\psi}a_{t}u_{x})=e^{-in\psi-i\xi t-td}$, which builds the basis of the $H_{\xi}$ due to Fourier expansions.

### The properties of the principal series representation

1. $\pi^{\xi}, \pi^{\xi,even},\pi^{\xi,odd}$ are unitary representations
2. For $\xi \in \mathbb{R}$, $\pi^{\xi,even}$ and for $\xi \in \mathbb{R}\backslash \{0\}$, $\pi^{\xi,odd}$ are irreducible.
3. $\pi^{0,odd}=\delta^{1,+}\oplus\delta^{1,-}$
in the property 3, $\delta$ is denoted for the [[Discrete series representation of SL(2,R)]].



#### Proof for unitary representation

The idea is to construct the unitary representation of $SL_{2}(\mathbb{R})$ over the unit circle, then show the equalence between unit circle representation and the principal series representation.

	Recall the theorem(Unitarily normalized representation) about the construct unitary representation via cocycle relations.

##### Thm :: 
Consider $G$ acting on the space $X$, $G$-action preserves [[Randon-Nikodym#^306315|measure class]], and $(X,\mu)$ is locally finite, Suppose there exists continuous map $c(g,x): G\times X \to \mathbb{C}^{\times}$ by $(g,x)\to \mid\mid g^{-1}x\mid\mid^{-2}$ and it satisfies the [[Randon-Nikodym]] derivate $$
\frac{dg_{*}\mu}{d\mu} =\mid\mid c(g,\cdot)\mid\mid^{2}$$  ^686105
 
and this map holds the cocycle relation $$
c(g_{1}g_{2},x)=c(g_{1},x)c(g_{2},g_{1}^{-1}\cdot x)
$$
Then the representation $\pi^{c}_{g}(f)(x)=c(g,x)f(g^{-1},x)$ is a unitary representation.



Now by using the theorem, we can construct the unitary representation of $G=SL_{2}(\mathbb{R})$ over the unit circle: 

#### Ex :: unitary normalized representation

Unit circle $S^{1}$ in 2-dim plane $\mathbb{R}^{2}$ with normalized measure class
$c(g,x)=\mid\mid g^{-1}x \mid\mid^{-1-i\xi}$
And the $G$-action is defined as $g\cdot x= \frac{gx}{\mid\mid gx\mid\mid}$.

The corresponding normalized unitary representation: 

^8d488c
$$
\pi^{S^{1},\xi}_{g}(f)(x)= \mid\mid g^{-1}x\mid\mid^{-1-i\xi}f(g^{-1}\cdot x)
$$
is unitary.

##### Proof of the unitary 

$$
\begin{align}
\mid\mid\pi^{S^{1},\xi}_{g}(f)\mid\mid^{2}=&\int_{X}\mid\pi^{S^{1},\xi}_{g}(f)\mid^{2}\,d\mu_{X}(x) \\
=&\int_{X}\mid\mid\mid g^{-1}x\mid\mid^{-1-i\xi}f(g^{-1}\cdot x)\mid^{2}\,d\mu_{X}(x)  \\
=&\int_{X}\mid\mid g^{-1}x\mid\mid^{-2}\mid\mid\mid g^{-1}x\mid\mid^{-i\xi}\mid^{2}f^{2}(g^{-1}\cdot x)\,d \mu_{X}(x) \\

\end{align}
$$
in the third line, it uses the fact that for $a\in\mathbb{R}$
$$
\begin{align}
\mid a^{i}\mid^{2}=&\mid e^{i\ln a}\mid^{2} \\
=& \mid \cos(\ln a)+ i\sin(\ln a)\mid^{2} \\
=& \cos^{2}(\ln a)+\sin^{2}(\ln a) \\
=&1
\end{align}
$$
Here we use the [[Euler formula]].

Then the proof of unitary representation can be done by the property of [[Randon-Nikodym]].

Now the second step is to show that isomorphism between $\pi^{S^{1},\xi}_{g}$ and $\pi^{\xi}$.

Define function $$
\begin{align}
U(f): G &\to  \mathbb{C} \\
g &\to  \mid\mid g e_{1}\mid\mid^{-1-i\xi}f(g\cdot e_{1})
\end{align}
$$
Show that $U$ is equivariant.
First to prove $U$ preserves the norm:
$$
\mid\mid U(f)\mid\mid_{L^{2}(K)}=\mid\mid f\mid\mid_{L^{2}(S^{1})}
$$
Here $U(f)$ belongs to the $L^{2}(K)$ because of [[Iwasawa decomposition of SL(2,R)]]

As shown in the [[Principal series representation of SL(2,R)#^686105|normalized unitary representation]],
$$
\frac{dg_{*}\mu}{d\mu}=\mid\mid c(g,\cdot)\mid\mid^{2}
$$
and $$
\int f \frac{dg_{*}\mu}{d\mu} \,d\mu_{X}(x) =\int f\,dg_{*}\mu
$$
So $\mid\mid U(f)\mid\mid_{L^{2}(K)}=\mid\mid f\mid\mid_{L^{2}(S^{1})}$.

In order to prove $\pi^{S^{1},\xi}\cong \pi^{\xi}$ we need to prove the diagram commutes:
![[Pasted image 20240203134129.png]]

1. $U(f)\in H_{\xi}$, here we need to verify the property of induced representation:
$$
\begin{align}
U(f)(gb)=&\mid\mid bge_{1}\mid\mid^{-1-i\xi}f(gb\cdot e_{1})\\ 
=& \mid\mid g \cdot a_{t}u_{x}\cdot e_{1} \mid\mid^{-1-i\xi}f(gb\cdot e_{1}) \\
=&e^{-t-i\xi t}\mid\mid g e_{1}\mid\mid^{-1-i\xi}f(g\cdot v) \\
=& \overline{\chi_{\xi}(b)}\Delta_{B}(b)^{1/2} U(f)(g) 
\end{align}
$$
2. $U(\pi^{S^{1},\xi}_{g}f)(g_{0})=\pi^{\xi}_{g}(U(f))(g_{0})$

Then in conclusion, $(\pi^{\xi},H_{\xi})$ is unitary, and $-I \in C(G), H^{even}_{\xi},H^{odd}_{\xi}$ invariant subspace so they are unitary.


##### Proof of the irreducible
Now the third step: irreducible

Here we need to admit some facts about [[Universal Enveloping Algebra]], 

Denote: $$
r^{+}=\frac{1}{2}(a+id), \ \ r^{-}= \frac{1}{2}(a-id) \in \mathfrak{sl}_{2}(\mathbb{C})
$$
in which $$
a= \begin{pmatrix}
1 & \\
& -1
\end{pmatrix},
d= \begin{pmatrix}
& 1  \\
1&
\end{pmatrix}.
$$
And $$
\begin{align}
\pi^{\xi}_{\partial}(r^{+})F_{\xi,n}= \frac{n+1+i\xi}{2} F_{\xi,n+2} \\
\pi^{\xi}_{\partial}(r^{-})F_{\xi,n}= \frac{-n+1+i\xi}{2} F_{\xi,n-2}.
\end{align}
$$
Suppose $\mathcal{V}\subset H^{even}_{\xi}$ closed non-trivial, invariant subspace and without lost of generality, $F_{\xi,n}\in \mathcal{V}$.

Then $\frac{{n+1+i\xi}}{2}\not=0$ for any $\xi$, $F_{\xi,n+2}$, $F_{\xi,n-2}\in \mathcal{V}$. It deduces that $<f_{\xi,n+2k}|k\in \mathbb{N}>=\mathcal{V}=H_{\xi}$.

Similarly for $H_{\xi}$, only problem: if $\xi=0, n=-1$.


##### Proof of isomorphism
$$
\begin{align}
\pi^{\xi,even}=\pi^{-\xi,even} \\
\pi^{\xi,odd}=\pi^{-\xi,odd} \\
\pi^{0,odd}=\delta^{1,+} \oplus \delta^{1,-} 
\end{align}
$$
Here recall some facts about [[Discrete series representation of SL(2,R)]].

And we need another theorem from earlier in the book:
#### Thm :: uniquely determined matrix coefficients 
$\pi$ unitary representation of $G$
$v \in H_{\pi}$ smooth $K$-eigenvector of weight $n\in \mathbb{Z}$
$\alpha \in \mathbb{R}$ Casimir eigenvalue
$\phi^{\pi}_{v}$ is uniquely determined by $\alpha$, $n, \mid\mid v\mid\mid$.

And for two representation $(\pi,H_{\pi}),(\rho,H_{\rho})$ of $G$, $v\in H_{\pi}$ and $w\in H_{\rho}$ with corresponding matrix coefficient $\phi^{\pi}_{v}=\phi^{\rho}_{w}$ for any $g\in G$. Then there exists the unitary isomorphism between the cycle representation generated by vector $v$ and $w$: $\pi\mid_{<v>}\cong \rho\mid_{<w>}$.

For the principal series representation, we admit the fact: $$
\alpha_{\delta^{1,+}}=\alpha_{\delta^{1,-}}=\alpha_{\pi^{0,odd}}=0
$$
and the construction of $\pi^{0,odd}$, it contains all odd weights. For $v_{1}\in H_{\pi}$ unit $K$-eigenvector of weight 1, so $$
\phi^{\pi^{0,odd}}_{v_{1}}=\phi^{\delta^{1,+}}_{e_{0}}
$$
Then this gives us that $$
<v_{1}>_{\pi^{0,odd}}=<e_{0}>_{\delta^{1,+}}=H_{\delta^{1,+}}
$$
in which $e_{l}: z \to z^{l}$ forms the basis of $H_{\delta^{1,+}}$.

On the other hand, $v_{-1}$ gives us $<v_{-1}>_{\pi^{O,odd}}=H_{\delta^{1,-}}$.