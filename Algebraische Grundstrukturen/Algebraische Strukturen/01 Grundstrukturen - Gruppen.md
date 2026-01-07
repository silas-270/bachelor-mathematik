## 1. Definition einer Gruppe

> [!summary] Definition: Gruppe
> Eine **Gruppe** $(G, \circ)$ besteht aus einer Menge $G$ und einer Verknüpfung $\circ: G \times G \to G$, die $(a, b) \mapsto a \circ b$ abbildet.

### Die Gruppenaxiome

Damit $(G, \circ)$ eine Gruppe ist, müssen folgende Bedingungen für alle $a, b, c \in G$ erfüllt sein:

1. **Abgeschlossenheit:**
   $$a \circ b \in G$$
2. **Assoziativgesetz:**
   $$(a \circ b) \circ c = a \circ (b \circ c)$$
3. **Existenz des neutralen Elements:**
   Es existiert ein $e \in G$, sodass gilt:
   $$e \circ a = a$$
4. **Existenz des inversen Elements:**
   Zu jedem $a \in G$ existiert ein $a' \in G$, sodass:
   $$a' \circ a = e$$

### Die Hierarchie der Strukturen

Hier bauen die Strukturen aufeinander auf:

| Struktur | Abgeschlossen | Assoziativ | Neutrales Elem. | Inverses Elem. |
| :--- | :---: | :---: | :---: | :---: |
| **Halbgruppe** | ✅ | ✅ | ❌ | ❌ |
| **Monoid** | ✅ | ✅ | ✅ | ❌ |
| **Gruppe** | ✅ | ✅ | ✅ | ✅ |

### Zusatz: Kommutativität

Eine Gruppe heißt **kommutativ** (oder *abelsch*), wenn zusätzlich gilt:
$$a \circ b = b \circ a \quad \forall a,b \in G$$

---

## 2. Wichtige Eigenschaften

Sei $(G, \circ)$ eine Gruppe mit neutralem Element $e$. Sei $a'$ das zu $a$ inverse Element (oft auch $a^{-1}$ geschrieben).

### Sätze zu Neutralität und Inversen

Unabhängig von der Kommutativität gilt in **jeder** Gruppe:

* **Links-neutral = Rechts-neutral:**
  $e \circ a = a \circ e = a$
* **Links-invers = Rechts-invers:**
  $a' \circ a = a \circ a' = e$

> [!tip] Wichtige Rechenregel
> Ein Element darf immer mit dem neutralen Element oder seinem *eigenen* Inversen vertauscht werden.
> Es darf jedoch **nicht** allgemein mit einem beliebigen Element vertauscht werden (außer die Gruppe ist abelsch).

### Eindeutigkeit und Lösbarkeit

1. **Lösbarkeit von Gleichungen:**
   Die Gleichungen $a \circ x = b$ und $x \circ c = d$ haben jeweils eine **eindeutige Lösung**.
2. **Eindeutigkeit der Elemente:**
   * Das neutrale Element $e$ ist eindeutig.
   * Das zu $a \in G$ inverse Element $a'$ ist eindeutig.

> [!example] Die "Gruppen-Sudoku-Regel"
> Für die Gruppentafel (Verknüpfungstabelle) gilt:
> Jedes Element der Gruppe taucht in **jeder Zeile** und in **jeder Spalte** genau einmal auf.

---

## 3. Untergruppen

> [!info] Definition: Untergruppe
> Sei $(G, \circ)$ eine Gruppe und $U \subseteq G$ eine Teilmenge.
> $(U, \circ)$ heißt **Untergruppe** von $G$, wenn $(U, \circ)$ selbst eine Gruppe ist.

Um zu prüfen, ob eine Teilmenge eine Untergruppe ist, nutzt man das **Untergruppenkriterium** (statt alle Axiome neu zu prüfen):

> [!check] Satz: Untergruppenkriterium
> Eine Teilmenge $U \subseteq G$ ist genau dann eine Untergruppe ($U \le G$), wenn gilt:
> 1. **Nicht-leere Menge:** $U \neq \emptyset$ (Praxistipp: Zeige $e \in U$).
> 2. **Abgeschlossenheit:** $\forall a, b \in U \Rightarrow a \circ b \in U$.
> 3. **Inverse Elemente:** $\forall a \in U \Rightarrow a' \in U$.

### Wichtige Beispiele

* **Untergruppen von $(\mathbb{Z}, +)$:**
  Jede Untergruppe von $\mathbb{Z}$ ist von der Form $n\mathbb{Z} = \{k \cdot n \mid k \in \mathbb{Z}\}$ für ein $n \in \mathbb{N}$.

* **Erzeugte Untergruppen $\langle M \rangle$:**
  Sei $M \subseteq G$. Die **von $M$ erzeugte Untergruppe** ist die *kleinste* Untergruppe von $G$, die $M$ enthält. Sie erfüllt zwei Eigenschaften:
  1. $M \subseteq \langle M \rangle$
  2. Für jede andere Untergruppe $V$ mit $M \subseteq V$ gilt $\langle M \rangle \subseteq V$.

---

## 4. Modulo-Gruppen

### Modulo und Division mit Rest

> [!note] Definition
> Sei $p \in \mathbb{N}$ und $a \in \mathbb{Z}$. Wir definieren $a \text{ mod } p := r$, wobei $r$ der Rest bei der Division durch $p$ ist.

Wir betrachten die Menge $\mathbb{Z}_p = \{0, 1, ..., p-1\}$ mit zwei Verknüpfungen:
1. **Addition modulo $p$ ($\oplus_p$):** $a \oplus_p b := (a + b) \text{ mod } p$
2. **Multiplikation modulo $p$ ($\odot_p$):** $a \odot_p b := (a \cdot b) \text{ mod } p$

### Satz: Gruppeneigenschaften

* **(i) Additive Gruppe:**
  $(\mathbb{Z}_p, \oplus_p)$ ist für **alle** $p \in \mathbb{N} \setminus \{0\}$ eine Gruppe.
* **(ii) Multiplikative Gruppe:**
  $(\mathbb{Z}_p \setminus \{0\}, \odot_p)$ ist **genau dann** eine Gruppe, wenn **$p$ eine Primzahl** ist.