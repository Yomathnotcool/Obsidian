# Tags
#lie-algebra #algebra #linear-space #matrix #notes 

---

# References


---


# Other related files


---

To prove that $B^n = 0$, we can use the concept of the trace.

First, let's take the trace of both sides of the given equation: $AB - BA = B$. The trace of a matrix is the sum of its diagonal elements.

$Tr(AB - BA) = Tr(B)$

Now, we know that the trace of a sum is equal to the sum of the traces:

$Tr(AB) - Tr(BA) = Tr(B)$

Since multiplication of matrices is not commutative in general, we cannot directly simplify $Tr(AB)$ and $Tr(BA)$. However, we can make use of a useful property of traces, namely that $Tr(AB) = Tr(BA)$ if $AB$ and $BA$have the same size. In our case, $AB$ and $BA$ are both $n \times n$matrices, so this property holds.

$Tr(AB) - Tr(AB) = Tr(B)$

$0 = Tr(B)$

Now, let's consider the powers of $B$:

$Tr(B^n) = Tr(B^{n-1}B)$

Expanding this further, we get:

$Tr(B^{n-1}B) = Tr(B^{n-1})Tr(B)$

By repeatedly applying this property, we can write:

$Tr(B^n) = Tr(B^{n-1})Tr(B) = Tr(B^{n-2})Tr(B) = \ldots = Tr(B^2)Tr(B) = Tr(B)Tr(B)$

Since we established earlier that $Tr(B) = 0$, we have:

$Tr(B^n) = 0$

The trace of a matrix is equal to the sum of its eigenvalues. Since $F$ is an algebraically closed field, every matrix has an eigenvalue. Therefore, $B^n$must have eigenvalues that sum up to zero, which means that all its eigenvalues must be zero.

A matrix with all eigenvalues equal to zero is nilpotent. In other words, there exists a positive integer $m$ such that $B^m = 0$. Since $B^{n-1} \neq 0$(otherwise, we would have $Tr(B) = 0$ from the above calculations), the smallest such $m$ is $n$.

Hence, we conclude that $B^n = 0$.



*What if $F$ is not algebraic closed?*

One way to approach this is by considering the Jordan canonical form of the matrix $B$. The Jordan canonical form decomposes a matrix into block matrices representing its Jordan blocks.

Since $F$ is not algebraically closed, there may exist eigenvalues of $B$ that are not in $F$. However, we can consider the eigenvalues and Jordan blocks in an extension field $\overline{F}$ (an algebraic closure of $F$).

Let $\lambda \in \overline{F}$ be an eigenvalue of $B$ and $J_\lambda$ be the corresponding Jordan block. In the Jordan canonical form, $B$ is represented as a direct sum of these Jordan blocks.

Now, let's consider the equation $AB - BA = B$. We can rewrite it using the Jordan canonical form as:

$(A - \lambda I)J_\lambda - J_\lambda (A- \lambda I) = J_\lambda$

Multiplying out, we get:

$AJ_\lambda - \lambda J_\lambda - J_\lambda A + \lambda J_\lambda = J_\lambda$

$AJ_\lambda - J_\lambda A = \lambda J_\lambda$

Remember that in the Jordan canonical form, $J_\lambda$ corresponds to the eigenvalue $\lambda$, and the above equation holds for each Jordan block.

Now, let's consider the powers of $B$. We know that $B^n$ is equal to the sum of the powers of each Jordan block in the Jordan canonical form of $B$. For a Jordan block $J_\lambda$, we have:

$(J_\lambda)^n = \lambda^n J_\lambda$

Therefore, we can write:

$B^n = (J_{\lambda_1})^n + (J_{\lambda_2})^n + \ldots + (J_{\lambda_k})^n$

where $\lambda_1, \lambda_2, \ldots, \lambda_k$ are distinct eigenvalues of $B$.

Since $\lambda^n = 0$ for any eigenvalue $\lambda \in F$, we have $(J_\lambda)^n = 0$ for all Jordan blocks corresponding to eigenvalues in $F$.

However, there may be eigenvalues in $\overline{F}$ that are not in $F$, and $(J_{\lambda})^n \neq 0$ for those blocks. Therefore, we cannot conclude that $B^n = 0$.

Hence, without the assumption of $F$ being algebraically closed, we cannot prove that $B^n = 0$.