# LIM - Assignment 2
##### Tim Sehested Poulsen - tpw705@alumni.ku.dk

### Exercise 3.1 (Schilling)
#### (i) $A_1, A_2, \dots , A_N \in \mathcal{A} \implies \bigcap_{i=1}^N A_i \in \mathcal{A}$
Assuming that 
$A_1, A_2, \dots , A_N \in \mathcal{A}$, then also have that $A_1^c, A_2^c, \dots , A_N^c \in \mathcal{A}$ by definition 3.1 in [1].
Using the same definition we can also conclude that $\bigcup_{i=1}^N A_i^c \in \mathcal{A}$. Using De Morgans laws we have that $\bigcup_{i=1}^N A_i^c = \left( \bigcap_{i=1}^N A_i \right)^c$.
Again by using the definition of a $\sigma$-algebra we have that $\left( \bigcap_{i=1}^N A_i \right)^c \in \mathcal{A} \implies \left( \left( \bigcap_{i=1}^N A_i \right)^c \right)^c = \bigcap_{i=1}^N A_i \in \mathcal{A}$ which is exactly what we wanted.
$\blacksquare$

#### (ii) $A \in \mathcal{A}  \iff A^c \in \mathcal{A}$
The fact that $A \in \mathcal{A}  \implies A^c \in \mathcal{A}$ is given by definition 3.1 in [1]. The other direction is given by the fact that $A^c \in \mathcal{A}  \implies A^{cc} \in \mathcal{A}$. But $A^{cc} = A$ so we have that $A \in \mathcal{A}$.
$\blacksquare$

#### (iii) $A,B \in \mathcal{A}  \implies A \setminus B, A \bigtriangleup B \in \mathcal{A}$
If $A,B \in \mathcal{A}$ then $B^c \in \mathcal{A}$ by definition and combining that with **(i)** we have that $A \cap B^c \in \mathcal{A}$.
Which is what we wanted since $A \cap B^c = A \setminus B$.
$\blacksquare$

Using this we can then also conclude that $B \setminus A \in \mathcal{A}$ by the same argument.
As a $\sigma$-algebra is closed under countable unions by definition, we can then say that since $(A \setminus B), (B \setminus A) \in \mathcal{A}$ we must also have that $(A \setminus B) \cup (B \setminus A) = A \bigtriangleup B \in \mathcal{A}$.
$\blacksquare$


### Exercise S2.3.
#### (i) $\sigma(G_1) = \mathcal{P}(X)$
We have that $\sigma(G_1) \subseteq \mathcal{P}(X)$ by the definition of a $\sigma$-algebra, so we need only to show that $\mathcal{P}(X) \subseteq \sigma(G_1)$.
Let $S \in \mathcal{P}(X)$ and $S \ne \emptyset$, then we have that $S = \bigcup_{x \in S} \{x\}$ and since $\{x\} \in G_1$ for all $x \in X$ we also have that $\{x \} \in \sigma(G_1)$ and so is their union as $\sigma(G_1)$ is a $\sigma$-algebra. Thus $S \in \sigma(G_1)$, and we have now shown that $\mathcal{P}(X) = \sigma(G_1)$.
$\blacksquare$

#### (ii) $\sigma(G_2) = \mathcal{P}(X)$
Yet again we can argue that $\sigma(G_2) \subseteq \mathcal{P}(X)$ by the definition of a $\sigma$-algebra. So to show that $\mathcal{P}(X) \subseteq \sigma(G_2)$, we show it by showing that $G_1 \subseteq \sigma(G_2)$ which would imply that 
$$\mathcal{P}(X) = \sigma(G_1)\subseteq \sigma(\sigma(G_2)) = \sigma(G_2)$$
which we have from Remark 3.5 in [1], and by definition of $\sigma(G_2)$ being the smallest $\sigma$-algebra containing $G_2$.

So to show $G_1 \subseteq \sigma(G_2)$, we simply observe that $G_2 \subseteq \sigma(G_2)$ and $X \in \sigma(G_2)$ and so is the union/intersection/difference of any of the sets in $G_2$ and $X$. 
We have the following
$$\{ 1\}  =  \{1,2\} \setminus \{2,3\}$$
$$\{ 2\}  =  \{1,2\} \cap \{2,3\}$$
$$\{ 3\}  =  \{2,3\} \setminus \{1,2\}$$
$$\{ 4\}  =  X \setminus \left(\{1,2\} \cup \{2,3\}\right)$$
As each set on the right hand side is in $\sigma(G_2)$, we must then have that each set on the left hand side is also in $\sigma(G_2)$. This concludes that $G_1 \subseteq \sigma(G_2)$ and we have shown that $\mathcal{P}(X) = \sigma(G_2)$.

$\blacksquare$



[1] Rene Schilling "Measures, Integrals and Martingales", second edition, Cambridge University Press, ISBN: 978-1-316-62024-3 (paperback)
