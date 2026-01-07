## 1. Quotientenstrukturen in Vektorräumen

In dieser Vorlesung wird das Konzept der aus der Gruppentheorie bekannten Nebenklassen und Quotientenstrukturen auf Vektorräume übertragen. Da Vektorräume spezielle (kommutative) Gruppen sind, lassen sich diese Konzepte analog anwenden.

### Nebenklassen und der Quotientenraum

> [!important] Definition: Nebenklasse (Affiner Unterraum)
> Sei $V$ ein $K$-Vektorraum und $U \subseteq V$ ein Untervektorraum. Für ein $v \in V$ ist die **Nebenklasse** von $v$ bezüglich $U$ definiert als:
> $$v + U := \{ v + u \mid u \in U \}$$

Die Menge aller solchen Nebenklassen bildet den Quotientenraum.

> [!important] Definition: Quotientenraum
> Die Menge aller Nebenklassen von $U$ in $V$ wird als **Quotientenraum** (oder Faktorraum) bezeichnet:
> $$V/U := \{ v + U \mid v \in V \}$$
> Dies entspricht einer Partition von $V$ in disjunkte Teilmengen.

### Vektorraumstruktur auf $V/U$

Auf der Menge der Nebenklassen lassen sich Vektorraumoperationen definieren. Diese sind wohldefiniert, d.h. unabhängig von der Wahl des Repräsentanten $v$ der Nebenklasse.

> [!important] Definition: Rechnen im Quotientenraum
> Für $v, w \in V$ und $\lambda \in K$ sind die Operationen wie folgt definiert:
> * **Addition:** $(v + U) + (w + U) := (v + w) + U$
> * **Skalarmultiplikation:** $\lambda \cdot (v + U) := (\lambda v) + U$

> [!abstract] Satz: Struktur des Quotientenraums
> Die Menge $V/U$ bildet zusammen mit der oben definierten Addition und Skalarmultiplikation einen $K$-Vektorraum.

Ein zentraler Zusammenhang besteht zwischen den Dimensionen der beteiligten Räume.

> [!abstract] Satz: Dimensionsformel für Quotientenräume
> Für einen Vektorraum $V$ und einen Unterraum $U$ gilt der folgende Zusammenhang der Dimensionen:
> $$\dim(U) + \dim(V/U) = \dim(V)$$

---

## 2. Der Homomorphiesatz für Vektorräume

Der Homomorphiesatz stellt eine fundamentale Beziehung zwischen linearen Abbildungen, ihren Kernen und ihren Bildern her. Er ist analog zum Homomorphiesatz für Gruppen.

> [!abstract] Satz: Isomorphiesatz für Vektorräume
> Gegeben sei eine lineare Abbildung $f: V \to W$ zwischen zwei $K$-Vektorräumen. Da $(V, +_V)$ und $(W, +_W)$ kommutative Gruppen sind, gilt:
> $$V / \ker(f) \cong \text{Bild}(f)$$

> [!important] Definition: Der induzierte Isomorphismus
> Die zugehörige Isomorphismus-Abbildung $\Phi: V/\ker(f) \to \text{Bild}(f)$ ist definiert durch:
> $$\Phi(v + \ker(f)) := f(v)$$
> Diese Abbildung ordnet jeder Nebenklasse das Bild ihres Repräsentanten zu.

**Eigenschaften der Abbildung $\Phi$:**
* **Wohldefiniertheit:** Das Ergebnis ist unabhängig vom gewählten Repräsentanten $v$.
* **Bijektivität:** Die Abbildung ist injektiv und surjektiv auf das Bild.
* **Linearität:** Die Abbildung ist verträglich mit Addition und Skalarmultiplikation (Strukturverträglichkeit).