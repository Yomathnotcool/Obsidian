# Tags
#representation #lie-group #GPT 

---

# References


---


# Other related files


---

# given a nonimpact connected simple higher rank matrix Lie group $G$ with finite centre and $K$ the maximal compact subgroup of $G$. Consider a unitary representation $(\pi, H)$ of $G$, in which $H$ is infinite dimensional hilbert space. We want to decomposition $H$ into irreducible representations of $K$: $H=\bigoplus_{\sigma\in \hat{K}}H_{\sigma}$ where $\hat{K}$ denotes the unitary dual of $K$ and $H_{\sigma}$ is the direct sum of the irreducible components isomorphic to $\sigma$.

This is a well-studied problem in the field of representation theory, a branch of abstract algebra dealing with the study of symmetries in formal mathematical structures. The decomposition you mentioned expresses the space $H$ as a direct sum of irreducible representations of $K$. 

Given that $G$ is a simple higher rank matrix Lie group, it follows that $K$ is a maximal compact subgroup in $G$. The decomposition of $H$ is somewhat analogous to the decomposition of any finite dimensional vector space given by the structure theorem for finitely-generated modules over a principal ideal domain.

In constructing the decomposition, we first take $\hat K$, the set of all equivalence classes of irreducible unitary representations of $K$. For any $\sigma$ in $\hat{K}$, we define $H_{\sigma}$ to be the direct sum of irreducible components isomorphic to $\sigma$. A component is said to be isomorphic to $\sigma$ if its characters, which are class functions that define the representations, match those of $\sigma$. 

In general, to write out $H$ as the direct sum, we have to invoke Zorn's lemma (a form of the axiom of choice), which allows us to select a maximal orthogonal set of vectors from the space without explicitly constructing such a set. In the infinite-dimensional case, this often entails analyzing the action of the group $G$ on $H$ and using various completeness arguments to extend our results from finite-dimensional subspaces to the entirety of $H$. 

Decompose the function space into a direct sum of irreducible representations. The Peter-Weyl Theorem gives us the decomposition of $L^2(G)$ into a direct sum of finite-dimensional, invariant subspaces: $L^2(G) = \bigoplus_{\pi \in \hat{G}} H_\pi \otimes H_\pi^*$where $\hat{G}$ is the set of equivalence classes of irreducible unitary representations of $G$, $H_\pi$ is the Hilbert space of the representation $\pi$, and $H_\pi^*$ is the dual space.


# $\hat K$, the set of all equivalence classes of irreducible unitary representations of $K$.

The equivalence classes of irreducible unitary representations of a group $K$ are defined by the isomorphism relation. Specifically, let's say we have two representations $(\rho_1, V)$ and $(\rho_2, W)$ of the group $K$, meaning two homomorphisms $\rho_1 : K \rightarrow GL(V)$ and $\rho_2 : K \rightarrow GL(W)$, where $GL(V)$ and $GL(W)$ denote the general linear groups of $V$ and $W$ respectively. 

Both $V$ and $W$ are vector spaces over a field (in this case, we are looking at complex Hilbert spaces, so our field is the set of complex numbers) and $\rho_1$ and $\rho_2$ are representations of the group $K$ simply if they preserve the group operation of $K$ under a mapping to the linear transformations of $V$ and $W$ respectively.

We say that $(\rho_1, V)$ and $(\rho_2, W)$ are equivalent, and write $(\rho_1, V) \sim (\rho_2, W)$, if there exists an invertible linear transformation $T: V \rightarrow W$ such that $\rho_2(k) \circ T = T \circ \rho_1(k)$ for all $k \in K$. 

In other words, the representations are equivalent if there's a change of basis making them identical. And thus, two irreducible unitary representations are in the same equivalence class if such a transformation $T$ exists. 

This may be more intuitive when we consider irreducible representations as 'preserving the structure' of the group - two representations which are equivalent carry in some sense the same information about the structure of the group, albeit perhaps in different bases or with different labels. 

