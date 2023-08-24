# Tags
#notes #dynamical-system 

---

# References


---


# Other related files


---
## Def :: circle homeomorphism
$T: \mathbb{R}/\mathbb{Z}\rightarrow\mathbb{R}/\mathbb{Z}$ is a group homeomorphism

### Ex :: [[Circle Rotation]] 
$T_{\alpha}:x\mapsto(x+\alpha)(\mod 1)$, for $\alpha\not\in\mathbb{Q}$, $T_{\alpha}$ is [[Lectures note about Dynamical System#^e0379f|topological transitive]].

### Ex :: Monotone interval map
For the circle $\mathbb{R}/\mathbb{Z}$, it can be divided into unions of intervals $I_{1},I_{2},I_{3}$, here are the interval exchange: $$ T_{1}: I_{1}\rightarrow I_{2}, T_{2}:I_{2}\rightarrow I_{3}, T_{3}: I_{3}\rightarrow I_{1}$$
Then $T^{3}:=T_{1}\sqcup T_{2}\sqcup T_{3}: I_{k}\rightarrow I_{k+1(\mod 3)}$ monotone interval map endpoints are periodic.



## Def :: Lift of continuous circle homeomorphism
A continuous $F:\mathbb{R}\rightarrow\mathbb{R}$ is a lift of $T$ if ![[Pasted image 20230819103128.png]]
In the diagram, $T$ is a continuous homeomorphism and $\pi:\mathbb{R}\rightarrow\mathbb{R}/\mathbb{Z}:x\mapsto.x(\mod1)$.


## Thm :: 
1. Lifts exist;
2. If $F_{1}$ and $F_{2}$ are lifts, $F_{1}=F_{2}+k$ for $k\in\mathbb{Z}$. 


## Def ::
$\exists k\in\mathbb{Z}:\forall x\in\mathbb{R}:F(x+1)-F(x)=k$, this $k$ is called the degree of $T.$

### Rmk :: $T$ is a homeomorphism if and only if $\text{deg}(T)=\pm 1$.

## Lem :: $a_{n}(x)=F^{n}(x)-x$

^ec5645

1. $\forall x,y\in\mathbb{R}:|a_{n}(x)-a_{n}(y)|<1$;
2. $\forall x\in\mathbb{R}:a_{n+m}(x)\leq a_{n}(x)+a_{m}(x)+1$;
3. $\lim_{n\rightarrow} \frac{a_{n}(x)}{n}$ exists.


## Def :: The rotation number of $T$ 
The rotation number of $T$ is 
$$\rho(T)=\lim_{n\rightarrow\infty}\frac{F^{n}(x)}{n}(\mod 1).$$
### Rmk :: rotation number doesn't depend on the choice of lift and $x$.
1. By [[Circle homeomorphism#^ec5645|lemma above]], $\rho(T)$ does not depend on $x$. 
2. If $G$ is another lift of $T$, then $G=F+k$ for $k\in\mathbb{Z}$. So $G^{2}=G(F+k)=F^{2}+2k$ and by induction $G^{n}=F^{n}+nk$. Hence $\lim_{n\rightarrow\infty}\frac{G^{n}(x)}{n}=\lim_{n\rightarrow\infty}\frac{F^{n}(x)}{n}+k$. This shows that $\rho(T)$ doesn't depend on the choice of the lift.


## Ex :: examples of rotations
1. For $T:x\mapsto (x+\alpha)(\mod 1)$, $F(x)=x+\alpha$ is a lift, and $\rho(T)=\alpha$.
2. If $T$ has a fixed point, for the lift we get: $F(x_{0})=x_{0}+k$ for some $k\in\mathbb{Z}$ Then $$\lim_{n\rightarrow\infty}\frac{F^{n}(x_{0})}{n}(\mod 1) = k(\mod 1)=0,$$ so $\rho(T)=0$.
3. $\forall l\in\mathbb{N}:\rho(T^{l})=l\cdot\rho(T)$;
4. If $T$ has a periodic point, then $\rho(T)$ is rational.


## Thm :: $\rho(T)$ rational if and only if $T$ has periodic points.




## Thm :: (Poincare) Let $\rho=\rho(T)\not\in\mathbb{R}\backslash\mathbb{Q}$. There exists semiconjugacy from $T$ to the rotation $T_{\rho}$:
![[Pasted image 20230821141245.png]]
If $T$ is topologically transitive, this is a conjugacy.


## Ex :: Denjoy example:
$\forall\rho\in\mathbb{R}\backslash\mathbb{Q}$, there exists non-transitive homeomorphism $T:\mathbb{R}/\mathbb{Z}\rightarrow\mathbb{R}/\mathbb{Z}$ with $\rho(T)=\rho$,
1. Take the circle rotation $T_{\rho}$;
2. Fix $x$ and cut at all $T^{n}_{\rho}(x)$;
3. Take intervals $I_{n}$ with $\sum\limits_{n\in\mathbb{Z}}|I_{n}|<\infty$. And homeomorphisms $\psi_{n}:I_{n}\rightarrow I_{n+1}$;
4. Glue $I_{n}$ at $T^{n}_{\rho}(x)$;
5. Define $T$ by: $$\psi_{n}:I_{n}\rightarrow I_{n+1},T_{\rho}:\mathbb{R}/\mathbb{Z}\rightarrow\mathbb{R}/\mathbb{Z}$$
![[Pasted image 20230821142412.png]]
### Thm :: (Denjoy)
* there exists such $C^{1}$ map;
* every $C^{2}$ map with $\rho(T)\not\in\mathbb{Q}$ is topological transitive.


## Thm :: A circle homeomorphism $T:X\rightarrow X$ with degree 1 without periodic points, then $T$ is [[Lectures note about ergodic theory#^56e37e|uniquely ergodic]].

^93b97b

