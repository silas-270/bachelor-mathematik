> [!Definition] Reihe und Konvergenz
> Sei $(a_k)_{k \ge n_0}$ eine Folge. Die zugehörige Reihe ist die Folge der Partialsummen $(s_n)_{n \ge n_0}$ mit:
> $$
> s_n := \sum_{k=n_0}^{n} a_k
> $$
> Die Reihe heißt konvergent gegen einen Reihenwert $s \in \mathbb{C}$, falls die Partialsummenfolge gegen $s$ konvergiert. Man schreibt dann $\sum_{k=n_0}^{\infty} a_k = s$.
> Divergiert die Partialsummenfolge, so heißt die Reihe divergent.

> [!Theorem] Satz
> Eine Reihe $\sum_{k=n_0}^{\infty} a_k$ mit reellen nicht-negativen Gliedern $a_k$ konvergiert genau dann, wenn die Folge der Partialsummen beschränkt ist.

> [!Theorem] Cauchy-Kriterium
> Eine Reihe $\sum_{k=n_0}^{\infty} a_k$ konvergiert genau dann, wenn gilt:
> $$
> \forall \varepsilon > 0 \exists N \in \mathbb{R} \forall m, n \in \mathbb{N} : n > m > N \implies \left| \sum_{k=m+1}^{n} a_k \right| < \varepsilon.
> $$

---

## 1. Wichtige Referenz-Reihen

### Geometrische Reihe

Für $q \in \mathbb{C}$ gilt für die Reihe $\sum_{k=0}^{\infty} q^k$:
* Konvergent für $|q| < 1$ mit dem Wert:
    $$
    \sum_{k=0}^{\infty} q^k = \frac{1}{1-q}
    $$
* **Divergent** für $|q| [cite_start]\ge 1$.

### Harmonische Reihe & $p$-Reihen
* Die **harmonische Reihe** $\sum_{k=1}^{\infty} \frac{1}{k}$ ist **divergent**.
* Die Reihe der **inversen Quadrate** $\sum_{k=1}^{\infty} \frac{1}{k^2}$ ist **konvergent**.
* **Allgemein:** Die Reihe $\sum_{k=1}^{\infty} \frac{1}{k^{\alpha}}$ konvergiert für $\alpha \in \mathbb{Q}$ mit $\alpha > 1$ und divergiert für $\alpha \le 1$.

---

## 2. Konvergenzkriterien

### Notwendiges Kriterium

> [!Important] Nullfolgen-Kriterium
> Wenn eine Reihe $\sum_{k=n_0}^{\infty} a_k$ konvergiert, dann ist $(a_k)$ eine Nullfolge.
> $$
> \sum a_k \text{ konvergent} \implies \lim_{k \to \infty} a_k = 0
> $$

### Absolute Konvergenz

> [!Definition] Absolute Konvergenz
> Eine Reihe $\sum a_k$ heißt absolut konvergent, falls die Reihe der Beträge $\sum |a_k|$ konvergiert.

> [!Theorem] Satz
> Jede absolut konvergente Reihe ist auch (im gewöhnlichen Sinne) konvergent.

### Majorantenkriterium

> [!Theorem] Majorantenkriterium
> Sei $|a_k| \le b_k$ für alle $k \ge n_0$ und sei $\sum b_k$ konvergent.
> Dann konvergiert $\sum a_k$ absolut und es gilt die Abschätzung:
> $$
> \left| \sum_{k=n_0}^{\infty} a_k \right| \le \sum_{k=n_0}^{\infty} b_k
> $$

### Quotienten- und Wurzelkriterium

> [!Theorem] Quotientenkriterium
> Sei $a_k \ne 0$ für fast alle $k$. Existiert der Grenzwert $q := \lim_{k \to \infty} \left| \frac{a_{k+1}}{a_k} \right|$, dann gilt:
> * $q < 1 \implies$ Die Reihe konvergiert **absolut**.
> * $q > 1 \implies$ Die Reihe **divergiert**.
> * $q = 1 \implies$ Keine Aussage möglich.
> _(Hinweis: Es genügt $\limsup < 1$ für Konvergenz bzw. $\liminf > 1$ für Divergenz)_.

