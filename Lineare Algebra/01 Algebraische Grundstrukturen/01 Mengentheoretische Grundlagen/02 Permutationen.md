## Grundlagen der Permutationen

> [!important] Definition: Permutation
> Sei $E_n = \{1, \dots, n\}$ eine endliche Menge mit $n$ Elementen. Eine **Permutation** $\pi$ ist eine bijektive Abbildung von $E_n$ in sich selbst:
> $$\pi: E_n \to E_n$$

> [!tip] Intuition
> Eine Permutation ist ein Synonym für **Vertauschung**. Man bringt Objekte in eine neue Reihenfolge.

### Die Symmetrische Gruppe $S_n$

> [!important] Definition: Symmetrische Gruppe $S_n$
> Die Menge aller Permutationen auf $n$ Elementen wird als $S_n$ bezeichnet. Das $S$ steht für "Symmetrisch".

> [!abstract] Satz P1: Mächtigkeit der $S_n$
> Die symmetrische Gruppe $S_n$ besitzt genau $n!$ (n-Fakultät) Elemente.
> $$|S_n| = n! = 1 \cdot 2 \cdot \dots \cdot n$$

## Die Gruppenstruktur der $S_n$

> [!abstract] Satz: $S_n$ als Gruppe
> Die Menge $S_n$ bildet bezüglich der **Hintereinanderausführung** (Komposition) von Abbildungen eine Gruppe.
> * **Verknüpfung:** $\pi_2 \circ \pi_1$ (erst $\pi_1$, dann $\pi_2$).
> * **Neutrales Element:** Die Identität ($id$), die alle Elemente fix lässt.
> * **Inverses Element:** Die Umkehrabbildung $\pi^{-1}$.
> * **Assoziativität:** Gilt allgemein für die Verkettung von Funktionen.

> [!abstract] Satz: Nicht-Kommutativität
> Für $n \geq 3$ ist die Gruppe $S_n$ **nicht abelsch** (nicht kommutativ). Das bedeutet im Allgemeinen: $\pi_1 \circ \pi_2 \neq \pi_2 \circ \pi_1$.

> [!abstract] Satz: Satz von Cayley (für endliche Gruppen)
> Jede endliche Gruppe mit $n$ Elementen ist isomorph zu einer Untergruppe der $S_n$.
> * **Konstruktion:** Man ordnet jedem Gruppenelement $g \in G$ eine Permutation $\pi_g$ zu, definiert durch $\pi_g(i) = g \circ i$.

## Zykel und Transpositionen

> [!important] Definition: Zykel
> Eine Permutation, die eine Teilmenge von Elementen zyklisch vertauscht ($i \to \pi(i) \to \pi(\pi(i)) \dots$) und alle anderen fix lässt.
> **Schreibweise:** $(a_1, a_2, \dots, a_k)$ bedeutet $a_1 \mapsto a_2$, $a_2 \mapsto a_3$, ..., $a_k \mapsto a_1$.
> * **Ordnung:** Die Ordnung eines Zykels entspricht seiner Länge $k$.

> [!abstract] Satz: Disjunkte Zykel
> Elementfremde (disjunkte) Zykel kommutieren miteinander.

> [!important] Definition: Transposition
> Eine Transposition ist ein Zykel der Länge 2, also eine Vertauschung von genau zwei Elementen $i$ und $j$.

> [!abstract] Satz: Zerlegung in Transpositionen
> Jede Permutation lässt sich als Produkt von Transpositionen darstellen.
> * **Zusatz:** Jede Permutation lässt sich sogar als Produkt von **benachbarten** Transpositionen darstellen.

## Das Vorzeichen (Signum) einer Permutation

> [!important] Definition: Fehlstand (Inversion)
> Ein Paar $(i, j)$ heißt Fehlstand einer Permutation $\pi$, wenn gilt:
> $$i < j \quad \text{aber} \quad \pi(i) > \pi(j).$$

> [!important] Definition: Signum (Vorzeichen)
> Das Vorzeichen einer Permutation ist definiert als:
> $$\operatorname{sgn}(\pi) = (-1)^{\text{Anzahl der Fehlstände}}.$$

> [!abstract] Satz: Geschlossene Formel für das Signum
> $$\operatorname{sgn}(\pi) = \prod_{i<j} \frac{\pi(j) - \pi(i)}{j - i}.$$

> [!abstract] Satz: Signum als Gruppenhomomorphismus
> Die Abbildung $\operatorname{sgn}: S_n \to \{+1, -1\}$ ist ein Gruppenhomomorphismus bezüglich der Multiplikation. Es gilt:
> $$\operatorname{sgn}(\pi \circ \sigma) = \operatorname{sgn}(\pi) \cdot \operatorname{sgn}(\sigma)$$

> [!abstract] Satz: Parität der Transpositionszerlegung
> Sei $\pi$ als Produkt von $k$ Transpositionen dargestellt. Dann ist die Parität von $k$ (ob $k$ gerade oder ungerade ist) eindeutig bestimmt und entspricht dem Vorzeichen von $\pi$:
> $$\operatorname{sgn}(\pi) = (-1)^k$$
> Das Vorzeichen einer einzelnen Transposition ist immer $-1$.

### Rechenverfahren

**Invertieren einer Permutation (Wertetabelle):**
1. Vertausche die Zeilen der Wertetabelle (Urbilder und Bilder).
2. Sortiere die Spalten wieder aufsteigend nach der oberen Zeile.

**Zykel-Zerlegung:**
1. Wähle ein Element $i$.
2. Verfolge den Pfad $i \to \pi(i) \to \pi(\pi(i))$ solange, bis man wieder bei $i$ ankommt.
3. Schreibe diese Elemente als Klammerausdruck (Zykel).
4. Wiederhole dies für alle noch nicht erfassten Elemente, bis $E_n$ ausgeschöpft ist.