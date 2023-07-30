
## Tags
#number-theory #notes #L-function #history

---

## References:


---
## Other related notes:


---

The most famous $L$-function is Riemann's $\zeta$-function:
$$
\begin{equation*}
    \zeta(s)=\sum_{n\geq 1}n^{-s}\ \ \ \ (\mathfrak{Re}s> 1).
\end{equation*}
$$

By an easy argument using the fact that every $n\geq 1$ has a unique prime factorisation, one shows that $\zeta(s)$ can be written as an Euler product
$$
\begin{equation*}
    \zeta(s)=\prod_{p\ prime} (1-p^{-s})^{-1}\ \ \ \ (\mathfrak{Re}s >1).
\end{equation*}
$$
This shows that $\zeta(s)$ does not have any zeroes in the region $\mathfrak{Re}s >1$.

We define the completed $\zeta$-function by $Z(s)=\pi^{s/2}\Gamma(s/2)\zeta(s)$. Here we have used the $\Gamma-$function
$$
\begin{equation*}
    \Gamma(s)=\int^{\infty}_{0}e^{-t}t^{s-1}\text{d}t\ \ \ \ (\mathfrak{Re}s>0). 
\end{equation*}
$$
#### Rem:
Let's recall a few important properties of $\Gamma$-function:

 1. The Gamma function satisfies the functional equation $\Gamma(s+1)=s\Gamma(s)$;
 2. The Gamma function has an analytic continuation on $\mathbb{C}$ with simple poles at $s=0,-1,-2,...$
 3. The reciprocal of the Gamma function is entire, i.e. 
$$
    \begin{equation*}
        \frac{1}{\Gamma(s)}=\frac{\sin(\pi s)}{\pi}\Gamma(1-s)
    \end{equation*}
$$
    is entire.

During the proofs of those properties, the identity $$\int^{\infty}_{0}e^{-(ax^{2}+b)} \text{d}x=\sqrt{\frac{\pi}{a}}$$ is essential.

#### Thm :: Possion summation

^eb3e0f

Given a Schwazrtz function $f$, and $\hat{f}$ is the Fourier transform, then
$$
\begin{equation*}
    \sum_{n\in\mathbb{Z}}f(n)=\sum_{m\in\mathbb{Z}}\hat{f}(m).
\end{equation*}
$$
#### Proof:
Denote $F(x)=\sum_{n\in\mathbb{Z}}f(x+n)$, which is 1-periodic, then we can calculate the Fourier coefficients: 
$$
\begin{equation*}
    \hat{F}(k)=\int^{1}_{0}F(x)e^{-2\pi ikx}\text{d}x=\int^{1}_{0}\sum_{n\in\mathbb{Z}}f(x+n)e^{-2\pi ikx}\text{d}x.
\end{equation*}
$$
Because $f$ is Schwartz, so this integral converges uniformly.
$$
\begin{equation*}
    =\sum_{n\in\mathbb{Z}}\int^{n+1}_{n}f(x)e^{-2\pi ikx} \text{d}x=\int_{\mathbb{R}}f(x)e^{-2\pi ikx}\text{d}x=\hat{f}(k),
\end{equation*}
$$
by the definition of Fourier series of $f$, $F(x)=\sum\limits_{k\in\mathbb{Z}}\hat{f}(k)e^{ikx}$. Choosing $x=0$, we get the formula as desired:
$$
\begin{equation*}
    \sum_{n\in\mathbb{Z}}f(n)=\sum_{k\in\mathbb{Z}}\hat{f}(k).
\end{equation*}
$$


#### Def :: Jacobi theta function

The Jacobi theta function, or called as the classical theta function is the on right half plane defined by 
$$
\begin{equation*}
    \theta(s)=\sum_{n\in\mathbb{Z}}e^{-\pi n^{2}s},\ \ \ \ \mathfrak{Re}s>0.
\end{equation*}
$$
The theta function here is a holomorphic function on the right half plane.


