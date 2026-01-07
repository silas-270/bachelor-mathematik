## 1. Definition: Ringe

Der Übergang von der Gruppentheorie zu Ringen führt eine zweite Verknüpfung ein, sodass nun Addition und Multiplikation gleichzeitig betrachtet werden

> [!important] Definition: Ring
> Ein **Ring** ist ein Tripel $(R, +, \cdot)$, bestehend aus einer Menge $R$ und zwei binären Verknüpfungen $+$ (Addition) und $\cdot$ (Multiplikation), für die gilt:
> 1. $(R, +)$ ist eine **abelsche (kommutative) Gruppe**.
> 2. Die Multiplikation ist **assoziativ**: $\forall a,b,c \in R: (a \cdot b) \cdot c = a \cdot (b \cdot c)$.
> 3. Es gelten die **Distributivgesetze** (Links- und Rechtsdistributivität):
>    $$a \cdot (b + c) = a \cdot b + a \cdot c$$
>    $$(a + b) \cdot c = a \cdot c + b \cdot c$$

> [!tip] Intuition
> Ringe sind eine "Zwischenstufe": Man hat bereits eine Multiplikation und darf ausklammern, aber man kann notwendigerweise noch nicht dividieren (es existieren noch keine multiplikativen Inversen).

### Spezielle Ringeigenschaften
* **Kommutativer Ring:** Ein Ring, in dem auch die Multiplikation kommutativ ist ($a \cdot b = b \cdot a$).
* **Ring mit Eins (Unitärer Ring):** Ein Ring, der ein neutrales Element der Multiplikation (geschrieben als $1$) besitzt, sodass $1 \cdot x = x$ für alle $x$ gilt.

### Konventionen und Notation
* $0$: Neutrales Element der Addition.
* $-a$: Additives Inverses von $a$.
* $a - b$: Kurzschreibweise für $a + (-b)$.
* $1$: Neutrales Element der Multiplikation (in Ringen mit 1).

## 2. Rechenregeln in Ringen

In einem Ring $(R, +, \cdot)$ gelten folgende grundlegende Sätze, die sich aus den Axiomen herleiten lassen.

> [!abstract] Satz: Elementare Rechenregeln
> Sei $R$ ein Ring (mit 1). Für alle $x \in R$ gilt:
> 1. **Null als absorbierendes Element:** $0 \cdot x = 0$ und $x \cdot 0 = 0$.
> 2. **Vorzeichenumkehr:** $(-1) \cdot x = -x$.
> 3. **Vorzeichenprodukt:** $(-1) \cdot (-1) = 1$.

## 3. Nullteiler und Polynomdivision

### Nullteiler
In Ringen ist es möglich, dass das Produkt zweier Zahlen ungleich Null trotzdem Null ergibt (was in den gewohnten Zahlenbereichen $\mathbb{R}$ oder $\mathbb{Q}$ nicht passiert).

> [!important] Definition: Nullteiler
> Ein Element $a \neq 0$ heißt Nullteiler, wenn es ein $b \neq 0$ gibt, sodass $a \cdot b = 0$ gilt.

* **Beispiel Restklassenringe:** Im Ring $\mathbb{Z}_n$ treten Nullteiler genau dann auf, wenn $n$ **keine** Primzahl ist (z.B. in $\mathbb{Z}_4$: $2 \cdot 2 = 0$).
* Ist $p$ eine Primzahl, ist $\mathbb{Z}_p$ nullteilerfrei.

### Polynomdivision (Teilen mit Rest)
In Polynomringen (Menge aller Polynome einer Variablen) ist eine Division mit Rest möglich, analog zur schriftlichen Division von Zahlen.

> [!abstract] Algorithmus: Polynomdivision mit Rest
> Für zwei Polynome $Y$ und $X$ lassen sich Polynome $A$ und $R$ finden, sodass gilt:
> $$Y = A \cdot X + R$$
> Dabei ist der Grad des Restpolynoms $R$ kleiner als der Grad des Divisors $X$ (bzw. $R$ ist möglichst "klein").

## 4. Definition: Körper

Ein Körper erweitert das Konzept des Rings um die Möglichkeit der Division (außer durch Null).

> [!important] Definition: Körper
> Eine Menge $K$ (oder $R$) mit zwei Verknüpfungen $(+, \cdot)$ ist ein **Körper**, wenn gilt:
> 1. $(K, +, \cdot)$ ist ein **kommutativer Ring mit Eins**.
> 2. $(K \setminus \{0\}, \cdot)$ ist eine **abelsche Gruppe**.
>
> **Äquivalente Kurzform:**
> * $(K, +)$ ist eine abelsche Gruppe.
> * $(K \setminus \{0\}, \cdot)$ ist eine abelsche Gruppe.
> * Es gelten die Distributivgesetze.

### Eigenschaften und Beispiele
* In einem Körper besitzt jedes Element $a \neq 0$ ein multiplikatives Inverses, geschrieben als $a^{-1}$ oder $\frac{1}{a}$.
* Körper sind immer nullteilerfrei.

> [!abstract] Satz: Endliche Körper
> Der Restklassenring $\mathbb{Z}_p$ (mit Modulo-Addition und -Multiplikation) ist genau dann ein Körper, wenn $p$ eine **Primzahl** ist[cite: 143].
> * Der kleinstmögliche Körper ist $\mathbb{Z}_2$ (Elemente: 0, 1)[cite: 142].