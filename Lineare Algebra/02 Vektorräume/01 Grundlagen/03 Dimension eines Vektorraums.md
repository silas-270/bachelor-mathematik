## 1. Der Austauschsatz und Dimension

### Der Steinitzsche Austauschsatz

> [!abstract] Steinitzsches Austauschlemma (1 Vektor)
> Sei $(v_1, \dots, v_n)$ eine Basis von $V$ und $w \in V$ mit $w \neq \vec{0}$.
> Dann existiert ein Index $i \in \{1, \dots, n\}$, sodass $(v_1, \dots, v_{i-1}, w, v_{i+1}, \dots, v_n)$ wieder eine Basis von $V$ ist.

> [!abstract] Steinitzscher Basisaustauschsatz (Allgemein)
> Sei $(v_1, \dots, v_n)$ eine Basis von $V$ und $\{w_1, \dots, w_r\}$ eine linear unabhängige Teilmenge von $V$. Dann gilt:
> 1.  **Längenvergleich:** $r \leq n$ (Die linear unabhängige Liste ist höchstens so lang wie die Basis).
> 2.  **Austausch:** Es gibt Indizes $i_1, \dots, i_r$, sodass man die Vektoren $v_{i_1}, \dots, v_{i_r}$ durch $w_1, \dots, w_r$ ersetzen kann und wieder eine Basis erhält.

> [!tip] Intuition
> Man kann Teile einer Basis durch andere linear unabhängige Vektoren ersetzen ("austauschen"), ohne die Eigenschaft, eine Basis zu sein, zu verlieren. Zudem kann eine linear unabhängige Menge nie mehr Elemente enthalten als eine Basis.

### Dimension eines Vektorraums

Aus dem Austauschsatz folgen zentrale Eigenschaften für endlich erzeugte Vektorräume.

> [!abstract] Dimensionssatz
> Alle Basen eines endlich erzeugten Vektorraums haben die gleiche Anzahl von Vektoren.

> [!important] Definition: Dimension
> Die Dimension eines endlich erzeugten Vektorraums $V$, notiert als $\dim(V)$, ist die Anzahl der Vektoren in einer (und damit jeder) Basis von $V$.

### Charakterisierung von Basen

In einem Vektorraum, dessen Dimension bereits bekannt ist, vereinfacht sich die Überprüfung der Basis-Eigenschaft.

> [!abstract] Satz: Basisprüfung bei bekannter Dimension
> Sei $V$ ein Vektorraum mit $\dim(V) = n$. Für eine Familie von $n$ Vektoren $\mathcal{B} = (v_1, \dots, v_n)$ sind folgende Aussagen äquivalent:
> 1.  $\mathcal{B}$ ist eine Basis.
> 2.  $\mathcal{B}$ ist linear unabhängig.
> 3.  $\mathcal{B}$ ist ein Erzeugendensystem ($\text{span}(\mathcal{B}) = V$).

> [!tip] Intuition
> Wenn die Anzahl der Vektoren genau der Dimension entspricht, muss man nicht mehr beides prüfen (linear unabhängig UND erzeugend). Es reicht, eine der beiden Eigenschaften zu zeigen, die andere folgt automatisch.

---

## 2. Unendlich-dimensionale Vektorräume & das Lemma von Zorn

### Erweiterte Definitionen

Für eine Indexmenge $I$ (potenziell unendlich) und eine Familie von Vektoren $M := (\vec{v}_i)_{i \in I}$:

> [!important] Definition: Lineare Hülle & Unabhängigkeit (Unendlich)
> * **Span:** $\text{span}(M)$ ist die Menge aller **endlichen** Linearkombinationen von Vektoren aus $M$.
> * **Lineare Unabhängigkeit:** $M$ heißt linear unabhängig, wenn jede **endliche** Teilmenge von Vektoren aus $M$ linear unabhängig ist.
> * **Basis:** $M$ ist eine Basis von $V$, wenn $M$ linear unabhängig ist und $\text{span}(M) = V$ gilt.

### Ordnungstheorie

Um das Lemma von Zorn zu formulieren, werden ordnungstheoretische Begriffe benötigt. Sei $M$ eine Menge mit einer Relation $\preceq$.

> [!important] Definition: Ordnungsrelationen
> * **Halbordnung:** Eine Relation ist eine Halbordnung, wenn sie reflexiv, antisymmetrisch und transitiv ist.
> * **Totalordnung:** Eine Halbordnung, bei der für alle $x, y$ gilt: $x \preceq y$ oder $y \preceq x$ (Totalität).
> * **Kette:** Eine total geordnete Teilmenge einer halbgeordneten Menge.

> [!important] Definition: Schranken und Elemente
> Sei $T \subseteq M$ eine Teilmenge einer halbgeordneten Menge.
> * **Obere Schranke:** Ein Element $s \in M$ heißt obere Schranke von $T$, wenn $\forall t \in T: t \preceq s$ gilt.
> * **Maximales Element:** Ein Element $m_{max} \in M$ heißt maximal, wenn es kein Element gibt, das "echt größer" ist (d.h. aus $m_{max} \preceq m$ folgt $m = m_{max}$).

### Das Lemma von Zorn und Basisexistenz

> [!abstract] Lemma von Zorn
> Jede halbgeordnete Menge, in der jede Kette eine obere Schranke besitzt, enthält mindestens ein maximales Element.

> [!tip] Intuition
> Das Lemma von Zorn erlaubt es, von verhältnismäßig schwachen Aussagen über spezielle Teilmengen (Ketten) auf eine starke Aussage über die Existenz eines maximalen Elements in der gesamten Menge zu schließen.

> [!abstract] Satz: Existenz einer Basis
> Jeder $\mathbb{K}$-Vektorraum $V$ hat eine Basis.
> *Hinweis: Der Beweis erfolgt über das Lemma von Zorn, angewendet auf die Menge aller linear unabhängigen Teilmengen von $V$.*