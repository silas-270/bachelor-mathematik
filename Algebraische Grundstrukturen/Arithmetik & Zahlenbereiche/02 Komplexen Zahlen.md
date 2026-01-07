### Definition und Körperstruktur

> [!important] Definition: Die Menge der Komplexen Zahlen
> Die Menge der komplexen Zahlen $\mathbb{C}$ wird formal als der Vektorraum $\mathbb{R}^2$ definiert, ausgestattet mit zwei Operationen:
> * **Addition (komponentenweise):**
> $$(a_1, b_1) + (a_2, b_2) := (a_1 + a_2, b_1 + b_2)$$
> * **Multiplikation:**
> $$(a_1, b_1) \cdot (a_2, b_2) := (a_1 a_2 - b_1 b_2, \ a_1 b_2 + a_2 b_1)$$

> [!abstract] Satz: $\mathbb{C}$ als Körper
> Die Struktur $(\mathbb{R}^2, +, \cdot)$ bildet einen Körper. Das neutrale Element der Addition ist $(0,0)$, das neutrale Element der Multiplikation ist $(1,0)$.

### Algebraische Darstellung
Durch die Identifikation $1 := (1,0)$ und $i := (0,1)$ (imaginäre Einheit) lässt sich jede komplexe Zahl $(a, b)$ schreiben als:
$$z = a + i \cdot b$$
wobei $a = \text{Re}(z)$ (Realteil) und $b = \text{Im}(z)$ (Imaginärteil).

> [!abstract] Eigenschaft der imaginären Einheit
> Es gilt:
> $$i^2 = -1$$

> [!important] Rechenverfahren: Multiplikatives Inverses
> Für $z = a + ib \neq 0$ ist das Inverse $z^{-1}$ gegeben durch:
> $$z^{-1} = \frac{a}{a^2 + b^2} - i \frac{b}{a^2 + b^2}$$

---

## Geometrie der Komplexen Zahlen

### Polarkoordinaten und Eulersche Formel

> [!important] Definition: Polarkoordinaten
> Jede komplexe Zahl $z \neq 0$ kann durch ihren Betrag $r$ (Abstand zum Ursprung) und den Winkel $\phi$ zur reellen Achse dargestellt werden:
> $$z = r (\cos \phi + i \sin \phi)$$
> * **Betrag:** $r = |z| = \sqrt{a^2 + b^2}$
> * **Winkel:** $\phi$ wird meist im Intervall $[0, 2\pi)$ angegeben.

> [!abstract] Satz: Eulersche Formel
> Es gilt der Zusammenhang zwischen der Exponentialfunktion und den trigonometrischen Funktionen:
> $$e^{i\phi} = \cos \phi + i \sin \phi$$
> Daraus folgt die **Exponentialdarstellung** komplexer Zahlen: $z = r \cdot e^{i\phi}$.

### Geometrische Interpretation der Rechenoperationen

> [!tip] Intuition: Multiplikation
> Die Multiplikation zweier komplexer Zahlen $z_1 = r_1 e^{i\phi_1}$ und $z_2 = r_2 e^{i\phi_2}$ entspricht geometrisch einer **Drehstreckung**:
> $$z_1 \cdot z_2 = (r_1 \cdot r_2) \cdot e^{i(\phi_1 + \phi_2)}$$
> * Die Beträge werden multipliziert (Streckung).
> * Die Winkel werden addiert (Drehung).

* **Potenzieren ($z^n$):** Der Betrag wird zur $n$-ten Potenz erhoben, der Winkel ver-n-facht (Moivrescher Satz).

### Komplexe Konjugation

> [!important] Definition: Komplexe Konjugation
> Zu $z = a + ib$ ist die konjugiert komplexe Zahl definiert als:
> $$\bar{z} := a - ib$$
> Geometrisch entspricht dies einer Spiegelung an der reellen Achse.

> [!abstract] Eigenschaften der Konjugation
> * $\overline{z_1 + z_2} = \bar{z}_1 + \bar{z}_2$
> * $\overline{z_1 \cdot z_2} = \bar{z}_1 \cdot \bar{z}_2$
> * Zusammenhang zum Betrag: $z \cdot \bar{z} = |z|^2 = a^2 + b^2$

---

## Lösen von Gleichungen

### Fundamentalsatz der Algebra

> [!abstract] Theorem: Fundamentalsatz der Algebra (Gauss)
> Jedes nicht-konstante Polynom $P(z) = a_n z^n + \dots + a_1 z + a_0$ mit komplexen Koeffizienten ($n \ge 1$) besitzt mindestens eine Nullstelle in $\mathbb{C}$.

> [!abstract] Korollar: Linearfaktorzerlegung
> Ein Polynom vom Grad $n$ zerfällt über $\mathbb{C}$ vollständig in Linearfaktoren. Es gibt genau $n$ Nullstellen (wenn diese mit ihrer Vielfachheit gezählt werden):
> $$P(z) = a_n (z - x_1) (z - x_2) \cdots (z - x_n)$$

> [!tip] Intuition: Reelle Polynome
> Ist $P(z)$ ein Polynom mit **reellen** Koeffizienten und ist $x$ eine nicht-reelle Nullstelle, so ist auch die konjugiert komplexe Zahl $\bar{x}$ eine Nullstelle. Komplexe Nullstellen treten bei reellen Polynomen immer in konjugierten Paaren auf.

### Wurzelziehen (Radikale)

Das Lösen der Gleichung $z^n = w$ (Bestimmen der $n$-ten Wurzeln) ist geometrisch das Finden eines regulären $n$-Ecks.

> [!important] Definition: $n$-te Einheitswurzeln
> Die Lösungen der Gleichung $z^n = 1$ heißen $n$-te Einheitswurzeln. Sie bilden die Eckpunkte eines regulären $n$-Ecks auf dem Einheitskreis:
> $$\zeta_k = e^{i \frac{2\pi k}{n}} \quad \text{für } k = 0, 1, \dots, n-1$$

> [!important] Rechenverfahren: Bestimmung aller Lösungen von $z^n = w$
> Gegeben sei $w = R \cdot e^{i\Phi}$. Die $n$ Lösungen $z_0, \dots, z_{n-1}$ erhält man wie folgt:
> 1.  Bestimme eine partikuläre Lösung ("Hauptwert"):
>     $$z_0 = \sqrt[n]{R} \cdot e^{i \frac{\Phi}{n}}$$
> 2.  Multipliziere diese Lösung mit allen $n$-ten Einheitswurzeln, um die restlichen Lösungen zu erhalten:
>     $$z_k = z_0 \cdot e^{i \frac{2\pi k}{n}} = \sqrt[n]{R} \cdot e^{i \frac{\Phi + 2\pi k}{n}}$$