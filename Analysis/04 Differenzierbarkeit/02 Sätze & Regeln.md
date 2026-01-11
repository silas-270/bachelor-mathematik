## 1. Ableitungsregeln

Sind zwei Funktionen $f, g$ an einer Stelle $a$ differenzierbar, so lassen sie sich verknüpfen.

### Grundrechenarten

> [!important] Satz: Linearität, Produkt- & Quotientenregel
> Seien $f, g$ differenzierbar bei $a$. Dann gilt :
> 1. **Linearität:** $(\lambda f + \mu g)'(a) = \lambda f'(a) + \mu g'(a)$
> 2. **Produktregel:** $(fg)'(a) = f'(a)g(a) + f(a)g'(a)$
> 3. **Quotientenregel:** $\left(\frac{f}{g}\right)'(a) = \frac{f'(a)g(a) - f(a)g'(a)}{g(a)^2}$ (falls $g(a) \neq 0$).

> [!example] Wichtige Ableitungen (Merkliste)
> * **Polynome:** $(x^n)' = n x^{n-1}$ (für $n \in \mathbb{Z}$).
> * **Trigonometrie:** $\sin' = \cos$, $\cos' = -\sin$.
> * **Hyperbolisch:** $\sinh' = \cosh$, $\cosh' = \sinh$.

### Kettenregel (Verkettung)

> [!abstract] Satz: Kettenregel
> Ist $f$ bei $a$ differenzierbar und $g$ bei $b := f(a)$ differenzierbar, so ist die Verkettung $g \circ f$ bei $a$ differenzierbar mit :
> $$(g \circ f)'(a) = g'(f(a)) \cdot f'(a)$$
> *"Äußere Ableitung mal innere Ableitung"*.

### Ableitung der Umkehrfunktion

> [!abstract] Satz
> Sei $f: I \to J$ stetig, streng monoton und bijektiv. Ist $f$ bei $a$ differenzierbar und gilt $f'(a) \neq 0$, so ist die Umkehrfunktion $f^{-1}$ an der Stelle $b = f(a)$ differenzierbar :
> $$(f^{-1})'(b) = \frac{1}{f'(f^{-1}(b))} = \frac{1}{f'(a)}$$

> [!example] Beispiel: Wurzel
> $f(x) = x^k \implies f'(x) = k x^{k-1}$.
> Die Umkehrfunktion $g(x) = \sqrt[k]{x}$ hat die Ableitung $g'(y) = \frac{1}{k (\sqrt[k]{y})^{k-1}}$ .

---

## 2. Die Mittelwertsätze

Diese Sätze stellen die Verbindung zwischen der lokalen Ableitung und dem globalen Verhalten der Funktion her.

### Lokale Extrema

> [!important] Notwendiges Kriterium
> Besitzt $f$ an einer Stelle $x_* \in (a, b)$ ein lokales Extremum (Minimum oder Maximum) und ist dort differenzierbar, so gilt:
> $$f'(x_*) = 0$$
> *Achtung:* Die Umkehrung gilt nicht (Sattelpunkt, z.B. $x^3$ bei 0).

### Der Mittelwertsatz (MWS)

> [!abstract] Satz: Mittelwertsatz (Lagrange)
> Sei $f: [a, b] \to \mathbb{R}$ stetig und auf $(a, b)$ differenzierbar. Dann existiert ein $\xi \in (a, b)$ mit :
> $$f'(\xi) = \frac{f(b) - f(a)}{b - a}$$
> *Geometrisch:* Es gibt eine Stelle, an der die Tangentensteigung gleich der Sekantensteigung ist.

> [!warning] Warnung: Komplexe Funktionen
> Der Mittelwertsatz gilt **nicht** für komplexwertige Funktionen ($f: \mathbb{R} \to \mathbb{C}$).
> *Beispiel:* $f(x) = e^{ix}$ auf $[0, 2\pi]$. Es gilt $f(0)=f(2\pi)=1$, aber $|f'(x)| = |ie^{ix}| = 1 \neq 0$ .

### Anwendungen des MWS

1. **Monotonie-Kriterium:** Sei $f$ differenzierbar auf $(a, b)$.
 * $f'(x) \ge 0 \iff f$ ist monoton steigend.
 * $f'(x) = 0 \iff f$ ist konstant .

2. **Regel von L'Hospital:**
 Seien $f, g$ differenzierbar und $\lim_{x \to a} f(x) = \lim_{x \to a} g(x) = 0$. Existiert der Grenzwert der Ableitungen, so gilt :
 $$\lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)}$$

---

## 3. Funktionenfolgen & Potenzreihen

Wann darf man Limes und Ableitung vertauschen? ($\lim f_n' = (\lim f_n)'$?)

> [!important] Satz: Gleichmäßige Konvergenz der Ableitung
> Sei $(f_n)$ eine Folge differenzierbarer Funktionen. Damit die Grenzfunktion $f$ differenzierbar ist und $f' = \lim f_n'$ gilt, müssen zwei Bedingungen erfüllt sein :
> 1. Die Ableitungen $(f_n')$ konvergieren **gleichmäßig** gegen $g$.
> 2. Die Funktionenfolge $(f_n)$ konvergiert an **mindestens einem Punkt**.
>
> Dann konvergiert $f_n \to f$ gleichmäßig und $f' = g$.

> [!note] Potenzreihen
> Potenzreihen $P(z) = \sum a_k z^k$ dürfen im Inneren ihres Konvergenzkreises **gliedweise differenziert** werden. Die abgeleitete Reihe hat denselben Konvergenzradius .

---

## 4. Taylor-Polynome & Höhere Ableitungen

Ist $f$ mehrfach differenzierbar, kann man sie durch Polynome approximieren.

> [!definition] Taylor-Polynom
> Das Taylor-Polynom vom Grad $m$ für $f$ an der Stelle $a$ ist :
> $$T_m^f(a; x) = \sum_{n=0}^{m} \frac{f^{(n)}(a)}{n!} (x - a)^n$$

> [!abstract] Satz von Taylor (mit Lagrange-Restglied)
> Sei $f$ $(m+1)$-mal stetig differenzierbar. Dann gilt für den Fehler der Approximation :
> $$f(x) = T_m^f(a; x) + \frac{f^{(m+1)}(\xi)}{(m+1)!} (x - a)^{m+1}$$
> für ein $\xi$ zwischen $a$ und $x$.

### Hinreichendes Kriterium für Extrema
Mithilfe der Taylor-Entwicklung (2. Ordnung) lässt sich die Art eines Extremums bestimmen:

> [!important] Satz
> Sei $f'(x_*) = 0$ und $f''(x_*) > 0$. Dann ist $x_*$ ein **lokales Minimum** .
> *(Analog: $f''(x_*) < 0 \implies$ Maximum).*
