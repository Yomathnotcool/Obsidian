## Tags:
#number-theory #l-adic #padic #trace-formula #Langlands-program #Galois-representation


---

# The definition of $l$-adic representation
In Galois representation theory, an $l$-adic representation refers to a representation of the absolute Galois group of a field, where $l$ is a prime number.

Formally, an $l$-adic representation of the Galois group of a field $K$ is a finite-dimensional vector space $V$ over a field $F$ with additional structure. This additional structure consists of a continuous action of the Galois group $Gal(K)$ on $V$, where $Gal(K)$ denotes the absolute Galois group of K. The term "$l$-adic" arises from the fact that the base field $F$ typically involves completion at the prime $l$, such as the field of p-adic numbers when $l = p$.

Now, let's consider an explicit example with $l$ = 3. Suppose we have a field $K$, and its absolute Galois group $Gal(K)$ acts on a three-dimensional vector space $V$ over a field $F$. We can denote this $l$-adic representation as $V_{3}$. The action of $Gal(K)$ on $V_3$ is given by a continuous homomorphism:
$$

\rho: Gal(K) -> GL(3, F)
$$

where $GL(3, F)$ represents the general linear group of 3x3 matrices with entries in $GL(3, F)$.

This explicit example showcases a three-dimensional $l$-adic representation when $l$ = 3.

For the base field, we can take $F$ as a [[Introduction to P-adic world|p-adic field]], it has very different behaviour when $l=p$ or $l\not=p$.

More specifically, a[[Introduction to P-adic world|p-adic field]] is a completion of a number field (a finite extension of the rational numbers) with respect to a non-archimedean absolute value that extends the $p$-adic absolute value on the rational numbers. The characteristic of a field refers to the smallest prime number $p$ such that the sum of 1 with itself $p$ times is equal to 0.

When $l \neq p$, it implies that the prime $l$ does not divide the characteristic of the[[Introduction to P-adic world|p-adic field]]. This means that the $l$-adic and [[Introduction to P-adic world|p-adic field]] have distinct characteristics, and their cardinalities (sizes) have different divisibility properties.

In Galois representation theory, the $l$-adic representations of the absolute Galois group of a field capture information about the field's arithmetic properties and can have different behavior depending on whether $l = p$ or $l \neq p$ for [[Introduction to P-adic world|p-adic field]].

# Example:
Let's consider the[[Introduction to P-adic world|p-adic field]] $\mathbb{Q}_5$, which is the completion of the rational numbers with respect to the $5$-adic absolute value. Now, let's work with an $\ell$-adic representation, where $\ell=3$.

We can consider the absolute Galois group $G=\text{Gal}(\overline{\mathbb{Q}_5}/\mathbb{Q}_5)$, where $\overline{\mathbb{Q}_5}$ is the algebraic closure of $\mathbb{Q}_5$. Let's denote this Galois group as $G$.

Now, let's define a 3-adic representation. Suppose we have a three-dimensional vector space $V$ over some field $F$. The $3$-adic representation is a continuous homomorphism:

$$  
\rho : G \to \text{GL}(3, F)  
$$

where $\text{GL}(3, F)$ represents the general linear group of 3x3 matrices with entries in $F$.

For our specific example, let's take $F$ to be the field $\mathbb{Q}_3$, the completion of the rational numbers with respect to the $3$-adic absolute value. So, our 3-adic representation can be denoted as $V_3$.

This example showcases a three-dimensional 3-adic representation when $l=3$ and $p=5$, where $l \neq p$.