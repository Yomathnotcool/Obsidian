# Tags
#notes #measure-theory #analysis

---

# References
[【测度论/Measure Theory】【IMPA】Measure Theory by Claudio Landim\_哔哩哔哩\_bilibili](https://www.bilibili.com/video/BV1EW411K7dN/?spm_id_from=333.1007.top_right_bar_window_default_collection.content.click&vd_source=b784936a1df86b94f46c299d99d457dc)


---


# Other related files


---
After knowing the natural length $\lambda((a,b]))=b-a$ of intervals $(a,b]$, naturally we want to generalise to all subsets of $\mathbb{R}$ with similar properties as usual length $\lambda$:
1. $\lambda((a,b])=b-a$;
2. $\lambda:\mathcal{P}(\mathbb{R})\rightarrow \mathbb{R}_{\geq0}\bigcup\{\infty\}$, in which $\mathcal{P}(\mathbb{R})$ is the power set of $\mathbb{R}$;
3. For any subset $A\subset \mathbb{R}$ and any $x\in \mathbb{R}$, $\lambda(A)=\lambda(A+x)$, in which $A+x=\{x+y|y\in A\}$.
4. $\lambda(\sqcup_{j}A_{j})=\sum\limits_{j}\lambda(A_{j})$. 

However, which is not possible due to the following theorem:
### Thm :: **non-measurable sets** exists.
#### Construction of non-measurable sets
Define an **Equivalence relation**： $x\sim y,\ x,y\in\mathbb{R}$ if $x-y\in\mathbb{Q}$.
Then we can pick one and only one representative element from every equivalence class $\mathbb{R}/\sim$ to collect them into set $\Omega\subset (0,1)$.


#### Claim: $\Omega$ is non-measurable.
$\lambda((0,1))=1>\lambda(\Omega)$, and we can prove that $\lambda(\Omega)=0$.
##### Claim: For any $p,q\in\mathbb{Q}$, either $\Omega+p=\Omega+q$ or $(\Omega+p)\bigcap(\Omega+q)=\emptyset$.
Assume $x\in(\Omega+p)\bigcap(\Omega+q)\not=\emptyset$. We can write $x=\alpha+p=\beta+q$ then $\alpha-\beta=q-p\in\mathbb{Q}$. 

Then we have the disjoint union $\lambda(\bigsqcup_{q\in\mathbb{Q}, -1<q<1}q+\Omega)\leq 3$, which gives us $\infty\cdot\lambda(q+\Omega)\leq3$. So $\lambda(q+\Omega)=0$. 
#### Claim: $(0,1)\subset\bigsqcup_{q\in\mathbb{Q},-1<q<1}(q+\Omega)$.
$\forall x\in(0,1)$, $\exists\alpha\in[x]\bigcap\Omega$, such that $\alpha\in(0,1)$. Then $\alpha-x=q\in(-1,1)\bigcap\mathbb{Q}$, $x=\alpha+q\in\Omega+q$.    

By this claim, we have that $\lambda(\bigsqcup_{q\in\mathbb{Q},-1<q<1}(q+\Omega))>1$, which contradicts to the earlier claim.

## Def :: Semi-algebra

^85e7d2

$S\subset\mathcal{P}(\Omega)$,
1. $\Omega\in S$;
2. $A,B\in S\Rightarrow A\bigcap B\in S$;
3. $A\in S\Rightarrow A^{c}=\bigsqcup^{n}_{i=1}E_{i}, \exists E_{i}\in S$.
### Ex :: $\Omega=\mathbb{R}$
$S=\bigg\{\{(a,b],a<b,a,b\in\mathbb{R}\},\{(\infty,b],\ b\in\mathbb{R}\},\{(a,+\infty),\ a\in\mathbb{R}\},\emptyset\bigg\}$ 
## Def :: algebra

^30d6ff

 $\mathcal{A}\subset\mathcal{P}(\Omega)$ an algebra
 1. $\Omega\in\mathcal{A}$;
 2. $A,B\in\mathcal{A}\Rightarrow A\bigcap B\in\mathcal{A}$;
 3. $A\in\mathcal{A}\Rightarrow A^{c}\in\mathcal{A}$.

### Rmk :: So clearly an algebra is a semi-algebra.

