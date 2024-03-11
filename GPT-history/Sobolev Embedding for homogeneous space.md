Define a function $\omega$ on space $X$ a weight if it is a positve meaurble function and for every $g \in G$, there exists a constant $C(g)$ such that  $$
\omega(xg)\leq C(g)\omega(x)

$$
for all $x \in X$. We assume $C(g)$ is locally bounded.

For homogeneous spaces, $X=\Gamma \backslash G$, in which $G$ is any Lie group and $\Gamma$ is the lattice of $G$. Measure on $X$ is induced by a left-$G$-Haar measure and introduce $L^{2}$ and Sobolev norm on the space $C^{\infty}(X)$ of smooth functions on $X$.
Fixed a ball $B \subset G$ which is a compact symmetric neighborhood of $e \in G$, for every point $x \in X$, we consider the map $p_{x}: B \to X$ given by $$
g \to  xg.
$$
The map induces the morphism of HIlbert spaces $$
p^{*}_{x}:L^{2}(X) \to  L^{2}(B),
$$
which is defined as 
how do we define the norm of $p^{*}(x)$?

Given the context of homogeneous spaces $X = \Gamma \backslash G$, where $G$ is a Lie group and $\Gamma$ a lattice in $G$, along with a suitable treatment of $L^2$ spaces and Sobolev norms on $C^\infty(X)$, your query revolves around defining the norm of the morphism $p_x^*: L^2(X) \to L^2(B)$induced by the map $p_x: B \to X$, defined as $g \to xg$. Let's delve into the details of defining the norm of this induced morphism in the rigorously mathematical manner of a mathematics professor.

To define the norm of the operator $p_x^*$, we consider it as a linear operator between Hilbert spaces. The operator norm $\|\cdot\|$ of a linear operator $T: H_1 \to H_2$ between two Hilbert spaces $H_1$ and $H_2$ is defined as follows: $$  
\|T\| = \sup \{\|Tf\|_{H_2} \, : \, f \in H_1, \|f\|_{H_1} = 1\}.  
$$ In simpler terms, it is the supremum of the norms of the images under $T$ of all unit vectors in $H_1$. This definition encapsulates the maximal "stretching" effect the operator $T$has on vectors in $H_1$.

Applying this to our specific case, $p_x^*$ as an operator from $L^2(X)$ to $L^2(B)$, can be understood as follows:

- For $f \in L^2(X)$, $p_x^* f = f \circ p_x^{-1}$ maps functions on $X$ to functions on $B$.
- The $L^2$-norms in question are induced respectively by the measures on $X$ and $B$. Let's denote $\mu_X$ as the measure on $X$ induced by a left-$G$-Haar measure on $G$, and $\mu_B$ as the measure on $B$ (typically the restriction of the Haar measure on $G$ to the subset $B$).

Accordingly, the norm of a function $f \in L^2(X)$ is given by $\|f\|_{L^2(X)} = \left(\int_X |f(x)|^2 \, d\mu_X(x) \right)^{1/2}$, and similarly for $L^2(B)$.

Thus, the norm of the operator $p_x^*$ can be expressed as: $$  
\|p_x^*\| = \sup \left\{\|p_x^*f\|_{L^2(B)} \, : \, f \in L^2(X), \|f\|_{L^2(X)} = 1\right\},  
$$ where $\|p_x^*f\|_{L^2(B)} = \left(\int_B |f(p_x^{-1}(g))|^2 \, d\mu_B(g) \right)^{1/2}$.

In the context of homogeneous spaces and the action by the group $G$, this norm reflects how the measure and structure of the space $X$ influence the translation of the $L^2$ norm from $X$ to the local setting in a neighborhood $B$ around the identity $e$ in $G$ through the action of $G$ on $X$. Importantly, this construction is meaningful due to the homogeneous nature of $X$; the local geometry around any point in $X$ is uniformly related to the geometry of $G$, modulo the lattice $\Gamma$. This allows for meaningful definitions and computations of operator norms such as $\|p_x^*\|$.


now denote $\omega(x)$ as the norm of $p^{*}_{x}$.


