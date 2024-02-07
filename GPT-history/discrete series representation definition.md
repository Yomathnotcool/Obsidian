Suppose there fore that $(v_{n})$ is a sequence in $D_{u_{0}}=\{v\in H_{\pi}\mid \phi^{\pi}_{u_{0},v}\in L^{2}(G)\}$ in which $H_{\pi}$ is the representation space of $\pi$ and $G$ is unimodular.
And it satisfies that $$
(v_{n},Tv_{n})\to  (v,f)\in H_{\pi}\times L^{2}(G)
$$
as $n \to \infty$. Choosing a subsequence if necessary we may upgrade the $L^{2}$ convergence and suppose without loss of generality that $Tv_{n}\to f$ almost everywhere.


for $f \in C_{c}(G)$, then $f \in L^{1}(G)$? and define the function $f(g^{-1})=\tilde{f}(g)$, we have that $\tilde{f}\in L^{1}(G)$?


$\int_{G}f*v(g)\overline{w}(g)\,dm(g)=<f*v,w>$, in which $f\in L^{1}(G)$,$v\in L^{2}(G)$, and fixed $w\in L^{2}(G)$, this shows that the integral defining $f*v$ exists almost everywhere, defines a function in $L^{2}(G)$.

why does the inner product show that the function $f*v$ is well-defined almost everywhere in $L^{2}(G)$. \


I have learnt the theorem that if a representation $(\pi,H_{\pi},G)$ of locally compact group $G$ is almost square integrable, then it's tempered. but is the inverse theorem true?


can you give a counterexample that a representation of $SL_{2}(\mathbb{R})$ that is tempered but not almost square integrable?

Why does unitary representation give that the representation is tempered? and the definition of almost square integrable is the diagonal matrix coefficient $\phi^{\pi}_{v}(g)=<\pi(g)v,v>\in L^{2+\epsilon}(G)$. I don't understand the definition that you used.

why does the principal series representation of $SL_{2}(\mathbb{R})$ is tempered?


Define sub-exponential growth as following: for locally compact group $G$, every compact subgroup $K$, $\lim\limits_{ n \to \infty }m(K^{n})^{1/n}=1$. Does $SL_{2}(\mathbb{R})$ have sub-exponential growth?

Why is $SL_{2}(\mathbb{R})$  unimodular? And why does unimodular give us that $m(K^{n})=m(K)^{n}$.

Then how do you show that $SL_{2}(\mathbb{R})$ has sub-exponential growth


 consider the complementary series representation $(\gamma^{s},V_{s})$ of $SL_{2}(\mathbb{R})=BK=AUK$, it's defined as following:

$$
V_{s}=\{f:SL_{2}(\mathbb{R})\to \mathbb{C}\mid f\ \text{is smooth,even and} f(gb)=\chi_{(s)}(b)^{-1}\Delta_{B}(b)^{1/2}f(g)\ \text{for all}\ g \in SL_{2}(\mathbb{R})\ \text{ and }\ b\in B\}.
$$
in which $\chi_{(s)}(a_{t}u_{x})=e^{st}$ is a non-unitary character, And $\gamma^{s}$ is the left-regular representation acting on $V_{s}$.

Now claim $\gamma^{s}$ does not preserve the $L^{2}(K)$-norm.



consider the Lie algebra $\mathfrak{sl}_{2}(\mathbb{R})$ of $SL_{2}(\mathbb{R})$, in order to define the [[Universal Enveloping Algebra]] of $\mathfrak{sl}_{2}(\mathbb{R})$, what is the corresponding complex associative algebra.


Prove the integral $$
\int^{\pi}_{0} \frac{d\theta}{\mid \sin(\theta)\mid^{1-s}}
$$
is finite.

To show that the integral is finite, we must ensure that it doesn't blow up to infinity at any point in the interval [0,π]. The tricky points here are 0 and π, where the denominator sin(θ) becomes 0. Let's try to estimate the integral near these points.

First consider a small positive quantity ε and evaluate the integral successively for ε→0+ using absolute values to handle negative fractions in the calculation:

$$\lim_{{ε→0}^+} \int^{ε}_{0} \frac{d\theta}{|\sin(\theta)|^{1-s}} = \lim_{{ε→0}^+} \int^{ε}_{0} \frac{d\theta}{\theta^{1-s}}$$

The latter integral equality is due to the fact that sin(θ)~θ near 0. The integral evaluates using standard results to [θ^s]^{ε}_{0} = ε^s for s>0. Given 0<s<1, this means the integral is finite for ε→0+.

Similarly, consider a small positive quantity δ and evaluate the integral successively for δ→0+ using the periodic property of the sin function to make the limit finite:

$$\lim_{{δ→0}^+} \int^{\pi}_{\pi-δ} \frac{d\theta}{|\sin(\theta)|^{1-s}} = \lim_{{δ→0}^+} \int^{\pi}_{\pi-δ} \frac{d\theta}{(\pi-\theta)^{1-s}}$$

The latter integral equality is due to the fact that sin(θ)~π−θ near π. The integral evaluates using standard results to [(\pi-\theta)^s]^{\pi}_{\pi-δ} = δ^s for s>0. Given 0<s<1, this means the integral is finite for δ→0+.

So, near 0 and π, where the denominator could create problems, we have shown that the integral is finite. Therefore, we can conclude that the entire integral over the range 0 to π is finite.

In the theory of Fourier analysis, we denote the coefficient $$
(c_{n})\in l^{1}(2\mathbb{Z})
$$
what is the notation $l^{1}(2\mathbb{Z})$.