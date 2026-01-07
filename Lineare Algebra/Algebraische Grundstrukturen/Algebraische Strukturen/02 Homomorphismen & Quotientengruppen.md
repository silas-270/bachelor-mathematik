## 1. Definition eines Homomorphismus

> [!summary] Definition: Gruppenhomomorphismus
> Seien $(G, \circ)$ und $(H, \bullet)$ zwei Gruppen. Eine Abbildung $f: G \to H$ heißt **Gruppenhomomorphismus**, wenn für alle $g_1, g_2 \in G$ gilt:
> $$
> f(g_1 \circ g_2) = f(g_1) \bullet f(g_2)
> $$
> *(Das bedeutet: Es ist egal, ob man erst verknüpft und dann abbildet, oder erst abbildet und dann verknüpft.)*

### Spezielle Homomorphismen

Die Bezeichnungen ändern sich je nach Eigenschaft der Abbildung und ob Start- und Zielgruppe identisch sind:

| Bezeichnung | Eigenschaft der Abbildung | Raum |
| :--- | :--- | :--- |
| **Monomorphismus** | Injektiv | $G \to H$ |
| **Epimorphismus** | Surjektiv | $G \to H$ |
| **Isomorphismus** | Bijektiv | $G \to H$ |
| **Endomorphismus** | Beliebig | $G \to G$ |
| **Automorphismus** | Bijektiv | $G \to G$ |

---

## 2. Kern und Bild

Sei $f: G \to H$ ein Homomorphismus.

> [!info] Definition: Bild (Image)
> Das **Bild** von $f$ ist die Menge aller Elemente in $H$, die getroffen werden.
> $$
> \text{Bild}(f) = \{ f(g) \mid g \in G \} \subseteq H
> $$

> [!info] Definition: Kern (Kernel)
> Der **Kern** von $f$ ist die Menge aller Elemente aus $G$, die auf das **neutrale Element** $e_H$ abgebildet werden.
> $$
> \ker(f) = \{ g \in G \mid f(g) = e_H \} \subseteq G
> $$

### Wichtige Zusammenhänge

Kern und Bild geben Aufschluss über die Eigenschaften der Abbildung:

* **Injektivität:** $\ker(f) = \{e_G\} \iff f$ ist injektiv.
* **Surjektivität:** $\text{Bild}(f) = H \iff f$ ist surjektiv.

Zudem sind sie strukturerhaltend:

> [!check] Satz: Untergruppeneigenschaft
> * Der **Kern** ist stets eine Untergruppe von $G$.
> * Das **Bild** ist stets eine Untergruppe von $H$.

---

## 3. Isomorphismen

Ein Isomorphismus beschreibt zwei Gruppen, die zwar unterschiedliche Bezeichnungen für ihre Elemente haben können, aber **strukturell identisch** sind.

> [!success] Definition: Isomorphie
> Ein **Isomorphismus** ist ein bijektiver Homomorphismus. Existiert ein solcher zwischen $G$ und $H$, schreibt man:
> $$G \cong H$$

---

## 4. Quotientengruppen

### Die Nebenklasse (Coset)

Sei $U$ eine Untergruppe von $G$.

> [!note] Definition
> Für ein Element $g \in G$ ist die Nebenklasse von $g$ bezüglich $U$ definiert als:
> $$
> g \circ U = \{ g \circ u \mid u \in U \}
> $$
> *(In additiver Schreibweise: $g + U = \{ g + u \mid u \in U \}$)*
>
> Man bezeichnet diese Menge oft auch als $[g]_U$ (**Äquivalenzklasse**).

> [!example] Intuition: Vektorraum
> Eine Nebenklasse ist eine "Verschiebung" der Untergruppe $U$ um das Element $g$.
> Im Vektorraum $\mathbb{R}^2$: Wenn $U$ eine Gerade durch den Ursprung ist, entspricht $g+U$ einer dazu **parallelen Gerade**, die durch den Punkt $g$ verläuft.

### Zusammenhang mit Partitionen

Die Nebenklassen von $G$ bzgl. $U$ bilden eine **Partition** von $G$. Das bedeutet, sie zerlegen die Gruppe vollständig und überschneidungsfrei (ähnlich wie Puzzleteile).

1. Jede Äquivalenzrelation liefert eine Partition (die Klassen).
2. Umgekehrt liefert jede Partition eine Äquivalenzrelation ($a \sim b \iff$ sie liegen in der gleichen Nebenklasse).

### Die Quotientenstruktur

Die Menge aller Nebenklassen wird als Quotient von $G$ nach $U$ bezeichnet.

> [!summary] Definition: Quotientengruppe
> $$
> G/U := \{ g \circ U \mid g \in G \}
> $$
> Wir definieren eine Verknüpfung auf dieser Menge, um sie selbst zur Gruppe zu machen:
> $$
> (g_1 \circ U) \cdot (g_2 \circ U) := (g_1 \circ g_2) \circ U
> $$

> [!check] Satz: Wohldefiniertheit
> Diese Verknüpfung ist **wohldefiniert** (hängt nicht von der Wahl der Repräsentanten ab) und macht $G/U$ zu einer Gruppe.
> * **Neutrales Element:** $e \circ U$ (also die Untergruppe $U$ selbst).
> * **Inverses Element:** Das Inverse zu $g \circ U$ ist $g^{-1} \circ U$.

---

## 5. Der Isomorphiesatz für Gruppen

Der Satz (auch Homomorphiesatz genannt) verknüpft den abstrakten Begriff der Quotientengruppe mit dem Bild eines Homomorphismus.

**Gegeben:** Homomorphismus $f: G \to H$ mit Kern $K$ und Bild $B$.

> [!abstract] Homomorphiesatz
> Die Quotientengruppe von $G$ nach dem Kern von $f$ ist isomorph zum Bild von $f$.
> $$
> G / \ker(f) \cong \text{Bild}(f)
> $$
> **Interpretation:** Wenn man im Definitionsbereich $G$ alles "zu eins macht" (faktorisiert), was auf die Null abgebildet wird (der Kern), erhält man exakt die Struktur des Bildbereichs.

### Beispiel: Modulo-Rechnung

Wie erzeugt man $\mathbb{Z}_5$ aus $\mathbb{Z}$?

1. **Gruppe $G$:** Die ganzen Zahlen $\mathbb{Z}$.
2. **Abbildung:** $f(z) = z \text{ mod } 5$.
3. **Kern:** Alle durch 5 teilbaren Zahlen ($5\mathbb{Z}$).
4. **Bild:** Die Reste $\{0, 1, 2, 3, 4\} = \mathbb{Z}_5$.

Anwendung des Satzes:
$$\mathbb{Z} / 5\mathbb{Z} \cong \mathbb{Z}_5$$