How to describe the fiber of $p_{x}$ explicitly? and what is the cardinality of the fibers?
The map $p_x: B \to X$ given by $g \mapsto xg$, where $X = \Gamma \backslash G$ is a homogeneous space, projects elements of a compact symmetric neighborhood $B \subset G$of the identity $e$ in the Lie group $G$ onto $X$. To describe the fibers of $p_x$ and their cardinality, let's explore the structure of this mapping in more detail.

### Understanding The Fibers of $p_x$

For any point $y = xg \in X$, where $g \in B$, the fiber $p_x^{-1}(y)$ consists of all elements $g' \in B$ such that $xg' = y$. Since $y = xg$, this means we are looking for all $g' \in B$ for which $xg' = xg$.

Given the definition of $X$ as the quotient $\Gamma \backslash G$, two elements $xg'$ and $xg$ in $X$ are considered the same if there exists a $\gamma \in \Gamma$ such that $xg' = xg\gamma$. This implies that $g' = g\gamma$ due to the cancellation of $x$ (noting that elements of $X$ are cosets $\Gamma g$).

Therefore, the fiber above $y$ can be described as all elements in $B$ that can be represented as $g\gamma$ for some $\gamma \in \Gamma$ that satisfies both $g, g\gamma \in B$.

### Cardinality of The Fibers

The cardinality of each fiber $p_x^{-1}(y)$ depends on the intersection of $\Gamma$ with the inverse image of $B$ through the action by $g$. Specifically, it counts the number of $\gamma \in \Gamma$ such that $g\gamma \in B$. Because $B$ is a compact (and thus bounded) neighborhood of $e$ and $\Gamma$ is a lattice in $G$, the intersection of $\Gamma$ with small enough neighborhoods around any point in $G$ is finite. However, the exact cardinality can vary based on the specific choice of $x$, $y$, and $B$.

In typical scenarios for Lie groups $G$ and lattices $\Gamma$, one main case to consider is when $B$ is small enough that for any $g \in B$, the set $\{ \gamma \in \Gamma : g\gamma \in B\}$is either empty or consists of a very small finite number of elements from $\Gamma$. The experienced cardinality is closely related to how densely $\Gamma$ sits in $G$ and the size of $B$ relative to this density.

For sufficiently small $B$, one might often find that the cardinality of the fibers is either $0$ or $1$, mirroring the fact that $B$ does not "wrap around" in $G$ significantly enough to intersect the same lattice points multiple times. However, as $B$ grows, or depending on the structure of $G$ and the distribution of $\Gamma$ within $G$, cardinalities greater than $1$ can occur, signifying the wrapping of $B$ over multiple lattice points.

This exploration relies on understanding the geometric and algebraic structure of $G$, $\Gamma$, and the definition of $B$. Precise cardinality calculations require deeper analysis of these entities.

we denote the fiber as $$
F_{g_{0}}(x)=\{g\in B\mid p_{x}(g)=\Gamma g_{0}\}
$$
and based on your explanation: 
$$
\begin{align}
p_{x}(g)=x\Gamma g=\Gamma g_{0} \\
\forall g \in F_{g_{0}}(x), p_{x}(g)=\Gamma g_{0} \iff x\Gamma g=\Gamma g_{0}\\
\end{align}
$$
so $$
F_{g_{0}}(x)=\{g\in B\mid x\Gamma g=\Gamma g_{0}\}
$$
Then when we consider the cardinality of the fiber $$
\lvert F_{g_{0}}(x) \rvert = \lvert \{\gamma \in \Gamma \mid \ \text{for any}\ g \in B,\exists \gamma \in \Gamma\ \text{such that }\ x\gamma g=g_{0}\} \rvert 
$$
now we want to show that $$
\lvert F_{g_{0}}(xh) \rvert \leq C(h) F_{g_{0}}(x) 
$$
in which $C(h)$ is a constant.

