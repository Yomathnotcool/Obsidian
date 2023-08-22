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