> [!Theorem] Wurzelkriterium
> Sei $q := \limsup_{k \to \infty} \sqrt[k]{|a_k|}$. Dann gilt:
> * $q < 1 \implies$ Die Reihe konvergiert **absolut**.
> * $q > 1 \implies$ Die Reihe **divergiert**.
> * $q = 1 \implies$ Keine Aussage möglich.

### Kriterien für spezielle Reihenformen

> [!Theorem] Leibniz-Kriterium (Alternierende Reihen)
> Sei $(a_k)$ eine monoton fallende reelle Nullfolge mit $a_k \ge 0$.
> Dann konvergiert die alternierende Reihe:
> $$
> \sum_{k=n_0}^{\infty} (-1)^k a_k.
> $$

> [!Theorem] Blocksummation (Verdichtungskriterium)
> Sei $(a_k)$ eine monoton fallende reelle Folge mit $a_k \ge 0$. Die Reihe $\sum_{k=1}^{\infty} a_k$ konvergiert genau dann, wenn die "verdichtete" Reihe konvergiert:
> $$
> \sum_{l=0}^{\infty} 2^l a_{2^l}
> $$

---

## 3. Der Umordnungssatz (Summierbare Familien)

Bei Reihen ist die Reihenfolge der Summanden normalerweise festgelegt. Der Umordnungssatz klärt, wann man diese Reihenfolge ändern darf.

> [!Definition] Summierbare Familie
> Eine Familie von Zahlen $(a_j)_{j \in I}$ (ohne feste Ordnung) heißt **summierbar** zur Summe $s$, wenn die Summe beliebiger endlicher Teilmengen gegen $s$ strebt.
> *Im Gegensatz zur Reihe ist hier keine Reihenfolge vorgegeben.*

> [!Important] Zusammenhang zur absoluten Konvergenz
> Eine Reihe $\sum_{k=0}^{\infty} a_k$ ist genau dann **absolut konvergent**, wenn die zugehörige Familie $(a_k)_{k \in \mathbb{N}}$ **summierbar** ist. 
>$\implies$  **Nur bei absoluter Konvergenz darf die Reihenfolge der Summanden beliebig vertauscht werden.**

> [!Theorem] Großer Umordnungssatz
> Sei $(a_j)_{j \in I}$ eine summierbare Familie und $(I_k)_{k \in K}$ eine disjunkte Zerlegung der Indexmenge $I$. Dann darf "päckchenweise" summiert werden:
> $$
> \sum_{j \in I} a_j = \sum_{k \in K} \left( \sum_{j \in I_k} a_j \right)
> $$
> Die Summe der Teilsummen entspricht der Gesamtsumme.

---

## 4. Rechenregeln und Produkte

Sind $\sum a_k$ und $\sum b_k$ konvergente Reihen, so konvergieren auch Summen und skalare Vielfache (Linearität).

### Cauchy-Produkt

Für das Produkt zweier Reihen gibt es keine einfache komponentenweise Regel. Stattdessen betrachtet man das Cauchy-Produkt ("Faltung").

> [!Definition] Cauchy-Produkt
> Das Cauchy-Produkt zweier Folgen $a$ und $b$ ist die Folge $c = (c_m)$ mit:
> $$
> c_m = \sum_{k=0}^{m} a_{m-k} b_k
> $$

> [!Theorem] Konvergenz des Cauchy-Produkts
> Wenn die Reihen $\sum_{k=0}^{\infty} a_k$ und $\sum_{l=0}^{\infty} b_l$ **absolut konvergieren**, dann ist auch ihr Cauchy-Produkt $\sum_{m=0}^{\infty} c_m$ absolut konvergent. Da absolut konvergente Reihen umgeordnet werden dürfen (siehe Umordnungssatz), gilt:
> $$
> \sum_{m=0}^{\infty} c_m = \left(\sum_{k=0}^{\infty} a_k\right) \cdot \left(\sum_{l=0}^{\infty} b_l\right).
> $$