in which $$
F_{g_{0}}(xh)=\{\gamma \in \Gamma \mid \text{for any}\ g \in B,\exists \gamma \in \Gamma\ \text{such that } xh\gamma g=g_{0}\}
$$
To establish the relationship $$  
\lvert F_{g_{0}}(xh) \rvert \leq C(h) \lvert F_{g_{0}}(x) \rvert,  
$$ where $F_{g_{0}}(xh)$ and $F_{g_{0}}(x)$ are defined as you've noted, and $C(h)$ is a constant dependent on $h$, we'll proceed with an analytical approach that delineates the effect of introducing the term $h \in G$ into the picture. This reflects changes in the fibers caused by a further action by $h$ on the "base point" $x$ in the quotient space $X = \Gamma \backslash G$.

### Preliminary Analysis

The fiber $F_{g_{0}}(x)$ contains elements $\gamma \in \Gamma$ such that for some $g \in B$, we have $x\gamma g = g_{0}$. Recasting this in terms of a condition for membership in $F_{g_0}(xh)$, we consider what happens when the point $x$ is further acted upon by $h$. Specifically, we need $\gamma \in \Gamma$ for which $xh\gamma g = g_{0}$ holds true.

### Converting Conditions into Cardinality

Given the definitions, here’s a clearer reformulation aiming at correctness and precision:

1. **Original Condition:** For $F_{g_0}(x)$, we find $\gamma \in \Gamma$ aligning with $x\gamma g = g_0$.
    
2. **Modified Condition:** For $F_{g_0}(xh)$, the condition adjusts to finding $\gamma \in \Gamma$ aligning with $xh\gamma g = g_0$.
    

### Strategy for Establishing the Inequality

The aim is to reason how the cardinality of fibers can be relatively compared based on the action by $h$. The inclusion of $h$ represents a "shift" in the action from $x$ to $xh$, potentially enlarging or transforming which $g \in B$ can participate in satisfying the condition for $F_{g_0}(xh)$ compared to $F_{g_0}(x)$.

- **Adjusting Action via $h$**: Observation reveals that the effect of $h$ potentially introduces a "distortion" or "expansion" relative to $F_{g_{0}}(x)$ because any $\gamma \in \Gamma$ satisfying the condition for $x$ may also satisfy it for $xh$, but the reverse doesn't necessarily hold.
    
- **Counting & Comparison Method**: To establish $\lvert F_{g_{0}}(xh) \rvert \leq C(h) \lvert F_{g_{0}}(x) \rvert$, we need to factor in how $h$ affects the availability and choice of $\gamma \in \Gamma$. If $h$ uniformly "spreads" or adjusts the action across $B$ in a way that the "density" of satisfying $\gamma$s increases by at most a constant factor, then $C(h)$ captures this maximum inflation rate. 
    

### Establishing $C(h)$:

To argue for the existence of such a $C(h)$, observe the following: - The specific group structure and properties of $\Gamma$ and $B$ are crucial. - The action of $h$ can be studied in terms of its effect on the coset space, i.e., how moving along the orbits (induced by $\Gamma$) within $G$ by $h$ might scale the number of $\gamma$ aligning with the required conditions. 

Considering a homogeneous space and assuming moderate behavior of $h$ (not severely distorting/distancing from the identity), one might invoke compactness arguments for $B$, discreteness and lattice properties of $\Gamma$, along with possible invariance characteristics of the measures involved, to argue that $h$'s action leads to a controllable, bounded alteration in the set sizes – hence, a $C(h)$ exists such that the inequality is satisfied.

The exact derivation of $C(h)$ might rely on more detailed properties of $G$, $\Gamma$, and the metric or topological structure of $B$. For a fully rigorous proof, one would dive into specifics about how $G$'s group operations, $\Gamma$'s lattice structure, and $B$'s compactness properties coalesce, leveraging the representation theory, geometric group theory, or harmonic analysis on Lie groups.


now we denote $$
\omega(x)=\text{sup}\{(\int_{B}\lvert f(p^{-1}_{x}(h)) \rvert^{2} \,d\mu(h) )^{1/2}\mid f\in L^{2}(H), \lvert \lvert f \rvert  \rvert_{L^{2}(X)}=1\}
$$
we want to show that $$
\omega(xg)\leq C(g)\omega(x)
$$
in which $C(g)$ is a constant.

