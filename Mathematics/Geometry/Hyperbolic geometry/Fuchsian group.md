# Tags
#group #hyperbolic-geometry #dynamical-system #trace-formula #automorphic-forms 

---

# References
[Svetlana Katok - Fuchsian groups.pdf](hook://file/UKqzoIW8l?p=Z2VvbWV0cnkvSHlwZXJib2xpYyBnZW9tZXRyeQ==&n=Svetlana%20Katok%20%2D%20Fuchsian%20groups%2Epdf#p=16&x=0&y=0&s=537&e=564)

---


# Other related files


---

# $\text{PSL}_{2}$
Let's start with $\text{PSL}_{2}=\text{SL}_{2}/\{\pm1\}$, which is a [[topological group]].
## Classification of elements of $PSL_{2}(\mathbb{R})$
### Def :: Mobüis transformation
Given an element $g=\begin{pmatrix}a&b\\c&d\end{pmatrix}\in PSL_{2}{\mathbb{R}}$, the action of $g$ is called the Mobüis transformation: $$z\mapsto \frac{az+b}{cz+d}, $$
* Hyperbolic elements: $\text{Tr}(g)>2$, with two different real fixed points on $\mathbb{R}\bigcup\infty$, for those two points are called the attractive point and the repulsive point;
	And they are conjugate to matrix of form $$\begin{pmatrix}\lambda & 0 \\ \\ 0 & \lambda^{-1}\end{pmatrix}$$
* Elliptic elements: $\text{Tr}(g)=2$, with fixed points $z_{0}\in \mathbb{H}$ and $\bar{z_{0}}$;
	Conjugate to the matrix of form $$\begin{pmatrix}\cos(\theta)&\sin(\theta)\\ \\ -\sin(\theta)&\cos(\theta)\end{pmatrix}$$
* Parabolic elements: $\text{Tr}(g)<2$, with a unique fixed point $z_{0}\in \mathbb{R}\bigcup\infty$.
	Conjugate to the matrix $$\begin{pmatrix}1&\lambda\\ 0 &1\end{pmatrix}$$
### Rmk ::
 If $c=0$, then $\begin{pmatrix}a&b\\0&a^{-1}\end{pmatrix}$ which acts as $$\frac{az+b}{a^{-1}},$$
 then which gives the fixed point as $z=\frac{b}{a-a^{-1}}.$ If $a=1$, then the transformation becomes $z+b$, which has a fixed point $\infty$.

  
### Def :: Fuchsian group

A discrete subgroup of $\text{Isom}(\mathbb{H})$ is called Fuchsian group if it consists of orientation-persevering transformations, in other words, A Fuchsian group is a discrete subgroup of $\text{PSL}_{2}(\mathbb{R})$. 


