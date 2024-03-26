

An operator is continuous if and only if it's closed, so generally for a sequence $x_{n}$ with limit $x$ in a separable  Hilbert space $H$ and a linear operator $A$, it doesn't satisfy $$
Ax_{n} \to  Ax
$$
For a compact symmetric neighborhood $B$ of topological group $X=\Gamma \backslash G$, in which $\Gamma$ is a discrete subgroup of any Lie group $G$ of dimension $n$
define projection $$
p_{x}:B \to  X\ \ g \to  xg
$$
Then claim $B$ can be decomposed into fibers. 

$$
B=\bigsqcup_{g_{0}\in X} F_{g_{0}}
$$
in which $F_{g_{0}}=\{h \in B\mid p_{x}(h)= \Gamma g_{0}\}$. And by compactness of $B$, $$
B= \bigsqcup_{i}^{n} B_{i}
$$
in which $B_{i}$'s is a family of finite open cover of $B$.
Combined the two decomposition together, $$
B=\bigsqcup_{g_{0}\in X} \bigsqcup_{i}^{n}\bigsqcup_{h \in F_{g_{0}}} B_{i}h
$$


Given a topological group $X=\Gamma \backslash G$, where $\Gamma$ is a discrete subgroup of a Lie group $G$ of dimension $n$, and $B$ is a compact symmetric neighborhood within $X$, we are tasked with examining a projection and a proposed decomposition of $B$.

Define the projection: $$ p_{x}:B \to X,\ \ g \to xg $$ The goal is to justify a decomposition of $B$ into fibers, and then argue that under the compactness of $B$, a certain type of combined decomposition is possible.

### Fibers Decomposition

Given: $$ B=\bigsqcup_{g_{0}\in X} F_{g_{0}} $$ where $F_{g_{0}}=\{h \in B \mid p_{x}(h)= \Gamma g_{0}\}$. This formulation assumes $B$ can be decomposed into distinct fibers $F_{g_0}$ over the elements $g_0$ in $X$.

### Compactness Decomposition

The compactness of $B$ implies: $$ B= \bigsqcup_{i}^{n} B_i $$ where $B_i$'s are part of a finite open cover of $B$. This is a typical use of compactness to guarantee such a cover exists.

### Combined Decomposition

Combining both decompositions leads to: $$ B=\bigsqcup_{g_{0}\in X} \bigsqcup_{i}^{n}\bigsqcup_{h \in F_{g_{0}}} B_ih $$

### Examination and Clarification

1. **Fibers Definition Correction**: The definition of fibers $F_{g_0}$ requires clarification for its formulation in the quotient space context. Specifically, $F_{g_0}$ would more accurately be defined by the preimage under the projection onto $\Gamma \backslash G$, ensuring $F_{g_0}$ accounts for the equivalence classes defined by $\Gamma$. Thus, we may reconsider $F_{g_0}$ as consisting of $h \in B$ where $p_x(h)$ equivalently identifies the coset $\Gamma g_0$ in $X$.
    
2. **Covering and Decomposition Logic**: The subsequent leap to $B=\bigsqcup_{g_{0}\in X} \bigsqcup_{i}^{n}\bigsqcup_{h \in F_{g_{0}}} B_ih$ suggests an intricate layering of coset representatives, open sets, and multiplication that deserves rigorous underpinning. Specifically, the expression $\bigsqcup_{h \in F_{g_{0}}} B_ih$ is attempting to articulate a further subdivision of the finite open cover $B_i$ through translation by elements $h$ that map into the fiber over $g_0$.
    
3. **Correctness and Feasibility**: The final combined decomposition presents a complex and somewhat convoluted picture. It's crucial to note that:
    
    - The operation $B_ih$ implies translating the set $B_i$ by an element $h$, which might not yield a direct subdivision of $B$ constrained within its original structure unless $h \in B$.
    - The direct sum over $i$ up to $n$ and then over $g_0$ in $X$ and further over $h$ in $F_{g_0}$ implies a level of partitioning and covering not necessarily prescribed by compactness alone or general topological group structure.

Therefore, while the underlying intuition about using compactness, fibers, and covers is of value, the exact interpretation requires refinement. To substantiate the claim rigorously, one must ensure clear definitions, particularly regarding how fibers are constructed in the quotient space and how translations act coherently within the desired decomposition framework. Moreover, exploring the intrinsic geometry and algebraic structure of $\Gamma \backslash G$ in the context of its compact neighborhoods and covering properties might yield the intended decompositional insight with greater clarity and accuracy.

Now we can have a bound over the identity $e \in G$, For any $f\in C^{\infty}(X)$,$$
\lvert f(e) \rvert \leq C \lvert \lvert f \rvert  \rvert _{W^{k,2}}
$$
in which $k> \frac{n}{2}$ and the norm $\lvert \lvert \cdot \rvert \rvert_{W^{k,2}}$ represents the Sobolev norm.