To demonstrate the inequality $\omega(xg) \leq C(g) \omega(x)$, where $\omega(x)$ is defined as $$  
\omega(x)=\sup\left\{ \left( \int_{B} |f(p_x^{-1}(h))|^2 \,d\mu(h) \right)^{1/2} \mid f \in L^{2}(X), ||f||_{L^{2}(X)}=1 \right\},  
$$ we must understand the nature of $\omega(x)$ in the context of transformations under the group action on $X = \Gamma \backslash G$, and $p_x: B \to X$ defined by $g \mapsto xg$. Here, $B$ is a compact subset of $G$ (often close to the identity $e \in G$), and $\mu$ is a measure on $B$ inherited from the Haar measure on $G$.

### Step 1: Understanding the Condition

$\omega(x)$ measures the maximal "spread" (in a sense defined by the $L^2$ norm) of functions in $L^2(X)$ when "observed" through the "window" $B$ around any point $x$ in $X$, normalized to unit norm in $L^2(X)$. The idea behind comparing $\omega(xg)$ with $\omega(x)$ is to understand how the action by an element $g \in G$ distorts this maximal spread.

### Step 2: Impact of the Group Action

The action by $g$ effectively alters the "observation window" from $x$ to $xg$. Specifically, for any given function $f \in L^2(X)$, the "view" through the window $B$ is shifted as follows when considering $\omega(xg)$: - Instead of evaluating $f$ at points "reachable" from $x$ via $B$, for $\omega(xg)$, we evaluate $f$ at points reachable from $xg$. - This shift can be absorbed into a transformation of $f$ itself, considering the group's action.

### Step 3: Demonstrating the Inequality

To prove that $\omega(xg) \leq C(g) \omega(x)$, we proceed by employing properties of the group action and the definition of $L^2$ norms. Consider an arbitrary function $f \in L^2(X)$. The transformation induced by action by $g$ can be thought to stretch or compress the "energy" (as measured by the $L^2$norm) of $f$ within $B$. This effect, ideally, is uniformly bounded by a factor that depends only on $g$ (and not on $x$ or $f$specifically), hence the introduction of $C(g)$.

Given the integral representation inside $\omega(x)$, we can argue that for each $f$ normalized to unit norm in $L^2(X)$, the mapping $f \mapsto f \circ g^{-1}$ (corresponding to considering the shift by $g$) scales the integral by at most a factor that depends on $g$ due to the change in the measure $\mu$ under the transformation induced by $g$ and possible changes in "energy concentration" induced by how the function $f$ behaves under the group action.

The explicit construction of $C(g)$ requires analyzing how measures on $B$ (derived from the Haar measure) transform under the group action, ensuring that it encapsulates all potential "spread" alterations of all $f$ in $L^2(X)$ when viewed through shifted windows (i.e., going from $x$ to $xg$).

### Conclusion

The inequality $\omega(xg) \leq C(g) \omega(x)$ reflects how the group action by $g$ uniformly distorts the observed $L^2$spread of functions in $X$ through the window $B$, independent of the base point $x$ in $X$. To make this argument rigorous, one would likely delve further into the specifics of how $L^2$norms and the measure $\mu$ on $B$ behave under the action by $G$, leveraging properties of the Haar measure and the group's representation on $L^2(X)$.

To demonstrate the inequality $\omega(xg) \leq C(g) \omega(x)$, where $\omega(x)$ is defined as $$  
\omega(x)=\sup\left\{ \left( \int_{B} |f(p_x^{-1}(h))|^2 \,d\mu(h) \right)^{1/2} \mid f \in L^{2}(X), ||f||_{L^{2}(X)}=1 \right\},  
$$ we must understand the nature of $\omega(x)$ in the context of transformations under the group action on $X = \Gamma \backslash G$, and $p_x: B \to X$ defined by $g \mapsto xg$. Here, $B$ is a compact subset of $G$ (often close to the identity $e \in G$), and $\mu$ is a measure on $B$ inherited from the Haar measure on $G$.

### Step 1: Understanding the Condition

