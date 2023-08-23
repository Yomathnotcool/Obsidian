## Tags:

#dynamical-system #notes 

---
# Doubling map
## Def :: Doubling map:

Given the space $X = \mathbb{R}/\mathbb{Z}$ with metric $d(x,y)=\text{min}_{n\in\mathbb{Z}}|x-y+n|$ ,
$T:x\mapsto 2x (\text{mod} 1)$ 

## Thm :: Doubling map $T$ has $2^{n}-1$ periodic points. And the set of periodic points are dense.



## Thm :: There exists dense orbits of $T$. Doubling map is topological transitive.



## Thm :: For the doubling map $T:\mathbb{R}/\mathbb{Z}\rightarrow\mathbb{R}/\mathbb{Z}$, if $x$ has dense orbit, it's not uniformly recurrent; if $x$ is periodic, it is uniformly recurrent.

^203fe9


## Thm :: Doubling map is [[Lectures note about Dynamical System#^3ec847|measure preserving]].

^e53326


## Thm :: Doubling map is [[Lectures note about ergodic theory#^3b262f|mixing]].

^0b208e
### Thm :: Doubling map is [[Lectures note about ergodic theory#^d8b2bc|ergodic]].

# other expansion maps
Consider $T:[0,1)\rightarrow [0,1): x\mapsto 10x (\mod1)$, which is [[Lectures note about ergodic theory#^d8b2bc|ergodic]], then by using [[Lectures note about ergodic theory#^7f42be|Birkhoff ergodic theorem]], we can prove the following theorem:
### Thm :: What are frequencies of digits?
$x\in [0,1)$ then $x$ can be written as decimal expansion, then the question is *what are frequencies of digits?*

For $k=0,...,9$, $D_{N}(x,k)=\#\{i=1,...,N:x_{i}=k\}$. For almost every $x\in[0,1)$ with Lebesgue measure,
$$\frac{D_{N}(x,k)}{N}\longrightarrow\frac{1}{10}.$$ ^999c28