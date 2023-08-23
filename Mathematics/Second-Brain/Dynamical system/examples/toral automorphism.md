# Tags


---

# References


---


# Other related files


---

For the flat torus $X=\mathbb{R}^{2}/\mathbb{Z}^{2}$, given a matrix $A=\begin{pmatrix}a&b\\c&d\end{pmatrix}$ in which $a, b, c, d\in \mathbb{Z}$. Then $A(\mathbb{Z}^{2})\subset \mathbb{Z}^{2}$ and we get a map: $$ T:X\rightarrow X: x\mapsto Ax (\mod \mathbb{Z}^{2})$$
Assume that $\det(A)=\pm1$, then $A^{-1}$ is also integral and $x\mapsto A^{-1}x(\mod\mathbb{Z}^{2})$ gives the inverse of $T.$

### Def :: hyperbolic automorphism
Suppose that for eigenvalues $\lambda$ of $A$, $|\lambda|\not=1$, then $T:X=\mathbb{R}^{2}/\mathbb{Z}^{2}\rightarrow X$ is called hyperbolic automorphism.

### Rmk : 
for eigenvalues, we have $\lambda_{1}\lambda_{2}=\pm1$, so we get $|\lambda_{1}|<1<|\lambda_{2}|$, which corresponds to two eigenvectors $Av_{1}=\lambda_{1}v_{1}$ and $Av_{2}=\lambda_{2}v_{2}$. It's as same as [[Fuchsian group#^e2227f|hyperbolic elements in Fuchsian group]].

### Def :: Stable manifolds
$$W^{s}(x)=\{(x+tv_{1})\mod\mathbb{Z}^{2}|t\in \mathbb{R}\},\ \ t\in X.$$

### Def :: unstable manifolds
$$W^{u}(x)=\{(x+tv_{2})\mod\mathbb{Z}^{2}|t\in \mathbb{R}\},\ \ t\in X.$$

### Thm :: Properties of stable/unstable manifolds
1. $$\forall y\in W^{s}(x):\ \text{d}(T^{n}x,T^{n}y)\rightarrow0,\ n\rightarrow 0.$$
2. $$\forall y\in W^{u}(x): \text{d}(T^{-n}x, T^{-n}y)\rightarrow 0,\ n\rightarrow 0.$$
3. $$T(W^{s}(x))=W^{s}(T(x)),\ \ T(W^{u}(x))=W^{u}(T(x)).$$
Proof: $$A^{n}(x+tv_{1})=A^{n}x+t\lambda^{n}_{1}v_{1},$$
in which $t\lambda^{n}_{1}v_{1}\rightarrow 0$.


### Thm :: $\overline{W^{s}(x)}=X$


### Thm :: $\forall \delta>0:\exists t$, such that $[-t,t]v_{2}+\mathbb{Z}^{2}$ is $\delta$-dense in $X$.


### Thm :: $T:x\rightarrow Ax(\mod\mathbb{Z}^{2})$ is [[Lectures note about Dynamical System#^cba4af|topological mixing]]


### Thm :: The periodic points of $T:X=\mathbb{R}^{2}/\mathbb{Z}^{2}\rightarrow X$ are $\mathbb{Q}^{2}/\mathbb{Z}^{2}$.



### Thm :: Structural stability
For the torus $X=\mathbb{R}^{2}/\mathbb{Z}^{2}$, $T: X\rightarrow X$ a hyperbolic automorphism:
For any $\epsilon>0$, there exists $\delta>0$, any homeomorphism $S:X\rightarrow X$: $\text{max}_{x\in X}\text{d}(Sx,Tx)<\sigma$, there exists a 




### Thm :: torus automorphism is measure preserving

^93f4ca
