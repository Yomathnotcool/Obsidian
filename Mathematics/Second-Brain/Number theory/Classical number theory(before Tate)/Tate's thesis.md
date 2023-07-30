## Tags
#notes #number-theory #padic #L-function #Langlands-program 

---

## References:
[James-Michael Leahy - An introduction to Tate’s Thesis.pdf](hook://file/TVoMgP9Gm?p=YmFzZSBmb3IgYWxnZWJyYSBhbmQgbnVtYmVyIHRob2VyeS9UQVRF&n=James%2DMichael%20Leahy%20%2D%20An%20introduction%20to%20Tate%E2%80%99s%20Thesis%2Epdf#p=8&x=0&y=0&s=1&e=12)


---
## Other related notes:
[[Riemann theory]]
[[Modular form]]

---


In this section, let $F$ be a number field and $\mathbb{A}_{F}$ its ring of adeles. An automorphic representation of $GL_{1}(F)$ is any irreducible unitary representation of $GL_{1}(\mathbb{A}_{F})$ appearing in $L^{2}(GL_{1}(F)\backslash GL_{1}(\mathbb{A}_{F}))$. As a $GL_{1}(\mathbb{A}_{F})$-module,
$$
\begin{equation*}
    L^{2}(GL_{1}(F)\backslash GL_{1}(\mathbb{A}_{F}))=\int^{\oplus}_{GL_{1}(F)\backslash GL_{1}(\mathbb{A}_{F})}\psi(g)
\end{equation*}
$$
so an automorphic representation is simply a grossencharacter of $F$, i.e.  a character $\psi:F^{\times}\backslash \mathbb{A}_{F}^{\times}\rightarrow S^{1}$. Thus the theory we are discussing is that in the case of $GL_{1}$, simply Hecke's theory of $L$-functions associated to grossencharacters. 
Let $\psi: F^{\times}\backslash \mathbb{A}_{F}^{\times}\rightarrow S^{1}$ be a grossencharacter of $F$. We can decompose it $\psi=\prod_{v}\psi_{v}$ as a product of characters $\psi_{v}$ on $F^{\times}$, with $\psi_{v}$ unramified for almost all $v$. Let $S$ be the set of ramified places. For every $v\not\in S$, define $\chi(v)=\psi_{v}(\pi_{v})$ where $\pi_{v}\in F_{v}$ is a uniformizer. Note that the choice of uniformizer does not matter. We can extend $\chi$ by multiplicativity to the set of ideals of $F$ prime to $S$. 

#### Def :: 
The L-function associated to $\phi$, or to $\chi$, is 
$$
\begin{equation*}
    L(s, \chi)=\sum_{S\nmid\mathfrak{a}}\frac{\chi(\mathfrak{a})}{N(\mathfrak{a})^{s}}=\prod_{v\not\in S}\bigg(1-\frac{\chi(v)}{N(v)^{s}}\bigg)^{-1}.
\end{equation*}
$$
#### Thm :: Properties of $L$-function with grössencharacter
$L(s,\chi)$ has nice $L$-function properties:

 1. It converges for $\mathfrak{Re}(s)>1$;
 2. It has a meromorphic continuation to the whole plane, with a simple pole at $s=1$ if $\chi$ is trivial and no poles otherwise;
 3. There is a constant $A$, a constant $W(\chi)$ of modulus 1, and a gamma factor $\Gamma(s,\chi)$ such that $\mathfrak{L}(s,\chi)=s(s-1)A^{s}\Gamma(s,\chi)L(s,\chi)$ is entire and satisfies the functional equation
    
$$
    \begin{equation*}
        Z(1-s,\chi^{-1})=W(\chi)Z(s,\chi)
    \end{equation*}
$$

We skip the proof of this theorem. For the detail of this theorem, check in §6. HECKE THEORY FOR GL(2) by Gelbart:
[Automorphic_forms_on_adele_groups - S. Gelbart.pdf](hook://file/TVl83XOC0?p=bGFuZ2xhbmRzIHByb2dyYW1tZS9BdXRvbXJwaGljIGZvcm1zIGFuZCBBdXRvbW9ycGhpYyByZXByZXNlbnRhdGlvbg==&n=Automorphic%5Fforms%5Fon%5Fadele%5Fgroups%20%2D%20S%2E%20Gelbart%2Epdf#p=106&x=0&y=0&s=2&e=27).
By choosing an appropriate set of test functions and an appropriate measures, we can extend Riemann zeta to an idelic integral.
For the set of test functions are defined as following:
#### Def :: Bruhat-Schwartz function
Adelic Bruhat-Schwartz functions are linear combinations of functions $\Phi: \mathbb{A}_{\mathbb{Q}}\rightarrow \mathbb{C}$ where $\Phi=\prod\limits_{v\leq\infty} \Phi_{v}$, in which $\Phi_{v}$ are the characteristic function of $\mathbb{Z}_{v}$ for all but finitely many $v< \infty$. And $\Phi_{\infty}$ is Schwartz on $\mathbb{R}$, $\Phi_{v}$ is Bruhat-Schwartz function on $\mathbb{Q}_{v}$. The space of Bruhat-Schwartz functions are denoted as $S(\mathbb{A_{\mathbb{Q}}})$.



Recall the definition of Schwartz on $\mathbb{R}$:
#### Def :: Schwartz function 
$$
\begin{equation*}
    S(\mathbb{R},\mathbb{C})=\{f\in C^{\infty}(\mathbb{R},\mathbb{C})|\forall \alpha,\beta\in \mathbb{N}, ||f||_{\alpha,\beta}=\text{sup}_{x\in\mathbb{R}}x^{\alpha}(D^{\beta}f)<\infty\}
\end{equation*}
$$
Now let's give the defition of Idelic integral: 
#### Def :: idelic integral

^d49cb1

Define the idelic integral for factorizable idelic functions $\Phi=\prod_{v}\Phi_{v}$ such that $\Phi_{p}$ is the characteristic function $\mathbb{1}_{\mathbb{Z}_{p}}$ for almost all primes $p$ by 
$$
\begin{equation*}
    \int_{\mathbb{A}^{\times}_{\mathbb{Q}}}\Phi(x)\text{d}^{\times}x=\prod_{v\in S}\int_{\mathbb{Q}^{\times}_{v}}\Phi_{v}(x_{v})\text{d}^{\times}x_{v},
\end{equation*}
$$
in which $S$ is a finite set containing $\infty$ and all primes that $\Phi_{p}\not=\mathbb{1}_{\mathbb{Z}_{p}}$. The measure $\text{d}^{\times}x$ is defined as following:
$$
\begin{equation*}
\text{d}^{\times}x= \left\{
    \begin{array}{cc}
        \frac{\text{d}x_{\infty}}{|x_{\infty}|_{\infty}}, &  \text{if}\ v=\infty\\
        \frac{1}{1-p^{-1}}\frac{\text{d}x_{p}}{|x_{p}|_{p}}, & \text{if}\ v=p, p\ \text{are finite primes}
    \end{array}
    \right\}
\end{equation*}
$$

Such that $\text{d}^{\times}x_{p}$ is normalized so that $\int_{\mathbb{Z}_{p}^{\times}}\text{d}^{\times}x_{p}=1$.


#### Def :: idelic absolute value
Idelic absolute value: $x=\{x_{\infty},x_{2},...\}\in\mathbb{A}^{\times}_{\mathbb{Q}}$, then $|x|_{\mathbb{A}}=\prod_{v\leq\infty}|x_{v}|_{v}$.


In order to get idelic absolute value, we choose a special test function: for $x=\{x_{\infty},x_{2},x_{3},...\}$, then
$$
\begin{equation*}
    h(x)=e^{-\pi x_{\infty}^{2}}\prod_{v<\infty}\mathbb{1}_{\mathbb{Z}_{v}}(x_{v})\in S(\mathbb{A}_{\mathbb{Q}}).
\end{equation*}
$$
After some calculation, we know that the Fourier transform of $h(x)$ is equal to $h(x)$.

Now we are ready to write down the zeta integral:
$$
\begin{equation*}
    Z(s)=\int_{\mathbb{A}^{\times}_{\mathbb{Q}}}h(x)|x|^{s}_{\mathbb{A}_{\mathbb{Q}}}\text{d}^{\times}x, \ \ s\in\mathbb{C},\ \mathfrak{Re}(s)>1.
\end{equation*}
$$
For every automorpic form $\phi$ on $\mathbb{A}_{\mathbb{Q}}^{\times}$ can be uniquely expressed in the form 
$$
\begin{equation*}
    \phi(x)=c\cdot \chi_{idelic}(x)\cdot |x|^{it}_{\mathbb{A}},\ \ \forall x\in\mathbb{A^{\times}_{Q}},\ 
\end{equation*}
$$
in which $c\in\mathbb{C},\ t\in\mathbb{R}$ are fixed constants. And the character $\chi_{idelic}$ is an idelic lift of a Dirichilet character $\chi(mod\ p^{f})$. The idelic lift of $\chi$ is the Hecke character $\chi_{idelic}:\mathbb{Q}^{\times}\backslash\mathbb{A}^{\times}_{\mathbb{Q}}\rightarrow\mathbb{C}$ defined as 
$$
\begin{equation*}
    \chi_{idelic}(g)=\chi_{\infty}(g_{\infty})\cdot\chi_{2}(g_{2})\cdot\chi_{3}(g_{3})\cdot\cdot\cdot\ \ \ g=\{g_{\infty},g_{2},g_{3},...\}\in\mathbb{A^{\times}_{Q}},
\end{equation*}
$$
where 
$$
\begin{equation*}
\chi_{\infty}(g_{\infty})=\left\{
\begin{array}{ccc}
     1& \chi(-1)=1 \\
     1&  \chi(-1)=-1\ \text{if}\  g_{\infty}>0\\ 
     -1& \chi(-1)=-1\ \text{if}\ g_{\infty}<0
     
\end{array}
\right\}
\end{equation*}
$$
and 
$$
\begin{equation*}
    \chi_{v}(g_{v})=\left\{
    \begin{array}{cc}
        \chi(v)^{m} &\text{if}\ g_{v}\in v^{m}\mathbb{Z}^{\times}_{v}\ \text{and}\  v\not=p  \\
         \chi(j)^{-1} & \text{if}\ g_{v}\in p^{k}(j+p^{f}\mathbb{Z}_{p})\ \text{with}\ j,k\in\mathbb{Z}.\ (j,p)=1,\ \text{and}\ v=p 
    \end{array}
    \right\}
\end{equation*}
$$
Let's write down adelic Poisson summation formula:
#### Def :: adelic Possion summation formula 
$$
\begin{equation}
    1+\sum_{\alpha\in\mathbb{Q}^{\times}}h(\alpha x)=\frac{1}{|x|_{\mathbb{A}}}+\frac{1}{|x|_{\mathbb{A}}}\sum_{\alpha\in\mathbb{Q}^{\times}}h(\frac{\alpha}{x})
\end{equation}
$$

By using the decomposition $\mathbb{A}^{\times}_{\mathbb{Q}}=\bigcup_{\alpha\in\mathbb{Q\times}}\alpha\cdot(\mathbb{Q}^{\times}\backslash\mathbb{A}^{\times}_{\mathbb{Q}})$, we obtain:
$$
\begin{equation*}
    \int_{\mathbb{A}^{\times}}h(x)|x|^{s}_{\mathbb{A}}\text{d}^{\times}x=\sum_{\alpha\in\mathbb{Q}^{\times}}\int_{\alpha\cdot(\mathbb{Q}^{\times}\backslash\mathbb{A}^{\times})}h(x)|x|^{s}_{\mathbb{A}}\text{d}^{\times}x
\end{equation*}
$$
In order to obtain the analytic coninuation and functional equation, we calculate this integral by Poisson summation formula:
$$
\begin{align*}
    \pi^{-\frac{s}{2}}\Gamma(\frac{s}{2})\zeta(s)&=\int_{x\in\mathbb{Q}^{\times}\backslash\mathbb{A}^{\times}_{\mathbb{Q}}}\sum_{\alpha\in\mathbb{Q}^{\times}}h(\alpha x)|x|^{s}_{\mathbb{A}}\text{d}^{\times}x\\
   &=\frac{1}{s-1}-\frac{1}{s}+\int_{x\in\mathbb{Q}^{\times}\backslash\mathbb{A}_{\mathbb{Q}^{\times}}\& |x|_{\mathbb{A}\geq 1}}\sum_{\alpha\in\mathbb{Q}^{\times}}h(\alpha x)(|x|^{s}_{\mathbb{A}}+|x|^{1-s}_{\mathbb{A}})\text{d}^{\times}x.
\end{align*}
$$
In Tate's thesis, we can obtain same result for any test function $\Phi$ in the adelic Bruhat-Schwartz space $S(\mathbb{A}_{\mathbb{Q}})$. Let's rewrite the adelic Poisson summation formula:
$$
\begin{equation*}
    \sum_{\alpha\in\mathbb{Q}^{\times}}\Phi(\alpha x)=\frac{\hat{\Phi}(0)}{|x|_{\mathbb{A}}}+\frac{1}{|x|_{\mathbb{A}}}\sum_{\alpha\in\mathbb{Q}^{\times}}\hat{\Phi}(\frac{\alpha}{x})-\Phi(0)
\end{equation*}
$$
by same kind of calculation, we get similar result:
$$
\begin{align*}
    \int_{x\in \mathbb{Q}^{\times}\backslash\mathbb{A}^{\times}}\sum_{\alpha\in\mathbb{Q}^{\times}}\Phi(\alpha x)|x|^{s}_{\mathbb{A}}\text{d}^{\times}x&=\frac{\hat{\Phi}(0)}{s-1}-\frac{\Phi(0)}{s}\\
    &+\int_{x\in\mathbb{Q}^{\times}\backslash\mathbb{A}_{\mathbb{Q}^{\times}}\& |x|_{\mathbb{A}\geq 1}}\sum_{\alpha\in\mathbb{Q}^{\times}}(\Phi(\alpha x)|x|^{s}_{\mathbb{A}}+\hat{\Phi}(\alpha x)|x|^{1-s}_{\mathbb{A}})\text{d}^{\times}xx
\end{align*}
$$
The right hand side is invariant under translation: $s\rightarrow 1-s,\ \Phi\rightarrow \hat{\Phi}$. For the left hand side, as we assumed in the definition, $\Phi\in S(\mathbb{A}_{\mathbb{Q}})$ is factorizable. It follows that
$$
\begin{align*}
    \int_{\mathbb{A}^{\times}_{\mathbb{Q}}}\Phi(x)|x|^{s}_{\mathbb{A}}\text{d}^{\times}x&=\int_{\mathbb{R}^{\times}}\Phi_{\infty}(x_{\infty})|x_{\infty}|^{s}_{\infty}\frac{\text{d}x_{\infty}}{|x_{\infty}|_{\infty}}\cdot\prod_{p}\int_{\mathbb{Q}^{\times}_{p}}\Phi_{p}(x_{p})|x_{p}|^{s}_{p}\text{d}^{\times}x_{p}\\
    &=\widetilde{\Phi}_{\infty}(s)\cdot\bigg(\prod_{p\in S}\frac{\int_{\mathbb{Q}^{\times}_{p}}\Phi_{p}(x_{p})|x_{p}|_{p}^{s}\text{d}^{\times}x_{p}}{(1-p^{-s})^{-1}}\bigg)\zeta(s)
\end{align*}
$$
where $\widetilde{\Phi}(s)=\int_{\mathbb{R}^{\times}}\Phi(y)y^{s}\frac{\text{d}y}{y}$.

Now let $v\leq \infty$ determine a local field $\mathbb{Q}_{v}$. Then we can have the local zeta integral:
#### Def :: local zeta integral
Fix $s\in\mathbb{C}$ with $\mathfrak{Re}(s)>0$. Let $\Phi:\mathbb{Q}_{v}\rightarrow \mathbb{C}$ be a locally constant compactly supported function as definition \ref{BruhatSchwartz} if $v<\infty$, and a Schwartz function if $v=\infty$. Let $\omega:\mathbb{Q}^{\times}_{v}\rightarrow\mathbb{C}^{\times}$ be a local unitary character, i.e. a continuous homomorphism of absolute value 1. 
 The local zeta integral associated to $\omega$ and $\Phi$ is defined as 
$$
    \begin{equation*}
        Z_{v}(s,\Phi, \omega)=\int_{\mathbb{Q}^{\times}_{v}}\Phi(x)\omega(x)|x|^{s}_{v}\text{d}^{\times}x,
    \end{equation*}
$$
 in which the $\text{d}^{\times}x$ denotes the multiplicative Haar measure as defined in [[Tate's thesis#^d49cb1|Haar measure]].


We state the main result for the local zeta integral without further detail:
#### Thm :: functional equation of local zeta integral
Let $s\in\mathbb{C}$ with $0<\mathfrak{Re}(s)<1$. The local zeta integral $Z_{v}(s,\Phi,\omega)$ satisfies the functional equation
$$
\begin{equation*}
    Z_{v}(s,\Phi,\omega)=\gamma(s,\omega)\cdot Z_{v}(1-s,\hat{\Phi},\bar{\omega})
\end{equation*}
$$
where $\hat{\Phi}$ is the Fourier transform of $\Phi$: 
$$
\begin{equation*}
    \hat{\Phi}(x )=\int_{\mathbb{Q}^{\times}_{v}}\Phi(y)e_{v}(-xy)\text{d}y,
\end{equation*}
$$
$\overline{\omega}=\omega^{-1}$ is the complex conjugate of $\omega$, and $\gamma(s,\omega)$ is a meromorphic function which is independent of the choice of $\Phi$.

#### Rem 
After some calculation, we can get the explicit form of the $\gamma(s,\omega)$. If we choose appropriate test function, the result of zeta integral will be the $L$-functions that we desire.
