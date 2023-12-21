
Given a finite group $G$, and subgroup $H$ and a field $F$ of characteristic zero, consider the group algebra $F[G/H]$, which is defined as follows:
$F[G/H]=\{f:G/H\to F \text{of finite support}\}$, it is equipped with module scalar product and module sum and convolution product to define as an associative algebra. Now claim identity $End_{G}(F[G/H])=F[G]^{H\times H}$ by mapping $G$-linear map $\phi$ to its evaluation at characteristic function $\chi_{H}$ of $H$.


Considering the given conditions, we have the set $F[G/H]$ of functions from $G/H$ to $F$ with finite support. Here, the support of a function is the set of points where the function is nonzero. These are essentially formal $F$-linear combinations of the cosets $gH$ for $g∈G$.
Now, $End_G(F[G/H])$ is the set of $G$-module endomorphisms of $F[G/H]$. That is, $End_G(F[G/H]) = {\phi: F[G/H]\to F[G/H]\, |\, \phi \text{ is a linear transformation that commutes with the action of}\, G }$.
On the other hand, $F[G]^{H\times H}$ is the set of $F$-valued functions on $G$ x $G$ that are invariant under the action of $H$ x $H$ : $(h_1, h_2) * (g_1, g_2) = (h_1g_1, g_2h_2)$ for $g_1, g_2 \in G$ and $h_1, h_2 \in H$.
We want to prove that these two sets are isomorphic as $F$-algebras. Here’s the approach to the proof:
It’s sufficient to identify an isomorphism $\Phi: F[G]^{H\times H} \to End_G(F[G/H])$.
Given $f \in F[G]^{H\times H}$, we define $\Phi(f) : F[G/H] \to F[G/H]$ by $(\Phi(f)(\sum a_{gH} gH)) = \sum a_{gH} f(g, g^{-1}) gH$. This is indeed a $G$-module endomorphism and its definition does not depend on the choice of representative $g$ in each coset $gH \in G/H$.
On the other hand, given $\phi \in End_G(F[G/H])$, the corresponding function $f_{\phi}: G \times G \to F$ is given by $f_{\phi}(g_1, g_2) = \phi(g_1H)(g_2H)$. This function is clearly invariant under the action of $H \times H$.
It can be checked that $\Phi$ is a bijective and preserves the algebra structures, i.e., it’s an isomorphism of $F$-algebras.

Furthermore, claim that the characteristic function $T_{g}$ of $HgH$ form the basis of $H(G,H)=End_{G}(F[G/H])$.

Firstly, let's clarify some notation: $T_g$ denotes the characteristic function of $HgH$ in $G$, which is defined as 

