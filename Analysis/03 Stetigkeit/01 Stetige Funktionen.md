## 1. Definition & Charakterisierung

### $\varepsilon$-$\delta$-Kriterium
Dies ist die fundamentale Definition, um Stetigkeit direkt nachzuweisen.

> [!important] Definition: Stetigkeit
> Eine Funktion $f: X \to Y$ heißt **stetig am Punkt** $a \in X$, falls gilt:
> $$
> \forall \varepsilon > 0 \quad \exists \delta > 0 \quad \forall x \in X : |x - a| < \delta \implies |f(x) - f(a)| < \varepsilon
> $$
> $f$ heißt **stetig** (auf ganz $X$), wenn sie an jedem Punkt $a \in X$ stetig ist.

> [!example] Beispiele aus dem Skript
> * $f(z) = z^2$ ist stetig auf $\mathbb{C}$.
> * Die Signumsfunktion $\text{sgn}(x)$ ist bei $a=0$ **nicht** stetig.

### Folgenstetigkeit
Dieses Kriterium eignet sich oft besser zum Rechnen oder zum Widerlegen von Stetigkeit.

> [!abstract] Satz: Folgenkriterium
> $f: X \to Y$ ist genau dann stetig bei $a \in X$, wenn für **jede** gegen $a$ konvergente Folge $(x_n)_{n \in \mathbb{N}}$ in $X$ gilt:
> $$
> \lim_{n \to \infty} f(x_n) = f(a).
> $$

### Topologische Charakterisierung

> [!note] Offene Mengen
> Eine Funktion $f: \mathbb{R} \to \mathbb{R}$ ist genau dann stetig, wenn die Urbilder offener Mengen wieder offen sind:
> $$B \subset Y \text{ offen} \implies f^{-1}(B) \subset X \text{ offen}.$$

---

## 2. Rechenregeln

Aus der Stetigkeit einfacher Funktionen lässt sich die Stetigkeit komplexer Funktionen ableiten.

> [!abstract] Satz: Algebraische Operationen
> Seien $f, g: X \to \mathbb{C}$ stetig bei $a \in X$. Dann sind auch folgende Funktionen bei $a$ stetig :
> * **Summe/Differenz:** $f \pm g$
> * **Produkt:** $f \cdot g$
> * **Quotient:** $\frac{f}{g}$ (auf $X \setminus \{g^{-1}(0)\}$, d.h. wo der Nenner nicht 0 ist).

> [!abstract] Satz: Verkettung
> Die Komposition stetiger Funktionen ist stetig.
> Ist $f$ stetig bei $a$ und $g$ stetig bei $f(a)$, dann ist $g \circ f$ stetig bei $a$.

> [!tip] Wichtige Funktionsklassen
> Aufgrund dieser Regeln gilt sofort :
> * **Polynome** sind auf ganz $\mathbb{C}$ stetig.
> * **Gebrochen rationale Funktionen** sind auf ihrem Definitionsbereich (wo Nenner $\neq 0$) stetig.

---

## 3. Lipschitz-Stetigkeit

Eine "stärkere" Form der Stetigkeit, die die Steigung der Funktion beschränkt.

> [!definition] Lipschitz-Stetigkeit
> Eine Funktion $f: X \to Y$ heißt **(global) Lipschitz-stetig**, falls eine Konstante $L \in \mathbb{R}_{>0}$ existiert, sodass für alle $x_1, x_2 \in X$ gilt:
> $$
> |f(x_1) - f(x_2)| \leq L |x_1 - x_2|
> $$

> [!important] Implikation
> **Lipschitz-stetig $\implies$ Stetig**.
> *Die Umkehrung gilt nicht!*

> [!example] Beispiele
> * **Betragsfunktion** $|x|$: Lipschitz-stetig mit $L=1$.
> * **Sinus** $\sin(x)$: Lipschitz-stetig mit $L=1$ (folgt aus $| \sin x | \le |x|$).
> * **Wurzel** $\sqrt{x}$: Ist stetig auf $\mathbb{R}_{>0}$, aber **nicht** Lipschitz-stetig (Steigung geht gegen $\infty$ bei 0).

**Funktionenräume:**
Wir definieren die Räume $C^0$ (stetig) und $C^{0,1}$ (Lipschitz-stetig). Es gilt die Inklusion $C^{0,1} \subset C^0$ .

---

## 4. Grenzwerte von Funktionen

Der Grenzwertbegriff untersucht das Verhalten einer Funktion in der *Nähe* eines Punktes, ohne den Funktionswert am Punkt selbst zu beachten.

### Definitionen

> [!definition] Häufungspunkt
> $x_*$ ist ein Häufungspunkt von $X$, wenn in jeder $\varepsilon$-Umgebung unendlich viele Punkte von $X$ liegen. Punkte in $X$, die keine Häufungspunkte sind, heißen **isoliert** .

> [!definition] Grenzwert
> Sei $x_*$ ein Häufungspunkt. $y_*$ heißt Grenzwert von $f$ für $x \to x_*$, wenn für **jede** Folge $(x_n)$ in $X \setminus \{x_*\}$ mit $x_n \to x_*$ gilt:
> $$
> \lim_{n \to \infty} f(x_n) = y_* \quad \text{bzw.} \quad \lim_{x \to x_*} f(x) = y_*
> $$

> [!important] Zusammenhang zur Stetigkeit
> $f$ ist genau dann stetig in $x_* \in X$, wenn Grenzwert und Funktionswert übereinstimmen:
> $$
> \lim_{x \to x_*} f(x) = f(x_*)
> $$

### Erweiterte Grenzwerte

* **Bestimmte Divergenz:** $\lim_{x \to x_*} f(x) = \pm \infty$.
* **Verhalten im Unendlichen:** $\lim_{x \to \pm \infty} f(x) = y_*$.
* **Einseitige Grenzwerte:** Rechtsseitig ($\lim_{x \downarrow x_*}$) und linksseitig ($\lim_{x \uparrow x_*}$).

### Stetige Fortsetzung

> [!abstract] Prinzip der stetigen Fortsetzung
> Hat $f$ an einer Definitionslücke $x_* \notin X$ einen existierenden Grenzwert $y_*$, so kann man $f$ dort "stetig fortsetzen", indem man definiert :
> $$
> \hat{f}(x_*) := \lim_{x \to x_*} f(x)
> $$

> [!example] Beispiel: der "Spalt"
> Die Funktion $f(x) = \frac{\sin x}{x}$ ist bei $x=0$ nicht definiert.
> Da aber $\lim_{x \to 0} \frac{\sin x}{x} = 1$, ist $\hat{f}(0) := 1$ die stetige Fortsetzung .
