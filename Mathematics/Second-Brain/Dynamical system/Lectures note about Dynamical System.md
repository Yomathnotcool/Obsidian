
## Tags
#dynamical-system #notes 

---

## Other related notes:
[[Dynamical System Course]]
[[Snapshot for dynamical system]]

---

### Def ::  Orbit:
The evolution of the system is described by the sequence:
$$\{T^{n}(x)|n\in \mathbb{N}_{\geq 0}\},$$
which is called the orbit of $x$.

### Def :: Fixed Point:
$x$ is a fixed point if $Tx=x$.

### Def :: Minimal:
A (topological) dynamical system is called minimal if all orbits are dense.

### Def :: Topological Transitive:

^7946a0

There is a dense orbit in the dynamical system.

## Def :: Periodic point

A point $x$ is periodic of period $n$ if $T^{n}x=x$.

## Ex :: [[Monotone Maps of Intervals]] 
## Ex :: [[Circle Rotation]]
## Ex :: [[Doubling Map]]
## Ex :: [[Shift map]]

[[Category Theory | Categorically]] speaking, an important tool to understand structure of dynamical system, we should get the information from another "simpler" system or get information from an equivalence class.

## Def :: Semiconjugacy and conjugacy

Given $X, Y$ two metric spaces with two continuous maps: $T: X\rightarrow X,\ S: Y\rightarrow Y$,
- A map $h:Y\rightarrow X$ is semiconjugacy from $S$ to $T$ if 
	- $$S\circ h = h\circ T$$
	- $h$ is continuous;
	- $h$ is surjective.
- If $h^{-1}$ exists and continuous, $h$ is called conjugacy between $S$ and $T$.



## Thm :: The properties keep by conjugacy:
- Periodic
- Topological transitive
- ergodicity



## Thm :: There exists semiconjugacy from the [[Shift map]] $S: \Omega_{2}\rightarrow \Omega_{2}$ to the [[Doubling Map]] $T:\mathbb{R}/\mathbb{Z}\rightarrow\mathbb{R}/\mathbb{Z}$. 



## Def :: Wandering point and Recurrent
Given $X$ compact metric space with $T: X\rightarrow X$ continuous map, 
- $x\in X$ is wandering if there exists an open neighbourhood $U$ of $x$, $T^{n}(U)\bigcap U=\emptyset$ for all $n\in \mathbb{N}$.
	- $W(T)$ as the set of wandering points
	-  $NW(T)$ as the set of non-wandering points 
- $x\in X$ is recurrent if there exists a sequence $n_{k}$ such that $T^{n_{k}}\rightarrow x$.
	- $R(T)$ as the set of recurrent points.



## Thm :: $W(T)$ is open and $R(T)\subset VW(T)$,



## Thm :: (Birkhoff) There exists a closed subset $Y\subset X$: $T(Y)\subset Y$, then $T:Y\rightarrow Y$ is minimal.
