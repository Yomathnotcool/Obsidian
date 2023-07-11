
## Tags
#L-function #notes #number-theory #Langlands-program #theta-correspondence #spectral-method #trace-formula 

---

## References:
[[2011.03313] Exotic Monoidal Structures and Abstractly Automorphic Representations for $\\mathrm{GL}(2)$](https://arxiv.org/abs/2011.03313)


---
## Other related notes:
[[Category Theory]]
[[Notes for traces formula]]
[[Snapshots of Number theory]]
[[Why do we need the moderate growth condition for automorphic forms]]



---
\documentclass[12pt,a4paper,english]{article}
\usepackage[a4paper]{geometry}
\usepackage[utf8]{inputenc}
\usepackage[OT2,T1]{fontenc}
\usepackage[keeplastbox]{flushend}
\usepackage{color}
\usepackage{tikz-cd}
\usepackage{appendix}
\usepackage{babel}
\usepackage{dsfont}
\usepackage{amsmath}
\usepackage{amssymb}
\usepackage{amsthm}
\usepackage{stmaryrd}
\usepackage{color}
\usepackage{array}
\usepackage{hyperref}
\usepackage{graphicx}
\usepackage{mathtools}
\usepackage{natbib}
\usepackage[bb=boondox]{mathalfa}
\geometry{top=3cm,bottom=3cm,left=2.5cm,right=2.5cm}
\setlength\parindent{0pt}
\renewcommand{\baselinestretch}{1.3}

\newcommand\restr[2]{{% we make the whole thing an ordinary symbol
  \left.\kern-\nulldelimiterspace % automatically resize the bar with \right
  #1 % the function
  \vphantom{\big|} % pretend it's a little taller at normal size
  \right|_{#2} % this is the delimiter
  }}
  
% definition of the "structure"
\theoremstyle{plain}
\newtheorem{thm}{Theorem}[section]
\newtheorem{lem}[thm]{Lemma}
\newtheorem{prop}[thm]{Proposition}
\newtheorem{coro}[thm]{Corollary}
\newtheorem{cla}[thm]{Claim}
\theoremstyle{definition}
\newtheorem{conj}{Conjecture}
\newtheorem{defi}{Definition}
\newtheorem*{ex}{Example}
\newtheorem*{rem}{Remark}
\newtheorem{step}{Step}

\newcommand{\cInd}{\mathrm{cInd}}
\newcommand{\mulldif}{\mathrm{d}^{\times}}

\title{The equivalence of Godement-Jacquet $L$ function and Jacquet-Langlands $L$ function}
\date{\today}
\author{Deng Zhiyuan\footnote{Email:\ \href{mailto:dengzymathnt@outlook.com}{dengzymathnt@outlook.com}} \\[0.5cm]{\small Advisor: Prof. Farrell Brumley}}


\begin{document}
\maketitle
\newpage

\tableofcontents
\newpage

\begin{abstract}
For my master thesis, there are two parts: first it is recollection of classical theory about Godement-Jacquet $L$-function and Jacquet-Langlands $L$-function. This part starts from Riemann and Tate's classical theory. Then the main result of Godement-Jacquet and Jacquet-Langlands associated with automorphic form is introduced. The second part is a new method to prove the equivalence of ingredient between those type of $L$-functions: we construct an $G$-module isomorphism between the ingredient of Godement-Jacquet $\widetilde{V}\otimes_{G}S(M_{2}(F)\times F^{\times})\otimes_{G}V$ and the ingredient of Jacquet-Langlands $\mathcal{K}(V(-1))(1)$ by using Weil representation.
\end{abstract}
\begin{abstract}
Pour mon mémoire de master, il y a deux parties: la première partie est un rappel de la théorie classique sur la fonction $L$ de Godement-Jacquet et la fonction $L$ de Jacquet-Langlands. Cette partie part de la théorie classique de Riemann et Tate, puis on introduit le résultat principal de Godement-Jacquet et Jacquet-Langlands associé à la forme automorphe. La deuxième partie est une nouvelle méthode pour démontrer l'équivalence entre ces deux types de fonctions $L$: on construit un isomorphisme de $G$-modules entre l'ingrédient de Godement-Jacquet $\widetilde{V}\otimes_{G}S( M_{2}(F)\times F^{\times})\otimes_{G}V$ et l'ingrédient de Jacquet-Langlands $\mathcal{K}(V(-1))(1)$ par la représentation de Weil.
\end{abstract}
\newpage

\vspace{0.5cm}
\section{Classical Theory of Godement-Jacquet and Jacquet-Langlands}
\subsection{Introduction}
Whenever we start to talk about number theory, the legend of $L$-function which begun with Riemann is always the prototype. Considering $L$-function, it's related to a lot of famous conjectures in number theory, for example the Riemann conjecture and Ramanujan conjecture. There are three different types of problems at least when one encounter with $L$-function: the analytic continuation and functional equation; the location of the zeros; and the values at special points. Here we are only interested in the analytic properties.

About 170 years ago, Leonhard Euler first introduced and studied the $\zeta$ function over $\mathbb{R}$. Later Bernhard Riemann published article "On the number of primes less than a given magnitude" which extended the Euler definition of zeta function to $\mathbb{C}$ in 1859 and proved its meromorphic continuation and functional equation, and established a relation between the zeros of $\zeta$ functions and the distribution of prime numbers \cite{riemann1859ueber}. In this famous paper, Riemann proposed the Riemann conjecture:
\begin{conj}
All non-trivial zeroes of $\zeta(s)$ lie on the line $\mathfrak{Re}(s)=\frac{1}{2}$. 

The Riemann hypothesis is equivalent to the error term in the prime number theorem:
\begin{equation*}
    \#\{\text{Prime numbers}\leq x\}=\int^{x}_{2}\frac{\text{d}t}{\log t}+\text{error term}
\end{equation*}
being as sharp as possible, namely, $O(\sqrt{x}\log x)$ as $x\rightarrow\infty$.
\end{conj}

The analytic theory of $L$-functions associated to modular forms was studied by Erich Hecke \cite{hecke1936bestimmung}, and later extended to non-holomorphic automorphic forms by Hans Maass \cite{maass1949neue}. The analytic continuation and functional equation of such an $L$-function was obtained by Mellin transform of an automorphic form $f(x)$:
\begin{equation*}
    f(x)\mapsto \{\mathcal{M}f\}(s)=\phi(s)=\int^{\infty}_{0}x^{s-1}f(x)\text{d}x, 
\end{equation*}
and applying the modular relation $z\mapsto -z^{-1}$ as same as Riemann's proof \cite{riemann1859ueber}. Then the idea was generalized to the Adelic setting by Gelfand-Graev-Pyatetski-Shapiro \cite{gelfand1968representation} and Jacquet-Langlands \cite{langlands1970automorphic}. In 1950, John Tate
developed used a translation invariant integration on the locally compact group of ideles to lift the zeta function twisted by a Hecke character, i.e. a Hecke $L$-function, of a number field to a zeta integral and study its properties \cite{tate1997fourier}.  By the Poisson summation formula, Tate proved the functional equation and meromorphic continuation of the zeta integral and the Hecke $L$-function. He also located the poles of the twisted zeta function. During that period, Kenkichi Iwasawa independently developed same results as Tate but without a analogue of local theory as Tate \cite{iwasawa1992letter}. Hence this theory is often taken as Iwasawa-Tate theory. Iwasawa–Tate theory was extended to the general linear group $GL(n)$ over an algebraic number field and automorphic representations of its adelic group by Roger Godement and Hervé Jacquet in 1972 which formed the foundations of the Langlands correspondence \cite{godement1974notes}. Tate's thesis can be viewed as the $GL(1)$ case of the work by Godement–Jacquet.
On the other side of the story, as same as for $GL_{1}$, Jacquet and Langlands did associate $L$-function to automorphic representations on $GL_{2}$ \cite{langlands1970automorphic}.

The research detailed in this paper was the result of taking a different point
of view on these automorphic $L$-functions. The idea is to study the entire space
of zeta integrals, instead of just the $L$-functions that are generated from them. The classical method to the equivalence between those two constructions is tedious due to case-by-case calculation without a clear conceptual understanding. Gal Dor's main idea is to construct Algebraic structures on the space of automorphic $L$-functions. As we can find out from the classic theory, $L$-functions are built as the great common divisors (shortened as GCD from now on) of classes of zeta integral. Instead of calculation, Gal Dor used theta correspondence to study the equivalence.  The exotic symmetric monoidal
structure of $GL_{2}$-modules enables us to construct an Abelian category of abstractly
automorphic representations, whose irreducible objects are the usual automorphic representations. The category setting that he constructed has more philosophical understanding about those two constructions of $L$-functions. For my thesis, I will focus on the first part of his paper, which is the construction of the equivalence of isomorphism of the ingredient spaces of those two types of zeta integrals. This is enough to understand the proof of the equivlence but without abstract monodial category.

The interesting thing based on Gal Dor is that his method can be generalized to $GL_{n}$ and global setting. And the paper that we cited here is only part of his Ph.D thesis \cite{dor2020exotic}.
\subsection{Godement-Jacquet Theory}
\subsubsection{Review of Riemann theory}
The most famous $L$-function is Riemann's $\zeta$-function:
\begin{equation*}
    \zeta(s)=\sum_{n\geq 1}n^{-s}\ \ \ \ (\mathfrak{Re}s> 1).
\end{equation*}

By an easy argument using the fact that every $n\geq 1$ has a unique prime factorisation, one shows that $\zeta(s)$ can be written as an Euler product
\begin{equation*}
    \zeta(s)=\prod_{p\ prime} (1-p^{-s})^{-1}\ \ \ \ (\mathfrak{Re}s >1).
\end{equation*}
This shows that $\zeta(s)$ does not have any zeroes in the region $\mathfrak{Re}s >1$.

We define the completed $\zeta$-function by $Z(s)=\pi^{s/2}\Gamma(s/2)\zeta(s)$. Here we have used the $\Gamma-$function
\begin{equation*}
    \Gamma(s)=\int^{\infty}_{0}e^{-t}t^{s-1}\text{d}t\ \ \ \ (\mathfrak{Re}s>0). 
\end{equation*}
\begin{rem}
Let's recall a few important properties of $\Gamma$-function:
\begin{enumerate}
    \item The Gamma function satisfies the functional equation $\Gamma(s+1)=s\Gamma(s)$;
    \item The Gamma function has an analytic continuation on $\mathbb{C}$ with simple poles at $s=0,-1,-2,...$
    \item The reciprocal of the Gamma function is entire, i.e. 
    \begin{equation*}
        \frac{1}{\Gamma(s)}=\frac{\sin(\pi s)}{\pi}\Gamma(1-s)
    \end{equation*}
    is entire.
\end{enumerate}
During the proofs of those properties, the identity $$\int^{\infty}_{0}e^{-(ax^{2}+b)} \text{d}x=\sqrt{\frac{\pi}{a}}$$ is essential.
\end{rem}
\begin{lem}\label{PoiR}
Given a Schwazrtz function $f$, and $\hat{f}$ is the Fourier transform, then
\begin{equation*}
    \sum_{n\in\mathbb{Z}}f(n)=\sum_{m\in\mathbb{Z}}\hat{f}(m).
\end{equation*}
\end{lem}
\begin{proof}
Denote $F(x)=\sum_{n\in\mathbb{Z}}f(x+n)$, which is 1-periodic, then we can calculate the Fourier coefficients: 
\begin{equation*}
    \hat{F}(k)=\int^{1}_{0}F(x)e^{-2\pi ikx}\text{d}x=\int^{1}_{0}\sum_{n\in\mathbb{Z}}f(x+n)e^{-2\pi ikx}\text{d}x.
\end{equation*}
Because $f$ is Schwartz, so this integral converges uniformly.
\begin{equation*}
    =\sum_{n\in\mathbb{Z}}\int^{n+1}_{n}f(x)e^{-2\pi ikx} \text{d}x=\int_{\mathbb{R}}f(x)e^{-2\pi ikx}\text{d}x=\hat{f}(k),
\end{equation*}
by the definition of Fourier series of $f$, $F(x)=\sum\limits_{k\in\mathbb{Z}}\hat{f}(k)e^{ikx}$. Choosing $x=0$, we get the formula as desired:
\begin{equation*}
    \sum_{n\in\mathbb{Z}}f(n)=\sum_{k\in\mathbb{Z}}\hat{f}(k).
\end{equation*}
\end{proof}
\begin{defi}
The Jacobi theta function, or called as the classical theta function is the on right half plane defined by 
\begin{equation*}
    \theta(s)=\sum_{n\in\mathbb{Z}}e^{-\pi n^{2}s},\ \ \ \ \mathfrak{Re}s>0.
\end{equation*}
The theta function here is a holomorphic function on the right half plane.
\end{defi}
\begin{lem}
By the Poisson formula \ref{PoiR}, one can prove that $\theta(s)$ satisfies the functional equation
\begin{equation*}
\theta(\frac{1}{s})=\sqrt{s}\theta(s).
\end{equation*}
\end{lem}

\begin{proof}
Given $g(x)=e^{-\pi tx^{2}}$, in order to get the formula, we need to calculate its Fourier transform of $g(x)$, 
\begin{equation*}
    \hat{g}(t)=\int^{+\infty}_{-\infty}e^{-\pi tx^{2}}\cdot e^{-2\pi iyx}\text{d}x=e^{\pi}(\frac{iy}{\sqrt{t}})\int^{+\infty}_{-\infty}e^{-\pi(\sqrt{t}x+\frac{ix}{\sqrt{t}})^{2}}\text{d}x=\frac{1}{\sqrt{t}} e^{-\pi \frac{y^{2}}{t}}
\end{equation*}
Then 
\begin{equation*}
    \theta(s)=\sum_{n\in\mathbb{Z}}e^{-\pi n^{2}s}=\sum_{n\in\mathbb{Z}}g(n)=\sum_{m\in\mathbb{Z}}\hat{g}(m)=\frac{1}{\sqrt{s}}\sum_{m\in\mathbb{Z}}e^{-\pi \frac{n^{2}}{s}}=\frac{1}{\sqrt{s}}\theta(\frac{1}{s}).
\end{equation*}
\end{proof}
Before we moved to the proof of the analytic continuation of Riemann Zeta function, we need to know the behaviour of the theta functions near zero and infinity to justify the Mellin transform later in proof.

For theta function, there exists a constant $C=\pi-1> 0$ such that for all sufficiently small $t>0$ the following inequality holds: 
\begin{equation*}
    |\theta(t)-t^{\frac{1}{2}}|< e^{-C/t}.
\end{equation*}

Usually the Mellin transform is that Given a function $f(t)$ with $\mathfrak{Re}t>0$, its Mellin transform is defined to be
\begin{equation*}
    \mathcal{M}_{f}(s):=\int^{\infty}_{0}f(t)t^{s-1}\text{d}t,
\end{equation*}
which is defined for all values $s$ for which the integral exists.
\begin{thm}
The function $Z(s)$ can be continued to a meromorphic function on the whole complex plane with a simple pole at $s=1$ with residue 1, a simple pole at $s=0$ with residue -1, and no other poles. It satisfies the functional equation 
\begin{equation*}
        Z(s)=Z(1-s)
\end{equation*}
i.e., $\zeta(s)$ satisfies the functional equation
\begin{equation*}        \pi^{s
/2}\Gamma(\frac{s}{2})\zeta(s)=\pi^{(1-s)/2}\Gamma(\frac{1-s}{2})\zeta(1-s).
\end{equation*}
\end{thm}
\begin{proof}
We express $Z(s)$ as the Mellin transform of a modular form. The modular form we need is Jacobin theta-function. But theta function behaves like $t^{-1/2}$ at 0 and converges rapidly to 1 at infinity. So we need to introduce some correction term to make the integral converge. So We now consider the Mellin transform of $\theta$, defined as \begin{equation*}
    \mathcal{M}_{\theta}(s)=\int^{\infty}_{1}(\theta(t)-1)t^{s-1}\text{d}t+\int^{1}_{0}(\theta(t)-\frac{1}{\sqrt{t}})t^{s-1}\text{d}t,\ \ \ \ (\mathfrak{Re}> 1).
\end{equation*}
From this we get the following equation, due to Riemann: $Z(s)=\frac{1}{2}\mathcal{M}_{\theta}(s/2)$. And we can rewrite $\mathcal{M}_{\theta}(s/2)$ as follows.  We obtain, for $\mathfrak{Re}s>1$, 
\begin{align*}
\int^{1}_{0}\bigg(\theta(t)-\frac{1}{\sqrt{t}}\bigg)t^{\frac{s}{2}-1}\text{d}t
&= \int^{1}_{0}\theta(t)t^{\frac{s}{2}-1}\text{d}t-\int^{1}_{0}t^{\frac{s-1}{2}}\text{d}t\\
&= \int^{1}_{0}\bigg(\sum_{n\in\mathbb{Z}}e^{-\pi n^{2}t}\bigg)t^{\frac{s}{2}-1}\text{d}t-\frac{2}{s-1}\\
&= \int^{1}_{0}t^{\frac{s}{2}-1}\text{d}t+2\int^{1}_{0}\bigg(\sum_{n\geq 1}e^{-\pi n^{2}t}\bigg)t^{\frac{s}{2}-1}\text{d}t +\frac{2}{1-s}\\
&= 2\sum_{n\geq 1}\int^{1}_{0}e^{-\pi n^{2}t}t^{\frac{s}{2}-1}\text{d}t+\frac{s}{2}+\frac{2}{1-s}
\end{align*}
Therefore we have
\begin{equation*}
    \mathcal{M}_{\theta}(s)=2\sum_{n\geq1}\int^{\infty}_{0}e^{-\pi n^{2}t}t^{\frac{s}{2}-1}\text{d}t+\frac{2}{s}+\frac{2}{1-s}
\end{equation*}
By the substitution $t\mapsto 1/t$ we get
\begin{equation*}
    \frac{1}{2}\mathcal{M}_{\theta}(s)=\pi^{-\frac{s}{2}}\Gamma(\frac{s}{2})\zeta(s)+\frac{1}{s}+\frac{1}{1-s}.
\end{equation*}
Both integrals in the definition of $\mathcal{M}_{\theta}(s)$ converge, it's an entire function. Then we can define an analytic continuation of the zeta function on the whole complex plane, which agrees with $\zeta(s)$ for $\mathfrak{Re}s>1$, by 
\begin{equation*}
    \zeta(s)=\frac{\pi^{\frac{s}{2}}}{\Gamma(\frac{s}{2})}\bigg(\frac{1}{2}\mathcal{M}_{\theta}(s)-\frac{1}{s}-\frac{1}{1-s}\bigg),
\end{equation*}
whose poles are at $s=0$ or $s=1$ as $\mathcal{M}_{\theta}(s) $ and $\frac{1}{\Gamma(s)}$ are entire. We can replace $s\Gamma(\frac{s}{2})$ by $\frac{2}{s}\Gamma(s/2)=2\Gamma(s/2+1)$ which converges to $2\Gamma(1)$ as $s$ goes to zero. Hence it's nonzero and the only pole is at 1. We now compute the residue:
\begin{equation*}
    \lim_{s\mapsto 1}(s-1)\frac{\pi^{s/2}}{\Gamma(s/2)}\bigg(\frac{1}{2}\mathcal{M}_{\theta}(s)-\frac{1}{s}-\frac{1}{1-s}\bigg)=\frac{\pi^{1/2}}{\Gamma(1/2)}=1.
\end{equation*}
Now the only thing left is $Z(s)=Z(1-s)$. Since $Z(s)=\frac{1}{2}\mathcal{M}_{\theta}(s)-\frac{1}{s}-\frac{1}{1-s}$, which means we only need to check that $\mathcal{M}_{\theta}(s)=\mathcal{M}_{\theta}(1-s)$, and we need to use $y=\frac{1}{t}$:
\begin{align*}
        \mathcal{M}_{\theta}(s)=
        &= \int^{1}_{0}y^{-s/2-1}(\theta(1/y)-1)\text{d}y+\int^{\infty}_{1}y^{-s/2-1}(\theta(1/y)-\sqrt{y})\text{d}y\\
        &= \int^{1}_{0}y^{(-1/2-s/2)}(\theta(y)-\frac{1}{\sqrt{y}})\text{d}y+\int^{\infty}_{1}y^{-1/2-s/2}(\theta(y)-\sqrt{y})\text{d}y\\
        &=\mathcal{M}_{\theta}(1-s).
\end{align*}
Now the proof is complete.
\end{proof}
\subsubsection{Review of Tate's thesis}

In this section, let $F$ be a number field and $\mathbb{A}_{F}$ its ring of adeles. An automorphic representation of $GL_{1}(F)$ is any irreducible unitary representation of $GL_{1}(\mathbb{A}_{F})$ appearing in $L^{2}(GL_{1}(F)\backslash GL_{1}(\mathbb{A}_{F}))$. As a $GL_{1}(\mathbb{A}_{F})$-module,
\begin{equation*}
    L^{2}(GL_{1}(F)\backslash GL_{1}(\mathbb{A}_{F}))=\int^{\oplus}_{GL_{1}(F)\backslash GL_{1}(\mathbb{A}_{F})}\psi(g)
\end{equation*}
so an automorphic representation is simply a grossencharacter of $F$, i.e.  a character $\psi:F^{\times}\backslash \mathbb{A}_{F}^{\times}\rightarrow S^{1}$. Thus the theory we are discussing is that in the case of $GL_{1}$, simply Hecke's theory of $L$-functions associated to grossencharacters. 

Let $\psi: F^{\times}\backslash \mathbb{A}_{F}^{\times}\rightarrow S^{1}$ be a grossencharacter of $F$. We can decompose it $\psi=\prod_{v}\psi_{v}$ as a product of characters $\psi_{v}$ on $F^{\times}$, with $\psi_{v}$ unramified for almost all $v$. Let $S$ be the set of ramified places. For every $v\not\in S$, define $\chi(v)=\psi_{v}(\pi_{v})$ where $\pi_{v}\in F_{v}$ is a uniformizer. Note that the choice of uniformizer does not matter. We can extend $\chi$ by multiplicativity to the set of ideals of $F$ prime to $S$. 

\begin{defi}
The L-series associated to $\phi$, or to $\chi$, is 
\begin{equation*}
    L(s, \chi)=\sum_{S\nmid\mathfrak{a}}\frac{\chi(\mathfrak{a})}{N(\mathfrak{a})^{s}}=\prod_{v\not\in S}\bigg(1-\frac{\chi(v)}{N(v)^{s}}\bigg)^{-1}.
\end{equation*}
\end{defi}
\begin{thm}
$L(s,\chi)$ has nice $L$-function properties:
\begin{enumerate}
    \item It converges for $\mathfrak{Re}(s)>1$;
    \item It has a meromorphic continuation to the whole plane, with a simple pole at $s=1$ if $\chi$ is trivial and no poles otherwise;
    \item There is a constant $A$, a constant $W(\chi)$ of modulus 1, and a gamma factor $\Gamma(s,\chi)$ such that $\mathfrak{L}(s,\chi)=s(s-1)A^{s}\Gamma(s,\chi)L(s,\chi)$ is entire and satisfies the functional equation
    \begin{equation*}
        \mathfrak{L}(1-s,\chi^{-1})=W(\chi)\mathfrak{L}(s,\chi)
    \end{equation*}
\end{enumerate}
\end{thm}
We skip the proof of this theorem. For the detail of this theorem, check in \cite{gelbart2016automorphic}.
By choosing an appropriate set of test functions and an appropriate measures, we can extend Riemann zeta to an idelic integral.
For the set of test functions are defined as following:
\begin{defi}\label{BruhatSchwartz}
Adelic Bruhat-Schwartz functions are linear combinations of functions $\Phi: \mathbb{A}_{\mathbb{Q}}\rightarrow \mathbb{C}$ where $\Phi=\prod\limits_{v\leq\infty} \Phi_{v}$, in which $\Phi_{v}$ are the characteristic function of $\mathbb{Z}_{v}$ for all but finitely many $v< \infty$. And $\Phi_{\infty}$ is Schwartz on $\mathbb{R}$, $\Phi_{v}$ is Bruhat-Schwartz function on $\mathbb{Q}_{v}$. The space of Bruhat-Schwartz functions are denoted as $S(\mathbb{A_{\mathbb{Q}}})$.
\end{defi}
Recall the definition of Schwartz on $\mathbb{R}$:
\begin{equation*}
    S(\mathbb{R},\mathbb{C})=\{f\in C^{\infty}(\mathbb{R},\mathbb{C})|\forall \alpha,\beta\in \mathbb{N}, ||f||_{\alpha,\beta}=\text{sup}_{x\in\mathbb{R}}x^{\alpha}(D^{\beta}f)<\infty\}
\end{equation*}
Now let's give the defition of Idelic integral: 
\begin{defi}
Define the idelic integral for factorizable idelic functions $\Phi=\prod_{v}\Phi_{v}$ such that $\Phi_{p}$ is the characteristic function $\mathbb{1}_{\mathbb{Z}_{p}}$ for almost all primes $p$ by 
\begin{equation*}
    \int_{\mathbb{A}^{\times}_{\mathbb{Q}}}\Phi(x)\text{d}^{\times}x=\prod_{v\in S}\int_{\mathbb{Q}^{\times}_{v}}\Phi_{v}(x_{v})\text{d}^{\times}x_{v},
\end{equation*}
in which $S$ is a finite set containing $\infty$ and all primes that $\Phi_{p}\not=\mathbb{1}_{\mathbb{Z}_{p}}$. The measure $\text{d}^{\times}x$ is defined as following:
\begin{equation*}\label{Haar}
\text{d}^{\times}x= \left\{
    \begin{array}{cc}
        \frac{\text{d}x_{\infty}}{|x_{\infty}|_{\infty}}, &  \text{if}\ v=\infty\\
        \frac{1}{1-p^{-1}}\frac{\text{d}x_{p}}{|x_{p}|_{p}}, & \text{if}\ v=p, p\ \text{are finite primes}
    \end{array}
    \right
\end{equation*}

Such that $\text{d}^{\times}x_{p}$ is normalized so that $\int_{\mathbb{Z}_{p}^{\times}}\text{d}^{\times}x_{p}=1$.
\end{defi}
\begin{defi}
Idelic absolute value: $x=\{x_{\infty},x_{2},...\}\in\mathbb{A}^{\times}_{\mathbb{Q}}$, then $|x|_{\mathbb{A}}=\prod_{v\leq\infty}|x_{v}|_{v}$.
\end{defi}
In order to get idelic absolute value, we choose a special test function: for $x=\{x_{\infty},x_{2},x_{3},...\}$, then
\begin{equation*}
    h(x)=e^{-\pi x_{\infty}^{2}}\prod_{v<\infty}\mathbb{1}_{\mathbb{Z}_{v}}(x_{v})\in S(\mathbb{A}_{\mathbb{Q}}).
\end{equation*}
After some calculation, we know that the Fourier transform of $h(x)$ is equal to $h(x)$.

Now we are ready to write down the zeta integral:
\begin{equation*}
    Z(s)=\int_{\mathbb{A}^{\times}_{\mathbb{Q}}}h(x)|x|^{s}_{\mathbb{A}_{\mathbb{Q}}}\text{d}^{\times}x, \ \ s\in\mathbb{C},\ \mathfrak{Re}(s)>1.
\end{equation*}
For every automorpic form $\phi$ on $\mathbb{A}_{\mathbb{Q}}^{\times}$ can be uniquely expressed in the form 
\begin{equation*}
    \phi(x)=c\cdot \chi_{idelic}(x)\cdot |x|^{it}_{\mathbb{A}},\ \ \forall x\in\mathbb{A^{\times}_{Q}},\ 
\end{equation*}
in which $c\in\mathbb{C},\ t\in\mathbb{R}$ are fixed constants. And the character $\chi_{idelic}$ is an idelic lift of a Dirichilet character $\chi(mod\ p^{f})$. The idelic lift of $\chi$ is the Hecke character $\chi_{idelic}:\mathbb{Q}^{\times}\backslash\mathbb{A}^{\times}_{\mathbb{Q}}\rightarrow\mathbb{C}$ defined as 
\begin{equation*}
    \chi_{idelic}(g)=\chi_{\infty}(g_{\infty})\cdot\chi_{2}(g_{2})\cdot\chi_{3}(g_{3})\cdot\cdot\cdot\ \ \ g=\{g_{\infty},g_{2},g_{3},...\}\in\mathbb{A^{\times}_{Q}},
\end{equation*}
where 
\begin{equation*}
\chi_{\infty}(g_{\infty})=\left\{
\begin{array}{ccc}
     1& \chi(-1)=1 \\
     1&  \chi(-1)=-1\ \text{if}\  g_{\infty}>0\\ 
     -1& \chi(-1)=-1\ \text{if}\ g_{\infty}<0
\end{array}
\right
\end{equation*}
and 
\begin{equation*}
    \chi_{v}(g_{v})=\left\{
    \begin{array}{cc}
        \chi(v)^{m} &\text{if}\ g_{v}\in v^{m}\mathbb{Z}^{\times}_{v}\ \text{and}\  v\not=p  \\
         \chi(j)^{-1} & \text{if}\ g_{v}\in p^{k}(j+p^{f}\mathbb{Z}_{p})\ \text{with}\ j,k\in\mathbb{Z}.\ (j,p)=1,\ \text{and}\ v=p 
    \end{array}
    \right
\end{equation*}
Let's write down adelic Poisson summation formula:
\begin{equation}
    1+\sum_{\alpha\in\mathbb{Q}^{\times}}h(\alpha x)=\frac{1}{|x|_{\mathbb{A}}}+\frac{1}{|x|_{\mathbb{A}}}\sum_{\alpha\in\mathbb{Q}^{\times}}h(\frac{\alpha}{x})
\end{equation}

By using the decomposition $\mathbb{A}^{\times}_{\mathbb{Q}}=\bigcup_{\alpha\in\mathbb{Q\times}}\alpha\cdot(\mathbb{Q}^{\times}\backslash\mathbb{A}^{\times}_{\mathbb{Q}})$, we obtain:
\begin{equation*}
    \int_{\mathbb{A}^{\times}}h(x)|x|^{s}_{\mathbb{A}}\text{d}^{\times}x=\sum_{\alpha\in\mathbb{Q}^{\times}}\int_{\alpha\cdot(\mathbb{Q}^{\times}\backslash\mathbb{A}^{\times})}h(x)|x|^{s}_{\mathbb{A}}\text{d}^{\times}x
\end{equation*}
In order to obtain the analytic coninuation and functional equation, we calculate this integral by Poisson summation formula:
\begin{align*}
    \pi^{-\frac{s}{2}}\Gamma(\frac{s}{2})\zeta(s)&=\int_{x\in\mathbb{Q}^{\times}\backslash\mathbb{A}^{\times}_{\mathbb{Q}}}\sum_{\alpha\in\mathbb{Q}^{\times}}h(\alpha x)|x|^{s}_{\mathbb{A}}\text{d}^{\times}x\\
   &=\frac{1}{s-1}-\frac{1}{s}+\int_{x\in\mathbb{Q}^{\times}\backslash\mathbb{A}_{\mathbb{Q}^{\times}}\& |x|_{\mathbb{A}\geq 1}}\sum_{\alpha\in\mathbb{Q}^{\times}}h(\alpha x)(|x|^{s}_{\mathbb{A}}+|x|^{1-s}_{\mathbb{A}})\text{d}^{\times}x.
\end{align*}
In Tate's thesis \cite{tate1997fourier}, we can obtain same result for any test function $\Phi$ in the adelic Bruhat-Schwartz space $S(\mathbb{A}_{\mathbb{Q}})$. Let's rewrite the adelic Poisson summation formula:
\begin{equation*}
    \sum_{\alpha\in\mathbb{Q}^{\times}}\Phi(\alpha x)=\frac{\hat{\Phi}(0)}{|x|_{\mathbb{A}}}+\frac{1}{|x|_{\mathbb{A}}}\sum_{\alpha\in\mathbb{Q}^{\times}}\hat{\Phi}(\frac{\alpha}{x})-\Phi(0)
\end{equation*}
by same kind of calculation, we get similar result:
\begin{align*}
    \int_{x\in \mathbb{Q}^{\times}\backslash\mathbb{A}^{\times}}\sum_{\alpha\in\mathbb{Q}^{\times}}\Phi(\alpha x)|x|^{s}_{\mathbb{A}}\text{d}^{\times}x&=\frac{\hat{\Phi}(0)}{s-1}-\frac{\Phi(0)}{s}\\
    &+\int_{x\in\mathbb{Q}^{\times}\backslash\mathbb{A}_{\mathbb{Q}^{\times}}\& |x|_{\mathbb{A}\geq 1}}\sum_{\alpha\in\mathbb{Q}^{\times}}(\Phi(\alpha x)|x|^{s}_{\mathbb{A}}+\hat{\Phi}(\alpha x)|x|^{1-s}_{\mathbb{A}})\text{d}^{\times}xx
\end{align*}
The right hand side is invariant under translation: $s\rightarrow 1-s,\ \Phi\rightarrow \hat{\Phi}$. For the left hand side, as we assumed in the definition, $\Phi\in S(\mathbb{A}_{\mathbb{Q}})$ is factorizable. It follows that
\begin{align*}
    \int_{\mathbb{A}^{\times}_{\mathbb{Q}}}\Phi(x)|x|^{s}_{\mathbb{A}}\text{d}^{\times}x&=\int_{\mathbb{R}^{\times}}\Phi_{\infty}(x_{\infty})|x_{\infty}|^{s}_{\infty}\frac{\text{d}x_{\infty}}{|x_{\infty}|_{\infty}}\cdot\prod_{p}\int_{\mathbb{Q}^{\times}_{p}}\Phi_{p}(x_{p})|x_{p}|^{s}_{p}\text{d}^{\times}x_{p}\\
    &=\widetilde{\Phi}_{\infty}(s)\cdot\bigg(\prod_{p\in S}\frac{\int_{\mathbb{Q}^{\times}_{p}}\Phi_{p}(x_{p})|x_{p}|_{p}^{s}\text{d}^{\times}x_{p}}{(1-p^{-s})^{-1}}\bigg)\zeta(s)
\end{align*}
where $\widetilde{\Phi}(s)=\int_{\mathbb{R}^{\times}}\Phi(y)y^{s}\frac{\text{d}y}{y}$.

Now let $v\leq \infty$ determine a local field $\mathbb{Q}_{v}$. Then we can have the local zeta integral:
\begin{defi}
    Fix $s\in\mathbb{C}$ with $\mathfrak{Re}(s)>0$. Let $\Phi:\mathbb{Q}_{v}\rightarrow \mathbb{C}$ be a locally constant compactly supported function as definition \ref{BruhatSchwartz} if $v<\infty$, and a Schwartz function if $v=\infty$. Let $\omega:\mathbb{Q}^{\times}_{v}\rightarrow\mathbb{C}^{\times}$ be a local unitary character, i.e. a continuous homomorphism of absolute value 1. 
    
    The local zeta integral associated to $\omega$ and $\Phi$ is defined as 
    \begin{equation*}
        Z_{v}(s,\Phi, \omega)=\int_{\mathbb{Q}^{\times}_{v}}\Phi(x)\omega(x)|x|^{s}_{v}\text{d}^{\times}x,
    \end{equation*}
    in which the $\text{d}^{\times}x$ denotes the multiplicative Haar measure as defined in \ref{Haar}.
\end{defi}
We state the main result for the local zeta integral without further detail:
\begin{thm}
Let $s\in\mathbb{C}$ with $0<\mathfrak{Re}(s)<1$. The local zeta integral $Z_{v}(s,\Phi,\omega)$ satisfies the functional equation
\begin{equation*}
    Z_{v}(s,\Phi,\omega)=\gamma(s,\omega)\cdot Z_{v}(1-s,\hat{\Phi},\bar{\omega})
\end{equation*}
where $\hat{\Phi}$ is the Fourier transform of $\Phi$: 
\begin{equation*}
    \hat{\Phi}(x )=\int_{\mathbb{Q}^{\times}_{v}}\Phi(y)e_{v}(-xy)\text{d}y,
\end{equation*}
$\overline{\omega}=\omega^{-1}$ is the complex conjugate of $\omega$, and $\gamma(s,\omega)$ is a meromorphic function which is independent of the choice of $\Phi$.
\end{thm}
\begin{rem}
After some calculation, we can get the explicit form of the $\gamma(s,\omega)$. If we choose appropriate test function, the result of zeta integral will be the $L$-functions that we desire.
\end{rem}
\subsubsection{Godement-Jacquet $L$-function}
Tate's method is generalized to $L$-functions of $GL_{n}$ for any $n\geq1$ by Roger Godement and Herv\'{e} jacquet \cite{goldfeld2006automorphic}. Godement and Jacquet considered the inner form of $GL_{n}$ and the affine emmbedding $\mathbb{G}_{m}\rightarrow\mathbb{G}_{a}$ is replaced as $GL_{n}\rightarrow M_{n}$. The theory of Tate is generalized in the modern setting of automorphic representations. The analytic continuation and functional equation of an $L$-function associated to an automorphic form on $GL(n,\mathbb{A}_{\mathbb{Q}})$ was derived directly from the Poisson summation formula for $GL(n,\mathbb{A}_{\mathbb{Q}})$ exactly as in Tate's thesis.

Denote $M_{2}(\mathbb{A}_{\mathbb{Q}})$ as the matrix:
\begin{equation*}
    \bigg\{\begin{pmatrix}
    a_{\infty} &b_{\infty}\\
    c_{\infty} & d_{\infty}
    \end{pmatrix},
    \begin{pmatrix}
a_{2} & b_{2}\\
c_{2} & d_{2}
\end{pmatrix},...,
\begin{pmatrix}
a_{p} & b_{p}\\
c_{p} & d_{p}
\end{pmatrix},...
    \bigg\},
\end{equation*}
\begin{defi}\label{BSA}
    Bruhat- Schwartz function on $M_{2}(\mathbb{A}_{\mathbb{Q}})$
    
    A complex valued function $\Phi:M_{2}(\mathbb{A}_{\mathbb{Q}})\rightarrow\mathbb{C}$ is said to be a Bruhat-Schwartz function if it is a finite sum of functions of the form 
\begin{equation*}
    \Phi^{(i)}(m)=\prod_{v}\Phi^{(i)}_{v}(m_{v}), \ \ \ \ (\forall m=\{m_{\infty},m_{2},...,m_{p},...\}\in M_{2}(\mathbb{A}_{\mathbb{Q}}))
\end{equation*}
where for each $i=1,2,3,...$
\begin{enumerate}
    \item $\Phi^{(i)}:M_{2}(\mathbb{R})\rightarrow \mathbb{C}$ is smooth and $\Phi^{(i)}(g_{\infty})$ is Schwartz in each of the variables $a_{\infty}, b_{\infty}, c_{\infty},d_{\infty}$, for $g_{\infty}=\begin{pmatrix}
    a_{\infty}&b_{\infty}\\
    c_{\infty} &d_{\infty}
    \end{pmatrix}\in M_{2}(\mathbb{R})$;
    \item $\Phi^{(i)}_{p}: M_{2}(\mathbb{Q}_{p})\rightarrow\mathbb{C}$ is locally constant and compactly supported for each finite prime $p$;
    \item $\Phi^{(i)}_{p}$ is the characteristic function of $M_{2}(\mathbb{Z}_{p})$ for all but finitely many primes $p$.
\end{enumerate}
\end{defi}
\begin{thm}\label{poissonA}
The Poisson summation formula for $M_{2}(\mathbb{A}_{\mathbb{Q}})$:

Let $\Phi$ be a Bruhat-Schwartz function as definition\ref{BSA}. Let $e:\mathbb{A}_{\mathbb{Q}}\rightarrow\mathbb{C}$ be the additive character as 
\begin{equation*}
    e(x)=\prod_{v\leq \infty}e_{v}(x_{v})
\end{equation*}
in which for $v<\infty$, $e_{p}=e^{-2\pi i\{x_{p}\}}$ and for $v=\infty$, $e_{\infty}(x_{\infty})=e^{2\pi ix_{\infty}}$.

Then we have the identity:
\begin{equation*}
    \sum_{\zeta\in M_{2}(\mathbb{Q})}\Phi(\zeta)=\sum_{\zeta\in M_{2}(\mathbb{Q})}\hat{\Phi}(\zeta)
\end{equation*}
in which the Fourier transform $\hat{\Phi}$ is defined as 
\begin{equation*}
    \hat{\Phi}\big(\begin{pmatrix}
    \alpha &\beta\\
    \gamma & \delta
    \end{pmatrix}\big)=\int_{\mathbb{A}_{\mathbb{Q}}}\int_{\mathbb{A}_{\mathbb{Q}}}\int_{\mathbb{A}_{\mathbb{Q}}}\int_{\mathbb{A}_{\mathbb{Q}}}\Phi\big(\begin{pmatrix}
    p &q\\
    r & s
    \end{pmatrix}\big)e(-p\alpha-q\gamma-r\beta-s\delta)\text{d}p\text{d}q\text{d}r\text{d}s
\end{equation*}
for all $\big(\begin{pmatrix}
    \alpha &\beta\\
    \gamma & \delta
    \end{pmatrix}\in M_{2}(\mathbb{A}_{\mathbb{Q}})$.
    
Equivalently, we can rewrite the Poisson formula as following:
\begin{align*}
    \sum_{\zeta\in GL_{2}(\mathbb{Q})}\Phi(\zeta)+\sum_{\zeta\in M_{2}(\mathbb{Q})\ rank\ 1}\Phi(\zeta) +\Phi\big(\begin{pmatrix}
    0&0\\
    0&0
    \end{pmatrix}\big)\\
    =\sum_{\zeta\in GL_{2}(\mathbb{Q})}\hat{\Phi}(\zeta)+\sum_{\zeta\in M_{2}(\mathbb{Q})\ rank\ 1} \hat{\Phi}(\zeta)+\hat{\Phi}\big(\begin{pmatrix}
    0&0\\
    0&0
    \end{pmatrix}\big)
\end{align*}
\end{thm}
 Godement and Jacquet introduced a global zeta integral associated to a cuspidal automorphic representation of $GL_{2}(\mathbb{A}_{\mathbb{Q}})$ by representing it as an integral transform of matrix coefficient. 
 \begin{defi}
 Global zeta integral for $GL_{2}(\mathbb{A}_{\mathbb{Q}})$
 
 Let $(\pi, V)$ be a cuspidal automorphic repsentation of $GL_{2}(\mathbb{A}_{\mathbb{Q}})$ with unitary central character, i.e. it is a smooth $(\mathfrak{gl}_{2}(\mathbb{C}),O_{2}(\mathbb{R}))$-module which is isomorphic to  a subquotient of the complex vecctor space of all adelic cusp forms for $GL_{2}(\mathbb{A}_{\mathbb{Q}})$ with unitary central character. Fix two vectors $f_{1},\ f_{2}\in V$ and the matrix coefficient of $(\pi, V)$ is defined as 
 \begin{equation*}
     \beta(g)=\int_{Z(\mathbb{A}_{\mathbb{Q}})GL_{2}(\mathbb{Q})\backslash GL_{2}(\mathbb{A}_{\mathbb{Q}})}f_{1}(hg)\overline{f_{2}(h)}\text{d}^{\times}h\ \ \ g\in GL_{2}(\mathbb{A}_{\mathbb{Q}}).
 \end{equation*}
 Given $\Phi$ as a Bruhat- Schwartz function as definition \ref{BSA}. For $s\in\mathbb{C}$ with $\mathfrak{Re}(s)$ sufficiently large, the global zeta integral is as following:
 \begin{equation*}
     Z(s, \Phi,\beta)=\int_{GL_{2}(\mathbb{A}_{\mathbb{Q}})}\Phi(g)\beta(g)|\text{det}(g)|^{s+1/2}\text{d}^{\times}g,\ \ \ g=\{g_{v}\}_{v\leq\infty}\in GL_{2}(\mathbb{A}_{\mathbb{Q}})
 \end{equation*}
 For the measure, we define $\text{d}^{\times}g=\prod_{v\leq\infty}\text{d}^{\times}g_{v}$ in which $\text{d}^{\times}g_{v}$ is a multiplicative normalized Haar measure on $GL_{2}(\mathbb{Q}_{v})$.
 
 \end{defi}
 
 For $\mathfrak{Re}(s)$ sufficiently large, the global zeta integral $Z(s, \phi ,\beta)$ converges. It has shown that $Z(s,\phi,\beta)$ has a holomorphic continuation to all $s\in \mathbb{C}$ and satisfies a functional equation \cite{godement2006zeta}. If $(\pi, V) $ is irreducible, the matrix coefficient $\beta$ factors as a product of local matrix coefficients, which means that the global zeta integral can be represented by a Euler product. So global zeta integral has the same properties as Riemann zeta function.
 
 Now let's state the main theorem for global zeta integral
 \begin{thm}
 Functional equation of the global zeta integral
 
 Let $(\pi,V)$ be a cuspidal automorphic representation of $GL_{2}(\mathbb{A}_{\mathbb{Q}})$. Then the global zeta integral $Z(s,\Phi,\beta)$ has a holomorphic continuation to all $s\in\mathbb{C}$ and satisfies the functional equation
 \begin{equation*}
     Z(s,\Phi, \beta)=Z(1-s,\hat{\Phi},\hat{\beta})
 \end{equation*}
 in which the Fourier transform of $\Phi$ is defined as \ref{poissonA} and $\beta(g^{-1})=\hat{\beta}(g)$.
 \end{thm}
 
 Now given $(\pi, V)$ an irreducible cuspidal automorphic representation, we can factor the global zeta integral to get the local zeta integral:
 \begin{thm}
 Let $\beta$ be the matrix coefficient of $(\pi, v)$ defined using two vectors $\phi_{1},\phi_{2}\in V$, which are mapped to pure tensors under the isomorphism $\pi\cong \otimes_{v\leq\infty}\pi_{v}$. Then there exists matrix coefficients $\beta_{v}$ of the local represenstations $\pi_{v}$ so that $\beta=\prod_{v\leq\infty}\beta_{v}$. The test function $\Phi$ is also given as a factroizable Bruhat-Schwartz function, which can be represented in the form
 \begin{equation*}
     \Phi(m)=\prod_{v\leq\infty}\Phi_{v}(m_{v}),\ \ \ m=(m_{v})_{v\leq\infty}\in M_{2}(\mathbb{A}_{\mathbb{Q}}),
 \end{equation*}
 then for $s\in \mathbb{C}$ with $\mathfrak{Re}(s)$ sufficiently large, we have the factorization 
 \begin{equation*}
     Z(s,\Phi,\beta)=\prod_{v\leq\infty}Z_{v}(s,\phi_{v},\beta_{v})
 \end{equation*}
 in which
 \begin{equation*}
     Z_{v}(s,\phi_{v},\beta_{v})=\int_{GL_{2}(\mathbb{Q}_{v})}\Phi_{v}(g)\beta_{v}(g)|\text{det}(g)|^{s+1/2}_{v}\text{d}^{\times}g.
 \end{equation*}
 \end{thm}
 For the local zeta integal, we also have local functional equation and other $L$-function properties:
 \begin{thm}
 Fix a rational prime $p$ and let $(\pi, V)$ be an admissible irreducible representation of $GL_{2}(\mathbb{Q}_{p})$. And $\beta: GL_{2}(\mathbb{Q}_{p})\rightarrow\mathbb{C}$ is denoted a matrix coefficient of $(\pi, V)$. Let $\Phi:M_{2}(\mathbb{Q}_{p})\rightarrow\mathbb{C}$ be a Bruhat-Schwartz function. Then for local zeta integral $Z_{p}(s,\Phi_{p},\beta_{p})$, we have:
 \begin{enumerate}
     \item There exists $s_{0}\in \mathbb{R}$ such that the integral converges absolutely for $\mathfrak{Re}(s)>s_{0}$;
     \item For each Bruhat-Schwartz function $\Phi$, and each matrix coefficient $\beta$, the local zeta integral $Z_{p}(s,\Phi_{p},\beta_{p})$ represents a rational function of $p^{-s}$. The set of such rational functions obtained admits a common divisor, $L_{p}(s, \pi)$, which is characterized up to scalar by the property that the ratio $\frac{Z_{p}(s,\Phi_{p},\beta_{p})}{L_{p}(s,\pi)}$ is an entire function of $s$ which is identically 1 for suitable choice of $\Phi, \beta$. Further $L_{p}(s,\pi)=Q(p^{-s})^{-1}$ for some polynomial $Q$ satisfying $Q(0)=1$;
     \item There exists a rational function of $p^{-s}$ denoted $\gamma(s,\pi)$ which does not depend not on $\Phi$ or $\beta$, such that the local zeta integral satisfies the functional equation:
     \begin{equation*}
         Z_{p}(s,\Phi_{p},\beta_{p})=\gamma(s,\pi)^{-1}Z_{p}(1-s,\hat{\Phi_{p}}, \hat{\beta}).
     \end{equation*}
     Further, there exists a local root number $\varepsilon_{p}(s,\pi)$ which is a rational function of $p^{-s}$ such that we have the functional equation:
     \begin{equation*}
         \frac{Z_{p}(1-s,\hat{\Phi},\hat{\beta})}{L_{p}(1-s,\tilde{\pi})}=\varepsilon_{p}(s,\pi)\frac{Z_{p}(s,\Phi_{p},\beta_{p})}{L_{p}(s,\pi)}.
     \end{equation*}
 \end{enumerate}
 \end{thm}
\subsection{Jacquet-Langlands Theory}
\subsubsection{Whittaker Model and Kirillov Model}
First let's review the Whittaker model and Kirillov model. 

Given $V$ smooth irreducible representation of $G(F)$, A linear functional $\lambda: V\rightarrow \mathbb{C}$ is called a Whittaker functional for $\chi$ if for all $u\in U(F)$ and $\zeta\in V$ we have $\lambda(u\circ\zeta)=\chi(u)\lambda(\zeta)$. Fix nonzero Whittaker functional $\lambda$, and for $v\in V$, define a function $w_{v}: G(F)\rightarrow \mathbb{C}$ by $w_{v}(g)=\lambda(gv)$. Denote the space of such functions by $W=W_{\lambda}$, $W$ is closed under addition and scalar multiplication if $gW_{v}=W_{gv}$. The representation $W$ is called a Whittaker model up to $G(F)-$isomorphism.

\begin{defi}
A representation $(\pi, V)$ is  generic if it has a non-zero Whittaker model. 
\end{defi}

Next is the Kirillov model, the goal of Kirillov model is that every admissible irreducible representation of $GL_{2}(F)$ can be taken as a space of function space over $F^{\times}$. And every finite dimensional irreducible admissible representation of $G(F)$ is 1-dimensional and $\pi(g)=\chi(\text{det}(g))$, in which $\chi$ is a character of $F^{\times}$ and $\pi(g)=\chi(\text{det}(g))$. If $|\chi(x)|=1$, then call it unitary. 

For every finite dimensional smooth representation of $GL_{2}(F)$, it's just one dimensional. Given $\forall g\in GL_{2}(F)$, we can write $g=\begin{pmatrix}
\text{det}(g) & 0\\
0 & 1
\end{pmatrix}\cdot  g'$,\ $g'\in SL_{2}(F)$. So we only need to construct infinite-dimensional representation. 
\begin{thm}
Given $(\pi, V)$ infinite-dimensional irreducible representation of $GL_{2}(F)$, there exists one and only one $V'$, which is a complex function space defined on $F^{\times}$, such that the representation $\pi'$ of $GL_{2}(F)$ satisfies the following conditions:
\begin{enumerate}
    \item The representation $(\pi',V')$ and $(\pi,V)$ are equivalent;
    \item $\pi'\begin{pmatrix}
    a& b\\
    0&1
    \end{pmatrix}\zeta'(x)=\tau_{F}(bx)\zeta'(ax)$, in which $a, x\in F^{\times},\ b\in F,\ \forall\zeta'\in V'$,
\end{enumerate}
in which the $\tau_{F}$ is a non-trivial additive character of $F$. Every $\zeta\in V'$ is locally constant and vanishes outside of compact subset of $F$. All locally constant functions that vanishes outside of compact subsets belong to $V'$. 

\end{thm}
Then $\pi'$ will be called a Kirillov representation of $GL_{2}(F)$ or Kirillov model of the corresponding class of irreducible representation.


\subsubsection{Jacquet-Langlands Zeta Integral and $L$-function}
Just as  for $GL_{1}$, we now want to associate $L$-functions to automorphic forms for $GL_{2}$ \cite{langlands1970automorphic}. Before we discuss Jacquet-Langlands, let's review the method for classical holomorphic cusp forms from Hecke: if $f\in S_{k}(N, \psi)$ has Fourier expansion $f=\sum_{n}a_{n}q^{n}$ at infinity, then we can define an $L$-function by 
\begin{equation*}
    L(f,s)=\frac{1}{(2\pi^{s})}\Gamma(s)\sum_{n\geq 1}\frac{a_{n}}{n^{s}}=\int^{\infty}_{0}f(iy)y^{s-1}
    \text{d}y.
\end{equation*}
That is, by taking the Mellin transform of $f$ along the vertical half-line $\{iy:y>0\}$. To see how to define our $L$-functions more generally we rewrite this in the adelic setting.

Let $\phi_{f}(g)=f(g_{\infty}(i))j(g_{\infty},i)^{-k}\psi(k_{0})$ in which $g=\gamma g_{\infty}k_{0}\in GL_{2}(\mathbb{A}_{\mathbb{Q}})= GL_{2}(\mathbb{Q})\cdot (GL^{+}_{2}(\mathbb{R}\times \prod_{p<\infty}K_{p})$ be the adelic automorphic form associated to $f$. For simplicity suppose $N=1$ and $\psi$ is trivial. Then $\phi_{f}(g)$ is right $K_{0}-$invariant, and left $GL_{2}(\mathbb{Q})-$invariant. From the definition of $\phi_{f}$ we see, for real $y>0$,
\begin{equation*}
    \phi_{f}\bigg(\begin{pmatrix}
    y&0\\
    0&1
    \end{pmatrix}\bigg)=f(iy).
\end{equation*}
Thus
\begin{equation*}
    L(f,s)=\int_{\mathbb{Q^{\times}}\backslash\mathbb{A}^{\times}}\phi_{f}\bigg(\begin{pmatrix}
    y&0\\
    0&1
    \end{pmatrix}\bigg) |y|^{s}\text{d}^{\times}y
\end{equation*}

Now we get Fourier analysis involved. Recall that the characters of $\mathbb{Q}^{\times}\backslash\mathbb{A}_{\mathbb{Q}}^{\times}$ are given by $\tau(\lambda x)$ for various $\lambda\in\mathbb{Q}^{\times}$, where $\tau(x)=\prod_{p\leq \infty}\tau_{p}(x)$ and $\tau_{\infty}(x)=e^{2\pi ix_{\infty}}$ and $\tau_{p}(x)=1$ if and only if $x_{p}\in \mathbb{Z}_{p}$. Thus $    \phi_{f}\bigg(\begin{pmatrix}
    1&x\\
    0&1
    \end{pmatrix}g\bigg)$ has a Fourier expansion as a function of $x$:
\begin{equation*}
    \phi_{f}\bigg(\begin{pmatrix}
    1&x\\
    0&1
    \end{pmatrix}\bigg)=\sum_{\lambda\in\mathbb{Q}}\phi_{f,\lambda}(g)\tau(\lambda x),
\end{equation*}
where 
\begin{equation*}
    \phi_{f,\lambda}(g)=\int_{\mathbb{Q}^{\times}\backslash\mathbb{A}^{\times}}\phi_{f}\bigg(\begin{pmatrix}
    1&x\\
    0&1
    \end{pmatrix}g\bigg)\overline{\tau(\lambda x)}\text{d}x
\end{equation*}
is the $\lambda-$th Fourier coefficient of $\phi_{f}\bigg(\begin{pmatrix}
    1&x\\
    0&1
    \end{pmatrix}g\bigg)$ depending on $g$.

Suppose $f\in S_{k}(\Gamma(1))$ has Fourier expansion $f=\sum_{n}a_{n}e^{2\pi i n\pi}$, and $\phi_{f}$ is the associated adelic automorphic form. Then for real $y>0$, 
\begin{equation*}
    \phi_{f}\bigg(\begin{pmatrix}
    y&0\\
    0&1
    \end{pmatrix}\bigg)=\sum_{n=1}^{\infty} a_{n}e^{-2\pi ny}\ \ \text{if}\ \lambda=n\in\mathbb{Z}
\end{equation*}
otherwise it's 0.
Letting $x=0$, so that $\begin{pmatrix}
1&x\\
0&1
\end{pmatrix}=\text{Id}$ and $\tau(\lambda x)=1$, and defining 
\begin{equation*}
    W_{\phi_{f}}(g)=\int_{\mathbb{Q}\backslash\mathbb{A}}\phi\bigg(\begin{pmatrix}
    1&x\\
    0&1
    \end{pmatrix}g\bigg)\overline{\tau(x)}\text{d}x
\end{equation*}
to be the first Fourier coefficient of $\phi_{f}$, we find 
\begin{equation*}
    \phi_{f}\bigg(\begin{pmatrix}
    y&0\\
    0&1
    \end{pmatrix}\bigg)=\sum_{\lambda\in\mathbb{Q}^{\times}}\phi_{f,\lambda}\bigg(\begin{pmatrix}
    y&0\\
    0&1
    \end{pmatrix}\bigg)=\sum_{\lambda\in\mathbb{Q}^{\times}}W_{\phi_{f}}\bigg(\begin{pmatrix}
    \lambda y&0\\
    0&1
    \end{pmatrix}\bigg)
\end{equation*}
Now our $L$-functions becomes
\begin{equation*}
    L(f,s)=\int_{\mathbb{Q}^{\times}\backslash\mathbb{A}^{\times}}\sum_{\lambda\in\mathbb{Q}^{\times}}W_{\phi_{f}}\bigg(\begin{pmatrix}
    \lambda y&0\\
    0&1
    \end{pmatrix}\bigg)|y|^{s}\text{d}^{\times}y=\int_{\mathbb{A}^{\times}}W_{\phi_{f}}\bigg(\begin{pmatrix}
    y&0\\
    0&1
    \end{pmatrix}\bigg)|y|^{s}\text{d}^{\times}y.
\end{equation*}
In other words, $L(f,s)$ is the adelic Mellin transform along $\begin{pmatrix}
y&0\\
0&1
\end{pmatrix}$ of the first Fourier coefficient of $\phi_{f}$. This is supposed to suggest that in general, the $L$-function associated to an automorphic representation $\pi$ should be the Mellin transform of the first Fourier coefficient of some distinguished functions in the space of $\pi$.

As it is described in this last section, the function $W_{\phi_{f}}$ satisfies the conditions of Whittaker model: the right-translations of $W_{\phi_{f}}$ generate a space $W_{\pi_{f}}$ of functions $W$ on $GL_{2}(\mathbb{\mathbb{A}})$. The equivalent representation $W(\pi_{f})$ is called the Whittaker model of $\pi_{f}$.

To every function in the local Whittaker model we associate a $\zeta-$function, a special one of which will be our local $L$-function. Let $\pi_{v}$ be an irreducible admissible representation of $GL_{2}(F_{v})$, $\chi$ a unitary character of $F^{\times}_{v}$, $g\in GL_{2}(F_{v})$, $W\in W(\pi_{v})$. Then define a local $\zeta-$ function for all of the data by
\begin{equation*}
    \zeta(g,\chi,W,s)=\int_{F^{\times}_{v}}W\bigg(\begin{pmatrix}
    a&0\\
    0&1
    \end{pmatrix}\bigg)\chi(a)|a|^{s-1/2}\text{d}^{\times}a.
\end{equation*}
\begin{thm}
\begin{enumerate}
    \item The integral $\zeta(g,\chi,W,s)$ converges in the right half plane;
    \item There is a $W^{0}\in W(\pi_{v})$ such that $L(\chi\otimes \pi_{v},s)=\zeta(1,\chi,W^{0},s)$ is an Euler factor making $\frac{\zeta(g,\chi,W,s)}{L(\chi\otimes\pi_{v},s)}$ entire for every $g, \chi, W$. ;
    \item $\zeta(W,s)$ has an analytic continuation the whole plane satisfying the functional equation
    \begin{equation*}
        \frac{\zeta(g,\chi,W,s)}{L(\chi\otimes\pi_{v},s)}\varepsilon(\pi_{v},\chi,s)=\frac{\zeta(wg,\chi^{-1}\psi^{-1},W,1-s)}{L(\chi^{-1}\psi_{v}^{-1}\otimes\pi_{v},1-s)}
    \end{equation*}
    for some function $\varepsilon(\pi_{v},\chi,s)$ independent of $g, W$, where $w=\begin{pmatrix}
    0&1\\
    -1&0
    \end{pmatrix}$, $\phi_{v}$ is the central character of $\pi_{v}$.
\end{enumerate}
\end{thm}
For a finite place $v$, Euler factor means $\frac{1}{P(q^{s})}$ where $P$ is a polynomial with constant term 1 and $q=|w_{v}|$, for an infinite place, it means some kind of $\Gamma$-factor. We skip the details of this theorem \cite{gelbart2016automorphic}. 


\section{Equivalence between the Ingredient of Two Types of $L$-Function}
\subsection{Introduction}
The goal of this section is to use theta correspondence to understand the equivalence between Godement-Jacquet Zeta integral and Jacquet-Langlans Zeta integral. Then by the relation of Zeta integral, we will be able to understand the equivalence of corresponding $L$-functions in a more conceptual way rather than cumbersome calculation. Here we only consider $GL_{2}(F)$, in which $F$ is a non-Archimedean local field and the characteristic of $F$ is not equal 2. But the method we used is available for $GL_{n}$ or global situation, which won't be covered in this thesis.

To construct the Godement-jacquet Zeta integral, there should be a test function from Bruhat-Schwartz function space $Y=S(M_{2}(F)\times F^{\times})$ and a matrix coefficient from $\widetilde{V}\otimes V$, in which $(\pi, V)$ is a representation of $G=GL_{2}(F)$ and $\tilde{V}$ is the contragredient representation of $V$. Putting all the ingredient for Godement-Jacquet Zeta integral together, we denote it as $\widetilde{V}\otimes_{G}Y\otimes_{G}V$. Notice that this tensor product is not as same as the tensor product of representations which we will explain the construction later.  On the other side, the Jacquet-Langlands only need one object for the ingredient: a vector from Kirillov model of the representtation $(\pi, V)$. Its ingredient saves in $\mathcal{K}(V(-1)(1)$. So the dream here is to construct an isomorphism between those two ingredient space of Godement-jacquet Zeta integral and Jacquet-Langlands Zeta integral with the respect to GCD procedure of constructing corresponding $L$-functions. Evidently, the Kirillov model can be taken as a $G-$module so we need to make $\widetilde{V}\otimes_{G}Y\otimes_{G} V$ into a $G$-module by Schr\"{o}dinger model as well. So the isomorphism of $G$-modules that are relevant to the Zeta integral is a categorification of the  equivalence between of Godement-Jacquet method and Jacquet-Langlands method. The relative category of $G-$modules have symmetric monoidal structure. But the topic of the monoidal structure on the category of $G$-module is not the main story of this thesis. 
\subsection{Recollection of Bernstein center}\label{Bernstein}

Before the story begins, let's explain why we need this categorically abstract definition of a center. However, the Bernstein center of $G$ contains much more information. It turns out that it contains enough operators that, given a generic representation of $G$, that representation can be fully characterized by the action of the Bernstein center on it (in fact, in this case, the Bernstein center is fully known).

For this section it's recollection of \cite{zhang2019bernstein}.
 First, let us set so notations. Given $F$ as a non-Archimedean local field and denote $G=GL_{2}(F)$. Then we pick a compact and open subgroup $K$ of $G$. $e_{K}=\chi(K)/\text{vol}(K)$ is the characteristic funtion of $K$. $\hat{G}$ denotes as the set of irreducible smooth representations of $G$ over $\mathbb{C}$. $H(G)$ is the Hecke algebra, which is the convolution algebra of locally constant $\mathbb{C}$-valued functions on $G$ with compact support. 
 \begin{cla}
 \begin{equation*}
     H(G)= \varinjlim_{K} H(G, K)
 \end{equation*}
 \end{cla}
 \begin{defi}
 We define the Bernstein center $Z(G)$ abstractly as the endomorphism ring of the identity functor of the category of smooth complex representaion $\mathfrak{G}$ of $G$. Then the Bernstein center $Z(G)$ acts on any smooth representation and this action commutes with any $G-$morphism. 
 \end{defi}
 \begin{rem}
 More precisely, $Z(G)=\text{End}(Id_{\mathfrak{G}})$. For an element $\phi\in Z(G)$ is a set of maps $\phi_{A}: A\rightarrow A$ for $A\in \text{ob}(\mathfrak{G})$ such that for $\alpha: A\rightarrow B$, the following diagram commutes:
 \begin{center}
\begin{tikzcd}
A \arrow[rr, "\phi_{A}"] \arrow[d, "\alpha"] &  & A \arrow[d, "\alpha"] \\
B \arrow[rr, "\phi_{B}"]                     &  & B                    
\end{tikzcd}
 \end{center}
 \end{rem}
\begin{ex}
 For example, given an algebra, the Bernstein center of the category of modules for that algebra is the center of the algebra (i.e., elements that commute with all others). In particular, the Bernstein center of $G$ contains the actual center (as a group) $Z(G)$ of $G$.
\end{ex}
 Next, our goal is to describe the abstract words in the definition of Bernstein center $Z(G)$.
 
 \begin{defi}
 Denote the center of $H(G, K)$ by $Z(G, K)$ and let 
 \begin{equation*}
     \hat{H}(G)=\varprojlim_{K} H(G, K),\ \ \ \ Z(G)=\varprojlim_{K} Z(G, K),
 \end{equation*}
 \end{defi}
 where the transition maps are given by applying idempotents(i.e.  $f\in H(G, K)\mapsto e_{K'}*f*e_{K'}$ for $K'\subset K$). 
\subsection{Recollection of Weil Representation}
Introduce the notation first, $F$ as a non-Archimedean local field, in order to avoid technical problem, we require that characteristic of $F$ is not equal 2. In this section we require that all representations $(\pi, V)$ are smooth and complex. And we require that $V$ are all finite dimensional. Denote the space of all locally constant and compact supported functions by $\mathcal{S}(V)$. This section is a recollecction of \cite{kudla1996notes}.

\begin{defi}
Given $W$ a finite dimensional vector space over $F$ with a non-degenerate alternating form $<, >$. Here, the word alternating means that $<x,x>=0,\ \forall x\in W$, nondegenerate means that if for all $y$ we have $<x, y>=0$, then $x$ must be zero. For convenience, we define that the dimension of $W$ is $2n$. Then the $W$ is the symplectic space.
\end{defi}
\begin{defi}
The Heisenberg group $H(W)$ is non-trivial central extension of $W$ by $F$, so $H(W)$ is a group of pairs as
\begin{equation*}
    \big\{ (w,t): w\in W, t\in F \big\},
\end{equation*}
and the operation of the group is as follow:
\begin{equation*}
    (w_{1},t_{1})(w_{2},t_{2})=(w_{1}+w_{2},t_{1}+t_{2}+\frac{1}{2}<w_{1},w_{2}>).
\end{equation*}
\end{defi}
\begin{rem}
We get a short exact sequence:
\begin{equation*}
   0\rightarrow F\rightarrow H(W)\rightarrow W\rightarrow 0 
\end{equation*}
$F$ is commutator subgroup of Heisenberg group. Now we can describe $H(W)$ as $H(W)= F^{\times}\times W$. 
\end{rem} 
\begin{rem}
Heisenberg group $H(W)$ is nilpotent.
\end{rem}
Next in order to consider the representation of Heisenberg group, all the finite dimensional representation are one dimensional, and factor through $W$. So the next task is to construct infinite dimensional representation:

First we break $W$ into $W_{1}\bigoplus W_{2}$, in which $W_{1}$ and $W_{2}$ are called the maximal totally isotropic subspace or called the Lagrangian subspace. Isotropic subspace of a symplectic vector space means a vector subspace on which the the symplectic form vanishes.  This is the complete polarisation of $W$.

Given an additive character $\phi$ of $F$, the Schr\"odinger representation of Heisenberg group $\rho_{\phi}: H(W)\rightarrow \mathcal{S}(W_{1})$ is defined as follow: 
\begin{enumerate}
    \item $\rho_{\phi}(w_{1})f(x)=f(x+w_{1}),\ x,w_{1}\in W_{1}$;
    \item $\rho_{\phi}(w_{2})f(x)=\phi(<x,w_{2}>)f(x),\ x\in W_{1},\ w_{2}\in W_{2}$;
    \item $\rho_{\phi}(t)f(x)=\phi(t)f(x),\ t\in F,\ x\in W_{1}$.
\end{enumerate}
By those properties, it defines smooth representation of $H(W)$, which is called Schr\"odinger representation.

The most important result regrading Weil representation, it's the following theorem:
\begin{thm}
\textbf{Stone, Von Neuman, Mackey}: Let $H(W)$ be a Heisenberg group. Then
\begin{enumerate}
    \item $H(W)$ has be unique irreducible unitary representation
    \begin{equation*}
        \rho_{\phi}: H(W)\rightarrow Aut(\mathcal{S}_{0})
    \end{equation*}
    such that $\rho_{\phi}((0, t))=\phi(t)\cdot Id_{\mathcal{S}_{0}}$, all $\lambda\in F^{\times}$.
    \item For all maximal isotropic subgroups $J\subset K$ and splittings $\sigma(x)=(\alpha(x),x)$ of $\pi$ over $J$, this representation may be realized by 
    \begin{equation*}
        \mathcal{S}_{0}=\{\text{Measurable functions}\ f: W\rightarrow F \}
    \end{equation*}
    such that $f(x+h)=\alpha(h)^{-1}\psi(h,x)f(x),\ \forall h\in J$ and $\int_{J/H}|f(x)|^{2}dx<+\infty$.
    
    $\rho_{(\phi(t),y)}f(x)=\phi(t)\cdot\psi\cdot f(x+y)$. We will write this $\mathcal{S}_{0}$ as $L^{2}(K//H)$.
    \item All representations $(\rho_{\phi},\mathcal{S})$ such that $\rho_{\phi}((0,t))=\phi(t)\cdot Id_{\mathcal{S}}$ are isomorphic to $\mathcal{S}_{0}\hat{\otimes}\mathcal{H}_{1}$, $G$ acting trivially on $\mathcal{S}_{1}$.
\end{enumerate}
\end{thm}



Next goal is to construct the Weil representation or the metaplectic representation, a projective representation of the metaplectic group which is constructed using interwing operators of this representation of Heisenberg group. 

The first object we need is the sympletic group $Sp(W)$ of $W$, which is the automorphism of $W$ that can preserve form $<,>$.
\begin{equation*}
    Sp(W):=\{g\in GL(W)|<g(x),g(y)>=<x,y>\}
\end{equation*}
The sympletic group takes action on $H(W)$ via $g(w,t)=(g.w,t)$. And this action is trivial on the center of $H(W)$: $Z((H(W))\cong F^{\times}$ .

\begin{defi}
The $\widetilde{Sp_{\phi}}(W)$ is a group under point-wise multiplication defined as following: 
\begin{equation*}
    \widetilde{Sp}_{\phi}(W):=\{(g,w_{\phi}):\rho_{\phi}(gw,t)\circ w_{\phi}(g)=w_{\phi}(g)\rho_{\phi}(w,t),\ for\ \forall (w,t )\in H(W)\},
\end{equation*}
in which $(\rho_{\phi}, \mathcal{S})$  is the representation of Heisenberg group $H(W)$. And the $\widetilde{Sp}_{\phi}(W)$ is called metaplectic group of $Sp(W)$.
$w_{\phi}(g)\in GL(\mathcal{S})$ is the interwining operator for the representation $(\rho_{\phi},\mathcal{S})$ of Heisenberg group, which is unique up to scaling.
\end{defi}
\begin{rem}
For the metapletic group, we have the short exact sequence:
\begin{equation*}
  0\rightarrow \mathbb{C}^{\times} \rightarrow \widetilde{Sp}_{\phi}(W)\xrightarrow{p}Sp(W)\rightarrow 0  
\end{equation*}
$\widetilde{Sp}_{\phi}(W):=Mp(W)$ is the metapletic group that we need. For this group, we have the projection map as 
\begin{align*}
     \pi_{p}: \widetilde{Sp}_{\phi}(W)&\rightarrow Aut(\mathcal{S})\\
      (g, w_{\phi}(g))&\rightarrow w_{\phi}(g),
\end{align*}
which provides a natural representation of $\widetilde{Sp}_{\phi}(W)$. This representation of the metaplectic group is called the Weil representation or the metaplectic
representation or the oscillator representation.
\end{rem}
\begin{thm}
The projection map $p$ that restricts to the commutator subgroup $\hat{Sp}_{\phi}(W)=[\widetilde{Sp}_{\phi}(W),\widetilde{Sp}_{\phi}(W)]$ is a map onto $Sp_{\phi}(W)$ with a kernel of order 2:
\begin{equation*}
    \widetilde{Sp}_{\phi}(W)=\hat{Sp}_{\phi}(W)\times \mathbb{C}^{\times}. 
\end{equation*}
2-sheeted covering $\hat{ Sp}_{\phi}(W)$ of $Sp(W)$ is independent of the additive character $\phi$ but Weil representation restricted to $\hat{Sp}_{\phi}(W)$ does so. 
\end{thm}
\begin{rem}
The subgroup $\hat{Sp}_{\phi}(W)$ satisfies an exact sequence:
\begin{center}
    \begin{tikzcd}
1 \arrow[r] & \mathbb{C}^{\times} \arrow[r] & \widetilde{Sp}_{\phi}(W) \arrow[r]     & Sp(W) \arrow[r]                                & 1 \\
1 \arrow[r] & \mu_{2} \arrow[r] \arrow[u]   & \hat{Sp}_{\phi}(W) \arrow[r] \arrow[u] & Sp(W) \arrow[r] \arrow[u, no head, Rightarrow] & 1,
\end{tikzcd}
\end{center}
in which $\mu_{2}=\{\pm1\}$.
\end{rem}
\begin{rem}
The metaplectic group $Mp(W)$ is not a matrix group: it has no faithful finite-dimensional representations. Therefore, the question of its explicit realization is nontrivial. It has faithful irreducible infinite-dimensional representations, such as the Weil representation described below.
\end{rem}

 The Schr\"odinger model comes from the calculation of Rao cocycle\cite{kudla1996notes}. Before getting into the general model, here is a toy example:
\begin{ex}
For symplectic group $Sp(2n,\mathbb{R})$, when $n=1$, $Sp(2,\mathbb{R})=SL_{2}(\mathbb{R})$. And we know there is a biholomorphic action on upper half plane: 
\begin{equation*}
    g.z=\frac{az+b}{cz+d},\ \ g=\begin{pmatrix}
    a & b \\
    c & d
    \end{pmatrix}\in SL_{2}(\mathbb{R}).
\end{equation*}
We can use this action to construct metaplectic group of $SL_{2}(\mathbb{R})$. The elements of $Mp(2,\mathbb{R})$ are the pairs of $(g,\epsilon_{g})$, in which $g\in SL_{2}(\mathbb{R})$ and $\epsilon_{g}$ is the holomorphic function on upper half plane: $\epsilon_{g}(z)^{2}=(cz+d)=j(g,z)$. The multiplication of $Mp(2,\mathbb{R})$ is defined by
\begin{equation*}
    (g_{1},\epsilon_{g_{1}})\cdot (g_{2},\epsilon_{g_{2}})=(g_{1}g_{2},\epsilon),\ \ \text{where}\  \epsilon(z)=\epsilon_{g_{1}}(g_{2}.z)\epsilon_{g_{2}}(z).
\end{equation*}
This product is well-defined follows from the cocycle relation:
\begin{equation*}
    j(g_{1}g_{2},z)=j(g_{1},g_{2}.z)j(g_{2},z).
\end{equation*}
Then the map $(g, \epsilon_{g})\rightarrow g$ is surjective from $Mp(2,\mathbb{R})\rightarrow SL_{2}(\mathbb{R})$ which does not have any continuous section. Hence we have constructed a non-trivial double cover of $SL_{2}(\mathbb{R})$.
\end{ex}





Now we give the explicit model called Schr\"odinger model of metaplectic representation over a local field $F$. $W=W_{1}\bigoplus W_{2}$ is the complete polarisation of $W$. 
Then $Sp(W)$ can be written as matrices with respect to the basis $\{e_{1},...,e_{n},f_{1},...,f_{n}\}$, $e_{i}\in W_{1}$, $f_{i}\in W_{2}$ and $<e_{i},f_{j}>=\delta_{ij}$.

Let's consider the generators of $Sp(W)$:
The first case is 
$\begin{pmatrix}
A & 0\\
0 & ^{t}A^{-1}
\end{pmatrix}\in Sp(W)$. The action of this matrix is metaplectic representation on $\mathcal{S}(W_{1})$ is given by 
\begin{equation*}
    w_{\phi}
    \begin{pmatrix}
    A & 0\\
    0 & ^{t}A^{-1}
    \end{pmatrix}f(x)=|\text{det}(A)|^{\frac{1}{2}}f(^{t}Ax),
\end{equation*}
in which the $|\text{det}A|^{\frac{1}{2}}$ makes action of $GL(W_{1})$ unitray for Hermitian structure $(f_{1},f_{2})=\int_{W_{1}}f_{1}\bar{f_{2}}\text{d} w$ on $\mathcal{S}(W_{1})$.

The second case is $\begin{pmatrix}
1 & B\\
0& 1
\end{pmatrix}\in Sp(W)$ if and only if $B=\ ^{t}B$, the action of this matrix is 
\begin{equation*}
    w_{\phi}\begin{pmatrix}
    1 & B\\
    0 &1
    \end{pmatrix}f(x)=\phi(^{t}xBx)f(x).
\end{equation*}

And the third case acts by $w_{\phi}\begin{pmatrix}
0 & 1 \\
-1 & 0
\end{pmatrix}f(x)=\gamma \hat{f}(x)$, in which $\gamma$ is the 8th root of unity and $\hat{f}$ is the Fourier transform given as 
\begin{equation*}
    \hat{f}(x)=\int_{F^{n}} f(y)\phi(\sum^{n}_{i=1}x_{i}y_{i})dy
\end{equation*}
and $\hat{\hat{f}}(x)=f(-x)$.

And it's obvious to see that those actions given above satisfy the condition for metaplectic group.


\subsection{The Construction of Middle Action and the Properties}
First consider $S(GL_{2}(F))$ 
 as bi-$G$-module with fixed Haar measure $\text{d}^{\times}g$ to make the volume of the maximal compact subgroup is 1. We need to understand the spectral decomposition of this bi-module $S(GL_{2}(F))$ by using Plancherel measure for $GL_2(F)$ \cite{arthur1991local}:
 For a pair of irreducible representations $(\pi,V)$ and $(\pi',V')$ of $GL_{2}(F)$, if $V\cong V'$, we have  
 \begin{equation*}
\widetilde{V}\otimes_{G}S(GL_{2}(F))\otimes_{G}V'\xrightarrow{\cong}\mathbb{C},
 \end{equation*}
otherwise,
\begin{equation*}
\widetilde{V}\otimes_{G}S(GL_{2}(F))\otimes_{G}V'=0
\end{equation*}
where $\widetilde{V}$ is the contragredient representation of $V$ taken as a right module, which means every bi-$G$-module $V\otimes_{G}\widetilde{V}$ appears uniquely up to isomorphism. Let's recall the definition of contragredient representation: given a smooth representation $(\pi, V)$ of $G$, then the contragredient representation of $(\pi, V)$ is the smooth representation $(\tilde{\pi}, \widetilde{V})$ of $G$ where $\tilde{V}$ is the space of linear forms on $V$ that are invariant by an open subgroup and for every $g\in G, \tilde{v}\in \tilde{V},\  \tilde{\pi}\circ\tilde{v}=\tilde{v}\circ\pi(g)^{-1}$. 
We skip the discussion about the dependence of this decomposition on the continuous part of the spectrum but focus on the detail about the construction of bi-$G$-module. 

The main theme that we need to discuss is the spectral decomposition of $S(M_{2}(F))$, which relates to the construction of Godement-Jacquet $L$-functions. The aspect we are going to consider is compute the spaces: $\tilde{V}\otimes_{G}S(M_{2}(F))\otimes_{G}V$ with irreducible generic representation $(\pi, V)$. As considering about the diagonal part of the spectral decomposition, we observe that the two actions of Bernstein center of $G$ on $S(M_{2}(F))$ coincide because the two actions of the center on $S(G)$ coincide, as well as that $S(M_{2}(F))$ embeds in the contragredient of $S(G)$. This means that the off-diagonal components $\widetilde{V}\otimes_{G}S(M_{2}(F))\otimes_{G}V'$ with $V\not=V'$ are 0. 
This can be shown using the fact that the elements of the Bernstein center of $G$ must commute with the action of $G$. Using this fact, one can indeed show that the tensor product $\widetilde{V} \otimes_G S(M_2(G)) \otimes_G V'$ is 0 for $V\neq V'$ generic. Indeed, the Bernstein center of $G$ acts on $V’$ with one character, and on $V$ with another. However, because it commutes with $S(M_2(G))$, it must act on both sides of it via the same character, unless the tensor product is actually 0.
















































Denote $Y=S(M_{2}(F)\times F^{\times})$. There are already two $G$-actions, then we need to use Weil representation to construct the middle action. This middle action is defined as the following theorem.
\begin{thm}\label{thm2.2}
There exists a third action on $Y$, and this action is defined uniquely by three properties:
\begin{enumerate}
    \item This middle action is commutative with the right and left actions;
    \item Given generic representation $(\pi, V)$, there is a $G-$module isomorphism:
    \begin{equation*}
        \nu:\widetilde{V}\otimes_{G}Y\otimes_{G}V\rightarrow\mathcal{K}(V(-1))(1)
    \end{equation*}
    \item The isomorphism is compatible with the commutative diagram:
\begin{center}
    \begin{tikzcd}
\widetilde{V}\otimes_{G}Y^{0}\otimes_{G}V \arrow[rr, "\mu"] \arrow[d] &  & S(F^{\times}) \arrow[d] \\
\widetilde{V}\otimes_{G}Y\otimes_{G}V \arrow[rr, "\nu"]               &  & \mathcal{K}(V(-1))(1)            
\end{tikzcd}
\end{center}
in which $Y^{0}:=S(GL_{2}(F)\times F)$.
\end{enumerate}
\end{thm}
\begin{rem}
The Kirillov model is unique up to scalar, which is the reason why we need to add the twist.

In the diagram, $\mu$ is an isomorphism described as  \begin{align*}
    \widetilde{V}\otimes_{G}Y^{0}\otimes_{G}V&\xrightarrow{\mu} S(F^{\times}) \\
    \widetilde{v}\otimes \Psi\otimes v&\mapsto \int_{GL_{2}(F)}<\tilde{v},\pi(g)v>\Psi(g,y\det(g)^{-1})\mulldif g
\end{align*}
\end{rem}
\subsubsection{The Construction of Middle Action}
To prove the theorem, we construct this middle action then prove the three properties. 
The idea is that we need to find the suitable metaplectic group via constructing the symplectic space to make $M_{2}(F)$ lagrangian subspace. This first step is to understand what $\widetilde{V}\otimes_{G}Y\otimes_{G}V$ is, in which $Y=S(M_{2}(F)\times F^{\times})$. Here we consider a generic representation $(\pi, V)$, i.e. has a Kirillov model. We can take the representation $(\pi, V)$ as a left $G-$module by the left action: $g\cdot v=\pi(g)v$ and the contragredient representation $(\tilde{\pi}, \widetilde{V})$ of $(\pi, V)$ has a left action of $G$, which can make it into a right action by $g\rightarrow g^{-1}$.

 $\widetilde{V}\otimes_{G}S(M_{2}(F))\otimes_{G}V$ is a 1-dimensional vector space. It's not interesting enough, to avoid the redundancy of proof, we need to consider  $\widetilde{V}\otimes_{G}Y\otimes_{G}V$, which is because Godement-jacquet Zeta integral is invariant under translation: $g\rightarrow hgh'$.

Now Let's admit the existence of middle action. Then $Y$ becomes a $G\times G\times G$-module. For the notation in the theorem \ref{thm2.2}, $\widetilde{V}\otimes_{G}Y\otimes_{G}V$ can be well defined as a result of tensor product of $ G$-modules. And by constructing this notation, we want to cancel the two trivial left and right action of $G$ on $Y$ by coinvariant with the $\widetilde{V}\otimes_{G}V$, then make $\widetilde{V}\otimes_{G}Y\otimes_{G}V$ a $G$-module with the action of Weil representation, in which the trivial left and right actions are defined as following:
\begin{equation*}
    g_{l}\cdot (g,y)\cdot g_{r}=(g_{l}gg_{r},y\cdot \text{det}(g_{l}g_{r})^{-1}).
\end{equation*}



First, we take these two products step by step. Next, we need to turn one of the actions into a right action. 
\begin{equation*}
    \widetilde{V}\otimes_{G}Y := \widetilde{V}\otimes Y/<g\cdot\tilde{v}\otimes y-\tilde{v}\otimes g_{r}\cdot y>,
\end{equation*}
in which $g_{r}$ means the right action of $G$ on $Y$. After canceling out the action on $\tilde{V}$ and the action of $g_{r}$. Now $\tilde{V}\otimes_{G}Y$ is a $G\times G$-module.
\begin{equation*}
    (\widetilde{V}\otimes_{G}Y)\otimes_{G} V:= (\widetilde{V}\otimes_{G}Y)\otimes V/<g_{l}\cdot\overline{(\tilde{v}\otimes_{G} y)}\otimes v-\overline{(\tilde{v}\otimes_{G} y)}\otimes g\cdot v>,
\end{equation*}
in which the $\overline{\tilde{v}\otimes_{G} y}$ is defined as the representative of the quotient module. And in order to inherit the left action of $Y$ into $\widetilde{V}\otimes_{G}Y$, we require that
\begin{equation*}
    g_{l}\cdot(\tilde{v}\otimes_{G} y)=\tilde{v}\otimes_{G} g_{l}\cdot y.
\end{equation*}
Taking those two tensor product, $\widetilde{V}\otimes_{G}Y\otimes_{G} V$ becomes a simple $G$-module with the action of Weil representation.

Except taking tensor product one by one, we can take $Y$ as $G\times G^{2}$-module, in which $G^{2}:=G\times G$. And $\widetilde{V}\boxtimes V$ is a $G\times G$-module with separate actions from the representation of $G$. $\tilde{V}\otimes V$ is a representation of $\Delta G\subset G^{2}$.
\begin{equation*}
    Y\otimes_{G^{2}} (\widetilde{V}\boxtimes V)=\widetilde{V}\otimes_{G} Y\otimes_{G} V
\end{equation*}
By using this box tensor product, we can directly get the $G$-module that we need.

On the other hand, we can also justify this notation by definition of tensor product of modules. 
\begin{rem}
For the $G$-modules, i.e. the modules over group ring $\mathbb{Z}[G]$, they form an Abelian category $G-Mod$.
\end{rem}
For group ring $\mathbb{Z}[G]$, and fixed the modules $\widetilde{V},\ Y,\ V$ as above, the tensor product $\widetilde{V}\otimes_{G}Y$ of modules over $\mathbb{Z}[G]$ is an Abelian group with a balanced product 
\begin{equation*}
    \otimes: \widetilde{V}\times Y\rightarrow \widetilde{V}\otimes_{G}Y,
\end{equation*}
which is universal in the following sense:
\begin{center}
\begin{tikzcd}
\widetilde{V}\times Y \arrow[rr, "\otimes"] \arrow[rrd, "f"] &  & \widetilde{V}\otimes_{G} Y \arrow[d, "\tilde{f}", dashed] \\
                                                         &  & \mathcal{A}                                          
\end{tikzcd}
\end{center}
\begin{rem}
Let's recall the construction of balanced product:

As we said earlier, for a given $G$-module, we can take it as a module over group ring $\mathbb{Z}[G]$. So for ring $\mathbb{Z}[G]$, a  right module $\widetilde{V}$, a module $Y$ with the three actions, and a left module $V$. Given an arbitrary Abelian group $\mathcal{A}$, for example, we deal with $\widetilde{V}$ and $Y$ first, a map $\Gamma_{\mathcal{A},\mathbb{Z}[G]}: \widetilde{V}\times Y\rightarrow \mathcal{A}$ is said to be a $\mathbb{Z}[G]$-balanced, $\mathbb{Z}[G]$-middle-linear or $\mathbb{Z}[G]$-balanced product, if for $\tilde{v},\ \tilde{v'}\in \widetilde{V}$, $y,\ y'\in Y$ and $g\in \mathbb{Z}[G]$ the following holds:
\begin{enumerate}
    \item $\Gamma_{\mathcal{A},\mathbb{Z}[G]}(\widetilde{v}, y+y')=\Gamma_{\mathcal{A},\mathbb{Z}[G]}(\widetilde{v},y)+ \Gamma(\widetilde{v},y')$;
    \item $\Gamma_{\mathcal{A},\mathbb{z}[G]}(\widetilde{v}+\widetilde{v'},y)=\Gamma_{\mathcal{A}+\mathbb{Z}[G]}(\widetilde{v},y)+\Gamma_{\mathcal{A},\mathbb{Z}[G]}(\widetilde{v'},y)$;
    \item $\Gamma_{\mathcal{A},\mathbb{Z}[G]}(g\cdot \widetilde{v},y)=\Gamma_{\mathcal{A},\mathbb{Z}[G]}(\widetilde{v},g\cdot y)$.
\end{enumerate}
The actions in the definition are introduced in earlier section. And
the set of all such maps as balanced product are denoted as $L_{\mathbb{Z}[G]}(\widetilde{V},Y,\mathcal{A})$.

And given two balanced product $\Gamma_{1},\ \Gamma_{2}$, the operations $\Gamma_{1}+\Gamma_{2}$ and $-\Gamma$ are defined pointwisely. Those two operations make $L_{\mathbb{Z}[G]}(\widetilde{V},Y,\mathcal{A})$ an Abelian group.
\end{rem}
For every Abelian group $\mathcal{A}$ and balanced product $f:\widetilde{V}\times Y\rightarrow \mathcal{A}$, there is a unique homomorphism $\widetilde{f}: \widetilde{V}\otimes_{G}Y\rightarrow \mathcal{A}$, such that $\widetilde{f}\circ \otimes=f$. 

The tensor product can also be defined as a representative object for the functor $\mathcal{A}\rightarrow L_{\mathbb{Z}[G]}(\widetilde{V}, Y, \mathbb{Z}[G])$. Explicitly, there is an isomorphism:
\begin{align*}
\text{Hom}_{\mathbb{Z}}(\widetilde{V}\otimes_{G}Y, \mathcal{A})&\xrightarrow{\cong} L_{\mathbb{Z}[G]}(\widetilde{V}, Y, V)\\
g&\rightarrow g\circ \otimes.
\end{align*}
  
For $\widetilde{v}\in \widetilde{V}$ and $y\in Y$, one can write $\widetilde{v}\otimes_{G} y$ for the image of $(\widetilde{v},y)$ under $\otimes: \widetilde{V}\times Y\rightarrow \widetilde{V}\otimes Y$. From the definition of balanced product:
\begin{enumerate}
    \item $\widetilde{v}\otimes_{G} (y+y')=\widetilde{v}\otimes_{G} y+\widetilde{v}\otimes_{G} y'$;
    \item $(\widetilde{v}+\widetilde{v'})\otimes_{G} y=\widetilde{v}\otimes_{G} y +\widetilde{v'}\otimes_{G} y$;
    \item $g\cdot\widetilde{v}\otimes_{G} y=\widetilde{v}\otimes_{G} g\cdot y$.
\end{enumerate}

For several modules, the binary tensor product is associative. So 
\begin{equation*}
    (\widetilde{V}\otimes_{G}Y)\otimes_{G}V\cong \widetilde{V}\otimes_{G}(Y\otimes_{G} V).
\end{equation*}

So the construction of $\widetilde{V}\otimes_{G}Y$ takes a quotient of a free Abelian group with basis the symbols $\widetilde{v}*y$, used here to denote the ordered pair $(\widetilde{v}, y)$, for $\widetilde{v}$ in $\widetilde{V}$ and $y$ in $Y$ by the subgroup generated by all elements of the form
\begin{enumerate}
    \item $-\widetilde{v}*(y+y')+\widetilde{v}*y+\widetilde{v}*y'$;
    \item 
    $-(\widetilde{v}+\widetilde{v'})+\widetilde{v}*y+\widetilde{y}*y$;
    \item $(g\cdot \widetilde{v})*y-\widetilde{
    v}*(g\cdot y)$,
\end{enumerate}
where $\widetilde{v},\ \widetilde{v'}\in \widetilde{V}$, $y,y'\in Y$ and $g\in G$. The quotient map which takes $\widetilde{v}*y=(\widetilde{v}, y)$ to the coset containing $\widetilde{v}*y$; That is 
\begin{equation*}
    \otimes : \widetilde{V}\times Y\rightarrow \widetilde{V}\otimes_{G} Y,\ \ (m,n )\rightarrow [m*n], 
\end{equation*}
is balanced.

So far based on the construction of tensor product of $G-$modules, we can see the actions from those two $G$-modules have been quotiented out, which can be same as the coinvraiant version of tensor product.













Other task is to explain the notation $\mathcal{K}(V(-1))(1)$.  For a representation $V$, the notation $V(n)$ stands for the twist of $V$ by the character $|\text{det}(g)|^n$.
The notation $\mathcal{K}(V)$ is just the Kirillov model of $V$, which is isomorphic to $V$.
So $\mathcal{K}(V(-1))(1)$ is still isomorphic to the original representation $V$ as a representation. The only difference is that it is realized in a slightly different way from the usual Kirillov model. That is, as a space of functions on $F^\times$, given non-trivial additive character $e:F\rightarrow  \mathbb{C}^{\times}$ the mirabolic group acts on it via:
$\begin{pmatrix} 
a & b \\ 
0 & 1 
\end{pmatrix}$
sending the function $f(y)$ to:
$|a| e(bx) f(ay)$
instead of $e(bx) f(ay)$.


Let's get back to the theorem \ref{thm2.2}. For the isomorphism in property (3), it's a canonical isomorphism defined as:
\begin{align*}
    \mu: \widetilde{V}\otimes_{G}Y^{0}\otimes_{G}V&\rightarrow S(F^{\times})\\
    \widetilde{v}\otimes_{G}\Phi\otimes_{G}v&\rightarrow \int_{GL_{2}(F)}<\widetilde{v},\pi(g)v>\cdot \Phi(g,y\text{det}(g)^{-1})\text{d}^{\times}g.
\end{align*}

Now the preparation of construction of middle action is done. 



The goal is to turn $S(M_{2}(F))$ into a Weil representation of a metapletic group. Then we use the action of this metapletic group to construct the desired middle action.  To show that, we need to find appropriate symplectic space to make $M_{2}(F)$ a Lagrangian space. 

Denote $U=M_{2}(F)$, and $
    (m, m')\rightarrow <m ,m'>=\text{tr}(m)\text{tr}(m')-\text{tr}(mm')$
is the polarization of the quadratic map $m\rightarrow \text{det}(m)$. Given a two dimensional vector space $W$ with a standard basis $<e_{1},e_{2}>$, $U\otimes W$ can be a symplectic space via 
\begin{equation*}
    <m\otimes v, m'\otimes v'>=(v\wedge v')\cdot <m, m'>=(v\wedge v')\cdot (\text{tr}(m)\text{tr}(m')-\text{tr}(mm')).
\end{equation*}
 
So the symplectic group is 
\begin{equation*}
    Sp(U\otimes W)=Sp(M_{2}(F)\otimes W)=Sp(8, F).
\end{equation*}
In particular, we have a map:
    $G^{3, \text{det}=1}\rightarrow Sp(U\otimes W)$
in which $$G^{3,\text{det}=1}=\{(g_{1},g_{2},g_{3})\in G_{3}:\text{det}(g_{1}g_{2}g_{3}=1)\}.$$
And this embedding is given as $(g_{1}, g_{2},g_{3})\cdot (m\otimes v)= g_{1}m
    g_{3}^{T}\otimes g_{2}v.$
\begin{rem}
$G^{3, \text{det}=1}$ acts on $U\otimes W$ symmetrically. Identify $U=M_{2}(F)$ as the endomorphism group of $W$ such that $M_{2}(F)=\text{End}(W)=W\otimes W^{*}$, where $W^{*}$ denotes the dual space of $W$. Then $U\otimes W=W\otimes W^{*}\otimes W$, which makes the symplectic form invariant. In another word, we can describe  this symmetrical embedding as 
$S_{3}\ltimes G^{3, \text{det}=1}\rightarrow Sp(U\otimes W)$.

And this gives a symmetry of the three actions on $Y$, in which the middle will be constructed later. So we can consider $Y$ takes actions of $S_{3}\ltimes G^{3}$. In particular, the action of transpose $(1,3)\in S_{3}$ on $Y$ is given by 
\begin{equation*}
    (1,3)\cdot \varrho(m,t)=\varrho(g^{T},t),\ \ \varrho\in Y.
\end{equation*}

Recall that $g\rightarrow g^{-T}$ is the Cartan invollution on $G$, given by the inverse of the transpose  map $g^{-T}=(g^{T})^{-1}$.
\end{rem}







\begin{rem}
The embedding above can canonically lift to the double cover $Mp(U\otimes W)$.
\begin{center}
% https://tikzcd.yichuanshen.de/#N4Igdg9gJgpgziAXAbVABwnAlgFyxMJZABgBpiBdUkANwEMAbAVxiRAHEA9YAZlIB1+OGAA8cwWDgC+AXgCMUkFNLpMufIRQAmclVqMWbAMpoAFAFVBEPAFt4AAgDqASiUqQGbHgJEdcvfTMrIggALJmlvzWWHZwTq5SejBQAObwRKAAZgBOEDZIZCA4EEgK7jl5SDpFJYhlWbn5iIXFVdQMWGDBIFB0cAAWySDtdABGMAwACmremiAMMJk4w-pBbII2dDj9AMaMwGiKiVJAA
\begin{tikzcd}
{G^{3,\text{det}=1}} \arrow[rr] \arrow[rrd, "p", dashed] &  & Sp(U\otimes W)           \\
                                                                   &  & Mp(U\otimes W) \arrow[u]
\end{tikzcd}
\end{center}
And we have the exact sequence:
\begin{equation*}
    1\rightarrow \mu_{2}\rightarrow Mp(U\otimes W)\rightarrow Sp(U\otimes W)\rightarrow 1.
\end{equation*} 
There is the explicit formula of he action of $Mp(U\otimes W)$ by Schr\"{o}dinger model. If we want to make the action of $G^{3 ,\text{det}=1}$ explicit as well, the map $p$ has to be a group homeomorphism, which is because $Mp(U\otimes W)$ splits over $G^{3, \text{det}=1}$. So we can compose the action of $Mp(U\otimes W)$ on $S(M_{2}(F))$ to get the action of $G^{3, \text{det}=1}$ on $S(M_{2}(F))$.


\end{rem}
Now let's prove there is a unique metaplectic lift for the map $S_{3}\ltimes G^{3, \text{det}=1}\rightarrow Sp(U\otimes W)$.
\begin{proof}
First thing to do is to show the existence of this lift. And the first step to prove is that the subgroup $SL_{2}(F)^{3}\subset G^{3,\text{det}=1}$ admits a unique lift. Then we prove the rest of the group $G^{3,\text{det}=1}$. 

Then for the lift of each copy of $SL_{2}(F)$ is unique because its abelianization is trivial. Note that the subgroup $SL_{2}(F)\times\{1\}\times SL_{2}(F)$ has metaplectic lift by the following action on $S(M_{2}(F))$:
\begin{equation*}
    (g_{1},1,g_{3})\cdot \Phi(m)=\Phi(g_{1}^{-1}mg^{-1}_{3}).
\end{equation*}
$SL_{2}(F)\times SL_{2}(F)\times\{1\}$ and $\{1\}\times SL_{2}(F)\times SL_{2}(F)$ are conjugate to it, these pairs admit metaplectic lifts as well, and all of those lifts agree on each factor $SL_{2}(F)$ separately by uniqueness. This shows that there is a metaplectic lift for $SL_{2}(F)\times SL_{2}(F)\times SL_{2}(F)$. Thanks to Schrödinger model, we can write down the action of the middle copy of $SL_{2}(F)$:
\begin{align*}
    \big(1,\begin{pmatrix}
    1&b\\
    0&1
    \end{pmatrix},1\big)\cdot \Psi(m)&=e(b\cdot \text{det}(m))\cdot \Psi(m)\\
    \big(1, \begin{pmatrix}
    t &0\\
    0& t^{-1}
    \end{pmatrix},1\big)\cdot \Psi(m)&=|t|^{2}\cdot \Psi(t\cdot m)\\
    \big(1, \begin{pmatrix}
    0&-1\\
    1 & 0
    \end{pmatrix},1\big)\cdot \Psi(m)&=\int_{M_{2}(F)}\Psi(n)e(-<m,n>)\text{d}n
\end{align*}
where the measure $\text{d}n$ on $M_{2}(F)$ is normalized such that $e(<\cdot, \cdot>)$ is a self-dual character. 

Now we have a split exact sequence:
\begin{equation*}
    1\rightarrow SL_{2}(F)^{3}\rightarrow S_{3}\ltimes G^{3,\text{det}=1}\rightarrow S_{3}\ltimes (F^{\times})^{3,\prod=1}\rightarrow 1
\end{equation*}
where $(F^{\times})^{3,\prod=1}=\{(a,b,c)\in (F^{\times})^{3}|abc=1\}$. This subgroup can be embedded into $G^{3,\text{det}=1}$ via
\begin{equation*}
    (a,b,c)\rightarrow \bigg(\begin{pmatrix}
    a&0\\
    0&1
    \end{pmatrix},\begin{pmatrix}
    b&0\\
    0&1
    \end{pmatrix},
    \begin{pmatrix}
    c&0\\
    0&1
    \end{pmatrix}\bigg)
\end{equation*}

Thus it still needs to show that there is a metaplectic lift for $S_{3}\ltimes (F^{\times})^{3,\prod=1}$ as it will act by conjugation on $SL_{2}(F)^{3}$ by uniqueness.

The construction of the lift for $S_{3}\ltimes (F^{\times})^{3,\prod=1}$ can be finished in three steps:

First, we construct a lift $S_{2}\ltimes(F^{\times})^{3,\prod=1}$ for the copy of $S_{2}\subset S_{3}$ generated by the permutation of $\tau=(1,3)$. Then we will construct a lift for a permutation $\sigma\in S_{3}$ of order 3. Finally we will show that all required relations beteween $\sigma$ and $S_{2}\ltimes (F^{\times})^{3,\prod=1}$ must hold.

We lift $S_{2}\ltimes (F^{\times})^{3,\prod=1}$ explicitly by
\begin{align*}
    \bigg(\begin{pmatrix}
    a&0\\
    0&1
    \end{pmatrix},\begin{pmatrix}
    b&0\\
    0&1
    \end{pmatrix},
    \begin{pmatrix}
    c&0\\
    0&1
    \end{pmatrix}\bigg)\cdot \Psi(m)&= |b|\cdot \Psi\bigg(\begin{pmatrix}
    a^{-1}&0\\
    0&1
    \end{pmatrix}m\begin{pmatrix}
    c^{-1}&0\\
    0&1
    \end{pmatrix}\bigg)\\
    \tau\cdot\Psi(m)&=\Psi(m^{T}),
\end{align*}
for $\Psi\in S(M_{2}(F))$ and $\tau=(1,3)\in S_{3}$ being the transposition of the first and third actions.

Let $\sigma\in S_{3}$ be the permutation $\sigma(1)=2,\ \sigma(2)=3,\ \sigma(3)=1$ of order 3. Observe that there is a unique lift for $\sigma$ in $Mp(U\otimes W)$ which respects the relation:
\begin{equation*}
    \tau\sigma\tau^{-1}=\sigma^{2}.
\end{equation*}
Note that such a lift automatically respects all relations of $S_{3}$ since $\tau$ has order 2. And we can write this lift explicitly:
\begin{equation*}
    \sigma\cdot\Psi\bigg(\begin{pmatrix}
    m_{00}&m_{01}\\
    m_{10}&m_{11}
    \end{pmatrix}\bigg)=\int_{F\times F}e(\beta\cdot m_{00}-\alpha\cdot m_{10})\Psi\bigg(\begin{pmatrix}
    \alpha &\beta\\
    m_{01}&m_{11}
    \end{pmatrix}\bigg)\text{d}\alpha\text{d}\beta.
\end{equation*}

We have now chosen lifts for both $S_{2}\ltimes (F^{\times})^{3,\prod=1}$ and $\sigma$. Thus, to show that $S_{3}\ltimes (F^{\times})^{3,\prod=1}$ admits a metaplectic lift and finish the proof, it suffices to check that the action of $S_{3}$ on the metaplectic lift of $(F^{\times})^{3,\prod=1}$ by conjugation is the one we want and it can be verified by the equations above.
\end{proof}


We can start on the construction of Middle action:
Consider $M_{2}(F)=M_{2}(F)\otimes e_{2}$ as a Lagrangian space of $U\otimes W$, which means it's a maximal isotropic subspace, i.e. it is a sub-vector space on which the symplectic form vanishes. Then by the Schr\"{o}dinger model of Weil representation of $Mp(U\otimes W)$ on $S(M_{2}(F))$ corresponding to the character $e: F\rightarrow \mathbb{C}^{\times}$, we get an action of 
\begin{equation*}
    G^{3,\text{det}=1}=(GL_{2}(F)\times GL_{2}(F)\times GL_{2}(F))^{1}=\{(g_{1}, g_{2}, g_{3}): \text{det}(g_{1} g_{2} g_{3})=1\}.
\end{equation*}
on $S(M_{2}(F))$.
Next, we need to use this model to construct the additional middle on $Y=S(M_{2}(F)\times F^{\times})$. By using compact induction to extend the action of $G^{3,\text{det}=1}$ of $S(M_{2}(F)\otimes e_{2})$ to the action of $G^{3}$ of $Y$, we can identify
\begin{equation*}
    Y=S(M_{2}(F)\times F^{\times})=\cInd^{S_{3}\ltimes G^{3}}_{S_{3}\ltimes G^{3,\text{det}=1}}S(M_{2}(F)),
\end{equation*}
via section 
\begin{center}
    % https://tikzcd.yichuanshen.de/#N4Igdg9gJgpgziAXAbVABwnAlgFyxMJZABgBoBGAXVJADcBDAGwFcYkQBxAPWAGZSAOgJwwAHjmCwcAXwC85OQDEeQvAFt40kNNLpMufIRQAmCtTpNW7bny0692PASKnj5hizaJOPfqrESUnIK2rogGI6GRGTE7pZeIACeoQ4GziaksTQeVt4AFOSkAASJxeQAlNrmMFAA5vBEoABmAE4QakhkIDgQSAphre19ND1IxvYggx2IXaOI4wNt0-zdvYgALBNTSCtzxFtLSOsjawqU0kA
\begin{tikzcd}

{G^{3,\text{det}=1}\backslash G^{3}=F^{\times}} \arrow[rr] \arrow[rrd] &  & G^{3} \arrow[d]       \\
                                                       &  & {G^{3,\text{det}=1}\backslash G^{3}} 
\end{tikzcd}
\end{center}
by sending $y\mapsto \bigg(1,\begin{pmatrix}
1 &y\\
0&1
\end{pmatrix}, 1\bigg)$. 
And this is the middle action of $GL_{2}(F)$ on $Y$ that we desire. 

But the first question is what is this representation of $G^{3,\text{det}=1}$ over $S(M_{2}(F))$.


Next we need to show two things: first we prove that as vector spaces, $Y=S(M_{2}(F)\times F^{\times })$ is the space of the induced representation and commutes with the left and right actions on both sides:
\begin{equation*}
    Y\cong \cInd^{S_{3}\ltimes G^{3}}_{S_{3}\ltimes G^{3,\text{det}=1}}S(M_{2}(F)).
\end{equation*}
Second, so far $Y$ is known as a $G\times G$-module. But $\cInd^{S_{3}\ltimes G^{3}}_{S_{3}\ltimes G^{3,\text{det}=1}}S(M_{2}(F))$ is a $G\times G\times G$-module. We explain  this tri-module structure later.   In order to introduce the middle action on $Y$, we use the extra action from Weil representation on $\cInd^{S_{3}\ltimes G^{3}}_{S_{3}\ltimes G^{3,\text{det}=1}}S(M_{2}(F))$.


Taking this representation of $G^{3,\text{det}=1}$ over $S(M_{2}(F))$ as $G\times G$-module, it should have two actions as following: given $g\in G$ and $\Phi\in S(M_{2}(F))$,
\begin{align*}
     \textbf{Left-action on $S(M_{2}(F))$:}\ \ (g_{l}\cdot \Phi)(x)&=\Phi(g_{l}x)\\
     \textbf{Right-action on $S(M_{2}(F))$:}\ \ ( \Phi\cdot g_{r})(x)&=\Phi(xg_{r})
\end{align*}
Let us denote the representation of $G^{3, \text{det}=1}$ as $(\sigma, S(M_{2}(F)))$, in which $\sigma$ is the composition of $p: G^{3,\text{det}=1}\rightarrow MP(U\otimes W)$ and the Weil representation of $Mp(U\otimes W)$. Then the induced representation is 
\begin{align*}
       \cInd^{S_{3}\ltimes G^{3}}_{S_{3}\ltimes G^{3,\text{det}=1}}S(M_{2}(F)):=\big\{f:G^{3}\rightarrow S(M_{2}(F)): f(hg)=\sigma(h)f(g)&\big\}
\end{align*}
And for $f\in G$, we require following properties:    
\begin{enumerate}
    \item There exists a compact open subgroup $K$ of $G$, for every $k\in K$ and $g\in G^{3}$, $f(kg)=f(g)$;
    \item The support of $f$ has compact image in $F^{\times}=G^{3, \text{det}=1}\backslash G^{3}$.
\end{enumerate}
For the left hand side, $S(M_{2}(F)\times F^{\times})= S(M_{2}(F))\otimes S(F^{\times})$. Now we are ready to establish the isomorphism above: Given $\Phi\otimes \Psi\in S(M_{2}(F))\otimes S(F^{\times})$ and $f\in   \cInd^{S_{3}\ltimes G^{3}}_{S_{3}\ltimes G^{3,\text{det}=1}}S(M_{2}(F))$,
\begin{align*}
    \Phi\otimes \Psi \mapsto f(g)(m)=f(g^{1}\cdot t)(m)=(g^{1}\cdot\Phi)(m)\Psi(t),
\end{align*}
in which $g\in G^{3}$, $g^{1}\in G^{3,\text{det}=1}$ and $t\in F^{\times }$. Since $\Psi\in S(F^{\times})$, $\Psi(t)\in \mathbb{C}$ is a scalar.

Explicitly, we can write the formula of this action by Schr\"odinger model: Given $\varrho(m, t)=\Phi(m)\cdot \Psi(t)\in S(M_{2}(F)\times F^{\times})$, then the action of $G^{3}$ on $Y$ is defined as
\begin{flalign*}
    \big((g_{1},g_{2},g_{3})\cdot\varrho\big)(m,t)&=    |\text{det}(g_{1}g_{2}g_{3})|\bigg(\big(g_{1},\begin{pmatrix}
    y & 0\\
    0 & 1
    \end{pmatrix}g_{2}\begin{pmatrix}
    y^{-1}\text{det}(g_{1}g_{2}g_{3})^{-1}&0\\
    0&1
    \end{pmatrix},g_{3}\big)\Phi\bigg)(m)\\
    &\times \Psi(t\cdot\text{det}(g_{1}g_{2}g_{3})),
\end{flalign*}
in which the action of $\bigg(\big(g_{1},\begin{pmatrix}
    y & 0\\
    0 & 1
    \end{pmatrix}g_{2}\begin{pmatrix}
    y^{-1}\text{det}(g_{1}g_{2}g_{3})^{-1}&0\\
    0&1
    \end{pmatrix},g_{3}\big)$ on $\Phi$
is the action obtained from Weil representation. We call the resulting action of the middle copy of $G$ on $Y$ as the middle action on $Y$.
\subsubsection{The Proof of Theorem \ref{thm2.2}}
After finishing the construction, we need to introduce some facts before the proof of theorem \ref{thm2.2}.

By the character $e$ above, the corresponding character $\theta$ of $U_{2}(F)\subset GL_{2}(F)$ of upper triangular
unipotent matrices is defined as follow:
\begin{equation*}
    \theta: U\rightarrow \mathbb{C}^{\times}\ \ \ \ \theta\bigg(\begin{pmatrix}
    1 & u\\
    0 & 1
    \end{pmatrix}\bigg)=e(u).
\end{equation*}
The mirabolic subgroup $P$ of $G=GL_{2}(F)$ is defined as $P=\begin{pmatrix}
a&b\\
0&1
\end{pmatrix}$, and because we are considering the case of $GL_{2}$, it's much easier: $G_{1}=P_{1}=U=\begin{pmatrix}
1 & a\\
0& 1
\end{pmatrix}.$ Denote $\mathfrak{Rep}(G)$ as the category of smooth representation of $G$, $\mathfrak{Rep}(P)$ as the category of representation of $P$, $\mathfrak{Rep}(G_{1})$ as the representation of $G_{1}$ and $\mathfrak{Rep}(P_{1})$ as the representation of $P_{1}$. In order to be more prise with the representation of groups, we will use the notations from  I N Bernshtein and A V Zelevinskii \cite{bernstein1976representations}. Given $(\pi, P_{2}, E)$ as a representation of subgroup $P_{2}$, then there exists a functor $\Phi^{-}$ which sends $(\pi,P_{2},E)$ to $(\Phi^{-}(\pi),P_{1}, E/E(U,\theta))$. and if given a representation $(\tau, P_{1}, V)$, then $\Phi^{+}(\tau)=Ind^{P_{2}}_{P_{1}}\tau$ as induced representation of $P_{2}$, which we denotes as $Ind(P_{2}, P_{1}, \tau')$ and it acts as $\tau'(p\cdot u)\zeta=\theta(u)\tau(p)\zeta$.


So we have a two functors as following:
\begin{enumerate}
    \item $\Phi^{-}:\mathfrak{Rep}(P_{2})\rightarrow \mathfrak{Rep}(P_{1}): (\pi,P_{2},E)\rightarrow (\Phi^{-}(\pi),P_{1}, E/E(U,\theta))$;
    \item $\Phi^{+}:\mathfrak{Rep}(P_{1})\rightarrow \mathfrak{Rep}(P_{2}):(\tau, P_{1}, V)\rightarrow Ind(P_{2},P_{1},\tau')$.
\end{enumerate}
And there are other two functors between categories $\mathfrak{Rep}(P_{2})$ and $\mathfrak{Rep}(G_{1})$. The functor $\Psi^{-1}$ sends $(\pi, P_{2},E)$ to $\Psi^{-1}(\pi)$ which representation space is $E_{U,1}=E/<\pi(u)\zeta-\zeta>$. Given a representation $(\rho,G_{1},V)$, then $(\Psi(\rho),P_{2},V)$ is a representation of $P_{2}$, in which $\Psi(\rho)(gu)=\rho(g)$ for $g\in G,\ u\in U$.
\begin{enumerate}
    \item $\Psi^{-}:\mathfrak{Rep}(P_{2})\rightarrow \mathfrak{Rep}(G_{1}):(\pi, P_{2}, E)\rightarrow (\Psi^{-}(\pi),G_{1},E_{U,1})$;
    \item $\Psi^{+}:\mathfrak{Rep}(G_{1})\rightarrow \mathfrak{Rep}(P):(\rho, G, V)\rightarrow (\Psi^{+}, P_{2}, V)$.
\end{enumerate}
\begin{prop}
For the properties of these four functors $\Phi^{+},\ \Phi^{-},\ \Psi^{+}, \ \Psi^{-}$:
\begin{enumerate}
    \item All these four functors are exact;
    \item $\Phi^{+}$ is the left adjoint of $\Phi^{-}$, i.e. for all any $\pi\in\mathfrak{Rep}(P_{2})$ and $\tau\in \mathfrak{Rep}(P_{1})$ then there exists isomorphism 
    \begin{equation*}
        \text{Hom}_{P}(\Phi^{+}(\tau),\pi)=\text{Hom}_{P_{1}}(\tau,\Phi^{-}(\pi)),
    \end{equation*}
    Similarly, $\Psi^{+}$ is the left adjoint of $\Psi^{-}$, i.e. 
    \begin{equation*}
        \text{Hom}_{P}(\pi,\Psi^{+}(\rho))=\text{Hom}_{G}(\Psi^{-}(\pi),\rho);
    \end{equation*}
    \item Based on the isomorphisms, we can have following morphisms: 
\begin{align*}
    i: \Phi^{+}\Phi^{-}(\pi)\rightarrow  \pi & i':\tau\rightarrow \Phi^{-}\Phi^{+}(\tau)\\
    j: \pi\rightarrow \Psi^{+}\Psi^{-}(\pi)& j':\Psi^{-}\Psi^{+}(\rho)\rightarrow \rho,
\end{align*}
in which 
\begin{align*}
    \Phi^{+}\Phi^{-}:\mathfrak{Rep}(P_{2})\rightarrow \mathfrak{Rep}(P_{2})\ \  & \Phi^{-}\Phi^{+}:\mathfrak{Rep}(P_{1})\rightarrow \mathfrak{Rep}(P_{1})\\
    \Psi^{+}\Psi^{-}: \mathfrak{Rep}(P_{2})\rightarrow \mathfrak{Rep}(P_{2})\ \ & \Psi^{-}\Psi^{+}: \mathfrak{Rep}(G_{1})\rightarrow \mathfrak{Rep}(G_{1})
\end{align*}
then there exists a exact sequence:
\begin{equation*}
    0\rightarrow \Phi^{+}\Phi^{-}(\pi)\xrightarrow{i}\pi \xrightarrow{j} \Psi^{+}\Psi^{-}(\pi)\rightarrow 0
\end{equation*}
\end{enumerate}

\end{prop}
\begin{rem}\label{BZ}
In the proof of this theorem, it follows that the representation $\pi^{0}=\mathcal{E}_{c}(Y)$ is isomorphic to the restriction of $\pi$ to $E(M,1)$. And we know that 
\begin{equation*}
    \phi^{+}\phi^{-}(\pi)\cong Ind(P_{2},P_{1},\phi^{-}(\pi)')\cong\pi^{0}
\end{equation*}
For the rest of the proof, it's in \cite{bernstein1976representations}.

\end{rem}

\begin{thm}\label{1dim}
Given a generic, irreducible, admissible representation $(\pi, V)$ of $G=GL_{2}(F)$, then $\text{dim} V_{U,\theta}=1$ for any  character $\theta$, in which $V_{U, \theta}$ is defined as 
\begin{equation*}
    V_{U,\theta}=V/V(U,\theta)=V/<\pi(u)\zeta-\theta(u)\zeta)>,\ \ (u,\zeta)\in U\times V.
\end{equation*}
\end{thm}
The proof of the this theorem is from \cite{bernstein1976representations}.



\begin{lem}
Let $Y$ be a $G^{3}$-module via left, right and middle actions respectively. Then the resulting three actions of Bernstein centers of each copy of $G$ on Y identify.
\end{lem}
\begin{rem}
For the definition and basic information about Bernstein center, check the section \ref{Bernstein}.
\end{rem}
\begin{proof}
For the left and right translation actions of $G$ on $S(M_{2}(F))$ because the $G\times G$-equivariant pairing:
\begin{align*}
    S(M_{2}(F))\otimes S(G)&\rightarrow  \mathbb{C}\\
    \Psi \otimes f &\mapsto \int_{G} \Psi(g)f(g)\text{d}^{\times}g
\end{align*}
is non-degenerate and because the Bernstein center of $G$ acts on $S(G)$ the same way from both sides. As the result, the left and right action of the center of $G$ on $Y$ coincide. By symmetry (i.e. by conjugation by a permutation from $S_{3}$), this also applies to the middle action.
\end{proof}
\begin{lem}
The map $\Phi^{+}\Phi^{-}Y\rightarrow Y$ is an embedding with the image $Y^{0}=S(GL_{2}(F)\times F^{\times})\subset Y$, where the functor $\Phi^{+}\Phi^{-}$ is taken with the respect to the middle action on $Y$.
\end{lem}
\begin{proof}
The middle action of the matrix $\begin{pmatrix}
a &b\\
0&1
\end{pmatrix}$ on the element $\Phi(g, y)\in Y$ is:
\begin{equation*}
\begin{pmatrix}
a &b\\
0&1
\end{pmatrix}\cdot \Phi(g, y)=|a|\cdot e(b\text{det}(g)y)\cdot \Phi(g, ay).
\end{equation*}
By \ref{BZ}, it follows that the image in lemma consists of the functions supported away from the set $\{\text{det}(g)y=0\}$.
\end{proof} 

Now we are ready to prove the theorem \ref{thm2.2}:
\begin{proof} 
We have finished the action of middle action of $G$ on $Y$. And we know that it's commutative with the left and right actions of $G $ on $Y$.

The first statement we are proving is the existence of the isomorphism $\nu$ of theorem \ref{thm2.2}.

The space $\Phi^{-}\widetilde{V}$ is one-dimensional by \ref{1dim}. A choice of vector $\mathbb{C}\rightarrow \Phi^{-}\widetilde{V}$ gives a map of $P-$modules by adjunction:
\begin{equation*}
    S(F^{\times})\cong \Phi^{+}\mathbb{C}\rightarrow \widetilde{V}.
\end{equation*}
Taking  the dual map, we obtain a morphism of $P-$modules: $V\rightarrow\widetilde{S(F^{\times})}$, where $\widetilde{S(F^{\times})}$ is identified with the space of smooth functions on $F^{\times}$, and $P$ acts on $\widetilde{S(F^{\times})}$ by:
\begin{equation*}
    \begin{pmatrix}
    a&b\\
    0&1
    \end{pmatrix}\cdot f(y)=e(by)f(ay).
\end{equation*}
The map $V\rightarrow \widetilde{S(F^{\times})}$ is the non-zero map of $P-$modules from $V\rightarrow $ to $\widetilde{S(F^{\times})}$, which is unique up to scalar. These maps are injective and have the same image. This image is called the Kirillov model $\mathcal{K}(V)$ of $V$. The related notation Whittaker model of $V$ is obtained by taking the map $S(F^{\times})\rightarrow \widetilde{V}$ of $P-$modules and extending it to a map of $G-$modules: $\mathbb{1}_{Y}\rightarrow\widetilde{V}$ by making $\mathbb{1}_{Y}$ the induction with compact support of $S(F^{\times})$ from $P$ to $G$. The space $\mathbb{1}_{Y}$ is called the Whittaker space, and the image of the resulting dual map $V\rightarrow\widetilde{\mathbb{1}_{Y}}$ is the Whittaker model of $V$.




First, we consider $(\pi, V)$ as irreducible principal series representation and supercuspidal representation. 


\end{proof}

\begin{lem}
Let $(\pi, V)$ be a representation of $G$, such that $V$ and $\widetilde{V}$ admits no $SL_{2}(F)$-invariant linear functionals. Then 
\begin{equation*}
    \widetilde{V}\otimes_{G}S(M^{\text{det}=0}_{2}(F)\times F^{\times})\otimes_{G} V =\text{Jac}(\widetilde{V})\otimes_{F^{\times}\times F^{\times}} \text{Jac}(V).
\end{equation*}
\end{lem}


 





\newpage
\bibliographystyle{plain}
\bibliography{bib.bib}


\end{document}
