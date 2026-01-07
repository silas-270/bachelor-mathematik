## 1. Vektorräume

### Definition und Axiome

Ein Vektorraum ist eine Struktur, die eine Menge von Vektoren mit einem Körper von Skalaren verknüpft.

> [!important] Definition: $K$-Vektorraum
> Sei $K$ ein Körper. Ein **$K$-Vektorraum** ist eine Menge $V$ zusammen mit zwei Verknüpfungen:
> 1. **Vektoraddition:** $+_V: V \times V \to V, (v, w) \mapsto v + w$
> 2. **Skalarmultiplikation:** $\cdot: K \times V \to V, (\lambda, v) \mapsto \lambda \cdot v$
> 
> Damit $V$ ein Vektorraum ist, müssen folgende Axiome erfüllt sein:
> * **(A) Gruppe:** $(V, +)$ ist eine **kommutative Gruppe**. Das bedeutet:
>     * Es existiert ein neutrales Element $0_V \in V$ (Nullvektor).
>     * Zu jedem $v \in V$ existiert ein additives Inverses $-v \in V$.
>     * Assoziativität und Kommutativität der Addition gelten.
> * **(B) Verträglichkeit mit dem Körper:** Für alle $\lambda, \mu \in K$ und $v, w \in V$ gelten:
>     1. **Distributivität 1:** $\lambda \cdot (v + w) = \lambda \cdot v + \lambda \cdot w$
>     2. **Distributivität 2:** $(\lambda + \mu) \cdot v = \lambda \cdot v + \mu \cdot v$
>     3. **Gemischte Assoziativität:** $(\lambda \cdot \mu) \cdot v = \lambda \cdot (\mu \cdot v)$
>     4. **Normierung (Unitäres Gesetz):** $1_K \cdot v = v$

> [!tip] Intuition
> Ein Vektorraum kombiniert eine abelsche Gruppe (die Vektoren) mit einem Körper (den Skalaren). Die Skalarmultiplikation bewirkt geometrisch oft eine Streckung oder Stauchung. Das Distributivgesetz erlaubt das "Ausklammern" sowohl von Skalaren als auch von Vektoren.

### Elementare Rechenregeln

Aus den Axiomen lassen sich direkt grundlegende Eigenschaften ableiten, die in jedem Vektorraum gelten.

> [!abstract] Satz: Rechenregeln im Vektorraum
> Sei $V$ ein $K$-Vektorraum. Dann gilt für alle $v \in V$ und $\lambda \in K$:
> 1. $0_K \cdot v = 0_V$ (Das Skalar 0 annulliert jeden Vektor).
> 2. $\lambda \cdot 0_V = 0_V$ (Der Nullvektor bleibt bei Skalierung der Nullvektor).
> 3. $\lambda \cdot v = 0_V \implies \lambda = 0_K \lor v = 0_V$ (Nullteilerfreiheit der Skalarmultiplikation).
> 4. $(-1_K) \cdot v = -v$ (Multiplikation mit -1 ergibt das additive Inverse).

---

## 2. Untervektorräume

### Definition und Kriterium

Ein Untervektorraum ist eine Teilmenge eines Vektorraums, die selbst wieder die Vektorraumstruktur trägt.

> [!important] Definition: Untervektorraum
> Sei $V$ ein $K$-Vektorraum. Eine Teilmenge $U \subseteq V$ heißt **Untervektorraum** von $V$, wenn $U$ zusammen mit den von $V$ geerbten Operationen (Addition und Skalarmultiplikation) selbst ein $K$-Vektorraum ist.

Um zu prüfen, ob eine Teilmenge ein Untervektorraum ist, müssen nicht alle Axiome erneut getestet werden. Es genügt das Unterraumkriterium.

> [!abstract] Satz: Unterraumkriterium
> Eine Teilmenge $U \subseteq V$ eines $K$-Vektorraums $V$ ist genau dann ein Untervektorraum, wenn folgende drei Bedingungen erfüllt sind:
> 1. **Nichtleere Menge:** $U \neq \emptyset$ (insbesondere muss $0_V \in U$ gelten).
> 2. **Abgeschlossenheit bzgl. Addition:** Für alle $u, w \in U$ gilt $u + w \in U$.
> 3. **Abgeschlossenheit bzgl. Skalarmultiplikation:** Für alle $u \in U$ und $\lambda \in K$ gilt $\lambda \cdot u \in U$.

> [!tip] Intuition
> Geometrisch sind Untervektorräume im $\mathbb{R}^3$ z.B. der Ursprung selbst, Geraden durch den Ursprung oder Ebenen durch den Ursprung. "Verschobene" Geraden oder Ebenen, die nicht durch die Null gehen, verletzen das Kriterium (kein Nullvektor, keine Abgeschlossenheit).

### Erzeugung von Unterräumen (Aufspann)

Man kann Unterräume konstruieren, indem man die Menge aller Linearkombinationen gewisser Vektoren betrachtet.

> [!important] Definition: Aufgespannter Unterraum (Lineare Hülle)
> Sei $v \in V$. Die Menge aller skalaren Vielfachen von $v$ bildet einen Untervektorraum $U_v$:
> $$U_v = \{ \lambda \cdot v \mid \lambda \in K \}$$
> Dies ist der kleinste Untervektorraum, der $v$ enthält (im Geometrischen oft eine Gerade durch den Ursprung).

> [!abstract] Satz: Aufspann mehrerer Vektoren
> Seien $v, w \in V$. Die Menge aller Linearkombinationen
> $$U = \{ \lambda v + \mu w \mid \lambda, \mu \in K \}$$
> ist ein Untervektorraum von $V$. Dies ist der kleinste Unterraum, der sowohl $v$ als auch $w$ enthält.

### Verbindung zu linearen Gleichungssystemen
Die Frage, ob ein Vektor $b \in V$ im Aufspann von Vektoren $v_1, v_2, \dots$ liegt (also ob er als Linearkombination darstellbar ist), führt auf das Lösen eines **linearen Gleichungssystems** (LGS).
* $b \in \text{span}(v, w) \iff \exists \lambda, \mu \in K: \lambda v + \mu w = b$.