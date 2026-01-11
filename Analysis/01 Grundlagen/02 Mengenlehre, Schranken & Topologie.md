## 1. Mengenlehre

> [!abstract] Definition: Mengen und Elemente
> Eine **Menge** ist eine Zusammenfassung von Objekten. Jedes Objekt $x$, das zur Menge $M$ gehört, heißt **Element** der Menge ($x \in M$).

### Mengenoperationen

> [!important] Grundlegende Operationen
> Für zwei Mengen $M$ und $N$ definieren wir:
> 
> * **Schnittmenge:** $M \cap N = \{ x \mid x \in M \land x \in N \}$
> * **Vereinigungsmenge:** $M \cup N = \{ x \mid x \in M \lor x \in N \}$
> * **Relatives Komplement:** $M \setminus N = \{ x \mid x \in M \land x \notin N \}$

---

### Spezielle Mengenrelationen

> [!info] Begriffe
> * **Disjunkt:** $M$ und $N$ heißen disjunkt, falls $M \cap N = \varnothing$.
> * **Disjunkte Zerlegung:** $P = M \cup N$ mit $M \cap N = \varnothing$.
> * **Potenzmenge $\mathcal{P}(M)$:** Menge aller Teilmengen von $M$. Mächtigkeit: $|\mathcal{P}(M)| = 2^n$ (für $|M|=n$).
> * **Produktmenge $M \times N$:** Menge der geordneten Paare $(x, y)$ mit $x \in M, y \in N$.

---

## 2. Schranken und Extremwerte

### Maximum und Minimum
Sei $M \subset \mathbb{R}$ eine nichtleere Teilmenge.

> [!abstract] Definition: Extremwerte
> * **Minimum:** Ein Element $a \in M$ heißt Minimum, falls $a$ eine untere Schranke von $M$ ist.
> * **Maximum:** Ein Element $b \in M$ heißt Maximum, falls $b$ eine obere Schranke von $M$ ist.

### Supremum und Infimum

> [!important] Supremumsaxiom
> Jede nach oben beschränkte, nichtleere Teilmenge von $\mathbb{R}$ besitzt ein **Supremum** in $\mathbb{R}$.

> [!tip] Definition: Schranken
> Sei $M \subset \mathbb{R}$ eine nichtleere Teilmenge:
> * **Supremum ($\sup M$):** Die kleinste obere Schranke. Es gilt: $\forall x \in M : x \leq \sup M$ und für jede obere Schranke $b$ gilt $\sup M \leq b$.
> * **Infimum ($\inf M$):** Die größte untere Schranke. Es gilt: $\forall x \in M : x \geq \inf M$ und für jede untere Schranke $a$ gilt $\inf M \geq a$.

---

## 3. Topologie von Teilmengen in $\mathbb{R}$ und $\mathbb{C}$

In diesem Kapitel bezeichnet $\mathbb{K}$ den Körper $\mathbb{R}$ oder $\mathbb{C}$.

### 3.1 Beschränktheit

> [!abstract] Definition: Beschränktheit
> Eine Teilmenge $X \subset \mathbb{K}$ heißt **beschränkt**, falls sie in einer Kugel um den Ursprung liegt:
> $$\exists R \in \mathbb{R}_{>0} : \forall x \in X \implies |x| \leq R$$
> 
> > [!info] Besonderheit in $\mathbb{R}$
> > Da $\mathbb{R}$ geordnet ist, existieren hier zusätzlich:
> > * **nach unten beschränkt:** $\exists a \in \mathbb{R} : X \subset [a, \infty)$
> > * **nach oben beschränkt:** $\exists b \in \mathbb{R} : X \subset (-\infty, b]$
> > 
> > *In $\mathbb{C}$ sind diese Begriffe aufgrund der fehlenden Ordnung nicht definiert.*

### 3.2 Die $\varepsilon$-Umgebung

> [!tip] Definition: $U_\varepsilon(x)$
> Für einen Punkt $x \in \mathbb{K}$ und einen Radius $\varepsilon > 0$ gilt:
> $$U_\varepsilon(x) := \{ y \in \mathbb{K} \mid |x - y| < \varepsilon \}$$
> 
> | Raum | Geometrische Form | Notation |
> | :--- | :--- | :--- |
> | $\mathbb{R}$ | Offenes Intervall | $(x - \varepsilon, x + \varepsilon)$ |
> | $\mathbb{C}$ | Offene Kreisscheibe | $\mathbb{B}_\varepsilon(x)$ |



### 3.3 Topologische Grundbegriffe

> [!important] Definitionen
> Eine Teilmenge $X \subset \mathbb{K}$ heißt:
> 1. **offen**, falls gilt: $\forall x \in X \exists \varepsilon > 0 : U_\varepsilon(x) \subset X$.
> 2. **abgeschlossen**, falls das Komplement $\mathbb{K} \setminus X$ offen ist.
> 3. **kompakt**, falls $X$ sowohl **abgeschlossen** als auch **beschränkt** ist.

### 3.4 Punktmengen: Inneres, Abschluss und Rand

Mithilfe der Umgebungen klassifizieren wir die Struktur einer Menge $X \subset \mathbb{K}$:

> [!important] Das Innere ($\mathring{X}$ oder $\operatorname{int}X$)
> $$\mathring{X} := \{ x \in \mathbb{K} \mid \exists \varepsilon > 0 : U_\varepsilon(x) \subset X \}$$

> [!important] Der Abschluss ($\bar{X}$ oder $\operatorname{cl}X$)
> $$\bar{X} := \mathbb{K} \setminus \operatorname{int}(\mathbb{K} \setminus X)$$

> [!important] Der Rand ($\partial X$)
> $$\partial X := \bar{X} \setminus \mathring{X}$$