$\omega(x)$ measures the maximal "spread" (in a sense defined by the $L^2$ norm) of functions in $L^2(X)$ when "observed" through the "window" $B$ around any point $x$ in $X$, normalized to unit norm in $L^2(X)$. The idea behind comparing $\omega(xg)$ with $\omega(x)$ is to understand how the action by an element $g \in G$ distorts this maximal spread.

### Step 2: Impact of the Group Action

The action by $g$ effectively alters the "observation window" from $x$ to $xg$. Specifically, for any given function $f \in L^2(X)$, the "view" through the window $B$ is shifted as follows when considering $\omega(xg)$: - Instead of evaluating $f$ at points "reachable" from $x$ via $B$, for $\omega(xg)$, we evaluate $f$ at points reachable from $xg$. - This shift can be absorbed into a transformation of $f$ itself, considering the group's action.

### Step 3: Demonstrating the Inequality

To prove that $\omega(xg) \leq C(g) \omega(x)$, we proceed by employing properties of the group action and the definition of $L^2$ norms. Consider an arbitrary function $f \in L^2(X)$. The transformation induced by action by $g$ can be thought to stretch or compress the "energy" (as measured by the $L^2$norm) of $f$ within $B$. This effect, ideally, is uniformly bounded by a factor that depends only on $g$ (and not on $x$ or $f$specifically), hence the introduction of $C(g)$.

Given the integral representation inside $\omega(x)$, we can argue that for each $f$ normalized to unit norm in $L^2(X)$, the mapping $f \mapsto f \circ g^{-1}$ (corresponding to considering the shift by $g$) scales the integral by at most a factor that depends on $g$ due to the change in the measure $\mu$ under the transformation induced by $g$ and possible changes in "energy concentration" induced by how the function $f$ behaves under the group action.

The explicit construction of $C(g)$ requires analyzing how measures on $B$ (derived from the Haar measure) transform under the group action, ensuring that it encapsulates all potential "spread" alterations of all $f$ in $L^2(X)$ when viewed through shifted windows (i.e., going from $x$ to $xg$).

### Conclusion

The inequality $\omega(xg) \leq C(g) \omega(x)$ reflects how the group action by $g$ uniformly distorts the observed $L^2$spread of functions in $X$ through the window $B$, independent of the base point $x$ in $X$. To make this argument rigorous, one would likely delve further into the specifics of how $L^2$norms and the measure $\mu$ on $B$ behave under the action by $G$, leveraging properties of the Haar measure and the group's representation on $L^2(X)$.


$$
\begin{align}
\int_{B}\lvert f(g^{-1}x^{-1}h) \rvert ^{2}\,d\mu(h) \\
=\int_{B} \lvert f(h) \rvert ^{2}\,d\mu(xgh) \\
=\Delta(x)\Delta(g)\int_{B}\lvert f(h) \rvert ^{2}\,d\mu(h)   
\end{align}
$$

but if the haar measure it's left $G$-invariant, then
$$
\begin{align}
\int_{B}\lvert f(g^{-1}x^{-1}h) \rvert ^{2}\,d\mu(h) \\
=\int_{B} \lvert f(h) \rvert ^{2}\,d\mu(xgh) \\
=\int_{B}\lvert f(h) \rvert ^{2}\,d\mu(h)   
\end{align}
$$
If the Haar measure $\mu$ on $G$ is left $G$-invariant, the property of invariance must be carefully applied especially in the context of transformations of variables within integrals over $G$. Your sequence of equalities aims to demonstrate the effect of such invariance under a specific group action, but it seems there's some confusion in the application of these properties. Let’s clarify these aspects:

### Left $G$-Invariance of Haar Measure

The left-invariance of the Haar measure $\mu$ on a group $G$means that for any left-translation $l_g: G \to G$ defined by $l_g(h) = g h$ for a fixed $g \in G$ and for every measurable set $A \subseteq G$, we have: $$ \mu(gA) = \mu(A). $$

### Change of Variables in Integrals

The change of variables in integrals, particularly with functions under transformations induced by the group action, should respect the properties of the Haar measure. For an integrand transformation of the form $f(g^{-1}x^{-1}h)$, assuming $g, x \in G$ and $h$ varying over $B \subseteq G$, it's essential to understand how this affects the domain of integration via the group actions.

