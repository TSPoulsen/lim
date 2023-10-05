# LIM - Aflevering 1
## Tim Sehested Poulsen

### Opgave 2.2 (Schilling)
Kommer ikke til at ske


### Opgave S1.3
#### (i) Vis at A er tællelig
Jeg vil først vise at ehvert element $x \in A$ er givet unikt ved et sæt $n,m \in \mathbb{Z}$.
Jeg vil gøre det ved en modstrids argument.
Antag for modstrid at for et $x \in A$ der findes $n_1,m_1,n_2,m_2 \in \mathbb{Z}$ så at 
$n_1 + m_1\sqrt{2} = x = n_2 + m_2\sqrt{2}$.
Da vil vi have at $n_1 - n_2 = \sqrt{2}(m_2 - m_1)$, men da $n_1 - n_2 \in \mathbb{Z}$ og $\sqrt{2}(m_2-m_1) \notin \mathbb{Z} $ eftersom $m_2 \neq m_2$.
Det giver altså en modstrid og derfor kan der ikke findes to forskellige sæt $n,m \in \mathbb{Z}$ så at $n + m\sqrt{2} = x$.
Vi kan derfor lave bijektionen $f: \mathbb{Z} \times \mathbb{Z} \rightarrow A$ givet ved $f(n,m) = n + m\sqrt{2}$.
Det vil per definition ramme alle elementerne i $A$ og $f$ er også injektiv da vi lige har vist at ehvert element i $A$ er givet unikt ved et sæt $n,m \in \mathbb{Z}$.

Altså er $ \# A = \# \mathbb{Z} \times \mathbb{Z}$.
Da vi har fra Schilling s. 9 at $\# \mathbb{Z} \le \# \mathbb{N}$ (lad os sige med injektiv funktion $j: \mathbb{Z} \rightarrow \mathbb{N}$) og $\# \mathbb{N} \times \mathbb{N} \le \# \mathbb{N}$ (med injektiv funktion $g: \mathbb{N} \times \mathbb{N} \rightarrow \mathbb{N}$) kan vi konstruere en injektiv funktion $h: \mathbb{Z} \times \mathbb{Z} \rightarrow \mathbb{N}$ givet ved $h(n,m) = g(j(n),j(m))$ som derfor også må være injektiv.
Altså har vi en injektiv funktion $g: \mathbb{Z} \times \mathbb{Z} \rightarrow \mathbb{N}$ og kan så konkludere at
$\# A = \# \mathbb{Z} \times \mathbb{Z} \le \# \mathbb{N}$, altså er $A$ tællelig.

#### (ii) Vis at B er overtællelig

Jeg finder først løsningerne til $x^2 -3x +2 = 0$. De er følgende:
$$
x = \frac{-(-3) \pm \sqrt{(-3)^2 - 4 \cdot 2}}{2} \implies x = 1 \lor x = 2
$$
Da kan man så hurtigt se at $B$ er et interval, præcist $B = (1,2)$.
Det kan hurtigt ses at funktionen $f: B \rightarrow (0,1)$ givet ved $f(x) = x - 1$ er en bijektion. Altså kan vi konkludere at $\# B = \# (0,1)$ og da vi har fra Schilling s. 12 at $\# (0,1) = c > \aleph_0$. Altså er $ \# B > \# \mathbb{N}$ så derfor er $B$ overtællelig.


