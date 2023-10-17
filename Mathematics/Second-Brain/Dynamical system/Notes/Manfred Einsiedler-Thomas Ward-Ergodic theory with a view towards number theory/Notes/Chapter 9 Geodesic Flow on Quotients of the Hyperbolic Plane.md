# Tags
#ergodic-theory #dynamical-system #number-theory #measure-theory 

---

# References


---


# Other related files


---






## The Hyperbolic Plane and the Isometric Action

### Thm :: hyperbolic metric
For any two points $z_{0},z_{1}\in\mathbb{H}$, there is a unique path $\phi:[0,\text{d}(z_{0},z_{1})]\rightarrow\mathbb{H}$ of unit speed with $\phi(0)=z_{0}$ and $\phi(\text{d}(z_{0},z_{1}))=z_{1}$.

## Def :: fundamental domain of $PSL_{2}(\mathbb{R})$
 $E=\{z\in\mathbb{H}||z|\geq1,|\mathfrak{R}(z)\leq \frac{1}{2}|\}$ 
$\mu(\gamma E\cap E)=0$ for $\gamma\in PSL_{2}\backslash\{Id\}$, and $\mathbb{H}=\bigcup_{\gamma}\gamma E$.


### Def :: Fuchsian group
A discrete subgroup $\Gamma\leq PSL_{2}(\mathbb{R})$

### Def :: Lattice
Discrete subgroup $\Gamma$ such that fundamental domain of $\Gamma\backslash PSL_{2}(\mathbb{R})$ is of finite area.

#### Def :: uniform lattice

^6d290e

If $\Gamma\backslash PSL_{2}(\mathbb{R})$ is compact.



### Thm :: Injective radius

^132adb
Proposition 9.14. Let $G$ be a closed linear group and $\Gamma \leqslant G$ a discrete subgroup. Then for any $x \in X=\Gamma \backslash G$ there exists some $r>0$ such that the map from
$$
B_r^G=\left\{g \in G \mid \mathrm{d}_G(g, e)<r\right\}
$$
to
$$
B_r^X(x)=\left\{y \in X \mid \mathrm{d}_X(x, y)<r\right\}
$$
defined by $g \mapsto x g$ is an isometry. For a compact subset $K \subseteq X$ we can choose $r>0$ so that the above property holds for all $x \in K$.
