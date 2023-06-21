## Tags:

#dynamical-system #notes 

---
## Def :: Thue-Morse sequence
- Construction:
	$$\begin{align}
	w_{0}&=0\\
	w_{1}&=0\bar{0}=01\\
	w_{2}&=w_{1}\overline{w_{1}}=0110\\
	w_{3}&=w_{2}\overline{w_{2}}=01101001\\
	w_{4}&=\ldots\\
	\vdots\\
	w_{n+1}&=w_{n}\overline{w_{n}}
	\end{align}$$
	In this limit, we get an infinite sequence called the Thue-Morse sequence.

- Another construction:
	$$W=\text{"All words in 0 and 1"}$$
	Define a substitution rule $s:W\rightarrow W$ by $s(0)=01, s(1)=10$,
	$$ s(w_{1},...,w_{l})=s(w_{1})...s(w_{l})$$
	$$\begin{align}
	s(0)&=01\\
	s^{2}(0)&=s(0)s(1)=0110\\
	s^{3}(0)&=s(0)s(1)s(1)s(0)=01101001\\
	\vdots
	\end{align}$$
	Claim: $w_{n}=s^{n}(0)$



## Thm :: The Thue-Morse word $w$ is uniformly recurrent but nor periodic.