## Def :: $\sigma-$algebra
$\sigma-$algebra $\mathcal{F}\subset\mathcal{P}(\Omega)$:
1. $\Omega\in\mathcal{F}$;
2. $\{A_{j}\in\mathcal{F}\}_{j|\geq 1}$, such that  $\bigcap_{j\geq1}A_{j}\in\mathcal{F}$;
3. $A\in\mathcal{F}$,such that  $A^{c}\in\mathcal{F}$.

## Thm :: Given $\Omega$ and a family of ($\sigma-$)algebra $\{\mathcal{A}_{\alpha}\subset \mathcal{P}(\Omega)\}_{\alpha\in I}$, then $\mathcal{A}=\bigcap_{\alpha\in I}\mathcal{A}_{\alpha}$ is $(\sigma-)$algebra.

^b135ea


By this theorem, we can define algebra generated by semi-algebra(or a class of subsets):
## Def :: algebra generated by semi-algebra(or a class of subsets)

^76953f

Given $\Omega$ and $\mathcal{C}\subset\mathcal{P}(\Omega)$, the generated by a class of subset $\mathcal{C}\subset\mathcal{P}(\Omega)$, then the algebra $\mathcal{A}(\mathcal{C})$ generated by the class $\mathcal{C}$ is the smallest algebra containing $\mathcal{C}$:
1. $\mathcal{C}\subset\mathcal{A}(\mathcal{C})$;
2. $\forall$ ($\sigma-$)algebra $\mathcal{B}$ containing $\mathcal{C}$, $\mathcal{B}$ ($\sigma-$)algebra, such that  $\mathcal{A}(\mathcal{C})\subset\mathcal{B}$.