$$T_g (x) = \left\{$$

Next, consider the following:

$H(G, H) = \text{End}_{G}(F[G/H])$, which is the space of $G$-equivariant maps from $F[G/H]$ to itself.

Given any $g \in G$, we define $\phi_{g}: F[G/H] \rightarrow F[G/H]$ by $\phi_{g}(f)(xH) = f(xgH)$. It is easy to see that $\phi_g$ is $G$-equivariant for every $g$ in $G$, and thus the $\phi_{g}$’s belong to $H(G, H)$.

Now, verify that the $\phi_{g}$'s are parameterized by the double cosets $HgH$ in $G$. This concludes that these $G$-equivariant maps construct a basis to the algebra $H(G, H)$ under the convolution product.

Finally, show that $\phi_{g}$ corresponds to the characteristic function $T_{g}$ of the double coset $HgH$ in $G$. This implies that the functions $T_{g}$, as $g$ varies over the set $G$, form a basis for the algebra $H(G, H)$.

Therefore, we can claim that the characteristic functions $T_g$ of the sets $HgH$ indeed form a basis of the convolution algebra $H(G, H) = \text{End}_{G}(F[G/H])$.

how to define the characteristic function $T_{g}$.
The characteristic function $T_g$ of a set $HgH$ in $G$ is a function that takes an element of $G$ and outputs whether or not that element is in $HgH$. In more formal terms, $T_g : G \rightarrow F$ is defined as follows:

$$T_g(x) =   
\begin{cases}   
1_F & \text{if } x \in HgH \\  
0_F & \text{otherwise}  
\end{cases}  
$$

To put it informally, $T_g(x)$ "checks" if $x$ belongs to the set $HgH$. If $x$ is in $HgH$, $T_g(x)$ equals $1_F$, the multiplicative identity in the field $F$. If $x$ is not in $HgH$, $T_g(x)$ equals $0_F$, the additive identity in $F$.

It should be noted that when the characteristic function $T_g$ is used in a context like this, the field $F$ is typically assumed to be a field with characteristic zero, such as the real numbers or the complex numbers. This is to ensure that the scalars 0 and 1 behave as expected.


Why do $T_{g}$ form the basis of $H(G,H)$.

The functions $T_g$ form a basis for $H(G,H)$ essentially because they generate all $G$-equivariant maps under the convolution operation in $G$. Let's break down this idea:

1. $G$-equivariant maps are those that are preserved under the action of the group. In this case, we want maps $\phi:F[G/H] \to F[G/H]$ for which $\phi(g \cdot f) = g \cdot \phi(f)$ for all $g \in G$ and $f \in F[G/H]$. Here, the group action is the usual group multiplication in $G$.
    
2. Convolution is a binary operation on functions from $G$ to $F$ – it's essentially a way of "multiplying" functions. If $f, g: G \to F$ are any two such functions, their convolution $(f * g)(h)$ is defined as $\sum_{xy=h} f(x)g(y)$, where the sum is over all pairs $(x, y)$ of elements in $G$ that multiply to $h$.
    
3. The set of characteristic functions $\{T_g\}_{g\in G}$ is essentially a complete collection of "building blocks" for all $G$-equivariant maps. You can express any such map as a finite linear combination (that is, sum and scalar multiple) of these functions.
    

To see why, suppose $\phi$ is a $G$-equivariant map. Technically we should verify for each element of $F[G/H]$. But for simplicity, let's just consider an element of the basis, say $e_k$, the characteristic function of the subgroup $Hk$. Then $\phi(e_k) = \phi(\sum_g a_g gH) = \sum_g a_g \phi(gH) = \sum_g a_g T_g$ for some coefficients $a_g$'s. The claim follows since the basis elements $\{e_k\}$ span $F[G/H]$.

So, by providing every possible "direction" in the space of $G$-equivariant maps, the characteristic functions $T_g$ form a basis for $H(G,H)$. This is the intuition behind the claim.


Consider a representation $(\pi,V)$ of finite group $G$, given a subgroup $K$ of $G$, then claim the identity:$$
V^{K}=Hom(1,Res^{G}_{K}V),
$$
in which $V^{K}=\{v\in V\mid \pi(k)v=v,\forall k \in K\}$, and $Res^{G}_{K}$ is the restriction of the representation $(\pi,V)$.

Sure, let's give the proof a try!

Firstly, we define a linear map $$  
\Phi: V^K \rightarrow Hom_K(1, Res^{G}_{K}V), v \mapsto (\lambda \mapsto \lambda v).  
$$ Here $\lambda \mapsto \lambda v$ is a K-equivariant map, because K acts trivially on 1.

Reciprocally, let's define a linear map $$  
\Psi: Hom_K(1, Res^{G}_{K}V) \rightarrow V^K,  
$$ where for a homomorphism f, $$  
\Psi(f) = f(1) \in V^K.  
$$ Now let's prove $\Psi$ is well-defined. Take $f \in Hom_K(1, Res^{G}_{K}V)$, so for all $k \in K$, $f(k \cdot 1) = \pi(k) f(1)$, but as $k \cdot 1 = 1$ we obtain $\pi(k)f(1)=f(1)$, i.e $f(1)\in V^K$. 

Now let's prove that $\Phi$ and $\Psi$ are inverses of each other.

1. Start with $v \in V^K$, then $v \mapsto \Phi(v) = \lambda \mapsto \lambda v$. Applying $\Psi$ gives us back $\Psi(\Phi(v)) = \Psi(\lambda \mapsto \lambda v) = v$.
2. Start with $f \in Hom_K(1, Res^{G}_{K}V)$, then $f \mapsto \Psi(f) = f(1)$, and applying $\Phi$ to this yields $\lambda \mapsto \lambda f(1)$, which is just $f$ again, since $f$ is K-equivariant and $\lambda$varies over the trivial representation, hence over scalars.

Hence, we see that $\Phi$ and $\Psi$ are mutual inverses, and therefore our claim is proven: $V^K \cong Hom(1, Res^{G}_{K}V)$.

why do we have $\lambda \mapsto \lambda v$ but not just $1\mapsto 1v$.

for checking $f(1)\in V^{K}$, I do not understand why $k\cdot 1=1$ and why $f(k)=\pi(k)f(1)$.

so you mean $k\cdot 1 =k$ and $K$-homomorphism means it's invariant under $K$-action, I am not sure how you define it here


Given a repsentation $(\pi,V)$ of finite group $G$ and $K$ is the subgroup of $G$, then for the $K$-invariant subspace $V^{K}$, $F(V)=V^{K}$ is functorial in $V$.

Yes, the assignment $V \mapsto V^K$ is indeed functorial in $V$. 

The category in question here is the category of representations of G, where the objects are linear representations of the group G (i.e., group homomorphisms from G to the general linear group of some vector space), and the morphisms are intertwiners (i.e., linear transformations between the corresponding vector spaces which commute with the action of the group).

The functor F maps a representation V of G to the subspace $V^K$ of vectors fixed by every element in the subgroup K of G. Given a morphism $f:V\to W$ in the category of G-representations (i.e., an intertwiner from V to W), the functor F maps f to the restriction $f|_{V^K}$.

The functoriality of F follows from the following two properties:

1. Identity morphisms are preserved: For every representation V of G, the restriction of the identity morphism on V to the subspace $V^K$ is the identity on $V^K$, i.e., $F(id_V) = id_{F(V)}$.
    
2. Composition of morphisms is preserved: For all representations V, W and X of G and all morphisms (intertwiners) f : V -> W and g : W -> X, the restriction of the composition g o f to the subspace $V^K$ is the composition of the restriction of g to $W^K$ with the restriction of f to $V^K$, i.e., $F(g o f) = F(g) o F(f)$.
    

These two properties make F a (covariant) functor from the category of representations of G to the category of vector spaces.

$F(V)$ is representable by $\mathbb{C}[G/K]$, in which $\mathbb{C}[G/K]$ is the group algebra over $\mathbb{C}$


About the definition of representable functor that I am familiar with, given a locally small category $\mathcal{C}$, and denote $\mathcal{Set}$ as the category of sets, then a functor $F$ is representable if for some $A\in ob(\mathcal{C})$, $F$ is naturally isomorphic to $Hom(A,-)$. And the representation of $F$ is a pair $(A,\Phi)$, for $A\in ob(\mathcal{C})$, where $\Phi:Hom(A,-)\to F$ is a natural isomorphism.

Based on this definition, I am not sure I understand your proof, so could you please check the proof again with more details explaining with definitions.


why do we have the functor $F:Rep_{\mathbb{C}}(G)\to \mathcal{Set}$ contravariant.


Now by Yoneda lemma, we have that $$
End(F)\cong End_{G}(\mathbb{C}[G/K])
$$

no, here we only consider the $F$ isomorphic to $Hom_{Rep_{\mathbb{C}}(G)}(\mathbb{C}[G/K],-)$ 


by the universal property, this can be identified with $\mathbb{C}[G/K]^{K}$, which can be further identified as a vector space with $\mathbb{C}[K\backslash G/K]$.


for an endomorphism $\phi \in End_{G}(\mathbb{C}[G/K])$, let's consider the map $\alpha: End_{G}(\mathbb{C}[G/K])\to \mathbb{C}[G/K]^{K}$, then what is the image of $\alpha(\phi)$.


let me try to understand your notation: $\phi(f)=g\cdot f=\pi(g)f$ and $\pi(g)f(x)=f(g\cdot x)$.