The full collection of these equivalence classes, denoted by $\hat{K}$, forms a complete set of irreducible unitary representations of $K$.


Let me expand on the concepts mentioned. First, an irreducible component is, by definition, a subspace of $H$ that is preserved under the action of $K$, and no proper, non-zero subspace of it is preserved under the action of $K$. These irreducible components can be seen as the "building blocks" of the representation. If we have an irreducible representation on a subspace of $H$, then we won't be able to find a smaller subspace taking that same structure under the action of $K$.

Now, regarding the term "isomorphic to $\sigma$", two representations are said to be isomorphic if there exists a bijective linear map between their underlying vector spaces that commutes with the group action. In the context of character theory, however, this boils down to: two representations are isomorphic if and only if they have the same character.

The character of a representation is a function that assigns to each element $g \in K$ the trace of the matrix representing the action of $g$ in the chosen basis of the space where the representation is defined. It synthesizes much of the information about the representation in a compact way: representations with the same character are isomorphic (and vice versa), and when the character is identical to the character of the irreducible representation $H_{\sigma}$, we say the representation is isomorphic to σ.

So, if a representation's character matches that of the irreducible representation $\sigma$, we consider that representation as part of the subspace $H_{\sigma}$. These subspaces are then "added" together, in the sense of forming a direct sum, to fully span $H$.

Finally, the direct sum notation $\oplus$ is used to denote a sum of subspaces, where each element of the resulting space $H$ can be uniquely written as a sum of elements from each subspace $H_{\sigma}$. In the infinite dimensional case, this sum will usually be infinite. It is the extension of the usual concept of a sum of subspaces to include an infinite number of summands.


# so in summary, we can decomposition $H$ as $\bigoplus_{\sigma\in K} H_{\sigma}$, then by Peter-weyl and compactness of $K$, we can further decompose $H_{\sigma}$ into isomorphic component of representation $\sigma$

The direct sum decomposition of $H$ is indeed given by $H = \bigoplus_{\sigma \in \hat{K}} H_{\sigma}$, where each $H_{\sigma}$is the direct sum of all components isomorphic to the irreducible representation $\sigma$. 

The Peter–Weyl theorem is crucial here as it gives us the tools to handle the decomposition of unitary representations of compact groups, which $K$ is. It states that every irreducible representation is finite-dimensional and occurs with finite multiplicity in the regular representation. Therefore, the regular representation of a compact group decomposes into a direct sum of matrix algebras, which indicates that $H_{\sigma}$ can be decomposed into a direct sum of $\sigma$.

Using these tools, you can further decompose each subspace $H_{\sigma}$ into a direct sum of mutually orthogonal irreducible components all isomorphic to $\sigma$. This can be crucial for understanding the structure of the original Hilbert space $H$ and how the group $G$ acts on it. You've consolidated the representations for the compact subgroup $K$, and thus effectively "reduced" the complexity of the original system.


# There is the Casimir operator $\mathcal{C}$ of $K$ which is the second order differential operator commuting with the action of $K$.

Yes, that's correct. The Casimir operator is an important concept in mathematical physics, particularly in representation theory and the study of Lie algebras.

For a given Lie group, the Casimir operator is a second-order differential operator that commutes with all elements of the Lie algebra, which roughly means that it shares the symmetries of the original Lie group. 

For the case of $K$, the maximal compact subgroup of $G$, we can define a Casimir operator $\mathcal{C}$ which commutes with the left regular action of K on functions on $K$. This operator is essentially constructed from the Lie algebra of $K$. It can serve as a tool to differentiate between different irreducible representations of $K$ and allow for easier computations in representation theory.

The use of the Casimir operator is really essential when dealing with the representations of Lie groups and algebras, as they are one of the few tools that can provide a full description of the structure of these complicated mathematical objects. The properties of these operators, such as their commutation relations and eigenvalues, often yield valuable information about the group's representations, like their dimensions or characters, and can even sometimes classify them.


# There is the Casimir operator $\mathcal{C}$ of $K$, what is the explicit formula of the action of $\mathcal{C}$.


