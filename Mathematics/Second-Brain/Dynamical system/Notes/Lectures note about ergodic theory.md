# Tags
#dynamical-system #notes #ergodic-theory #measure-theory 

---

# References


---


# Other related files


---

Given a [[measure theory#^431c38|measure space]] $(X,a,\mu)$ with $\mu$ a probability measure, and $T:X\rightarrow X$ a measure-preserving transformation,
# Ergodic measures
## Def :: Ergodic

^d8b2bc

The transformation $T$ above is called ergodic if $\forall A\in a$, such that $T^{-1}(A)=A$ then $\mu(A)=0$ or $=1$.

### Rmk :: All subsets that are invariant under the transformation are of trivial measure.
### Rmk :: If $T^{-1}(A)=A$, then $T:A\rightarrow A$, then $T:A\rightarrow A$ and $T:X\backslash A\rightarrow X\backslash A$.

## Thm :: Other equivalent definitions of ergodic
1. $T$ is ergodic;
2. $\forall A\in a: \mu(T^{-1}(A)\Delta A)=0$, then $\mu(A)=0$ or $=1$.
3. For any measurable $f:X\rightarrow \mathbb{R}$, if $f$ is invariant under the transformation $T$, i.e. $f(Tx)=f(x)$ almost everywhere, then $f$ is a constant almost everywhere.


## Def :: Mixing

^3b262f

$T$ is mixing if $\forall A, B\in a: \mu(T^{-n}(A)\bigcap B)\rightarrow B\rightarrow \mu(A)\mu(B)$.

## Thm :: other equivalent definition of mixing
$T$ is mixing if and only if $\forall f,g \in L^{2}(X): \int_{X}f(T^{n}x)g(x)\text{d}\mu(x)\rightarrow\int_{X}f\text{d}\mu\int_{X}g\text{d}\mu$.


The relation between mixing and ergodic is given as 
## Thm :: mixing $\Rightarrow$ erogidc


### Ex :: [[Circle Rotation#^0bb64c|Rational rotation is not ergodic, but the irrational rotation is ergodic but not mixing.]]

## Ex :: [[Doubling Map#^0b208e|Doubling map is mixing]]



# Ergodic Theorems

The setting: $(X,a,\mu)$ measure space, $\mu(X)=1$, $T$ measure preserving and $f:X\rightarrow \mathbb{R}$ measurable.

Considering the time average $$A_{N}(f)(x)=\frac{1}{N}\sum\limits^{N-1}_{n=0}f(T^{n}x)$$
## Thm :: mean ergodic theorem
For any $f\in L^{2}(X): ||A_{N}(f)-P(f)||_{2}\rightarrow 0$, where $P$ Is orthogonal projection on the space of $T$-invariant functions.