#### Lem
By the [[Riemann theory#^eb3e0f| Possion formula]], one can prove that $\theta(s)$ satisfies the functional equation
$$
\begin{equation*}
\theta(\frac{1}{s})=\sqrt{s}\theta(s).
\end{equation*}
$$


#### Proof:
Given $g(x)=e^{-\pi tx^{2}}$, in order to get the formula, we need to calculate its Fourier transform of $g(x)$, 
$$
\begin{equation*}
    \hat{g}(t)=\int^{+\infty}_{-\infty}e^{-\pi tx^{2}}\cdot e^{-2\pi iyx}\text{d}x=e^{\pi}(\frac{iy}{\sqrt{t}})\int^{+\infty}_{-\infty}e^{-\pi(\sqrt{t}x+\frac{ix}{\sqrt{t}})^{2}}\text{d}x=\frac{1}{\sqrt{t}} e^{-\pi \frac{y^{2}}{t}}
\end{equation*}
$$
Then 
$$
\begin{equation*}
    \theta(s)=\sum_{n\in\mathbb{Z}}e^{-\pi n^{2}s}=\sum_{n\in\mathbb{Z}}g(n)=\sum_{m\in\mathbb{Z}}\hat{g}(m)=\frac{1}{\sqrt{s}}\sum_{m\in\mathbb{Z}}e^{-\pi \frac{n^{2}}{s}}=\frac{1}{\sqrt{s}}\theta(\frac{1}{s}).
\end{equation*}
$$
Before we moved to the proof of the analytic continuation of Riemann Zeta function, we need to know the behaviour of the theta functions near zero and infinity to justify the Mellin transform later in proof.

For theta function, there exists a constant $C=\pi-1> 0$ such that for all sufficiently small $t>0$ the following inequality holds: 
$$
\begin{equation*}
    |\theta(t)-t^{\frac{1}{2}}|< e^{-C/t}.
\end{equation*}
$$

Usually the Mellin transform is that Given a function $f(t)$ with $\mathfrak{Re}t>0$, its Mellin transform is defined to be
$$
\begin{equation*}
    \mathcal{M}_{f}(s):=\int^{\infty}_{0}f(t)t^{s-1}\text{d}t,
\end{equation*}
$$
which is defined for all values $s$ for which the integral exists.
#### Thm :: Properties of Riemann zeta function
The function $Z(s)$ can be continued to a meromorphic function on the whole complex plane with a simple pole at $s=1$ with residue 1, a simple pole at $s=0$ with residue -1, and no other poles. It satisfies the functional equation 
$$
\begin{equation*}
        Z(s)=Z(1-s)
\end{equation*}
$$
i.e., $\zeta(s)$ satisfies the functional equation
$$
\begin{equation*}        \pi^{s
/2}\Gamma(\frac{s}{2})\zeta(s)=\pi^{(1-s)/2}\Gamma(\frac{1-s}{2})\zeta(1-s).
\end{equation*}
$$


#### Proof:
We express $Z(s)$ as the Mellin transform of a modular form. The modular form we need is Jacobin theta-function. But theta function behaves like $t^{-1/2}$ at 0 and converges rapidly to 1 at infinity. So we need to introduce some correction term to make the integral converge. So We now consider the Mellin transform of $\theta$, defined as
$$
 \begin{equation*}
    \mathcal{M}_{\theta}(s)=\int^{\infty}_{1}(\theta(t)-1)t^{s-1}\text{d}t+\int^{1}_{0}(\theta(t)-\frac{1}{\sqrt{t}})t^{s-1}\text{d}t,\ \ \ \ (\mathfrak{Re}> 1).
\end{equation*}
$$
From this we get the following equation, due to Riemann: $Z(s)=\frac{1}{2}\mathcal{M}_{\theta}(s/2)$. And we can rewrite $\mathcal{M}_{\theta}(s/2)$ as follows.  We obtain, for $\mathfrak{Re}s>1$, 
$$
\begin{align*}
\int^{1}_{0}\bigg(\theta(t)-\frac{1}{\sqrt{t}}\bigg)t^{\frac{s}{2}-1}\text{d}t
&= \int^{1}_{0}\theta(t)t^{\frac{s}{2}-1}\text{d}t-\int^{1}_{0}t^{\frac{s-1}{2}}\text{d}t\\
&= \int^{1}_{0}\bigg(\sum_{n\in\mathbb{Z}}e^{-\pi n^{2}t}\bigg)t^{\frac{s}{2}-1}\text{d}t-\frac{2}{s-1}\\
&= \int^{1}_{0}t^{\frac{s}{2}-1}\text{d}t+2\int^{1}_{0}\bigg(\sum_{n\geq 1}e^{-\pi n^{2}t}\bigg)t^{\frac{s}{2}-1}\text{d}t +\frac{2}{1-s}\\
&= 2\sum_{n\geq 1}\int^{1}_{0}e^{-\pi n^{2}t}t^{\frac{s}{2}-1}\text{d}t+\frac{s}{2}+\frac{2}{1-s}
\end{align*}
$$
Therefore we have
$$
\begin{equation*}
    \mathcal{M}_{\theta}(s)=2\sum_{n\geq1}\int^{\infty}_{0}e^{-\pi n^{2}t}t^{\frac{s}{2}-1}\text{d}t+\frac{2}{s}+\frac{2}{1-s}
\end{equation*}
$$
By the substitution $t\mapsto 1/t$ we get
$$
\begin{equation*}
    \frac{1}{2}\mathcal{M}_{\theta}(s)=\pi^{-\frac{s}{2}}\Gamma(\frac{s}{2})\zeta(s)+\frac{1}{s}+\frac{1}{1-s}.
\end{equation*}
$$
Both integrals in the definition of $\mathcal{M}_{\theta}(s)$ converge, it's an entire function. Then we can define an analytic continuation of the zeta function on the whole complex plane, which agrees with $\zeta(s)$ for $\mathfrak{Re}s>1$, by 
$$
\begin{equation*}
    \zeta(s)=\frac{\pi^{\frac{s}{2}}}{\Gamma(\frac{s}{2})}\bigg(\frac{1}{2}\mathcal{M}_{\theta}(s)-\frac{1}{s}-\frac{1}{1-s}\bigg),
\end{equation*}
$$
whose poles are at $s=0$ or $s=1$ as $\mathcal{M}_{\theta}(s)$ and $\frac{1}{\Gamma(s)}$ are entire. We can replace $s\Gamma(\frac{s}{2})$ by $\frac{2}{s}\Gamma(s/2)=2\Gamma(s/2+1)$ which converges to $2\Gamma(1)$ as $s$ goes to zero. Hence it's nonzero and the only pole is at 1. We now compute the residue:
$$
\begin{equation*}
    \lim_{s\mapsto 1}(s-1)\frac{\pi^{s/2}}{\Gamma(s/2)}\bigg(\frac{1}{2}\mathcal{M}_{\theta}(s)-\frac{1}{s}-\frac{1}{1-s}\bigg)=\frac{\pi^{1/2}}{\Gamma(1/2)}=1.
\end{equation*}
$$
Now the only thing left is $Z(s)=Z(1-s)$. Since $Z(s)=\frac{1}{2}\mathcal{M}_{\theta}(s)-\frac{1}{s}-\frac{1}{1-s}$, which means we only need to check that $\mathcal{M}_{\theta}(s)=\mathcal{M}_{\theta}(1-s)$, and we need to use $y=\frac{1}{t}$:
$$
\begin{align*}
        \mathcal{M}_{\theta}(s)=
        &= \int^{1}_{0}y^{-s/2-1}(\theta(1/y)-1)\text{d}y+\int^{\infty}_{1}y^{-s/2-1}(\theta(1/y)-\sqrt{y})\text{d}y\\
        &= \int^{1}_{0}y^{(-1/2-s/2)}(\theta(y)-\frac{1}{\sqrt{y}})\text{d}y+\int^{\infty}_{1}y^{-1/2-s/2}(\theta(y)-\sqrt{y})\text{d}y\\
        &=\mathcal{M}_{\theta}(1-s).
\end{align*}
$$
Now the proof is complete.
\end{proof}