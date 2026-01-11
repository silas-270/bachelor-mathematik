## 1. Definitionen & Berechenbare Reihen

> [!important] Definition: Konvergenz einer Reihe
> Sei $(a_k)_{k \ge n_0}$ eine Folge. Die **Reihe** ist die Folge der Partialsummen $(s_n)_{n \ge n_0}$ mit:
> $$s_n := \sum_{k=n_0}^{n} a_k$$
> * Die Reihe heißt **konvergent** gegen $s \in \mathbb{C}$, falls $\lim_{n \to \infty} s_n = s$.
> * Sie heißt **absolut konvergent**, falls $\sum |a_k|$ konvergiert.
> * **Linearität:** Sind $\sum a_k$ und $\sum b_k$ konvergent, so gilt für $\lambda, \mu \in \mathbb{C}$:
>     $$\sum (\lambda a_k + \mu b_k) = \lambda \sum a_k + \mu \sum b_k$$

### Wichtige berechenbare Reihentypen

#### 1. Geometrische Reihe
Für $q \in \mathbb{C}$ gilt für $\sum_{k=0}^{\infty} q^k$:
* **Konvergent** für $|q| < 1$ mit Wert: $\frac{1}{1-q}$
* **Divergent** für $|q| \ge 1$.
    * Für $q > 1$ sogar *bestimmte Divergenz* gegen $\infty$.

#### 2. Teleskopsumme
Eine Reihe, bei der sich durch Partialbruchzerlegung oder Umformung fast alle Terme gegenseitig aufheben.
> [!example] Beispiel (aus Skript)
> $$\sum_{k=1}^{\infty} \frac{1}{k(k+1)} = \sum_{k=1}^{\infty} \left( \frac{1}{k} - \frac{1}{k+1} \right)$$
> Partialsumme: $s_n = (1 - \frac{1}{2}) + (\frac{1}{2} - \frac{1}{3}) + \dots + (\frac{1}{n} - \frac{1}{n+1}) = 1 - \frac{1}{n+1}$
> Grenzwert: $s = \lim_{n \to \infty} \left(1 - \frac{1}{n+1}\right) = 1$.

---

## 2. Standard-Referenzreihen (Vergleichsreihen)

Diese Reihen dienen als Referenz für das Majoranten-/Minorantenkriterium:

* **Harmonische Reihe:** $\sum_{k=1}^{\infty} \frac{1}{k}$ ist **divergent** (Wächst sehr langsam gegen $\infty$).
* **$p$-Reihen / Zeta-Reihen:** $\sum_{k=1}^{\infty} \frac{1}{k^{\alpha}}$
    * **Konvergent** für $\alpha > 1$ (z.B. $\sum \frac{1}{k^2}$ konvergiert).
    * **Divergent** für $\alpha \le 1$.

---

## 3. Konvergenzkriterien

### Notwendiges Kriterium (Ausschlussprinzip)
> [!warning] Nullfolgen-Kriterium
> $$\sum a_k \text{ konvergent} \implies (a_k) \text{ ist eine Nullfolge.}$$
> **Achtung:** Die Umkehrung gilt nicht! (Gegenbeispiel: Harmonische Reihe).
> *Nutzen:* Wenn $a_k$ **keine** Nullfolge ist, divergiert die Reihe sofort.

### Kriterien für absolute Konvergenz

> [!abstract] Majorantenkriterium
> Gilt $|a_k| \le b_k$ für fast alle $k$ und ist $\sum b_k$ eine **konvergente** Majorante, so konvergiert $\sum a_k$ **absolut**.
> $$\left| \sum a_k \right| \le \sum |a_k| \le \sum b_k$$

> [!abstract] Quotientenkriterium
> Sei $a_k \ne 0$. Betrachte $q := \lim_{k \to \infty} \left| \frac{a_{k+1}}{a_k} \right|$.
> * $q < 1 \implies$ **absolut konvergent**.
> * $q > 1 \implies$ **divergent** (da $a_k$ keine Nullfolge).
> * $q = 1 \implies$ **Keine Aussage** (alles möglich).
> *(Es reicht $\limsup < 1$ bzw. $\liminf > 1$).*

> [!abstract] Wurzelkriterium (Stärker als Quotientenkrit.)
> Sei $q := \limsup_{k \to \infty} \sqrt[k]{|a_k|}$.
> * $q < 1 \implies$ **absolut konvergent**.
> * $q > 1 \implies$ **divergent** (da $a_k$ keine Nullfolge).
> * $q = 1 \implies$ **Keine Aussage**.

### Kriterien für spezielle Reihen

> [!abstract] Leibniz-Kriterium (Alternierende Reihen)
> Eine Reihe der Form $\sum_{k=0}^{\infty} (-1)^k b_k$ (mit $b_k \ge 0$) konvergiert, wenn $(b_k)$ eine **monoton fallende Nullfolge** ist.
>
> **Wichtig: Fehlerabschätzung**
> Der Wert der Reihe $s$ liegt immer zwischen zwei aufeinanderfolgenden Partialsummen. Der Fehler bricht beim ersten weggelassenen Glied ab:
> $$|s - s_n| \le b_{n+1}$$

> [!abstract] Verdichtungskriterium (Blocksummation)
> Sei $(a_k)$ reell, nicht-negativ und monoton fallend.
> $\sum_{k=1}^{\infty} a_k$ konvergiert $\iff \sum_{l=0}^{\infty} 2^l a_{2^l}$ konvergiert.
> *Anwendung:* Beweis der Konvergenz von $\sum \frac{1}{k^\alpha}$.

---

## 4. Umordnungssatz & Summierbare Familien

Bei endlichen Summen ist die Reihenfolge egal (Kommutativität). Bei unendlichen Reihen gilt das **nur** eingeschränkt.

> [!important] Großer Umordnungssatz
> Eine Reihe darf genau dann beliebig umgeordnet werden (ohne dass sich der Wert ändert), wenn sie **absolut konvergent** ist.
>
> * Ist die Reihe nur bedingt konvergent (z.B. alternierende harmonische Reihe), kann durch Umordnung jeder beliebige Grenzwert erreicht werden!
> * Absolut konvergente Reihen entsprechen **summierbaren Familien** $(a_j)_{j \in I}$.

---

## 5. Das Cauchy-Produkt

Das Produkt zweier Reihen ("Ausmultiplizieren") ist definiert wie die Faltung von Folgen.

> [!definition] Cauchy-Produkt
> Das Produkt der Reihen $\sum a_k$ und $\sum b_k$ ist die Reihe $\sum c_n$ mit:
> $$c_n = \sum_{k=0}^{n} a_{n-k} b_k$$

> [!abstract] Satz (Konvergenz des Produkts)
> Sind $\sum a_k$ und $\sum b_k$ **absolut konvergent**, so ist auch das Cauchy-Produkt $\sum c_n$ absolut konvergent und es gilt:
> $$\sum_{n=0}^{\infty} c_n = \left(\sum_{k=0}^{\infty} a_k \right) \cdot \left(\sum_{l=0}^{\infty} b_l \right)$$

> [!example] Wichtiges Beispiel: Exponentialfunktion
> Die Funktionalgleichung $e^{z+w} = e^z \cdot e^w$ wird mithilfe des Cauchy-Produkts und des Binomischen Lehrsatzes bewiesen (da die Exponentialreihe absolut konvergiert).