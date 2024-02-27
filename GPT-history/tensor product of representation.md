$\mathfrak{X}^{*}=\mathfrak{X}^{-}\bigsqcup \mathfrak{X}^{+}$ is the inverse image under the transformation of $SL_{2}(\mathbb{R})$of $\mathfrak{X}_{\mathbb{C}}=\mathbb{C}\backslash\{0\}$ of the the complement $\mathcal{H}^{\pm}$ of $\mathbb{P}(\mathbb{R})$, in which $\mathcal{H}$ is the upper half plane, $\mathbb{P}(\mathbb{R})$ is the projective line defined as the space of lines in $\mathbb{R}^{2}$ and $\mathfrak{X}^{\pm}=\left\{ (z,w)\mid sign \mathrm{Im}\left(  \frac{z}{w}\right)=\pm  \right\}$. so how to describe the space $\mathfrak{X}^{*}$?

consider the discrete series representation $\pi^{n}$ of $SL_{2}(\mathbb{R})$, the action is defined as $$
\pi^{n}(g)f(z)=j(g^{-1},z)^{n}f(g^{-1}z)
$$
in which $j(g,Z)=(cz+d)$ if $$
g=\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}.
$$
Now I need you to help me verify the tensor product of two copy of the discrete series representation: $$
\pi^{n}\otimes \pi^{n}(g)f\otimes f(z)=j(g^{-1},z)^{2n} f(g^{-1}z)\otimes f(g^{-1}z)
$$

Now given a continuous unitary representation $(\pi,H)$ of $SL_{2}(\mathbb{R})$, by the standard decomposition, it can be written as a sum of multiplicity free representations $$
(\pi,H)= \oplus^{\infty}_{n=1}(\mathcal{l}_{n},\alpha_{n})
$$
then the tensor product $\pi \otimes \pi$ can be written as $$
\oplus^{\infty}_{n=1}\alpha_{n} \otimes \oplus^{\infty}_{n=1}\alpha_{n}=\oplus^{\infty}_{n=1}\oplus^{\infty}_{m=1}\alpha_{n}\otimes\alpha_{m}
$$


given a cofinite Fuchsian group $\Gamma$ of $SL_{2}(\mathbb{R})$, denote $\mathcal{F}$ as the canonical fundamental domain. then here are the vertices $\mu_{1},\mu_{2},\dots,\mu_{k}$ which are not $\Gamma$-equivalent. Then consider the stabilizer $\Gamma_{\mu_{i}}$ of $\mu_{i}$, it can be written $$
\Gamma_{\mu_{i}}=N_{i}^{-1}\begin{pmatrix}
1 & -1 \\
0 & 1 
\end{pmatrix}N_{i}
$$
in which $N_{i}(\mu_{i})=\infty$.


The question here is to understand why the stabilizer can be written as a conjugation of $N_{i}$.


what is the inverse of $$
\begin{pmatrix}
a  & b \\
 0 & 0
\end{pmatrix}
$$


Consider a linear functional defined as $$
F(f)= \frac{1}{T}\int^{T}_{0}f(xn(t))\,dt 
$$
in which $T$ is a fixed constant, and $x$ is a fixed point in the upper half plane, and $n(t)$ is the unitrangular matrix that represents the horocycle flow.

and the $f$ is a continuous function in $W_{4}$ which is the space of Sobolev norm of order 4. The function $f$ satisfies condition $$
\mid f (x) \mid \ll_{\Gamma} C\mid\mid f\mid\mid_{W_{2}}
$$
in which $\Gamma$ is the lattice of $SL_{2}(\mathbb{R})$ and $C$ is a constant that depends on the fixed point $x.$


Then let's try to simplify this claim:
The linear functional $$
F(f)=\int^{T}_{0}f(n(t))\,dt
$$
and $f\in W_{4}$ is continuous and $$
\mid f(x)\mid< C(x)\mid\mid f\mid\mid_{W_{2}}
$$
in which the $C(x)$ is a function that depends on $x$. then prove the $F(f)$ depends continuously on $f \in W_{4}$ with the norm $\mid\mid \cdot \mid\mid_{W_{4}}$. 


under what condition, that a bounded operator from Hilbert space $H$ to itself becomes continuous?


what does it mean by the function $f$ in the Hilbert space is orthogonal to the space of constant functions.


for a unitary representation $(\pi,H)$ of $SL_{2}(\mathbb{R})$, it can be decomposed into direct integral:
$$
H=\int^{\oplus}_{Z}H(\xi)\,d\mu(\xi)
$$
in which $Z$ is Borel measurable space, and $\mu$ is a measure that is defined on $Z$.

Furthermore, if $H=L^{2}(\Gamma \backslash G)$ the decomposition can be refined based on the eigenvalue $\lambda$ of Laplacian $\Delta$, $\lambda$ can be written as $s(1-s)$. Then $$
H=H_{0}\oplus H_{ct} \oplus H_{rs}=\int^{\oplus}_{Z}H(\xi)\,d\mu(\xi) 
$$
in which $H_{0}$ is the cuspidal part, and $H_{ct}$ represents the continuous part and $H_{rs}$ is the residue part.
Now the question is that we want to find an explicit relationship between $\xi$ and $s$. 

now we have a function $$
t_{y}(\xi)=y^{s}
$$
based on the discussion, how to prove this function is uniformly continuous for $\xi$, in which $s=s(\xi)$. my confusion is about this "hidden" function $s(\xi)$.


Based on the discussion before, the problem is that I dont understand the property of this function $s(\xi)$ about whether this function is continuous ?

