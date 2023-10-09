# Tags
#dynamical-system #measure-theory #analysis 

---

# References
This conversation is aimed to understand Lemma 11.28.

[GTM 259 - ISBN978-0-85729-020-5 - Manfred Einsiedler, Thomas Ward - Ergodic Theory - with a view towards Number Theory.pdf](hook://file/WsbMqOJbf?p=R29vZE5vdGVzL+WKqOWKm+ezu+e7nyAoMSk=&n=GTM%20259%20%2D%20ISBN978%2D0%2D85729%2D020%2D5%20%2D%20Manfred%20Einsiedler%2C%20Thomas%20Ward%20%2D%20Ergodic%20Theory%20%2D%20with%20a%20view%20towards%20Number%20Theory%2Epdf)

---


# Other related files


---






## Consider the group $G=SL_{2}(\mathbb{R}),$and the lattice $\Gamma,$then there is the injective from $G$ to the quotient space $X=\Gamma\backslash G$, then for any $x\in X$, there is an isometry from $B^{G}_{r}=\{g|d_{G}(g,e)<r\}$ to $B^{X}_{r}=\{\{y|d_{X}(x,y)<r\}$.

The injective radius is a concept from the field of differential geometry and topology, specifically in the realm of Riemannian geometry. This concept is closely tied to concepts of distance, curvature, and the geometry of spaces.

The injective radius at a given point in a Riemannian manifold is the greatest radius for which the exponential map (which maps each nonzero tangent vector at the given point to a point on the manifold via a geodesic in the direction of that tangent vector) is diffeomorphic (continuous and smoothly invertible) to its image. In other words, it can be thought of as the greatest distance at which the geometry of the manifold around the given point can be faithfully represented in the tangent space at that point.

For the injective mapping from $G$ to the quotient space $X = \Gamma \backslash G$, it implies that an isometry (distance preserving mapping) exists between balls $B^{G}_{r}$ in $G$ and $B^{X}_{r}$ in $X$. The injective radius 'r' is the radius of the largest such balls for which this isometry exists.

Analogously, if we think about curvature, the injective radius can be seen as a measure of how 'flat' the manifold is around a given point. If the manifold is flat, then the injective radius is large, because the geometry of the manifold is well-represented in the tangent space also on larger scales. Conversely, if the manifold is highly curved, then the injective radius will be small, because the curvature of the manifold causes the geometry in the tangent space to differ appreciably from that on the manifold itself already at small scales.

In the context of group theory, this is measuring how 'similar' or faithfully the group structure can be represented in the quotient space on a certain 'scale' given by the injective radius. The manifold $G$, being a Lie group, has a natural Riemannian metric coming from the Killing form and the injective radius is essentially detecting the failure of $\Gamma$ to be a normal (i.e., congruence) subgroup of $G$.
## based on your explanation, how should I interpret $X$ as the tangent space of $G$?
In fact, it's perhaps not the best idea to think of $X$ as the tangent space of $G$ because it's likely to confuse more than clarify. The tangent space is a local linear approximation to a smooth manifold at a certain point, just like a tangent line to a curve or a tangent plane to a surface, and is a vector space. However, $X = \Gamma \backslash G$ is a quotient space of $G$, formed by 'collapsing' each left $\Gamma$-coset in $G$ to a single point. So, it's a non-linear, global object that is typically not a vector space unless $G$ is commutative and $\Gamma$ is a normal subgroup.

Instead, following the analogy, for each point $x \in X$, we can define a Riemannian metric $g_x$ on its tangent space $T_xX$ such that the projection $\pi: G \to X$ is a local isometry. This means that, for each point $g \in G$ and every two tangent vectors $v, w \in T_gG$, we have $g_g(v, w) = g_{\pi(g)}(d\pi_g(v), d\pi_g(w))$, where $d\pi_g$ is the derivative of $\pi$ at $g$. Therefore, for small enough $r$, we have an isometry from $B^G_r$ to $B^X_r$.

Given that $G = SL_2(\mathbb{R})$, its Lie algebra (tangent space at the identity) can be identified with the set of $2 \times 2$ real matrices with trace zero, which carries a natural Riemannian metric coming from the Killing form of $G$. Note however that $\Gamma$ not being a normal subgroup introduces some twists and identifications in the global structure of the manifold $X$ that are not apparent in the (locally isomorphic) tangent space.

## now we assume that $X$ is compact, then there exists a uniform radius $r$ for the entire $X$.
When $X=\Gamma\backslash G$ is a compact space, there exists a uniform injectivity radius $r>0$ for $X$.

This statement can be understood by realizing that compactness is a sort of 'boundedness' condition in topology. Formally, a topological space is compact if every open cover of the space has a finite subcover. In terms of our $r$-balls, this implies that we can cover the entire space of $X$ with a finite number of these balls.

Now, since $X$ is compact, if we pick any $x\in X$ and let $r_x$ be the injective radius at $x$, the collection of all these radii $\{r_x: x\in X\}$ has a positive minimum value (since it is bounded below by zero and it reaches its minimum because $X$ is compact). This minimum is precisely the uniform injectivity radius $r$ you mentioned. This $r$-ball can be considered as the "largest sphere of uniform radius that fits into the space X without crossing any geodesics, no matter where in X you place it". This is a formal way to say that the injectivity property holds uniformly for each point in the space.

The uniformity of the injective radius is also strongly related to the curvature of the space and directly linked with the compactness of $X$. On a highly curved space or non-compact space, the injective radius might vary from point to point. However, in a compact space with "fairly tame" curvature, we can find a uniform injective radius for the entire space.


## I don't understand that why do we need to find the minnimum value but not the upper bound for $r_{x}$
The injective radius is defined as the maximum radius in which one can retain the isometry between the balls $B^{G}_{r}$ in $G$ and $B^{X}_{r}$ in $X$ around a point $x$. So, consider this: you're trying to maintain this isometry for every point in the space.

Because $X$ is compact, you can cover it with a finite number of these balls. Some points will allow for a larger injective radius than others. If you choose the maximum of all $r_{x}$, you may find some points where the radius is too large, breaking the isometry.

To maintain the isometry throughout the entire mapping, across all points $x$, we sensibly choose the smallest (minimum) of these radii. That's why we are concerned with finding a minimum here.

The notion of this uniform injectivity radius is only to ensure that, if we work within this value of $r$, we can always guarantee that the isometry is preserved. The idea is to find a ball size that we can 'safely' use anywhere in $X$ without worry about breaking this isometry, and due to the differences at different points, that happens to be the smallest of the possible radii.

If we were to take an upper bound radius, it might work for some points, but not for others, and so wouldn't provide a uniform standard throughout the space. Hence, the minimum.

## now claim: there exists some $s>0$ depending only on $r$, such that  for $x\in X$ and $l\in\mathbb{R}\backslash\{0\}$ with $|l|<s$ then $h(l)x\not=x$.

The horocycle flow $h(l)$ on $X$ corresponds to a kind of "shift" along the horocycles in the space, where a horocycle at a point is roughly speaking a curve whose normal geodesics all converge to the same point at infinity. One can imagine it as a flow along the "lines of constant curvature" on a hyperbolic space.

Let's attempt to understand the claim and the dependencies involved. It means there's a minimum amount $s$ such that if we "flow" a distance less than $s$, then we're guaranteed to shift the point $x$ to a new point $h(l)x \neq x$.

Since the horocycle flow is continuous, for each $x \in X$ there exists $\epsilon > 0$ such that $h(l)x \neq x$ for $0<|l|<\epsilon$, but this $\epsilon$ may depend on $x$.

However, if $X$ is compact, then a standard argument from analysis implies that there exists a uniform lower bound $s>0$ that works for all $x \in X$. The way to see this is to consider the continuous function $f:X \rightarrow \mathbb{R}$ defined by $f(x) = \sup\{|l| : h(l)x \neq x, 0<|l|<r\}$. As $X$ is compact, $f$ attains a minimum at some $x \in X$, which we take as $s$. This provides an $s$ that works uniformly across all the points in $X$.
 
The value of $s$ will certainly depend on the value of $r$ chosen as the injective radius for the following reason: $r$ effectively determines the "scale" on which we measure distances in $X$. Increasing $r$ would correspond to looking at $X$ under a magnifying glass, and as a result, any given amount of horocycle flow will result in a "larger" perceived displacement of the point $x$. Conversely, decreasing $r$ would correspond to a zooming-out effect, where the same amount of flow results in a "smaller" perceived displacement. Thus, the amount $s$ of horocycle flow needed to guarantee that $x$ is displaced will depend on the chosen injective radius $r$.

In conclusion, the proof of this claim involves a combination of the geometry of the horocycles in $X$, the compactness of $X$, and a standard compactness argument from real analysis. The dependency of $s$ on $r$ comes from how the horocycle flow and the isometry between $G$ and $X$ interact with each other.

Please note that the above argument assumes that the horocycle flow $h(l)$ is a well-defined continuous flow on $X$ regardless of the curvature of $X$. This is certainly true for and an important characteristic of negatively curved spaces, and in particular for $X$ when $G$ is $SL_2(\mathbb{R})$ and $\Gamma$ is a discrete, cocompact (and thus lattice) subgroup.

## could you please explain a standard compactness argument from real analysis in more details

a standard compactness argument using the Extreme Value Theorem (EVT), which is a fundamental result in real analysis.

The Extreme Value Theorem states: If a real-valued function $f$ is continuous on a closed and bounded interval $[a, b]$, then $f$ attains a maximum and a minimum, each at least once, on $[a, b]$.

So, for the problem at hand, let's consider the continuous function $f: X \rightarrow \mathbb{R}$ defined by $f(x) = \sup\{|l| : h(l)x \neq x, 0<|l|<r\}$. This function measures for each $x$ the supremum of the "amount of flow" before the point $x$ moves under the horocycle flow $h(l)$.

We are considering $X$ here as being analogous to the closed, bounded interval $[a, b]$. That is, $X$ is compact. This is where we are applying the concept of compactness.

Applying EVT to $f$ means that there exists some $x \in X$ where $f(x)$ attains its minimum. We choose this minimum to be the $s$ in the question. This $s$ serves as a universal lower bound applicable to all $x \in X$, because for any $x' \in X, f(x') \geq f(x)=s$.

