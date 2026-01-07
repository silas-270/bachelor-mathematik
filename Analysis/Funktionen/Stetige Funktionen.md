## 1. Charakterisierung der Stetigkeit

### $\varepsilon$-$\delta$-Charakterisierung

> [!Definition] Stetigkeit ($\varepsilon$-$\delta$)
> Eine Funktion $f: X \to Y$ heißt stetig am Punkt $a \in X$, falls:
> $$
> \forall \varepsilon > 0 \quad \exists \delta > 0 \quad \forall x \in X : |x - a| < \delta \implies |f(x) - f(a)| < \varepsilon
> $$
> $f$ heißt **stetig**, falls sie an jedem Punkt $a \in X$ stetig ist.

### Folgenstetigkeit

> [!Theorem] Folgenkriterium
> Eine Funktion $f: X \to Y$ ist genau dann stetig bei $a \in X$, wenn für jede gegen $a$ konvergente Folge $(x_n)_{n \in \mathbb{N}}$ mit $x_n \in X$ gilt:
> $$
> \lim_{n \to \infty} f(x_n) = f(a)
> $$

### Topologische Charakterisierung

> [!Note] Topologische Stetigkeit
> Eine Funktion $f: \mathbb{R} \to \mathbb{R}$ ist genau dann stetig, wenn alle offenen Mengen $B \subset Y$ offene Urbilder $f^{-1}(B) \subset X$ besitzen.

---

## 2. Rechenregeln und Komposition

> [!Theorem] Algebraische Operationen
> Seien $f, g: X \to \mathbb{C}$ stetig bei $a \in X$. Dann sind auch folgende Funktionen stetig bei $a$:
> * Summe/Differenz: $f \pm g$
> * Produkt: $f \cdot g$
> * Quotient: $\frac{f}{g}$ (sofern $g(a) \neq 0$)

> [!Theorem] Verkettung
> Seien $f: X \to Y$ und $g: Y \to Z$ stetige Funktionen. Dann ist auch die Verkettung $g \circ f: X \to Z$ stetig.

---

## 3. Lipschitz-Stetigkeit

Die Lipschitz-Stetigkeit ist eine stärkere Form der Stetigkeit.

> [!Definition] Lipschitz-Stetigkeit
> Eine Funktion $f: X \to Y$ heißt (global) Lipschitz-stetig, falls eine Konstante $L \in \mathbb{R}_{>0}$ existiert, sodass für alle $x_1, x_2 \in X$ gilt:
> $$
> |f(x_1) - f(x_2)| \leq L |x_1 - x_2|
> $$

> [!Important] Zusammenhang zur Stetigkeit
> Jede Lipschitz-stetige Funktion ist stetig.
> Die Umkehrung gilt nicht (z.B. $f(x) = \sqrt{x}$ auf $\mathbb{R}_{>0}$ ist stetig, aber nicht Lipschitz-stetig).

**Funktionenräume:**
* $C^0(X; Y) := \{f: X \to Y \mid f \text{ ist stetig}\}$.
* $C^{0,1}(X; Y) := \{f: X \to Y \mid f \text{ ist global Lipschitz-stetig}\}$.
* Es gilt: $C^{0,1}(X; Y) \subset C^0(X; Y)$.

---

## 4. Grenzwerte von Funktionen

Der Grenzwertbegriff für Funktionen ist eng mit dem Häufungspunktbegriff verbunden.

> [!Definition] Häufungspunkt & Isolierter Punkt
> $x_*$ heißt **Häufungspunkt** der Menge $X$, falls in jeder $\varepsilon$-Umgebung von $x_*$ unendlich viele Punkte von $X$ liegen.
> * Formal: $\forall \epsilon > 0 \exists x \in X \setminus \{x_*\}: |x - x_*| < \varepsilon$.
> * Ein Punkt $x \in X$, der kein Häufungspunkt ist, heißt isoliert.

> [!Definition] Grenzwert einer Funktion 
> Sei $x_*$ ein Häufungspunkt von $X$. $y_*$ heißt Grenzwert von $f$ bei $x_*$, geschrieben $\lim_{x \to x_*} f(x) = y_*$, falls für jede Folge $(x_n)$ in $X \setminus \{x_*\}$ mit $x_n \to x_*$ gilt:
> $$
> \lim_{n \to \infty} f(x_n) = y_*
> $$

> [!Theorem] Grenzwert und Stetigkeit
> $f$ ist stetig bei $x_* \in X$ genau dann, wenn an jedem Häufungspunkt $x_*$ von $X$ gilt:
> $$
> \lim_{x \to x_*} f(x) = f(x_*)
> $$

### Rechenregeln für Grenzwerte

Seien $F := \lim_{x \to x_*} f(x)$ und $G := \lim_{x \to x_*} g(x)$. Dann gilt:
* $\lim (f \pm g)(x) = F \pm G$
* $\lim (fg)(x) = F \cdot G$
* $\lim (\frac{f}{g})(x) = \frac{F}{G}$ (sofern $G \neq 0$)

### Weitere Grenzwert-Varianten

- **Bestimmte Divergenz:** $\lim_{x \to x_*} f(x) = \pm \infty$ .
- **Verhalten im Unendlichen:** $\lim_{x \to \pm \infty} f(x) = y_*$.
- **Einseitige Grenzwerte:** Rechtsseitig ($\lim_{x \downarrow x_*} f(x)$) und linksseitig ($\lim_{x \uparrow x_*} f(x)$) .

> [!Definition] Stetige Fortsetzung
> Sei $x_* \notin X$ ein Häufungspunkt von $X$. Existiert $y_* := \lim_{x \to x_*} f(x)$, so heißt die Funktion $\hat{f}: X \cup \{x_*\} \to Y$ mit
> $$
> \hat{f}(x) = \begin{cases} f(x) & x \in X \\ y_* & x = x_* \end{cases}
> $$
> die **stetige Fortsetzung** von $f$ bei $x_*$.