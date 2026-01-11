## 1. Relationen

> [!summary] Definition: Relation
> Eine Relation $R$ zwischen zwei Mengen $A$ und $B$ ist eine **Teilmenge** des kartesischen Produkts:
> $$
> R \subseteq A \times B
> $$

**Schreibweise:**
Anstatt $(x, y) \in R$ schreibt man meist $x \sim y$ (sprich: "$x$ steht in Relation zu $y$").
$$
(x, y) \in R \iff x \sim y
$$

---

## 2. Äquivalenzrelationen

Eine Äquivalenzrelation verallgemeinert das Konzept der "Gleichheit". Sie gruppiert Elemente, die in einer bestimmten Eigenschaft übereinstimmen.

### Definition

> [!important] Definition: Äquivalenzrelation
> Eine Relation $\sim$ auf einer Menge $M$ (also $R \subseteq M \times M$) heißt **Äquivalenzrelation**, wenn sie für alle $x, y, z \in M$ drei Eigenschaften erfüllt:
> 
> 1. **Reflexivität:**
>    $$x \sim x$$
> 2. **Symmetrie:**
>    $$x \sim y \implies y \sim x$$
> 3. **Transitivität:**
>    $$x \sim y \land y \sim z \implies x \sim z$$

### Äquivalenzklassen und Partitionen

Diese beiden Begriffe sind zwei Seiten derselben Medaille.

> [!def] Definition: Äquivalenzklasse
> Die Äquivalenzklasse von $x$ (geschrieben $[x]_\sim$ oder $\bar{x}$) ist die Menge aller Elemente, die zu $x$ äquivalent sind:
> $$[x]_\sim := \{ y \in M \mid x \sim y \}$$
> *$x$ nennt man dabei den **Repräsentanten** der Klasse.*

> [!def] Definition: Partition
> Eine Partition (Zerlegung) einer Menge $M$ ist eine Familie von Teilmengen $P_i \subseteq M$, die drei Bedingungen erfüllt:
> 1. **Nicht leer:** $P_i \neq \emptyset$
> 2. **Paarweise disjunkt:** $P_i \cap P_j = \emptyset$ für $i \neq j$ (keine Überschneidungen).
> 3. **Überdeckend:** $\bigcup P_i = M$ (jedes Element gehört zu einer Teilmenge).

### Der fundamentale Zusammenhang

> [!check] Satz: Zerlegung in Äquivalenzklassen
> Die Menge aller Äquivalenzklassen bildet eine **Partition** der Menge $M$.
> 
> *Das bedeutet:*
> Jedes Element von $M$ liegt in **genau einer** Äquivalenzklasse.

---

## 3. Konkrete Anwendungsbeispiele

Hier sind zwei Beispiele, die zeigen, wie aus einer unendlichen Menge durch Äquivalenzrelationen eine endliche oder strukturiertere Menge wird.

### Beispiel A: Die Restklassen (Algebra)
Dies ist die Grundlage für Kryptografie und Computer-Arithmetik.

* **Menge:** $M = \mathbb{Z}$ (alle ganzen Zahlen).
* **Relation:** $x \sim y :\iff x - y$ ist durch $n$ teilbar (Modulo $n$).
* **Beobachtung:**
    * $5$ und $8$ sind bezüglich Modulo $3$ äquivalent, da beide Rest $2$ lassen.
* **Äquivalenzklasse:** $[2]_3 = \{ ..., -4, -1, 2, 5, 8, ... \}$.
* **Partition:** Die unendlich große Menge $\mathbb{Z}$ wird in genau $n$ Klassen zerlegt ($\mathbb{Z}_n$). Man rechnet nicht mehr mit den Zahlen, sondern mit den Klassen.

### Beispiel B: Der "Vektor" (Geometrie)
In der Physik zeichnet man Pfeile an bestimmten Orten. In der LinA ist uns der Ort egal.

* **Menge:** $M$ ist die Menge aller gerichteten Pfeile im Raum (Pfeile haben eine Länge, Richtung und einen Startpunkt).
* **Relation:** Zwei Pfeile sind äquivalent ($x \sim y$), wenn sie **parallel** sind, die **gleiche Länge** haben und in die **gleiche Richtung** zeigen.
* **Äquivalenzklasse:** Ein **Vektor** ist mathematisch definiert als die Äquivalenzklasse all dieser Pfeile.
* **Effekt:** Es ist egal, wo man den Pfeil hinzeichnet (Repräsentant). Alle Pfeile, die man durch Parallelverschiebung ineinander überführen kann, sind *ein und derselbe* Vektor.