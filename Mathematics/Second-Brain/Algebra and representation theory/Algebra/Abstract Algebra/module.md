
## Tags
#algebra #notes #representation 

---

## References:
[Module (mathematics) - Wikipedia](https://en.wikipedia.org/wiki/Module_(mathematics))

---
## Other related notes:
[[vector space]]

---
Module is the abstract generalisation for [[vector space]], 

## Def :: Left module
Given a ring $R$, and a left module consists of  abelian group $(M,+)$ and an additional operation: $\cdot: R\times M\rightarrow M$, which satisfies the following conditions:
1. 1$\cdot x$ = $x$, for $\forall x\in M, 1\in R$;
2. $r\cdot(x+y)=r\cdot x+r\cdot y, \forall r\in R, x,y\in M$;
3. $(r+s)\cdot x=r\cdot x+s\cdot y, \forall r,s\in R,x\in M$;
4. $r(s\cdot y)=(rs)\cdot y$.

Right module defines in the same manner. If the left action and right action commutes, then there is no need to distinguish left or right module.


### Def :: Annihilator of module $M$

^f586ef

The annihilator of $R$-module $M$ is defined as 
$$
\text{Ann}(M)=\{r\in R| r\cdot x=0, \forall x\in M\}.
$$
### Def :: faithful module

^a1e137

A $R-$module $M$ is called faithful if the [[module#^f586ef|annihilator]] of $M$ is zero.
