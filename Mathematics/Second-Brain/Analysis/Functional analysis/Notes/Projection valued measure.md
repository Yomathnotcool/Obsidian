# Tags
#Functional-analysis #measure-theory #spectral-theory #representation #GPT

---

# References


---


# Other related files


---

# given a unitary representation of $\mathbb{R}^{2}$, then it can be decomposed with respect irreducible one dimensional unitary representations of $\mathbb{R}^{2}$, which are the unitary characters of $\mathbb{R}^{2}$: $\chi_{z}(r)=e^{i<z,r>}, z\in \mathbb{R}^{2}$.


A unitary representation of a topological group $\mathbb{R}^{2}$ on a Hilbert space $H$ is a group homomorphism $\pi:\mathbb{R}\to B(H)$ to the bounded linear operators on $H$ that preserves the group operation and is compatible with the topology of $\mathbb{R}^{2}$, such that its image lies in the group $U(H)$ of unitary operators on $H$.

For the two-dimensional real numbers group $\mathbb{R}^{2}$, a unitary representation $\pi: \mathbb{R}^{2}\to B(H)$ can indeed be decomposed with respect to one-dimensional irreducible unitary representations, often referred to as the unitary characters of the group. 

The expression $\chi_{z}(r)=e^{i<z,r>}$ represents the unitary character associated with a vector $z$ in $\mathbb{R}^{2}$ evaluated at a point $r$ in $\mathbb{R}^{2}$. The function $\chi$ is a function from the group to the complex numbers of modulus 1 that respects the group operation. In this case, the group operation for $\mathbb{R}^{2}$ is ordinary vector addition, while the complex exponential function ensures the output lies within complex numbers of modulus 1 - i.e., it is a unitary operator. 

The decomposition of representation $\pi$ with respect to these characters signifies that each element of $\mathbb{R}^{2}$ can be expressed as a linear combination of these basis vectors, where the basis vectors are determined by the unitary characters of the group. 


# explain in details why do we have this decomposition and how to obtain such decomposition


This decomposition whatsoever comes from group representation theory and it is a concept majorly used in Quantum Mechanics to illustrate state spaces.

In group representation theory, you would choose an abstract group of operations and you convert it or represent it in terms of linear operators acting on a vector space. The motivation behind this theory is to reduce the complex and abstract group structures into linear algebra in which we are more comfortable with.

The decomposition into irreducible representations simply means that you can't find a nontrivial invariant subspace under all the operators of the representation. In practical terms, you can't find a smaller space in which all of the operations of the group stay if restricted to this subspace.

While the theory itself demands a thorough understanding of advanced mathematics, probably the best way to understand it is through examples.

For example, let's take the group of integers under addition, and let it act on the set of real functions in one variable by translation: $(n,f)\to f_n$ with $f_n(x)=f(x+n)$. This is a representation of the integers. It's not irreducible, though, because if you take the space of functions $f$ which are periodic with period 1, the integers still act on this space by translation, and the representation restricted to this space is equivalent to the original one.

So, once we have a group representation and we understand that it might have an invariant subspace for a restricted group of operations, we go on with the irreducible representations.

Now coming to the original point, For $\pi: \mathbb{R}^{2} \to B(H)$,

It can be decomposed into irreducible representations (unitary characters) that are labeled by $\mathbb{R}^{2}$ itself. This set of characters form an orthonormal basis for the space of square integrable functions on $\mathbb{R}^{2}$, and any square integrable function can be expanded in terms of this basis.

This expansion is achieved by performing an integral over the whole set of labels, like this:

$\psi(r) = \int_{\mathbb{R}^{2}} \chi_z(r) a(z) dz$

where $a(z)$ are the expansion coefficients, determined by taking the inner product of the state with the basis vectors:

$a(z) = <\chi_z,\psi> = \int_{\mathbb{R}^{2}} \chi_z^*(r) \psi(r) dr$

For each point in the group manifold $\mathbb{R}^{2}$, associating these coefficients to the characters of the group, we get the original function/operator back. This goes to say that these representations are complete and form a basis for the representation space of the group.

The purpose of using these decompositions or dealing with representations is multi-fold. For instance, we can reduce the number of variables in computations, or deal with symmetries in physical problems. They're particularly useful in quantum mechanics and quantum field theory.


# Namely there exists a Borel projection-valued measure $P$ on $\mathbb{R}^{2}$ such that  the representation $\pi$ of $\mathbb{R}^{2}$ can be written as $\int_{\mathbb{R}^{2}}\chi_{z}(r)dP_{z}, r\in\mathbb{R}^{2}$

Yes, you are correct. The representation of $\mathbb{R}^{2}$ can indeed be expressed as an integral with respect to a projection-valued measure $P$ on $\mathbb{R}^{2}$. This is known as direct integral decomposition of the representation. 