The important idea here is that compactness ensures that continuous functions will always attain maximum and minimum values. We transferred this concept to the non-linear setting of $X$, and used it to find an $s$ that works across the whole space.

This is a pattern you'll find coming up a lot in mathematical analysis: compactness tends to help turn local information (like "$f(x)$ is bounded for each $x$") into global information (like "there is a bound that works for all $x$ at once").


## can you explain why does $s$ depend on $r$ more mathematically formally and in more details


Recall that by definition, the injective radius $r$ at a point $x$ in $X$ is the greatest radius for which the exponential map (which maps each nonzero tangent vector at $x$ to a point on the manifold via a geodesic in the direction of that tangent vector) is a diffeomorphism to its image.

What this means in more concrete terms is that $r$ acts as a kind of "cut-off scale" at each point $x$. Up to this scale (distance) around $x$, the space $X$ looks just like the tangent space at $x$ and hence just like $\mathbb{R}^n$ for some $n$.

The horocycle flow $h(l)$ moves points along the horocycles, curves each of whose normals are geodesics. Now, the "size" of the effect of $h(l)$ is directly tied to this cut-off scale $r$ . If $r$ is large, a "small" move along the horocycle may take us outside the $r$-ball around $x$ in $X$ and hence break the isometry between the $r$-ball in $X$ and the corresponding ball in the Lie group $G$. On the other hand, if $r$ is small, the same "small" move may still keep us within the $r$-ball in $X$.