To construct an explicit formula for the Casimir operator, we usually start with the generators of the Lie algebra associated with the maximal compact subgroup $K$. 

Let me denote $k_1, k_2, ..., k_n$ as the set of generators of Lie algebra associated with $K$. In the universal enveloping algebra of this Lie algebra, we can define the quadratic Casimir operator $\mathcal{C}$ as:

$\mathcal{C} = \sum_{i=1}^n k_i^2$

The action of the Casimir operator $\mathcal{C}$ on a vector $v$ in a representation space of the Lie algebra of $K$ is then displayed as $\mathcal{C}(v)$.

This formula is the standard way of representing the Casimir operator for any Lie group or algebra. Depending on the specific structure of the representation and the group at hand, the actual computation of the action of this operator can be quite involved. The operator $\mathcal{C}$commutes with all elements from the algebra, making it a central element of the universal enveloping algebra. Its diagonalizable action on any finite-dimensional, irreducible representation is a scalar multiple of the identity operator.


# There is only finitely generated generators of the Lie algebra of $K$ because $K$ is maximal compact subgroup. And what is the formula for $\mathcal{C}(v)$.

Certainly. Given the finite number of generators of the Lie algebra of $K$, let's denote these by $k_1, k_2, ..., k_n$. The Casimir operator $\mathcal{C}$ was previously defined as the quadratic operator: 

$\mathcal{C} = \sum_{i=1}^{n} k_{i}^2$

The action of the Casimir operator $\mathcal{C}$ on a vector v in a given representation space of the Lie algebra of $K$ is then obtained by simply replacing each $k_i$ in the sum with the corresponding linear operator in the representation, and then applying this to the vector $v$.

That is, given a representation $\rho: \mathfrak{k} \rightarrow \mathfrak{gl}(V)$ (where $\mathfrak{k}$ is the Lie algebra of $K$ and $\mathfrak{gl}(V)$is the set of linear operators on V), and assuming that $v$ is an element of $V$, the action of the Casimir operator on $v$ is given by

$\mathcal{C}(v) = \sum_{i=1}^{n} \rho(k_i) \circ \rho(k_i)(v)$

To make it more explicit, if $V$ is a finite dimensional vector space and $\{e_1, e_2, ..., e_d\}$ is a basis of V, and $v$ is expressed in this basis as $v = \sum_{j=1}^{d} a_j e_j$ where $a_j$ are scalars, then

$\mathcal{C}(v) = \sum_{i=1}^n \rho(k_i) \circ \rho(k_i) \left( \sum_{j=1}^{d} a_j e_j \right)$

So the action of $\mathcal{C}$ depends on both the specific representation $\rho$ and the vector $v$ in question. In practice, this calculation can be quite complex, depending on the actual form of the representation $\rho$and the vector space $V$.


# It leaves each of the subspaces $H_{\sigma}$ invariant. Moreover one can deduce from the Schur lemma that $\mathcal{C}\mid_{H_{\sigma}}=\lambda_{\sigma}Id_{H_{\sigma}}$.

Yes, that's a key point about the Casimir operator and the role it plays in the theory of representations. We say that the operator $\mathcal{C}$ is an "intertwining" operator, as it commutes with all elements from the algebra, which means it leaves each of the subspaces $H_{\sigma}$ invariant.

The related Schur's Lemma states that if an operator commutes with all the operators in an irreducible representation, it must act as a scalar multiple of the identity. This scalar is usually denoted by $\lambda_{\sigma}$ and may depend on the equivalence class $\sigma$ under consideration.

Hence, the restriction of the Casimir operator $\mathcal{C}$ to each $H_{\sigma}$ acts as a scalar multiple of the identity:

$\mathcal{C}|_{H_{\sigma}}=\lambda_{\sigma}Id_{H_{\sigma}}$

where $Id_{H_{\sigma}}$ represents the identity operator on $H_{\sigma}$.