A projection-valued measure is a function defined on the Borel sets (the smallest $\sigma$-algebra containing all open sets) of $\mathbb{R}^{2}$ that takes values in the set of projection operators on the Hilbert space $H$. A projection operator $P$ on $H$ is an operator that satisfies $P^{2}=P$ .

The explicit formula for the representation is given by: 

$\pi(r) = \int_{\mathbb{R}^{2}}\chi_{z}(r)dP_{z}, r\in\mathbb{R}^{2}$

This formula describes the total action of the element r in $\mathbb{R}^{2}$as a [[Projection valued measure#^2cfcf2|superposition]] (via integration) of the actions of the "elementary" characters $\chi_{z}(r)$, each weighted by the corresponding projection operator dP_{z}. This highlights the intrinsic connection between the representation theory of groups and the spectral theory of operators in the Hilbert space. 

In other words, the decomposition permits us to think of an action of $\mathbb{R}^{2}$ as being built up from these "smaller" or "simpler" actions. 


# $dP_{z}$, what is the definition of superposition and how to understand the projection valued measure as a sup-erpositon

^2cfcf2
The concept of [Quantum superposition - Wikipedia](https://en.wikipedia.org/wiki/Quantum_superposition) in quantum mechanics is a fundamental principle that allows particles to be in various states at once. This principle allows the combination of 'basis states' (or vectors) in a Hilbert space to create a new state. 

A projection-valued measure (PVM) is a function that assigns to each event in a $\sigma$-algebra of sets a projection operator on a Hilbert space. The PVM allows us to generalize standard measure theory concepts to operations acting in a vector space. When we cannot define a standard measure for a particular set of events, the PVM can provide an alternative. 

Projection operators are used in quantum mechanics to denote the measurement of a certain state. If you measure the state of a quantum system, the probability of finding the system in a certain state is given by the length (squared) of the component of the state vector in the direction of the measured state. Once measured, the quantum system 'collapses' into the state that has been measured.

Now, speaking of the projection-valued measure as a superposition, in the context of $\pi(r) = \int_{\mathbb{R}^{2}}\chi_{z}(r) dP_z$. Here $\chi_z$ are the characters of the group $\mathbb{R}^{2}$ that form an orthonormal basis in a well-defined sense in the space of square-integrable functions on $\mathbb{R}^{2}$. 

We are 'superposing' or integrating the unitary characters (which are the simplest representation of the group and are multiplied by the PVM $dP_{z}$), in order to build the wider representation $\pi$ of the group. 

Each unitary character $\chi_{z}(r)$ is multiplied by the infinitesimal projection operator $dP_{z}$ which is essentially projecting the function onto a 'small neighborhood' around each point $z$ in $\mathbb{R}^{2}$, and this process is integrated or 'summed' over the entire group. This can be thought of as a 'superposition' of the projections on all of the small or different regions. 

Thus, the PVM provides a manner of 'weighting' the contribution of each $\chi_{z}(r)$ when forming the representation $\pi(r)$. The weights are chosen in such a way as to make the representation $\pi$ unitary.

This kind of integral where different terms in the integral are superposed is called a 'direct integral', referring to a sort of integral that represents a superposition of different objects, weighted by a measure.


# $\int_{\mathbb{R}^{2}}\chi_{z}(r)dP_{z}, r\in\mathbb{R}^{2}$, explain the details about the meaning of this integral

The integral you propose,

$\int_{\mathbb{R}^{2}}\chi_{z}(r)dP_{z}$

is called a [Direct integral - Wikipedia](https://en.wikipedia.org/wiki/Direct_integral), which merges the concepts from group representation theory, operator theory and measure theory. 

Let's consider a measurable family of Hilbert spaces (i.e., a Hilbert bundle) indexed by $\mathbb{R}^{2}$. Meaning to each point $z$ in $\mathbb{R}^{2}$, we associate a Hilbert space $H_z$. In this context, $\chi_z(r)$ is an operator acting on the Hilbert space $H_z$. 
[Vector bundle - Wikipedia](https://en.wikipedia.org/wiki/Vector_bundle)

The projection-valued measure $P$, assigns to each Borel set $\mathcal{B}$ of $\mathbb{R}^{2}$ a projection operator $P(B)$ on the Hilbert space $H$ such that:

1. $P(\emptyset) = 0$.
2. For any disjoint collection $\{B_i\}$ of Borel sets, $P(\bigcup_i B_i) = \sum_i P(B_i)$.
3. $P_{z} = P(\{z\})$.

So, $dP_{z}$ can be thought of as an "infinitesimal" projection operator associated with an "infinitesimal" subset of $\mathbb{R}^{2}$ containing the point $z$.

The direct integral is then a kind of "continuous sum" - an integral version of a direct sum of Hilbert spaces. In the context of group representations, it provides a way to "add together" all these representation spaces associated with "each point" $z$ in $\mathbb{R}^{2}$, in a way governed/weighted by the projection-valued measure $P$.

In the integral

$\int_{\mathbb{R}^{2}}\chi_{z}(r)dP_{z}$,

we are picturing integrating $\chi_z(r)$ across all of $\mathbb{R}^{2}$, where $\chi_z(r)$ acts on the Hilbert space associated to each $z$, each multiplied by the infinitesimal projection operator $dP_{z}$. As such, it ensures that the integration yields another operator and summarizes the joint action of all these "elementary" operations into an overall action on the Hilbert space $H$. 

This interpretation requires certain technical conditions to ensure this "continuous sum" of Hilbert spaces is well-defined and results in another (well-behaved) Hilbert space, and the integral itself is a well-defined bounded operator.

# combine all the information together, for a square integral function $\psi(x)=\int_{\mathbb{R}^{2}}\chi_{z}(x)a(z)dz$, and the unitary operator $\pi(r)=\int_{\mathbb{R}^{2}}\chi_{z}(r)dP_{z}, r\in\mathbb{R}^{2}$, then how to define the action of $\pi(r)$ on $\psi$ explicitly by those formula?

	Keeping in mind that $\pi(r)$ is an operator acting on the function $\psi(x)$, we may write the action of $\pi(r)$ on $\psi$ as:
	
	$\pi(r)\psi(x) = (\int_{\mathbb{R}^{2}}\chi_{z}(r)dP_{z})\psi(x)$
	
	Given that $\psi(x) = \int_{\mathbb{R}^{2}}\chi_{z}(x)a(z)dz$, we can substitute this into the equation:
	
	$\pi(r)\psi(x) = \int_{\mathbb{R}^{2}}\chi_{z}(r)dP_{z}(\int_{\mathbb{R}^{2}}\chi_{z}(x)a(z)dz)$
	
	After the interchange of the order of integration and the action of the projection operator (dPz), we get the following expression:
	
	$\pi(r)\psi(x) = \int_{\mathbb{R}^{2}}\int_{\mathbb{R}^{2}}\chi_{z}(r)\chi_{z}(x)a(z)dP_{z}dz$
	
	It is clear that this expression can be technically complex, but it essentially describes the action of the operator $\pi(r)$ on the square integral function $\psi(x)$, where the contribution of each elementary operation $\chi_z(r)\chi_z(x)$ is weighted by the coefficient function $a(z)$ and the projection operator $dP_{z}$.


# I understand that $P_{z}$ is the projection to the single point $z$ but what is the meaning of the notation $dP_{z}$?

The notation $dP_{z}$ represents the measure generated by the projection-valued measure $P$ at the point $z$. 

Typically, "$dz$" would denote a small change in $z$, or an infinitesimal, in the usual differential notation. However in the context of the projection-valued measure, "$dP_{z}$" does not correspond to an "infinitesimal change" in the projection $P$. Instead, it represents a "small" or "infinitesimal" projection associated with a "small" (in the measure-theoretic sense) subset of the space containing the point $z$. Therefore, as such, it is a measure generated by the projection or an "infinitesimal" projection operator. 

It's similar in nature to the usage of "$dx$" in the Lebesgue integral which denotes the Lebesgue measure. Likewise, "$dP_{z}$" refers to the projection measure at the point $z$ in its respective space. 

Furthermore, the specific meaning of "$dP_{z}$" can heavily depend on the specific mathematical context and the properties of the projection-valued measure $P$. One commonly assumed property is that P is countably additive, which means that it correctly measures (countable) disjoint unions of subsets. Additionally, projection-valued measures are positive in the sense that they assign nonnegative values to all measurable sets. This is similar to probabilities which can be understood as a measure that is countably additive and assigns a total "size" of 1 to the whole space. 

In the integral $\int_{\mathbb{R}^{2}}\chi_{z}(r)dP_{z}$, aside from the standard conditions that make this operator integral well-defined, the projection measure "$dP_{z}$" is used to weight the contributions from different points in the space $\mathbb{R}^{2}$.


# then the character $\chi_{z}$ forms an orthonormal basis?

Yes, in the space of square-integrable functions over the additive group $\mathbb{R}^{2}$, the characters $\chi_{z}$ do indeed form an orthonormal basis. 

The term "characters" in this context refers to homomorphisms from the group $\mathbb{R}^{2}$ (endowed with the group operation of vector addition) to the circle group $S^1$ of all complex numbers with absolute value 1 (with the group operation of multiplication). 

Because $\mathbb{R}^{2}$ is a locally compact abelian group, the structure theorem for unitary representations tells us that every irreducible unitary representation is one-dimensional. Thus, the irreducible representations of $\mathbb{R}^{2}$ are in one-to-one correspondence with its characters.

More information about the structure theorem: [Irreducible representations of an abelian group $G$ are $1$-dimensional. - Mathematics Stack Exchange](https://math.stackexchange.com/questions/3789088/irreducible-representations-of-an-abelian-group-g-are-1-dimensional)

These characters (which we denote as $\chi_{z}$, with $z\in \mathbb{R}^{2}$) are given by the recipe $\chi_{z}(r) = e^{}$, where $<.,.>$represents the standard inner product on $\mathbb{R}^{2}$.

It turns out that these characters form an orthonormal basis of $L^2(\mathbb{R}^{2})$, the space of square-integrable functions over $\mathbb{R}^{2}$. This fact is a manifestation of the [Pontryagin duality - Wikipedia](https://en.wikipedia.org/wiki/Pontryagin_duality) for locally compact abelian groups, and can be informally understood as a higher-dimensional analogue of Fourier series (with the irreducible characters playing the role of complex exponentials). Specifically, the characters satisfy the orthonormality relations:

$\int_{\mathbb{R}^{2}} \chi_{z}(r) \overline{\chi_{w}(r)} dr = \delta(z-w)$

where $\delta$ is the Dirac delta function, and the overline denotes complex conjugation. This relation says that the basis vectors are orthogonal (as the integral is zero for $z\neq w$) and normalized (as the integral is one for $z=w$).

It is this orthonormality property that allows us to represent any square-integrable function as a linear combination (technically, an integral) of the basis elements, which is essentially a Fourier transform in $\mathbb{R}^{2}$.


# so we can think about the action of $\pi(r)$ by the projection-valued measure, it's like we project to a small neighborhood of $z$ then the function twisted by character $\chi_{z}$ at this neighborhood, the integral means we do the "operation" over the entire space

Yes, you have captured the essence of the action of $\pi(r)$ very well. The notation $\pi(r)$ represents a unitary operator that acts on functions over $\mathbb{R}^{2}$. This operator is "built" by integrating over all of $\mathbb{R}^{2}$ and at each point "$z$", applying the character operation $\chi_{z}(r)$ and a projection specified by the measure $dP_{z}$.

Indeed, you can interpret $dP_{z}$ informally as projecting onto a small neighborhood around a point $z$ in $\mathbb{R}^{2}$. In each such small "neighborhood", the projection-value measure $dP_{z}$ picks out the component of our function along the direction of $z$, and the character $\chi_{z}(r)$ performs a "twisting" operation determined by the group element $r$ and the point $z$. Then, integrating against $dP_{z}$ and summing over all $z$ in $\mathbb{R}^{2}$ combines all these small "twisted" components into a whole that constitutes the action of the operator $\pi(r)$.

This reflects the general principle in representation theory that a unitary representation of a group can be built by piecing together smaller "elementary" operations (specified by the characters) in a manner governed by some measure (in this case, projection-valued). The resulting operator, $\pi(r)$ in this case, encapsulates the action of the original group on the function or state in question. 

# by this understanding and projection-valued measure, how to show that $\pi(r)$ is unitary

The operator $\pi(r)$ is said to be unitary if it preserves the inner product in the Hilbert space. In other words, for all $\psi$ and $\phi$ in the Hilbert space, we have:

$<\pi(r)\psi, \pi(r)\phi> = <\psi, \phi>$

In showing that $\pi(r)$ is unitary, we use the integral form of the operator $\pi(r)$ and the properties of the characters and the projection valued measure. So we have to show that:

$<\int_{\mathbb{R}^{2}}\chi_{z}(r)dP_{z}\psi, \int_{\mathbb{R}^{2}}\chi_{z}(r)dP_{z}\phi> = <\psi, \phi>$

Due to the properties of the inner product, we can take the integral out:

$<\int_{\mathbb{R}^{2}}\chi_{z}(r)dP_{z}\psi,\phi> = <\psi, \phi>$ 
Since we have a projection valued measure, $dP_{z}$ $\psi$ and $dP_{z}$ $\phi$are vectors in the same reduced Hilbert space that $dP_{z}$ projects onto:

$\int_{\mathbb{R}^{2}}<\chi_{z}(r)dP_{z}\psi, \chi_{z}(r)dP_{z}\phi> = <\psi, \phi>$

Noting that each character $\chi_{z}(r)$ is a phase factor (a complex number with modulus 1), and using the property that characters preserve norm:

$\int_{\mathbb{R}^{2}} = <\psi, \phi>$

This shows that $\pi(r)$ is indeed unitary, since it preserves the inner product $<\psi, \phi>$ in the Hilbert space.

Please note that the above calculation relies on the strong convergence property of integrals with respect to projection valued measures, as well as the continuity of the inner product. These properties follow from the assumptions in the direct integral theory in functional analysis and measure theory.