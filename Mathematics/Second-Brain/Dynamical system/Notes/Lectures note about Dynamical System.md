
## Tags
#dynamical-system #notes 

---

## Other related notes:
[[Dynamical System Course]]
[[Snapshot for dynamical system]]

---

# Perliminares

### Def ::  Orbit:

The evolution of the system is described by the sequence:
$$\{T^{n}(x)|n\in \mathbb{N}_{\geq 0}\},$$
which is called the orbit of $x$.


### Def of fixed point:
$x$ is a fixed point if $Tx=x$.

### Def of minimal:
A (topological) dynamical system is called minimal if all orbits are dense.

### Def of topological transitive:
There is a dense orbit in the dynamical system.



### Def :: Fixed Point:
$x$ is a fixed point if $Tx=x$.

### Def :: Minimal:
A (topological) dynamical system is called minimal if all orbits are dense.

### Def :: Topological Transitive:

^7946a0

There is a dense orbit in the dynamical system.

## Def :: Periodic point
A point $x$ is periodic of period $n$ if $T^{n}x=x$.

### Def :: topological mixing

^cba4af

A  dynamical system $T$ on space $X$ is called topological mixing if for any two open subsets $U, V\subset X$, there exists a $N$ for any $n>N$ such that $T^{n}(U)\bigcap V\not=\emptyset$.

https://i.stack.imgur.com/1hMNx.png

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
- Topological transitive ^e0379f
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






## Def :: uniformly recurrent (almost periodic)

^88fab3

A point $x\in X$ is uniformly recurrent (or almost periodic) if $\forall \epsilon>0: \exists n_{k}\rightarrow \infty: d(T^{n_{k}},x)<\epsilon$, in which $\text{sup}_{k}(n_{k+1}-n_{k})<\infty$.

### Example
- [[Circle Rotation#^8903ec]]
- [[Doubling Map#^203fe9]]

A direct question from the definition: uniformly recurrent but not periodic point for $S:\prod^{\infty}_{i\geq1}\{0,1\}\rightarrow \prod^{\infty}_{i\geq 1}\{0,1\}$ ?
### Ex :: [[Thue-Morse sequence]]






### Thm :: A point $x$ is uniformly recurrent if and only if $\overline{\{T^{n}:n\geq 0\}}$ is minimal.


### Ex :: [[toral automorphism]]



### Ex :: [[circle homeomorphism]]

### Ex :: [continued fractions]


# Measurable Dynamics

More information about [measure theory].

### Def :: measurable transformation
$T:X\rightarrow X$ is called measurable transformation if $\forall A\in a: T^{-1}(A)\in a$.

### Def :: measure-preserving transformation

^3ec847

a measurable $T:X\rightarrow X$ is measure-preserving if $\forall A\in a:\mu(T^{-1}(A))=\mu(A)$.

#### Ex :: periodic orbits
Suppose that $T^{n}x=x$. Let $\mu(A)=|\{n=0,..,n-1:T^{n}x\in A\}|$, $$\mu^{-1}(A)=|\{n=0,...,n-1:T^{n}\in T^{-1}(A)\}|=|\{n=0,...,n-1:T^{n+1}x\in A\}|=\mu(A).$$
Hence, $\mu$ is $T$-invariant.

#### Ex :: [[Doubling Map#^e53326|Doubling map is measure preserving.]] 

#### Ex :: [[Gauss map#^416b99|Gauss map is measure preserving]]

#### Ex :: [[toral automorphism#^93f4ca|Torus automorphsim is measure preserving]]


### Thm :: $\mu$ is $T$-invariant if and only if $\forall f\in L^{1}(X,\mu): \int_{X}f(T(x))\text{d}\mu(x)=\int f \text{d}\mu$.


### Thm :: Poincare Recurrence theorem

$T:(X,\mu)\rightarrow(X,\mu)$ measure preserving then for any $A\subset X$ with $\mu(A)>0$, such that for almost every $x\in A, \exists n\geq 1: T^{n}x\in A$.
![[Pasted image 20230821153415.png]]


