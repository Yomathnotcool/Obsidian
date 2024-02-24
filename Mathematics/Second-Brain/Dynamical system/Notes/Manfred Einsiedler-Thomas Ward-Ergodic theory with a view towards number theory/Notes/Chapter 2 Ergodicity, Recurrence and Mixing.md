# Tags
#dynamical-system #measure-theory 

---

# References


---


# Other related files


---


### Thm :: Poincaré recurrence theorem
*Expect for a measure set, otherwise it will always return*
Let $T:X \to X$ be a [[Lectures note about Dynamical System#^3ec847|measure-persevering transformation]] on a probability space $(X,\mathcal{B},\mu)$, and let $E\subset X$ be measurable subset. Then almost every point $x \in E$ returns to $E$ infinitely often. That is, there exists a measurable subset $F \subset E$ with $\mu(F)=\mu(E)$ with the property that every $x \in F$ there exists integers $0<n_{1}<n_{2}<\dots$ with $T^{n_{i}}\in E$ for all $i$.





### Thm :: Birkhoff ergodicity theorem

For a measure-persevering system $(X,\mathcal{B},\mu)$, if $f\in L^{1}_{\mu}$, then $$
\lim\limits_{ n \to \infty } \frac{1}{n} \sum\limits^{n-1}_{j=0}f(T^{j}x)=f^{*}(x)
$$
converges almost everywhere in $L^{1}_{\mu}$ to a $T$-invariant function $f^{*}\in L^{1}_{\mu}$ and $$
\int f^{*}\,d\mu=\int f\,d\mu.
$$
If $T$ is ergodic, then $f^{*}=\int f\,d\mu$ almost everywhere.






















### Thm :: Poincaré recurrence theorem
There exits a measurable set $E\subset X$ of measure zero, then for any $x \in E$, for any $n\geq 1$, $R_{a_{t}}^{n}\not\in E$. 
