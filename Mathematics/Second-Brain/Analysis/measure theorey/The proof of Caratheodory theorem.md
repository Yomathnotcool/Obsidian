# Tags
#measure-theory #notes #analysis 

---

### Thm :: Caratheodory theorem

^08973e

For a [[measure theory#^85e7d2|semi-algebra]] $\mathcal{S}\subset\mathcal{P}(\Omega)$ and a [[measure theory#^007702|additive]] set function $\mu$ defined on $\mathcal{S}$, then there is a unique extension $\nu$ of $\mu$ satisfying:
1. $\exists \nu:\mathcal{A}(\mathcal{S})\rightarrow \overline{\mathbb{R}_{\geq0}}$;
2. $\nu(A)=\mu(A),\ \forall A\in\mathcal{A}$;
3. $\mu_{1},\mu_{2}:\mathcal{A}(\mathcal{S}\rightarrow\overline{\mathbb{R}_{\geq0}})$ and  $\mu_{1}(A)=\mu_{2}(A),\forall A\in\mathcal{S}$ such that  $\forall E\in\mathcal{A}(\mathcal{S}), \mu_{1}(E)=\mu_{2}(E)$.

#### Proof:
$A\in\mathcal{A}(\mathcal{S})$ such that  $A=\bigsqcup^{n}_{j=1}E_{j},\ E_{j}\in\mathcal{S}$ by the definition of [[measure theory#^85e7d2|semi-algebra]].

By additive assumption and the definition of extension, we want the extension to be $$\nu(A)=\sum\limits^{n}_{j=1}\nu(E_{j})=\sum\limits^{n}_{j=1}\mu(E_{j}),$$
Now we need to show that
1. $\nu$ is well-defined:
	i.e. if $A=\bigsqcup^{n}_{j=1}E_{j}=\bigsqcup^{m}_{k=1}F_{k}$, then $\nu(A)=\sum\limits^{n}_{j=1}\mu(E_{j})=\sum\limits^{m}_{k}\mu(F_{k})$.
	then $E_{j}\cap A=E_{j}\bigcap\bigsqcup^{m}_{k}F_{k}=\bigsqcup^{m}_{k}E_{j}\cap F_{k}$ which shows that $\mu(E_{j})=\sum\limits^{m}_{k=1}\mu(E_{j}\cap F_{k})$. So $\nu(A)=\sum\limits^{n}_{j=1}(E_{j})=\sum\limits^{n}_{j=1}\sum\limits^{m}_{k=1}\mu(E_{j}\cap F_{k})$. Similarly explanation for $F_{k}$.
2. $\nu$ is additive;
	i.e. $\forall A\cap B=\emptyset\in\mathcal{A}(\mathcal{S}), \nu(A\sqcup B)=\nu(A)+\nu(B)$, in which $A=\bigsqcup^{n}_{j=1}E_{j},\ B=\bigsqcup^{m}_{k=1}F_{k},\ E_{j}, F_{k}\in\mathcal{S}$.
	$\nu(A\sqcup B)=\nu(\bigsqcup^{n}_{j=1}E_{j}\sqcup\bigsqcup^{m}_{k=1}F_{k})=\sum\limits^{m}_{k=1}\mu(F_{k})+\sum\limits^{n}_{j=1}\mu(E_{j})=\nu(A)+\nu(B).$
3. $\nu(A)=\mu(A),\ A\in\mathcal{S}$ indeed an extension.
4. Uniqueness: $\mu_{1},\mu_{2}:\mathcal{A}(\mathcal{S}\rightarrow\overline{\mathbb{R}_{\geq0}})$ and  $\mu_{1}(A)=\mu_{2}(A),\forall A\in\mathcal{S}$ such that  $\forall E\in\mathcal{A}(\mathcal{S}), \mu_{1}(E)=\mu_{2}(E)$.
	$E\in\mathcal{A}(\mathcal{S}),\ E=\bigsqcup^{n}_{j=1}E_{j},\ E_{j}\in\mathcal{S},$ so $\mu_{1}(E)=\sum\limits^{n}_{j=1}\mu_{1}(E_{j})=\sum\limits^{n}_{j=1}\mu_{2}(E_{j})=\mu_{2}(E).$ 
5. If $\mu$ is $\sigma-$additive, then $\nu$ is $\sigma-$additive.
	i.e. for $A,A_{j}\in\mathcal{A}(\mathcal{S})$ and $A=\bigsqcup_{j\geq 1}A_{j}$, in which $A_{j}=\bigsqcup^{m_{k}}_{l=1}E_{k_{l}},\ A=\bigsqcup^{n}_{j=1}E_{j},\ E_{j},E_{k_{l}}\in\mathcal{S}$, show that $\nu(A)=\sum\limits_{j=1}\nu(A_{j})$.
	$\nu(A)=\sum\limits^{n}_{j=1}\mu(E_{j})$, in which $E_{j}=\bigsqcup_{k\geq1}\bigsqcup^{m_{k}}_{l=1}E_{j}\cap E_{k_{l}}$. So $\nu(A)=\sum\limits^{n}_{j}\sum\limits_{k\geq1}\sum\limits^{m_{k}}_{l=1}\mu(E_{j}\cap E_{k_{l}})=\sum\limits_{k\geq1}\sum\limits^{m_{k}}_{l=1}\mu(E_{k_{l}})$. And $\nu(A_{k})=\sum\limits^{m_{k}}_{l=1}\mu(E_{k_{l}})$. This proves the $\sigma-$additive.

The [[The proof of Caratheodory theorem#^08973e| theorem]] can be further extended:
![[Pasted image 20230909134939.png]]

In order to construct the extension $\pi$, we can construct the [[measure theory#^36aaff|outer measure]] $\pi^{*}:\mathcal{P}(\Omega)\rightarrow \overline{\mathbb{R}_{\geq0}}$, for a class of subset $\mathcal{M}\subset\mathcal{P}(\Omega)$, it satifies:
1. it's $\sigma-$algebra;
2. $\mathcal{A}\subset\mathcal{M}$;
3. $\pi^{*}|_{\mathcal{M}}$ is $\sigma-$additive;
4. $\pi^{*}|_{\mathcal{A}}=\nu$.
And $\pi^{*}$ is constructed as $A\subset\Omega,\ \pi^{*}(A)=\text{inf}_{\{E_{i}\}}\sum\limits_{i\geq1}\nu(E_{i})$ in which $\{E_{i}|i\geq1\}\subset\mathcal{A}$ and $A\subset\bigcup_{i\geq1}E_{i}$.

##### Step1
##### Thm :: $\pi^{*}$ is a outer measure.
1. $\pi^{*}(\emptyset)=0$;
	1. $E_{i}=\emptyset,\ \{E_{i}\}=\{\emptyset\},\pi^{*}(\emptyset)\leq\sum\limits_{i\geq1}\nu(E_{i})$;
	2. $E_{i}\in\mathcal{A},\ \emptyset\subset\bigcup E_{i},\ \sum\limits_{i\geq1}\nu(E_{i})\geq0$, then $\pi^{*}(\emptyset)\geq0$.
2. $E\subset F,\ \pi^{*}(E)\leq \pi^{*}(F)$;
	For a family of subsets $\{E_{i}\}$, $E_{i}\in\mathcal{A}$, $F_{i}\subset E_{i}$, and any covering of $F_{i}$ covers of $E$. Then $\pi^{*}(E)\leq\pi^{*}(F)$.
3. $E\subset \bigcup_{i\geq1}E_{i},\ \pi^{*}(E)\leq\sum\limits_{i\geq 1}\pi^{*}(E_{i})$.
	1. $\pi^{*}(E_{i})=\infty$, it's trivial;
	2. $\pi^{*}<\infty$, $\pi^{*}(E_{i})=\text{inf}_{E_{i}\subset\{H_{k}\}}\sum\limits_{k\geq1}\nu(H_{k})<\infty$.
			$\exists \{H_{i,k}\},\ H_{i,k}\in\mathcal{A},\ E_{i}\subset \bigcup_{k\geq1}H_{i,k}$. $\pi^{*}(E_{i})\leq \sum\limits_{k\geq1}\nu(H_{i,k})\leq\pi^{*}+ \frac{\epsilon}{2^{i}}$ and $\pi^{*}(E)\leq\sum\limits_{i,k}\nu(H_{i,k})\leq\sum\limits_{i\geq1}(\pi^{*}(E_{i})+ \frac{\epsilon}{2^{i}})=\sum\limits_{i\geq1}\pi^{*}(E_{i})+\epsilon$
##### Step2
##### Thm :: $\mathcal{M}$ measurable subsets, for $A\in\mathcal{A}$, $A\in\mathcal{M}$ if $\forall E\subset\Omega, \pi^{*}(E)=\pi^{*}(E\cap A^{c})+\pi^{*}(E\cap A^{c})$. Then $\mathcal{A}\subset\mathcal{M}$ is a $\sigma$-algebra.
In order to prove the equality, 
1. $\mathcal{A}\subset\mathcal{M}$:
	1. $\pi^{*}(E)\leq\pi^{*}(E\bigcap A)+\pi^{*}(E\bigcap A^{c})$ 
			since $E\subset (E\bigcap A)\bigcup(E\bigcap A^{c})$.
	2. $\pi^{*}(E)\geq\pi^{*}(E\bigcap A)+\pi^{*}(E\bigcap A^{c})$ :
			If $\pi^{*}(E)=\infty$, then it's trivial. Let's prove if $\pi^{*}(E)<\infty$. Fix $\epsilon>0$ and there is a covering $\{E_{i}\in\mathcal{A}\}$ of $E$, $\pi^{*}(E)\leq\sum\limits_{i\geq1}\nu(E_{i})\leq\pi^{*}(E)+\epsilon$. $E_{i}\cap A\in\mathcal{A}$ by the definition of [[measure theory#^30d6ff|algebra]], then $E\cap A\subset \bigcup_{i\geq 1}(E_{i}\bigcap A)$ such that  $\pi^{*}(E\cap A)\leq \sum\limits_{i\geq1}\nu(E_{i}\cap A)$ and similarly $\pi^{*}(E\cap A^{c})\leq\sum\limits_{i\geq1}\nu(E_{i}\cap A^{c})$. By adding together, $\begin{array}&&\pi^{*}(E\cap A)+\pi^{*}(E\cap A^{c})\\ &\leq\sum\limits_{i\geq1}(\nu(E_{i}\cap A)+\nu(E_{i}\cap A^{c}))\\ &=\sum\limits_{i\geq1}\nu(E_{i})\leq\pi^{*}(E)+\epsilon.\end{array}$ 
2. $\mathcal{M}$ is a $\sigma-$algebra:
	1. 