This is an essential property when considering the decomposition of representations in terms of irreducible components, as the Casimir operator gives a simple way to "separate" different subspaces $H_{\sigma}$. Moreover, the scalars $\lambda_{\sigma}$ provide a method for classifying and distinguishing different irreducible representations.

# The eigenvalues $\lambda_{\sigma}$ of Casmir operator $\mathcal{C}$ and the dimensions $dim(\sigma)$ are computed explicitly in the representation theory of compact groups, and one can verify that $dim(\sigma)\leq \lambda^{c_{1}}_{\sigma}$ and $\sum_{\sigma \in \hat{K}}dim(\sigma)^{-c_{2}}<\infty$, for some postive $c_{1}$ and $c_{2}$.

These are important results from the representation theory of compact groups, they underline several essential properties of the representations of such groups. As you've mentioned, both the dimensions $dim(\sigma)$of the representation $\sigma$ and the eigenvalues $\lambda_{\sigma}$ of the Casimir operator $\mathcal{C}$ can be explicitly computed.

The first inequality you've written, $dim(\sigma)\leq \lambda^{c_{1}}_{\sigma}$, is known as a bound on the dimension of the irreducible representations. It states that the dimension of each irreducible representation is bounded above by a power of the corresponding eigenvalue of the Casimir operator. Different approaches might yield different values of $c_1 > 0$.

The second relation, $\sum_{\sigma \in \hat{K}}dim(\sigma)^{-c_{2}}<\infty$, means that the sum of the reciprocals of the dimensions (to the power of $c_2$) of all irreducible representations is finite, which is a different kind of bound but quite important when considering the "totality" of all representations. Akin to the previous case, the constant $c_2 > 0$ can vary depending on the specifics of the approach and the group $K$.


# recall the results about the computation of eigenvalues $\lambda_{\sigma}$

Typically, the computation of the eigenvalues $\lambda_{\sigma}$ of the Casimir operator involves an intricate interplay between the structure of the Lie algebra, the properties of the specific representation $\sigma$, and the details of the Casimir operator itself.

In general, the eigenvalues of the Casimir operator for an irreducible representation are constants that are determined by the structure of the Lie algebra and the properties of the representation. Specifically, they are often given by a quadratic function on the weight or highest weight of the representation.

For instance, in the case of a semisimple Lie algebra $\mathfrak{g}$ with a chosen Cartan subalgebra $\mathfrak{h}$, and for a weight $\lambda\in\mathfrak{h^*}$, the eigenvalue of the Casimir element in the universal enveloping algebra of $\mathfrak{g}$ on a weight vector of weight $\lambda$ in an irreducible representation is usually given by the formula:

$\lambda_{\sigma} = \langle \lambda+\rho, \lambda \rangle$

where $\rho$ is the Weyl vector (half the sum of positive roots) and $\langle , \rangle$ stands for the Killing form (which is basically an invariant symmetric bilinear form).

However, the computation might differ based on specifics of the Lie algebra and the group. Sometimes additional structures or relations may provide simplifications. For example, certain classes of groups or algebras might have additional symmetric properties that allow eigenvalues to be calculated more succinctly.

Nevertheless, determining $\lambda_{\sigma}$ usually involves advanced tools from representation theory, differential geometry, and Lie theory.

For compact groups, let's denote by $\mathfrak{k}$ the Lie algebra of $K$corresponding to your compact Lie group, and denote by $\sigma: \mathfrak{k}\to GL(V)$ its complex irreducible finite-dimensional representation, where $V$ is some vector space over $\mathbb{C}$.

By using the representation $\sigma$, you can push forward the Casimir operator $\mathcal{C}$ to get some endomorphism of $V$ that we still call $\mathcal{C}$. 

Denote by $H$ the corresponding Cartan subalgebra of $\mathfrak{k}$ and $R$ the root system, then the weight lattice $\Lambda$ of $H$ can be defined. 

Every irreducible representation is highest weight with respect to some choice of positive roots and has the form $V(\lambda)$ for some $\lambda\in\Lambda$. Here $\lambda$ is a dominant integral weight and highest weight of $V(\lambda)$. You will find:

