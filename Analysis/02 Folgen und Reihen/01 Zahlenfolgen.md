## 1. Grundlagen der Konvergenz

### Definitionen

> [!important] Definition: Konvergenz
> Eine Folge $(a_n)_{n \in \mathbb{N}}$ **konvergiert** gegen einen **Grenzwert** $a \in \mathbb{C}$, falls gilt:
> $$\forall \varepsilon > 0 \; \exists N \in \mathbb{R} \; \forall n \in \mathbb{N} : n > N \implies |a_n - a| < \varepsilon$$
> * Notation: $\lim_{n \to \infty} a_n = a$ oder $a_n \to a$.
> * Eine Folge mit Grenzwert $0$ heißt **Nullfolge**.

> [!note] Satz: Eindeutigkeit des Grenzwerts
> Der Grenzwert einer konvergenten Folge ist **eindeutig** bestimmt. (In Hausdorff-Räumen wie $\mathbb{R}$ oder $\mathbb{C}$ kann eine Folge nicht gegen zwei verschiedene Werte konvergieren).

### Bestimmte Divergenz (Uneigentliche Konvergenz)
Eine reelle Folge $(a_n)$ divergiert **bestimmt gegen $+\infty$**, falls:
$$\forall K \in \mathbb{R} \; \exists N \in \mathbb{R} \; \forall n > N : a_n > K$$
(Analog für $-\infty$).

---

## 2. Wichtige Beispiele & Beweistechniken

> [!example] Beispiel: $\epsilon-N$-Beweis
> **Behauptung:** $a_n = \frac{1}{n}$ konvergiert gegen $0$.
> **Beweis:**
> Sei $\varepsilon > 0$ beliebig. Wähle $N := \frac{1}{\varepsilon}$.
> Für alle $n > N$ gilt:
> $$|a_n - 0| = \frac{1}{n} < \frac{1}{N} = \varepsilon$$
> $\square$

> [!tip] Wichtige Standard-Grenzwerte (Auswendig wissen!)
> * $\lim_{n \to \infty} \frac{1}{n^\alpha} = 0$ für $\alpha > 0$
> * $\lim_{n \to \infty} \sqrt[n]{n} = 1$
> * $\lim_{n \to \infty} \sqrt[n]{c} = 1$ für $c > 0$
> * $\lim_{n \to \infty} q^n = 0$ für $|q| < 1$
> * $\lim_{n \to \infty} \left(1 + \frac{x}{n}\right)^n = e^x$ für $x \in \mathbb{R}$

> [!quote] Hilfsmittel: Bernoulli-Ungleichung
> Für $x \ge -1$ und $n \in \mathbb{N}$ gilt:
> $$(1+x)^n \ge 1 + n \cdot x$$
> *Essienziell für Abschätzungen bei Potenzen.*

---

## 3. Rechenregeln für Grenzwerte

Seien $(a_n) \to a$ und $(b_n) \to b$.

| Operation | Regel | Bedingung |
| :--- | :--- | :--- |
| **Summe/Diff** | $\lim (a_n \pm b_n) = a \pm b$ | |
| **Produkt** | $\lim (a_n \cdot b_n) = a \cdot b$ | |
| **Quotient** | $\lim \frac{a_n}{b_n} = \frac{a}{b}$ | $b \neq 0, b_n \neq 0$ |
| **Betrag** | $\lim |a_n| = |a|$ | |
| **Wurzel** | $\lim \sqrt{a_n} = \sqrt{a}$ | $a_n \ge 0$ |
| **Komplex** | $\lim a_n = a \iff \lim \operatorname{Re}(a_n) = \operatorname{Re}(a) \land \lim \operatorname{Im}(a_n) = \operatorname{Im}(a)$ | |

> [!warning] Achtung bei unbestimmten Ausdrücken
> Ausdrücke wie $\frac{0}{0}, \frac{\infty}{\infty}, 0 \cdot \infty, \infty - \infty, 1^\infty$ erlauben **keine** direkte Aussage. Hier muss umgeformt werden!

---

## 4. Konvergenzkriterien

### Vergleichskriterium (Majorantenkriterium)
Seien $(a_n), (b_n)$ reelle Folgen.
1.  **Majorante:** Ist $|a_n| \le b_n$ für fast alle $n$ und ist $(b_n)$ eine Nullfolge, so ist auch $(a_n)$ eine Nullfolge.
2.  **Ungleichungserhalt:** Konvergieren $a_n \to a$ und $b_n \to b$ und gilt $a_n \le b_n$ für fast alle $n$, so folgt $a \le b$. (Strikte Ungleichung $<$ überträgt sich **nicht** notwendig strikt, es bleibt $\le$).

