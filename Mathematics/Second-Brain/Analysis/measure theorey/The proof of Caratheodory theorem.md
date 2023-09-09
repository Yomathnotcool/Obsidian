# Tags
#measure-theory #notes #analysis 

---

### Thm :: Caratheodory theorem

^08973e

For a [[measure theory#^85e7d2|semi-algebra]] $\mathcal{S}\subset\mathcal{P}(\Omega)$ and a [[measure theory#^007702|additive]] set function $\mu$ defined on $\mathcal{S}$, then there is a unique extension $\nu$ of $\mu$ satisfying:
1. $\exists \nu:\mathcal{A}(\mathcal{S})\rightarrow \overline{\mathbb{R}_{\geq0}}$;
2. $\nu(A)=\mu(A),\ \forall A\in\mathcal{A}$;
3. $\mu_{1},\mu_{2}:\mathcal{A}(\mathcal{S}\rightarrow\overline{\mathbb{R}_{\geq0}})$ and  $\mu_{1}(A)=\mu_{2}(A),\forall A\in\mathcal{S}$ such that  $\forall E\in\mathcal{A}(\mathcal{S}), \mu_{1}(E)=\mu_{2}(E)$.

### Proof:
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