$\lambda_\sigma = \langle \lambda+\rho, \lambda \rangle$

where $\langle \cdot, \cdot \rangle$ stands for the Killing form, $\rho=\frac{1}{2}\sum_{\alpha \in R^{+}} \alpha$ is half the sum of positive roots, and $\lambda$ is the highest weight. 

Now this value $\lambda_\sigma$ ends up being the eigenvalue of the Casimir operator on the irreducible representation $\sigma$ (since under the representation, the Casimir goes to an endomorphism of $V$, which will be diagonalizable if $V$ is a complex irreducible representation). 

So, that is how you can compute explicitly the eigenvalue $\lambda_{\sigma}$ associated to representation $\sigma$ of compact group $K$.

When dealing with a compact group, there's a natural relation between the group and its associated Lie algebra. The Killing form is a bilinear form on the Lie algebra that captures key properties of this algebra's structure.

Let's denote $\mathfrak{k}$ as the Lie algebra of $K$. If $x,y \in \mathfrak{k}$ are any two elements in this Lie algebra, the Killing form is given by:

$B(x, y) = tr(ad_x \circ ad_y)$

where $ad_x$ and $ad_y$ are adjoint operations, which involve the commutator of the Lie algebra: $ad_x(y) = [x, y]$. Here, $tr$ denotes the trace of the corresponding linear map, and the commutator $[x,y]=xy-yx$signifies the Lie bracket operation. 

For compact groups and their corresponding Lie algebras, the Killing form actually turns out to be negative definite. This property is quite useful. In fact, one alternative definition for a compact Lie algebra is a Lie algebra with a negative definite Killing form.

The point of the Killing form, in the context of the eigenvalue computations for the Casimir operator, is that it provides an invariant way to measure lengths or more generally to take scalar products in the underlying vector space of the Lie algebra. This scalar product structure turns out to be just the right tool to compute eigenvalues of the Casimir operator.

Keep in mind that while the Killing form gives valuable structure to the Lie algebra, as always in mathematics, it's the particular properties of a given situation (like compactness here) which let you reduce this general tool to explicit formulas.

# consider the compact group $K$, how to calculate the dimension of the representation $dim(\sigma)$?

Calculating the dimension of a representation $\sigma$ for a compact group $K$ involves a deep understanding of the fundamental theorem of finite-dimensional representations of compact groups, also known as Peter-Weyl theorem.

For a compact group $K$, every finite-dimensional representation is completely reducible, meaning it can be decomposed into a direct sum of irreducible representations. 

A basis for the representation $\sigma$ can be given by matrix entries of finite-dimensional irreducible unitary representations.

To compute the dimension of an irreducible representation $\sigma$, one approach involves using the weight theory.

Assume that we have a maximal torus $T$ of your group $K$, and choose a set of positive roots $R^{+}$ in the corresponding root system $R$ of the Lie algebra of $K$. Based on these choices, certain weights in the weight lattice of the dual of the Lie algebra of $T$ are identified as dominant. Representation of $K$ is completely determined by specifying the highest weight in $\sigma$.

Here, the weight lattice is a free abelian group whose rank is the dimension of $T$.

Then the dimension of the representation $\sigma$ (determined by the highest weight $\lambda$), or $dim(\sigma)$, can be given by Weyl's dimension formula:

$dim(\sigma) = \prod_{\alpha\in R^{+}}\frac{\langle\lambda+\rho,\alpha^{\vee}\rangle}{\langle\rho,\alpha^{\vee}\rangle}$

where $\rho$ is half of the sum of all positive roots, $\langle,\rangle$ is the associated natural pairing, and $\alpha^{\vee}$ is the coroot associated with $\alpha$.

This is, however, a somewhat sophisticated formula and the calculation could be quite complex based on the specific structure of the group $K$and the representation $\sigma$.

# then how to verify the bounds for $dim(\sigma)$ and $\sum_{\sigma \in \hat{K}}dim(\sigma)^{-c_{2}}$.


