Exercises for TA-finite field

Exercise about Extension degree:
Calculate and prove the following:
$[\mathbb{R}:\mathbb{Q}]=\infty$
$[\mathbb{Q}[\sqrt{ 7 }]:\mathbb{Q}]=2$
$[\mathbb{Q}[x]/(x^{7}+3x+6):\mathbb{Q}]=7$

Here is the fundamental fact that $K$ a field and that $p(x)\in K[x]$ is irreducible, then $K[x]/<p(x)>$ has basis $$
\mathcal{B}=\{1+<p(x)>,x+<p(x)>,\dots,x^{d-1}+<p(x)>\},
$$
in which $d$ is the degree of $p(x)$.
So for $[\mathbb{R}:\mathbb{Q}]=\infty$ because all the roots of $x^{n}-2$ are contained in $\mathbb{R}$.
and $\mathbb{Q}[\sqrt{ 7 }]=\mathbb{Q}[x]/<x^{2}-7>$. 

By Einsenstein, $x^{7}+3x+6$ is irreducible.

$\mathbb{Q}[x]/<x>=\mathbb{Q}$ and $\mathbb{Q}[x]/<x^{2}>=\mathbb{Q}[\sqrt{ d }]$



Complete the proof of the following:
Let $K$ be a field and assume a ring homomorphism $\phi: R \to K$ exists. Then there exists a unique ring homomorphism $\tilde{\phi}:F(R)\to K$ such that $\tilde{\phi}\mid_{R}=\phi$.


Consider the field extension of $\mathbb{Q}$, if $K$ is a number field of degree 2, i.e. an extension field of $\mathbb{Q}$ such that $[K:\mathbb{Q}]=2$, prove that $K=\mathbb{Q}(\sqrt{d })$ for some square-free integer $d$. 

if $[K:Q]=2$ then $K=\mathbb{Q}(t)$, where $t$ is the square root of some rational number in reduced number in reduced form, e.g. $t=\sqrt{ \frac{n}{m} }$. Then $\text{gcd}(n,m)=1.$ Then the integer $nm$ is clearly square free, so the key of proof is to show $$
\mathbb{Q}\left( \sqrt{ \frac{n}{m} } \right)=\mathbb{Q}(\sqrt{ nm }).
$$

For a field extension of $\mathbb{Q}$, if it's complete, will it  be also algebraic closed? Vice versa, if it's algebraic closed, will it be also complete?
$\mathbb{R}$ and $\mathbb{Q}_{p}$.
Quick review of the definition of complete space:

A metric space $(X, d)$ is complete if every Cauchy sequence in $X$ converges in $X$ with respect to  metric $d$.







### Exercise 2

Consider the following polynomials $f(x)$ over finite fields $\mathbb{F}_{q}$, if they are irreducible then find all the roots of the irreducible polynomials $f(x)$ in the algebraic extension $\mathbb{F}_{q}[x]/<f(x)>$, if they are not irreducible, then factorize the polynomials over the finite field.

$X^{3}-2$ over $\mathbb{F}_{7}$

$X^{3}+X^{2}+1$ over $\mathbb{F}_{5}$

$X^{9}-X$ over $\mathbb{F}_{3}$

$X^{27}-X$ over $\mathbb{F}_{3}$



Solutions: 
$X^{3}-2$ is irreducible in $\mathbb{F}_{7}[X]$. It has a root in $F=\mathbb{F}_{7}[t]/<t^{3}-2>$, namely $\overline{t}$. It has two other roots in $F,$ $2\overline{t}$ and $4\overline{t}$. 

$X^{3}+X^{2}+1$ is irreducible in $\mathbb{F}_{5}[X]$. In the field $F=\mathbb{F}_{5}[t]/<t^{3}+t^{2}+1>$, the polynomial has the root $\overline{t}$ and also the roots $2 \overline{t}^{2}+3\overline{t}$ and $3\overline{t}^{2}+\overline{t}+4$.

The last two polynomials are reducible in $\mathbb{F}_{3}$, by listing out all the irreducible polynomials, we get the results $$
x^{9}-x=x(x+1)(x-1)(x^{2}+1)(x^{2}+x+1)(x^{2}-x-1)
$$
and $$
\begin{array}
\ x^{27}-x=x(x+1)(x-1)(x^{3}+x^{2}+x+1)(x^{3}+x^{2}+x-1)\cdot \\ (x^{3}+x^{2}-x+1)(x^{3}-x^{2}+x+1)(x^{3}-x^{2}+x-1)(x^{3}-x^{2}-x-1)
\end{array}
$$





When $f(X)\in \mathbb{F}_{p}[X]$ has distinct roots, raising all roots of $f(X)$ to the $p$-th power permutes the roots:$$
\{\alpha_{1}^{p},\dots,\alpha^{p}_{m}\}=\{\alpha_{1},\dots,\alpha_{m}\}.
$$
Let $S=\{\alpha_{1},\dots,\alpha_{m}\}$. Since $f(X)^{p}=f(X^{p})$, the $p$-th power of each root of $f(X)$ is again a root of $f(X)$.
And we know $a^{p}=b^{p} \iff a=b$, so the function $\phi:S \to S$, takes different values on different elements of $S$. injective function from a finite set to itself is surjective, so $\phi$ is a permutation of $S$.


Let $\mathbb{F}_{q}$ be a finite field and $n$ a positive integer prime to $q$. Let $E_{d}$ be the set of monic irreducible polynomials in $\mathbb{F}_{q}[X]$ of degree $d$, where $d\geq 1$ divides $n$. Check $$
X^{q^{n}}-X = \prod_{d | n} \prod_{f\in E_{d}}f
$$
$X^{q^{n}}-X$ has no multiple factor in characteristic $p$. For an irreducible divisor $f$  of $X^{q^{n}}-X$ of degree $d$ with a root $f(\alpha)=0$ in $\overline{\mathbb{F}_{p}}$,  we know that $d$ divides $n$ from the field extensions $\mathbb{F}_{q} \subset \mathbb{F}_{q}(\alpha) \subset F_{q^{n}}$ and vice versa, i.e. given an irreducible polynomial $f$ of degree $d$ where $d$ divides $n$ with a root $\alpha$ of $f$ in $\overline{\mathbb{F}_{p}}$, which implies $f$ divides $X^{q^{n}}-X$. So in the factorial ring $\mathbb{F}_{q}[X]$, the polynomial $X^{q^{n}}-X$ having no multiple factor is the product of the monoic irreducible polynomials which divides it.





Take any prime $p$ and any integers $n,d \in \mathbb{N}_{\geq 1}$. Then in $\mathbb{F}_{p}[x]$, show that $$
\text{gcd}(x^{p^{n}}-x,x^{p^{d}}-x)=x^{p^{\text{gcd}(n,d)}}.
$$

for any $k$, we can write $x^{p^{n}}-x$ as the following sum/product:
$$
\begin{array}
\ x^{p^{n}}-x = \left( \sum\limits^{k}_{i=1}x^{p^{n}-i(p^{d}-1)-1} \right)\cdot (x^{p^{d}}-x)+(x^{p^{n}-k(p^{d}-1)}-x)
\end{array}
$$


$\mathbb{F}_{7}/<x^{3}-2>=\mathbb{F}_{7}(\alpha)=\mathbb{F}_{7^{3}}$.