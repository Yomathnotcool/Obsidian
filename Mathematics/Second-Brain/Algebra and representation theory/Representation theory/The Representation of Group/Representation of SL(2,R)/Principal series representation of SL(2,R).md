### Def :: Principal series representation

^62e5c4

Consider $G=SL_{2}(\mathbb{R})$, by [[Iwasawa decomposition of SL(2,R)|Iwasawa decomposition]], $G=KAU=KB$, in which $$
B=AU=\{\begin{pmatrix}
e^{x}  & t  \\
 & e^{-x}
\end{pmatrix}\mid x,t\in\mathbb{R}\}
$$
define the character of $B$: $\chi_{\xi}(a_{t}u_{x})=e^{i\xi t}$ for any $b=a_{t}u_{x}\in B$. 

The principal series representation of $SL_{2}(\mathbb{R})$ is defined as the induced representation $(\pi^{\xi},H_{\xi})=(Ind^{G}_{B}\chi_{\xi},Ind \mathbb{C}^{\times})$, in which 
$$
H_{\xi}=\{f:G\to \mathbb{C}^{\times} \mid f\ \text{is measurable}\ \ \text{with finite norm} \mid\mid f\mid_{K}\mid\mid<\infty\}
$$
and $f$ satisfies $f(gb)=\overline{\chi_{\xi}(b)}\Delta_{B}(b^{1/2})f(g)$ for any $b\in B$, which $\Delta_{B}$ as the modular function of $SL_{2}(\mathbb{R})$ is $e^{-2t}$.

And the norm $\mid\mid f\mid_{K}\mid\mid_{L^{2}(K)}^{2}$ is defined as $$
\int_{K}\mid\mid f(k)\mid\mid_{H_{B}}^{2}\,dm_{K}(k) 
$$
The representation $\pi^{\xi}_{g}$ acts as the [[Regular representation of SL(2,R)|left regular representation]]: $\pi^{\xi}_{g}(f)(x)=f(g^{-1}x)$.


#### Def :: even or odd representation

For a representation $\pi \in \widehat{SL_{2}(\mathbb{R})}$, it's called even representation if $\pi_{-I}f=f$, otherwise it's odd.

For the [[Principal series representation of SL(2,R)#^62e5c4|Principal series representaition]], its even part is 
$$
H^{even}_{\xi}=\{f\in H_{\xi}\mid f(g)=f(-g)\}=\{\pi_{-I}f=f\}
$$
on the other side, the odd part of the [[Principal series representation of SL(2,R)#^62e5c4|Principal series representaition]] is 
$$
H^{odd}_{\xi}=\{f\in H_{\xi}\mid f(g)=-f(-g)\}=\{\pi(f)=-f\}
$$

There is more explicit construction of this two spaces that will be provided later.

