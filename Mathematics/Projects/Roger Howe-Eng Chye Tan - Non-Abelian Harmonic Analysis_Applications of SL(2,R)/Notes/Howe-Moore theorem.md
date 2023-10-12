
### Notion
$G$ locally compact $\sigma$- compact group 
$(X,\mu,\mathcal{B})$ a probability space with $L^{2}(X)$ separable 
	if $X$ is separable and $\mu$ is Borel, then the function space $L^{2}(X)$ is separable.

$G\times X\rightarrow X$ measurable measure-preserving action
	i.e. $\mu(g^{-1}A)=\mu(A),\ \forall g\in G, A\in \mathcal{B}$.
For $\forall g\in G$, define $\pi_{x}(g):L^{2}(X)\rightarrow L^{2}(X)$ by $f\rightarrow f(g^{-1}x)$ 

it has serval properties:
#### Thm :: Properties of $\pi_{x}(g)$
1. $\pi_{x}(g_{1}g_{2})=\pi_{x}(g_{1})\pi_{x}(g_{2})$;
2. $||\pi_{x}(g)f||_{2}=(\int_{X}|f(g^{-1}x)|^{2}\text{d}\mu(x))^{\frac{1}{2}}$=$||f||_{2}$
	i.e. $\pi_{x}(g)$ is [[unitary representation#^3f05ae|unitary operator]].

Then the operator can induce a [[unitary representation]]:
$\pi_{x}:G\rightarrow U(L^{2}(X))$, in which $U(L^{2}(X))$ is the group of unitary operators.


#### Thm :: for any function $f\in L^{2}(X)$, the map $G\rightarrow L^{2}(X)$ with $g\rightarrow \pi_{x}(g)f$ is continuous.
##### Rmk :: the proof of this lemma is very confusing.

##### Proof:
$G$ as a [[topological group#^9f267a|topological group]], we only need to consider the continuity at $Id$.
By [[Integral#^ed8a6a|Fubini theorem]], the function $$<\pi_{x}(g)f,f>=\int_{X}f(g^{-1}x)\overline{f(x)}\text{d}\mu.$$
is measurable. 
