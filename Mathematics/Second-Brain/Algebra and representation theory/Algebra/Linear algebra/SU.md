The Lie algebra of the special unitary group SU(2), often denoted by su(2), consists of 2x2 skew-Hermitian (Hermitian and traceless) matrices. This algebra is a vector space spanned by the following three basis elements, usually represented in terms of the Pauli matrices: 

$$
[σ_{1} = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}, \quad σ_{2} = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix}, \quad σ_{3} = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}]
$$

where each of these matrices is multiplied by a factor of i and 1/2 so that their commutation relations become the required su(2) Lie bracket relations:

$$
[ [σ_{i}, σ_{j}] = 2iε_{ijk}σ_{k} ]
$$

where ε_{ijk} is the Levi-Civita symbol. 

This Lie algebra is isomorphic to the Lie algebra so(3) of the special orthogonal group SO(3), which represents rotations in three dimensions, making SU(2) the double cover of SO(3).



it's isomorphic to $SL_{2}(\mathbb{R})$.


what is the Lie algebra of $SL_{2}(\mathbb{R})$?

The Lie algebra of SL(2,ℝ), often denoted as sl(2,ℝ), consists of all 2x2 real matrices with trace equal to zero.
The basis for the Lie algebra sl(2,ℝ) can be represented by the following three matrices:
$$
[ H = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}, \quad E = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}, \quad F = \begin{pmatrix} 0 & 0 \\ 1 & 0 \end{pmatrix}]
$$
The associated commutation relations defining the Lie algebra are given by:
$$
[ [H, E] = 2E, \quad [H, F] = -2F, \quad [E, F] = H ]
$$
It's important to note that this Lie algebra is not semi-simple and has a non-zero radical. It has applications in the theory of automorphic forms and more generally in representation theory and number theory.

how to calculate $\exp(td)$ as the expontial map from Lie algebra to Lie group, in which $d=\begin{pmatrix} 0 & 1 \\ 1& 0\end{pmatrix}$.


when we consider the representation of $G$, why do we need to consider $\pi(X)v=\lim\frac{\exp(tX)v-v}{t}$


Calculate the integral $\int^{2\pi}_{0}(1-r(\tanh t)e^{i\theta})^{-n}\,d\theta$, in which $\mid r(\tanh t)\mid<1$ and $n>2$ we can simply expand the innermost term in a power series. Then we get the integral as a constant $2\pi$.


what is the self-adjoint of matrix $k_{\theta}=\begin{pmatrix}e^{-i\theta}&0\\0&e^{i\theta}\end{pmatrix}$.


Change $z\to z=r\cdot e^{i\theta}$, then calculate $dz$ in terms of $r,\theta$.

Consider the integral $\int f(z)\,dz$ how to change variable into $r,\theta$ as double integral $\int f(r\cdot e^{i\theta})\,dr d\theta$

how to get the area element $rdr d\theta$ 

how to change variable in  $\oint_{\mid z\mid=R} \frac{f(z)}{z-z_{0}} \, dz$ into $\int^{2\pi}_{0}\frac{f(Re^{i\theta})}{Re^{i\theta}-z_{0}}Rie^{i\theta}\,d\theta$. 


Given a sequence that we have $\sum\limits^{\infty}_{l=0}\mid\mid a_{l}z^{l}\mid\mid=\mid\mid f\mid\mid$is convergent then under what condition will we have $\sum\limits^{\infty}_{l=0}a_{l}z^{l}$ is convergent to $f$.


Given a $K$ as compact subgroup of $G$, then consider the unitary representation $(\pi,H)$ of $G$, then suppose $K\cong S^{1}$, then there are non-trivial eigenvector $v\in H$ of $k_{\theta}\in K$.