To guarantee that $h(l)x \neq x$ for $0 <|l|<r$, we want to ensure that $h(l)$ displaces the point $x$ significantly, i.e., $h(l)$ should move $x$ by a distance at least $r$. Therefore, the range of $l$ (which is $s$) will need to be large enough to ensure this displacement. Conversely, if $r$ is small, a smaller $s$ might suffice to create a significant displacement.

This is why we expect $s$ to depend on $r$. Specifically, we might expect that $s$ needs to decrease as $r$ decreases and vice versa, though the exact relationship will also depend on the specific geometry of $X$ and the behavior of the horocycle flow.

Remember, the idea is to find a displacement $s$ such that for any $x$ in the compact space $X$, applying the horocycle flow will result in a "significant" change, hence $h(l)x \neq x$. And in making sure this $s$ applies to any point, the injective radius $r$ comes into play as it directly influences the scale on which we measure this "significance". That's as mathematically formal as the reasoning can be without specific calculations.


## I don't understand your definition with horoccyle: a horocycle at a point is roughly speaking a curve whose normal geodesics all converge to the same point at infinity.

I apologize if my previous explanation about the horocycle was unclear. Let me explain it in a different way.

In the case of a hyperbolic space, you have certain kinds of curves that are important -- geodesics, which are the equivalent of 'straight lines' in hyperbolic geometry, and horocycles, which are a kind of 'circle' but in a hyperbolic sense.

The horocycles have an interesting property in hyperbolic geometry. While in Euclidean geometry every point on a circle is the same distance (the radius) from a central point, a horocycle in hyperbolic geometry is defined differently.

If we fix a point $p$ in the boundary at infinity of hyperbolic space and consider the family of geodesics asymptotic to $p$ (meaning they approach p as they reach the boundary of the hyperbolic space), we can think of a horocycle at this point p as a curve that intersects all these geodesics perpendicularly (meaning forming a right angle with them) and at the same hyperbolic distance from p.

What this means geometrically is that as you move along a horocycle, you aren't getting closer or farther from a fixed central point (unlike in a circle), but instead what’s constant is your speed of approach to a point at infinity. In other words, all geodesics normal to the horocycle converge to the same point at the infinity.

For analogue, if we think in terms of the Poincaré disc model of hyperbolic space, horocycles appear as circles contained within the disc that are tangent to the boundary at a single point. This point is the "center" of the horocycle – all geodesics orthogonal to the horocycle converge to this point as they're extended to the boundary.

In the context of your original question about horocycle flow, imagine you were on a tangent vector field that flows along a horocycle on $X$. The flow parameter $l$ represents how far along the horocycle your flow is.

The crux of the matter is that there is a smallest non-zero amount you can flow, say $s > 0$, so that you do not remain at the same point in the quotient space $X$. This $s$ depends on $r$, the injective radius, because the geometry via the injective radius determines just how much you must flow along the horocycle in order to end up at a new point in $\Gamma \backslash G$.