### Addressing the Mistake in the Application

The step in your sequence where you move from $$ \int_{B}\lvert f(g^{-1}x^{-1}h) \rvert ^{2}\,d\mu(h) $$ to $$ \int_{B} \lvert f(h) \rvert ^{2}\,d\mu(xgh) $$ is not an accurate representation of how left-invariance or change of variables operates, especially the $d\mu(xgh)$ part suggests a transformed measure directly related to individual $h$ transformations, which misinterprets the measure's behavior under left-invariance.

### Correct Interpretation

The correct approach for transforming an integral with the consideration of left-invariance does not directly change the measure's domain in the manner you've described. Instead, suppose you're aiming to reflect a transformation under a group action (especially for integrals over transformed functions $f(g^{-1}x^{-invariant(h)})$). In that case, left-invariance directly ensures that for any compact set $B$ and its translation, the measure remains the same, i.e., $\mu(B) = \mu(gB)$, but the domain of the function in the integrand respects the transformation accordingly.

The fundamental property for left-invariance applicable to integrals over $G$ would mean that any transformation of the form seen doesn't alter the integral's value over $B$ due to changing the point of view (or variables) inside the function $f$. However, the exact form and property application heavily depend on what transformation (and interpretation) you’re aiming for in practice—be it changing the point $h \in B$ is evaluated at via $f$, or how you consider the grouping of $g^{-1}x^{-1}h$ affects $f$'s evaluation.

Thus, in precise mathematical terms, the left-invariance of $\mu$under the group action simply allows us to say: $$ \int_{B} |f(g^{-1}x^{-1}h)|^2 \, d\mu(h) = \int_{g^{-1}x^{-1}B} |f(h)|^2 \, d\mu(h), $$ assuming the appropriate conditions for such a transformation are met and properly interpreting how $\mu$responds to the group actions (without mistakenly transforming $\mu(h)$ into $\mu(xgh)$ directly). The conclusion about integral equality should focus on how invariance assures us that transformations akin to $g^{-1}x^{-1}h$ do not affect the overall "weight" or measure of sets over which we're integrating, within the context of how $f$ is incorporated into the integral.


$x^{-1}F_{g_{0}}(x)=\{\gamma \in \Gamma \mid \text{for any}\ g \in B,\exists \gamma \in \Gamma\ \text{such that } \gamma g=g_{0}\}$



for the map $$
p_{x}:B \to  X, p_{x}(g)=x\Gamma g
$$
For the inverse of this map: 
$$
p_{x}^{-1}: X \to B: p^{-1}_{x}(\Gamma g)=x^{-1}g
$$
in order to make sure this inverse map is well defined, we need to make sure that for any $\Gamma g \in X$, $\Gamma g \cap B\not= \emptyset$. Then we can pick the element $g$ from the intersection $\Gamma g \cap B$ as the the representative of coset $\Gamma g$. But I am confused about why  for any $\Gamma g \in X$, $\Gamma g \cap B\not= \emptyset$.


But how about the induced morphism between function space:
$$
p^{*}_{x}:L^{2}(X) \to L^{2}(B): p^{*}_{x}(f)(g)=f(x^{-1}g)
$$

why do we know that $p^{*}_{x}f \in L^{2}(B)$?



then consider the fibers $F_{g}(x)=\{b\in B \mid p_{x}(b)=\Gamma g\}$ of $B$, $$

\begin{align}
\int_{B}\lvert p^{*}_{x}(f)(h) \rvert^{2} \,d\mu(h)  \\
=\sum_{\Gamma g \in X}\int_{F_{g}}\lvert p^{*}_{x}(f)(h) \rvert^{2} \,d\mu(h)
\end{align}
$$



for quotient group $X=\Gamma \backslash G$, what is the inverse of $\Gamma g$ in $X$.


Consider the cuspidal function $f$ on homogeneous space $\Gamma \backslash H$, which is called cuspidal if $$
\int^{1}_{0}f(n(t)g)\,dt=0.
$$
I do not understand that why integrate over $(0,1)$ in the definition.