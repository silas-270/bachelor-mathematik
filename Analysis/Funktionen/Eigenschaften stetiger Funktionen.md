## 1. Satz vom Minimum und Maximum

Stetige Funktionen verhalten sich auf kompakten Mengen (z.B. abgeschlossenen, beschränkten Intervallen) besonders gut.

> [!Definition] Globales Maximum und Minimum
> Eine Funktion $f: X \to \mathbb{R}$ hat ein globales Maximum $M$ auf $A \subset X$, falls $\max f(A) = M$.
> * Entsprechend wird das globale Minimum definiert.

Ein zentrales Resultat besagt, dass stetige Funktionen auf kompakten Mengen ihre Extremwerte tatsächlich annehmen.

> [!Theorem] Satz vom Minimum und Maximum
> Sei $f: X \to \mathbb{R}$ stetig und $A \subset X$ kompakt. Dann nimmt $f$ auf $A$ ein Maximum und ein Minimum an.

Die Grundlage dafür bildet folgende topologische Eigenschaft:

> [!Note] Kompaktheit unter stetigen Abbildungen
> Eine stetige Funktion $f: X \to Y$ bildet kompakte Mengen $A \subset X$ in kompakte Mengen $f(A) \subset Y$ ab.

---

## 2. Zwischenwertsatz und Umkehrfunktionen

Der Zwischenwertsatz garantiert, dass stetige Funktionen keine "Sprünge" machen und alle Werte zwischen zwei Funktionswerten annehmen.

> [!Theorem] Zwischenwertsatz
> Sei $f: [\alpha, \beta] \to \mathbb{R}$ eine stetige Funktion mit $f(\alpha) < f(\beta)$.
> Für jedes $y \in (f(\alpha), f(\beta))$ existiert ein $x_y \in [\alpha, \beta]$ mit $f(x_y) = y$.

### Umkehrbarkeit monotoner Funktionen

Aus dem Zwischenwertsatz folgt direkt die Existenz und Stetigkeit von Umkehrfunktionen für monotone Funktionen.

> [!Theorem] Satz über die Umkehrfunktion
> Sei $f: [\alpha, \beta] \to [\xi, \eta]$ stetig und streng monoton wachsend mit $f(\alpha) = \xi$ und $f(\beta) = \eta$. Dann gilt:
> 1. $f$ ist bijektiv.
> 2. Die Umkehrfunktion $f^{-1}: [\xi, \eta] \to [\alpha, \beta]$ ist ebenfalls stetig und streng monoton wachsend.
> _Analoges gilt für streng monoton fallende Funktionen_.

**Wichtige Anwendungen:**
* **Arcus Sinus:** Die Einschränkung $\sin: [-\frac{\pi}{2}, \frac{\pi}{2}] \to [-1, 1]$ ist stetig, streng monoton und bijektiv. Ihre Inverse ist der Arcus sinus.
* **Polarkoordinaten:** Für jedes $z \in \mathbb{C} \setminus \{0\}$ existieren eindeutige $r > 0$ und $\phi \in (-\pi, \pi]$ mit $z = r e^{i\phi}$.
* **Existenz von Nullstellen:** Der Cosinus besitzt eine Nullstelle im Intervall $(0, 2)$, da $\cos(0) > 0$ und $\cos(2) < 0$.

---

## 3. Konvergenz von Funktionenfolgen

Betrachtet wird eine Folge von Funktionen $(f_n)_{n \in \mathbb{N}}$ mit $f_n: X \to Y$. Es gibt zwei wesentliche Konvergenzbegriffe.

### Punktweise vs. Gleichmäßige Konvergenz

> [!Definition] Punktweise Konvergenz
> Eine Funktionenfolge $(f_n)$ konvergiert punktweise gegen $f_*: X \to Y$, falls für jedes $x \in X$ die Zahlenfolge $(f_n(x))$ gegen $f_*(x)$ konvergiert.
> * Problem: Stetigkeit bleibt hierbei nicht zwingend erhalten (der Limes stetiger Funktionen kann unstetig sein).

> [!Definition] Gleichmäßige Konvergenz
> Eine Funktionenfolge $(f_n)$ konvergiert gleichmäßig gegen $f_*$, falls:
> $$
> \forall \varepsilon > 0 \exists N \in \mathbb{N} \forall n > N \forall x \in X : |f_n(x) - f_*(x)| < \varepsilon.
> $$
> * **Unterschied:** Bei der gleichmäßigen Konvergenz muss das $N$ für **alle** $x \in X$ gleichzeitig funktionieren (es hängt nicht von $x$ ab).

### Stetigkeit der Grenzfunktion

> [!Theorem] Stetigkeitssatz
> Konvergiert eine Folge stetiger Funktionen $f_n: X \to Y$ gleichmäßig gegen $f_*$, so ist die Grenzfunktion $f_*$ stetig.

### Anwendung auf Potenzreihen

Potenzreihen sind ein wichtiges Beispiel für gleichmäßige Konvergenz innerhalb ihres Konvergenzradius.

> [!Theorem] Stetigkeit von Potenzreihen
> Sei $P_a(z) = \sum_{k=0}^{\infty} a_k z^k$ eine Potenzreihe mit Konvergenzradius $\rho > 0$.
> Dann ist die Funktion der Reihenwerte $p_a: \mathbb{B}_{\rho} \to \mathbb{C}$ stetig.
> * Beweisidee: Die Partialsummen (Polynome) konvergieren auf jeder kleineren Kreisscheibe $\mathbb{B}_r$ (mit $r < \rho$) gleichmäßig gegen die Potenzreihe.

> [!Note] Elementare Funktionen
> Die Funktionen $\exp, \sin, \cos, \sinh$ und $\cosh$ sind auf ganz $\mathbb{C}$ stetig.