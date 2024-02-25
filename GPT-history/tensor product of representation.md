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