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