By the [[measure theory#^b135ea|theorem before]], it guarantees the existence of the generated algebra.

Similarly, we can define the algebra generated by [[measure theory#^85e7d2|semi-algebra]].
## Thm :: Given $\Omega$ and semi-algebra $\mathcal{S}\subset\mathcal{P}(\Omega)$, the algebra $\mathcal{A}(\mathcal{S})$ generated by $\mathcal{S}$, $A\in\mathcal{A}(\mathcal{S})$ if and only if $\exists E_{j}\in\mathcal{S}, 1\leq j\leq n, A=\bigsqcup^{n}_{j=1}E_{j}$.
### Proof:
$\Leftarrow$ $A=\bigsqcup^{n}_{j}E_{j}$, $E_{j}\in\mathcal{S}\subset\mathcal{A}(\mathcal{S})$, we need to show that $A\in\mathcal{A}(\mathcal{S})$.

For $E, F\in\mathcal{A}(\mathcal{S})$, then $E\bigcup F\in\mathcal{A}(\mathcal{S})$, since $E\bigcup F=(E^{c}\bigcap F^{c})^{c}$. 

$\Rightarrow$ $A\in\mathcal{A}(\mathcal{S})$, we need to show that $\exists E_{j}\in S,1\leq j\leq n,\ A=\bigsqcup^{n}_{j=1}E_{j}$.

The idea is for any $\mathcal{B}=\{\bigsqcup^{n}_{j}F_{j}|F_{j}\in\mathcal{S}\}\subset\mathcal{P}(\Omega)$, indeed $\mathcal{S}\subset \mathcal{B}$, we need to show that $\mathcal{B}$ is an algebra then by the definition of [[measure theory#^76953f|generated algebra]], $\mathcal{A}(\mathcal{S})\subset\mathcal{B}$.
Check the definitions:
1. $\Omega\in\mathcal{B}$;
2. $A,B\in\mathcal{B}$, such that  $A\bigcap B\in\mathcal{B}$;
	$A=\bigsqcup^{n}_{i}E_{i},\ E_{i}\in\mathcal{S}$ and $B=\bigsqcup^{m}_{j}F_{j},\ F_{j}\in\mathcal{S}$. 
	$A\bigcap B=(\bigsqcup^{n}_{i}E_{i})\bigcap(\bigsqcup^{m}_{j}F_{j})= \bigsqcup^{n}_{i}\bigsqcup^{m}_{j}(E_{j}\bigcap F_{i})$.
	By the definition of [[measure theory#^85e7d2|semi-algebra]], $E_{i}\bigcap F_{j}\in\mathcal{S}$. Then $A\bigcap B\in\mathcal{B}$.
3. $A\in\mathcal{B}$, such that $A^{c}\in\mathcal{B}$.
	$A=\bigsqcup^{n}_{i}E_{i}$, then $A^{c}=(\bigsqcup^{n}_{i}E_{i})^{c}=\bigcap^{n}_{i}E_{i}^{c}$.
	By the definition of [[measure theory#^85e7d2|semi-algebra]], $E_{i}^{c}=\bigsqcup^{l_{i}}_{k_{i}}E_{i,k}$ in which $E_{j,k}\in\mathcal{S}$.

## Def :: Additive set function

^007702

Given a class of subsets $\mathcal{C}\subset\mathcal{P}(\Omega)$ with $\emptyset\in\mathcal{C}$, a set function $$\mu:\mathcal{C}\rightarrow\mathbb{R}_{\geq0}\cup\{\infty\}$$ is called additive if 
1. $\mu(\emptyset)=0$;
2. $\mu(\bigsqcup^{n}_{i} E_{i})=\sum\limits^{n}_{i}\mu(E_{i})$.
### Thm :: Basic property of additive set function
1. proof of $\mu(\emptyset)=0$:
	$\exists A\in\mathcal{A}<\infty, A=A\cup\emptyset$ such that  $\mu(A)=\mu(A)+\mu(\emptyset)\Rightarrow \mu(\emptyset)=0$.
  2. $\mu(E)\leq\mu(F)$:
	  $E\subset F$ and $F\backslash E\in\mathcal{C}$:
	  * $\mu(E)<+\infty$:
		   $\mu(F\backslash E)=\mu(F)-\mu(E)$ such that  $\mu(E)\leq\mu(F)$.
	  * $\mu(E)=+\infty$:
		   $F=E\cup F\backslash E$ such that  $\mu(F)=\mu(E)+\mu(F\backslash E)$
		   Then $\mu(F)=+\infty$.

### Ex :: discrete measure
$\Omega=\{x_{j},j\geq1\}$ and a set of constants $\{P_{j}\geq0,j\geq 1\}$ 
$A\in\mathcal{C}$, $\mu(A)=\sum\limits_{j}P_{j}1_{A}$.

## Def :: $\sigma-$additive set function
Given a class of subsets $\mathcal{C}\subset\mathcal{P}(\Omega)$ with $\emptyset\in\mathcal{C}$, a set function $$\mu:\mathcal{C}\rightarrow\mathbb{R}_{\geq0}\cup\{\infty\}$$ is called $\sigma-$additive if 
1. $\mu(\emptyset)=0$;
2. $\{E_{j}\}_{j>0}\in\mathcal{C}$ such that  $E=\bigsqcup_{j>0}E_{j}\in\mathcal{C}$, $\mu(E)=\sum\limits_{j>0}\mu(E_{j})$.
### Ex :: additive but not $\sigma$-algebra

^994a94

$\Omega=(0,1)$
$\mathcal{C}=\{(a,b],0\leq a<b<1\}$
$\mu:\mathcal{C}\rightarrow\mathbb{R}_{\geq0}\cup\{+\infty\}$
$\mu((a,b])=\bigg\{\begin{array} +\infty,\ \ a=0\\ b-a,\ \ a>0\end{array}$  


As for a function, it is useful to define the "continuous":
## Def :: Continuous set function
$\mathcal{C}\subset \mathcal{P}(\Omega)$ a class of subsets
$\mu:\mathcal{C}\rightarrow\mathbb{R}_{\geq0}\bigcup\in\{\infty\}$.
1. $\mu$ is called continuous from below at $E\in\mathcal{C}$, if $\forall (E_{n})_{n\geq1}, E_{n}\in\mathcal{C}$ and $E_{n}\uparrow E$ (i.e. $E_{n}\subset E_{n+1},\ \bigcup_{n\geq1}E_{n}=E$), such that  $\mu(E_{n})\rightarrow \mu(E)$;
2. $\mu$ is called continuous from above at $E$ if $\forall (E_{n})_{n\geq1}, E_{n}\in\mathcal{C}$ and similarly $E_{n}\downarrow E$ (i.e. $E_{n+1}\subset E_{n}, \bigcap_{n\geq1} E_{n}=E$), $\exists n_{0},\ \mu(E_{n_{0}}<\infty)$, such that  $\mu(E_{n})\rightarrow \mu(E)$; 
3. $\mu$ is continuous if it's both from below and above.

### Ex :: why do we need $\exists n_{0},\ \mu(E_{n_{0}}<\infty)$?
$\Omega=\mathbb{R}$, $E_{n}=\{(a+n,\infty), \text{fixed}\ a\ \& \ n\in\mathbb{N}\}$ 
$\lim_{n}E_{n}=\emptyset$ but $\mu(\emptyset)=0$.



### Thm :: relation between $\sigma$-additive and continuous

^04d668

1. $\mu$ is $\sigma-$additive then $\mu$ is continuous at $\forall E\in\mathcal{A}$;
2. $\mu$ is continuous from below then $\mu$ is $\sigma-$additive;
3. $\mu$ is continuous from above at $\emptyset$ and finite then $\mu$ is $\sigma$-additive.

#### Proof:
1. $\mu$ is $\sigma-$additive then $\mu$ is continuous at $\forall E\in\mathcal{A}$;
	1. $\mu$ is $\sigma$-additive then $\mu$ is continuous from below.
		 For $E\in \Omega$ and the increasing sequence $E_{n}\uparrow E$, by this sequence, we can define $F_{1}=E_{1},\ F_{2}=E_{2}\backslash E_{1},....,F_{n}=E_{n}\backslash E_{n-1}$ which are disjoint and $\bigcup_{n\geq1}E_{n}=\bigsqcup_{k\geq1}F_{k}$. $\mu(E)=\sum\limits_{k}\mu(F_{k})=\lim_{k\rightarrow\infty}\sum\limits^{n}_{k=1}\mu(F_{k})=\lim_{n}\mu(\bigsqcup^{n}_{k}F_{k})=\lim_{n\rightarrow\infty}\mu(E_{n})$   
	2.  $\mu$ is $\sigma-$additive then $\mu$ is continuous from above.
		   Similarly we want to construct a sequence of sets $G_{1}=E_{n_{0}}\backslash E_{n_{0}+1},...,G_{k}=E_{n_{0}}\backslash E_{n_{0}+k}$ and this sequence $\mathcal{A}\ni G_{k}\uparrow E_{n_{0}}\backslash E$.  By 1, we have $\mu(G_{k}) \rightarrow \mu(E_{n_{0}}\backslash E)$.   And $\mu(E_{n_{o}}\backslash E)=\lim_{k\rightarrow \infty}\mu(E_{n_{0}}\backslash E_{n_{0}+k})$, since $\mu(E_{n_{0}})$ is finite, $\mu(E_{n_{0}})-\mu(E)=\mu(E_{n_{0}})-\lim_{k\rightarrow\infty}\mu(E_{n_{0}+k})$. $\mu(E)=\lim_{k\rightarrow\infty}\mu(E_{n_{0}+k})$.
2. $\mu$ is $\sigma-$additive if $\mu$ is continuous from below. 
		 $E=\bigsqcup_{k\geq1}E_{k},\  \  E, E_{k}\in\mathcal{A}$
		 $\bigsqcup^{n}_{k=1}E_{k}\subset E, \ \sum\limits^{n}_{k=1}\mu(E_{k})\leq \mu(E)$
		 we want to prove that $\sum\limits^{n}_{k=1}\mu(E_{k})\leq \mu(E),\ \forall n\in\mathbb{N}_{>0}$.
		 $F_{n}=\bigsqcup^{n}_{k=1}E_{k}\in\mathcal{A}$, this should give an increasing sequence $F_{n}\uparrow E$. By continuous from below, we have $\mu(F_{n})=\sum\limits^{n}_{k=1}\mu(E_{k})\rightarrow \mu(E)$.   
3. $\mu$ is finite if $\mu$ is continuous from above at $\emptyset$ and is finite.
	  $E_{k}, E\in\mathcal{A},\ E=\bigcup_{k\geq1}E_{k},$ Construct a decreasing subsets $F_{n}=\sum\limits_{k\geq n}E_{k}=E\backslash\sum\limits^{n-1}_{j=1}E_{j}\in\mathcal{A}$ then $F_{n}\downarrow\emptyset, \mu(F_{1})<\infty, \mu(F_{n})\rightarrow\infty$.     $\mu(E)=\mu((\bigcup^{n}_{k=1})\bigcup(\bigcup_{k>n}E_{k}))=\sum\limits^{n}_{k=1}\mu(E_{k})+\mu(F_{n+1})\rightarrow\sum\limits_{k\geq1}\mu(E_{k})$ 

#### Ex :: why do we need $\mu$ finite for [[measure theory#^04d668|the theorem above]]?
Considering the [[measure theory#^994a94|set function additive but not $\sigma-$additive]], define $E_{n}=(a_{n,1},b_{n,1}]\cup...\cup(a_{n,k},b_{n,k}]$ in which $a_{n,j}<a_{n,j+1}$ and $$\bigg\{\begin{array}  aa_{n,1}=0, \forall n\\ 
a_{n_{0},1}>0, \exists n_{0}, \mu(E_{n_{0}})<\infty\end{array}$$
It's not $\sigma-$additive because it's not finite. 

### Thm :: Caratheodory theorem
For a [[measure theory#^85e7d2|semi-algebra]] $\mathcal{S}\subset\mathcal{P}(\Omega)$ and a [[measure theory#^007702|additive]] set function $\mu$ defined on $\mathcal{S}$, then there is a unique extension $\nu$ of $\mu$ satisfying:
1. $\exists \nu:\mathcal{A}(\mathcal{S})\rightarrow \overline{\mathbb{R}_{\geq0}}$;
2. $\nu(A)=\mu(A),\ \forall A\in\mathcal{A}$;
3. $\mu_{1},\mu_{2}:\mathcal{A}(\mathcal{S}\rightarrow\overline{\mathbb{R}_{\geq0}})$ and  $\mu_{1}(A)=\mu_{2}(A),\forall A\in\mathcal{S}$ such that  $\forall E\in\mathcal{A}(\mathcal{S}), \mu_{1}(A)=\mu_{2}(A)$.
[[The proof of Caratheodory theorem]] 


#### Def :: outer measure

^36aaff

Given a class $\mathcal{C}\ni\emptyset\subset\mathcal{P}(\Omega)$, $\mu:\mathcal{C}\rightarrow\overline{\mathbb{R}_{\geq0}}$ satisfies:
1. $\mu(\emptyset)=0$;
2. If $E\subset F,\ E,F\in\mathcal{C}$, such that $\mu(E)\leq\mu(F)$;
3. $E,\ E_{i}\in\mathcal{C},\ E\subset \bigcup E_{i}$ such that  $\mu(E)\leq\sum\limits_{i}\mu(E_{i})$.





























### Def :: measure space 

^431c38

Given a measure space $(X,a,\mu)$: 
- $a$ is a $\sigma$-algebra: a collection of subsets of $X$ closed under complements countable unions, and countable intersections;
- $\mu$ a measure: $\mu:a\rightarrow [0,\infty]$ countably additive: $\forall A_{n}\in a, n\geq1, A_{n_{1}}\bigcup A_{n_{2}}=\emptyset$, in which $n_{1}\not= n_{2}$. And $\mu(\bigcup^{\infty}_{n=1})=\sum\limits^{\infty}_{n=1}\mu(A_{n})$.
- for probability measure, we assume $\mu(X)=1$.

### Thm :: extension of measure
- $\mathcal{B}$ an algebra;
- $a$ the smallest of $\sigma$-algebra containing algebra $\mathcal{B}$;
- $\mu:\mathcal{B}\rightarrow [0,\infty]$ a measure on algebra $\mathcal{B}$.
Then there exists a unique measure $\mu':a\rightarrow[0,\infty]$ extending $\mu$.

#### Ex :: Lebsegue measure
$X=\mathbb{R}$ and $\mathcal{B}=\{\bigcup^{l}_{i=1}[a_{i},b_{i})_\}$, the measure $\lambda([a_{i},b_{i}))=b_{i}-a_{i}$. Then the $\sigma-$algebra generated by $\mathcal{B}$ is the Borel $\sigma-$alegbra. We obtain the lebesgue measure.   ^03ea1a