### Einschließungskriterium ("Sandwich-Theorem")
> [!abstract] Satz
> Gilt $a_n \le c_n \le b_n$ für fast alle $n$ und $\lim a_n = \lim b_n = a$, dann konvergiert auch $(c_n)$ gegen $a$.

### Cauchy-Kriterium (Vollständigkeit)
Eine Folge konvergiert in $\mathbb{R}$ (oder $\mathbb{C}$) genau dann, wenn sie eine **Cauchy-Folge** ist:
$$\forall \varepsilon > 0 \; \exists N \in \mathbb{R} \; \forall m, n > N : |a_m - a_n| < \varepsilon$$
* **Nutzen:** Nachweis von Konvergenz, ohne den Grenzwert zu kennen.

---

## 5. Monotonie & Beschränktheit

### Definitionen
* **Beschränktheit:** * **Nach oben:** $\exists K \in \mathbb{R} \forall n: a_n \le K$ (obere Schranke).
    * **Nach unten:** $\exists k \in \mathbb{R} \forall n: a_n \ge k$ (untere Schranke).
    * **Beschränkt:** Sowohl nach oben als auch nach unten beschränkt. Bei komplexen Folgen: $(|a_n|)$ ist beschränkt.
* **Monotonie:**
    * **Monoton wachsend:** $a_{n+1} \ge a_n$ für alle $n \in \mathbb{N}$.
    * **Monoton fallend:** $a_{n+1} \le a_n$ für alle $n \in \mathbb{N}$.

### Monotoniekriterium (Wichtig für Rekursion!)
> [!abstract] Satz
> Jede **monotone** und **beschränkte** reelle Folge konvergiert.
> * Wachsend + nach oben beschränkt $\implies$ konvergent.
> * Fallend + nach unten beschränkt $\implies$ konvergent.

> [!example] Strategie für rekursive Folgen ($a_{n+1} = f(a_n)$)
> 1.  **Beschränktheit** zeigen (meist Induktion).
> 2.  **Monotonie** zeigen (meist Induktion oder $a_{n+1} - a_n$ untersuchen).
> 3.  Konvergenz folgern (Monotoniekriterium).
> 4.  **Grenzwert berechnen:** $a = \lim a_n = \lim a_{n+1}$. Gleichung $a = f(a)$ lösen.

---

## 6. Teilfolgen & Häufungspunkte

> [!important] Definitionen
> * **Teilfolge:** Auswahl von Folgengliedern $(a_{n_k})$ mit $n_1 < n_2 < \dots$
> * **Häufungspunkt (HP):** Grenzwert einer konvergenten Teilfolge.
>     * Alternative Definition: In jeder $\varepsilon$-Umgebung des HP liegen unendlich viele Folgenglieder.

### Satz von Bolzano-Weierstraß
> [!abstract] Satz
> Jede beschränkte Folge in $\mathbb{R}$ (oder $\mathbb{C}$) besitzt mindestens einen Häufungspunkt (also eine konvergente Teilfolge).

### Limes Superior / Inferior
* $\limsup a_n$: Der größte HP (oder $+\infty$).
* $\liminf a_n$: Der kleinste HP (oder $-\infty$).
* Eine Folge konvergiert $\iff \limsup a_n = \liminf a_n$.

---

## 7. Topologie (Zusammenhang Folgen & Mengen)

Eine Menge $A \subset \mathbb{K}$ (mit $\mathbb{K} \in \{\mathbb{R}, \mathbb{C}\}$) lässt sich durch Folgen charakterisieren:

| Eigenschaft | Definition über Folgen |
| :--- | :--- |
| **Abgeschlossenheit** | $A$ ist abgeschlossen $\iff$ Der Grenzwert jeder konvergenten Folge aus $A$ liegt wieder in $A$. |
| **Kompaktheit** | $A$ ist kompakt $\iff$ Jede Folge in $A$ besitzt eine Teilfolge, die gegen ein $a \in A$ konvergiert. |

> [!note] Satz von Heine-Borel (in $\mathbb{R}^n / \mathbb{C}$)
> Eine Menge ist **kompakt** genau dann, wenn sie **beschränkt** und **abgeschlossen** ist.