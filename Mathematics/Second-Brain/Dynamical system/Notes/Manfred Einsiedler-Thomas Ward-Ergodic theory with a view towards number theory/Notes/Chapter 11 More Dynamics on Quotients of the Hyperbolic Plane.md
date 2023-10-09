
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
i.e. any compact subset of $X$ only intersects with finitely many orbit points of action. 

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
Hnuhnuh iunuh 