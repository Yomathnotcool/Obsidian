



Given a set $X$ and a group $G$ without further structure: topology and measure, for an easy understanding, we can even consider the set $X$ and $G$ as finite.

Given group action of $G$ on the set $X$, 
$$
G\times X\to X: (g,x)\to g\cdot x
$$
then by this action, we can have an easy dynamical system.

Now we define the chain and cochain:
### Def :: $n$-Chain
Given a $n$-family $(g_{1},g_{2},\dots,g_{n},x)$ which can take as a oriented $n-$simplex
![[Pasted image 20231126214801.png]]


so for 1-chain, it’s just formal combination $\sum\limits^{m}_{i=1}c_{i}(g_{i},x_{i})$, in which $(g_{i},x_{i})$ means the line $x_{i}\to g_{i}x_{i}$. Similarly we can imagine the $n$-simplex.

Denote $C_{n}(G,X)=\{\text{Space of }\ n-\text{Chains}\}$, when $n=0$, $C_{0}=\{0\}$ is just trivial. 

### Def :: Boundary map
$$
\partial:C_{n}(G,X)\to C_{n-1}(G,X)
$$
is the unique homomorphism such that  
$$
\begin{array}
\partial(g_{1},\dots,g_{n},x)&=(g_{1},\dots,g_{n-1},g_{n}x)\\ \\
&+\sum\limits^{n-1}_{i=0}(-1)^{n-i}(g_{1},\dots,g_{i-1}g_{i},g_{i+2},\dots,g_{n},x) \\
&+(-1)^{n}(g_{2},\dots,g_{n},x)
\end{array}
$$

### Def :: Cochain
$n$-cochain $\rho:C_{n}(G,X)\to U$, in which $C_{n}(G,X)=<g_{1},\dots,g_{n},x>$.
Define function $F:G^{n}\times X\to U: ((g_{1},\dots,g_{n}),x)\to F(x,g_{1},\dots,g_{n})$.

Then the space of all $n$-cochain $C^{n}(G,X,U):=Hom(C_{n}(G,X),U)$, is an abelian group. 

### Def :: Cobounary
Given the bounary map:
$$
\partial: C_{n}(G,X)\to C_{n-1}(G,X)
$$
Then the corresponding cobounary 
$$
\begin{array}
\ \delta : C^{n-1}(G,X,U)\to C^{n}(G,X,U)\\ \\
Hom(C_{n-1}(G,X),U)\to Hom(C_{n}(G,X),U)
\end{array}
$$
Given a $n$-chain $c$ and a function $F\in C^{n-1}(G,X,U)$, then 
$$
\delta F(c)=F(\partial c).
$$