The bounds you've mentioned, i.e., $dim(\sigma) \leq \lambda_{\sigma}^{c_1}$ and $\sum_{\sigma \in \hat{K}}dim(\sigma)^{-c_2} < \infty$ for $c_1$ and $c_2$ positive, deal with subtle properties of representations for compact Lie groups and make extensive use of highly advanced topics in Lie theory. Verifying these bounds can be quite nontrivial and the below isn't a formal proof, just a sketch of how one might approach it:

1. For the first property $dim(\sigma) \leq \lambda_{\sigma}^{c_1}$, we might consider the role of the highest weights. In this case, we rely on the fact that the eigenvalues $\lambda_{\sigma}$ of the Casimir operator $\mathcal{C}$ correspond to certain quadratic forms on the weight spaces, and the dimension of the representation is related to the number of integral points in these weight spaces. The bound follows from estimates of the growth of these integral points in increasing radius balls in the weight spaces.
    
2. The second property $\sum_{\sigma \in \hat{K}}dim(\sigma)^{-c_2} < \infty$ uses the Peter-Weyl theorem, which asserts an isomorphism between the regular representation of the Lie group and a sum of the square of the dimensions of its irreducible unitary representations. Because the regular representation is square-integrable, this leads to the concept of 'Plancherel measure', a probability measure supported on the set of equivalence classes of irreducible representations $\hat{K}$ such that the measure of a subset of $\hat{K}$ can be understood as the "proportion" of the regular representation supported there. Therefore, $\sum_{\sigma \in \hat{K}}dim(\sigma)^{-2} < \infty$.
    

Still, this falls far from a complete derivation of the properties you stated. Complete proofs would likely involve sophisticated analysis such as the asymptotic representation theory of compact groups, using tools from harmonic analysis and lie theory. I suggest consulting a detailed text on representation theory for a rigorous treatment, as the proofs are likely beyond the scope of a text-based dialogue.


# now with information provided, show that $\sum_{\sigma \in \hat{K}}dim(\sigma)\mid\mid v_{\sigma}\mid\mid \leq \sum_{\sigma \in \hat{K}}dim(\sigma)\lambda^{-s}_{\sigma}\mid\mid \pi(\mathcal{C})^{s}v_{\sigma}\mid\mid$ for a sufficiently large $s$. 

Given $\sigma \in \hat{K}$, on the left-hand side of the inequality, we have $dim(\sigma)||v_{\sigma}||$ in each of the summands. On the right-hand side, we have $dim(\sigma)\lambda_{\sigma}^{-s}|| \pi(\mathcal{C}^{s})v_{\sigma}||$ as the summands.

From the properties of the Casimir operator, we know that in each representation space, it scales by $\lambda_{\sigma}$. After applying Casimir operator $s$ times on $v_{\sigma}$, we get a scaling of $(\lambda_{\sigma})^{s}$, resulting in $|| \pi(\mathcal{C}^{s})v_{\sigma}|| = \lambda_{\sigma}^{s}||v_{\sigma}||$.

Multiplying both sides by of this equality by $\lambda_{\sigma}^{-s}$ and comparing the summands from the left and right sides of your inequality, we can see that as $s$ increases, the right-hand-side summand is strictly larger, assuming $\lambda_{\sigma}>1$.

However, if we are dealing with eigenvalues $\lambda_{\sigma}$ that are less than 1, then choosing $s$ large enough such that $\lambda_{\sigma}^s < 1$, will still ensure that the right-hand-side summand is larger.

Thus, the inequality given:

$\sum_{\sigma \in \hat{K}}dim(\sigma)||v_{\sigma}|| \leq \sum_{\sigma \in \hat{K}}dim(\sigma)\lambda_{\sigma}^{-s}||\pi(\mathcal{C}^{s})v_{\sigma}||$,

holds for a sufficiently large $s$. Please note that this explanation assumes that all eigenvalues of the Casimir operator are non-negative.