We want to deduce to any point $x$ in $X$, $$
\lvert f(x) \rvert \leq C \omega(x) \lvert \lvert f \rvert  \rvert _{W^{k,2}}
$$
in which $\omega(x)$ is a weight over space $X$. My confusion is how this weight comes into the formula.


Claim if $X$ is compact, the weight function $\omega(x)$ is bounded.


The claim that if $X$ is compact, the weight function $\omega(x)$ is bounded leverages fundamental properties of compact spaces in topology, particularly as they relate to continuous functions defined on these spaces.

Given: - $X$ is a compact space. This could be a compact topological group, a compact manifold, or any compact topological space. - $\omega: X \rightarrow \mathbb{R}$ is a weight function defined on $X$.

To establish the boundedness of $\omega(x)$ over $X$, we proceed as follows:

### Compactness and Continuous Functions

A fundamental theorem in topology states that if $K$ is a compact space and $f: K \rightarrow \mathbb{R}$ is a continuous function, then $f$ is bounded on $K$. Moreover, $f$ attains its maximum and minimum on $K$. This implies that there exist $x_{\text{min}}, x_{\text{max}} \in K$ such that for all $x \in K$, $$ f(x_{\text{min}}) \leq f(x) \leq f(x_{\text{max}}). $$

### Application to the Weight Function

Let's assume for the purpose of this argument that the weight function $\omega(x)$ is continuous on $X$. Given the compactness of $X$, by applying the above theorem, it follows that $\omega(x)$ must be bounded over $X$. Thus, there exists a maximum value $M$ and a minimum value $m$ such that for all $x \in X$, $$ m \leq \omega(x) \leq M. $$

This assertion relies critically on the continuity of $\omega$. While the original formulation did not explicitly state the continuity of $\omega$, in many practical scenarios, especially in mathematical analysis and geometric analysis on manifolds or groups, weight functions are often designed to be continuous to ensure well-behaved interactions with other continuous or smooth structures.

### Conclusion

If $\omega(x)$ is indeed a continuous function (as is often the case for weight functions used in analysis), then its boundedness on a compact space $X$ follows directly from the compactness of $X$ and the properties of continuous functions on compact spaces. This boundedness is crucial for various analytical arguments, ensuring that estimates or inequalities involving $\omega(x)$ remain globally applicable across $X$.



function $f(t)=t^{2}$, what is the integral of $f(t)$ over $(-r,r)$. 

what is the $L^{2}$ norm of $f(t)$ over $(-r,r)$.

what is the $2,3$ Sobolev norm of $f(t)$ over $(-r,r)$, which means $$
\lvert \lvert f \rvert  \rvert_{2,3}^{2}=\sum\limits_{\lvert \alpha \rvert <3} \lvert \lvert D^{\alpha}f \rvert  \rvert_{2} 
$$


claim that $\lvert \lvert f \rvert \rvert^{2}_{2,3}\ll r$


what is the 2,3 Sobolev norm of $f(t)$ over $\mathbb{R}$


Consider function $\phi: SL_{2}(\mathbb{R}) \to \mathbb{R}$, which is defined as following:$$
\phi(g)=\phi(n(x)a(t)r(\theta))=\phi(a(t))=t^{2},
$$what is the 2,3 Sobolev norm of $\phi$ over $SL_{2}(\mathbb{R})$.


Consider the Iwasawa decomposition of $SL_{2}(\mathbb{R})$, i.e. $$
g=pk
$$
in which $p=au$ are from the parabolic subgroup $P=AU$ and $k\in K=SO(2)$. 

Now given integral over $SL_{2}(\mathbb{R})$, $$
\int_{SL_{2}(\mathbb{R})}f(g)\,d\mu(g)=\int_{AUK}f(auk)\Delta(a)\,d\mu_{1}(a)d\mu_{2}(u)d\mu_{3}(k)  
$$

how to Calculate this modular function $\Delta$.





Now we have a different decomposition $$
g= \begin{pmatrix}
1 & 0 \\
t_{1} & 1
\end{pmatrix} \begin{pmatrix}
e^{t_{2}/2} &  0\\
0 & e^{-t_{2}/2}
\end{pmatrix} \begin{pmatrix}
1 & t_{3} \\
0& 1
\end{pmatrix}
$$
then similarly when we have the integral $$
\int_{SL_{2}(\mathbb{R})}\phi(g)\,d\mu(g)=\int_{H^{-}H_{0}H}\phi(\begin{pmatrix}
1 & 0 \\
t_{1} & 1
\end{pmatrix} \begin{pmatrix}
e^{t_{2}/2} &  0\\
0 & e^{-t_{2}/2}
\end{pmatrix} \begin{pmatrix}
1 & t_{3} \\
0& 1
\end{pmatrix})\,d\mu_{1}(t_{1})d\mu_{2}(t_{2})d\mu_{3}(t_{3})  
$$

Now claim the $$
\Delta(\begin{pmatrix}
e^{t_{2}/2} &  0\\
0 & e^{-t_{2}/2}
\end{pmatrix})=e^{-t}
$$