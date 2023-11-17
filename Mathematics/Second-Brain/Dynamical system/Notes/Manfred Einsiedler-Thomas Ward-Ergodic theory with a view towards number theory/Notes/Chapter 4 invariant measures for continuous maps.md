# Tags
#measure-theory  #dynamical-system #ergodic-theory 

---

# References


---


# Other related files
[[measure theory]]

---

Given a topological group $G$ and a measure space $(\Omega, \mathcal{B}, \mu)$,

### Def :: measurable action
$$
\begin{array}
\ G\times \Omega \to \Omega\\
(g,x) \to gx
\end{array}
$$
is measurable.

### Def :: Pullback of measure
$g_{*}\mu(A)=\mu(g^{-1}A)$


### Def :: invariant measure and quasi-invariant measure
$g_{*}\mu(A)=\mu$ for $\forall g\in G$.

quasi-invariant: if $g_{*}\mu$ and $\mu$ are equivalent: $\forall A\in \mathcal{B},\mu_{1}(A)=0$ if and only if $\mu_{2}(A)=0$.


### Def :: $\sigma$-finite
$\Omega$ is $\sigma$-finite if a countable union of measurable subsets of $\mu$-finite measure.



### Def :: Radon-Nikodym derivative of $g_{*}\mu$ with respect to $\mu$



### Thm :: measures invariant under horocycle flow
$T:X \to X$ continuous map os a compact metric space. Let $(\nu_{n})$ be any sequence in $\mathcal{M}(X)$. Then any $weak^{*}$-limit point of sequence $\mu_{n}$ defined by 
$$
\mu_{n}=\frac{1}{n}\sum^{n-1}_{j=0}T^{j}_{*}\nu_{n}
$$
is a member of $\mathcal{M}^{T}(X)$. 

#### Remark
For flows $h(t):X\to X$, $\mu_{n}$ be any sequence in $\mathcal{M}(X)$. Then any $weak^{*}$-limit point of sequence $M_{T_{n}}$ defined by 
$$
\begin{align}
M_{T_{n}}&=\frac{1}{n}\int^{T_{n}}_{0}f(h(t)\cdot x)\,dt \\
&=\int f\,d\mu_{n}   
\end{align}
$$



### Thm :: ergodic decomposition theorem

^2a6b16

let $T:(X,\mathcal{B},\mu)\to(X,\mathcal{B},\mu)$ be measure-persevering map of a Borel probaility space then there exists $(Y,\mathcal{B},\nu)$ and a measurable map $y\to \mu_{y}$ for which $\nu:\mathcal{B}\to \mathbb{R}_{\geq 0}$,
1. $\mu_{y}$ is a $T$-invariant ergodic probability measure on $X$ for almost every $y$;
2. $\mu=\int_{Y}\mu_{y}\,d\nu(y)$.