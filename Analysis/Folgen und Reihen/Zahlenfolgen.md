> [!Definition] Konvergenz einer Folge
> Eine Folge $(a_n)_{n \in \mathbb{N}}$ **konvergiert** gegen einen **Grenzwert** $a \in \mathbb{C}$, falls gilt:
> $$\forall \varepsilon > 0 \exists N \in \mathbb{R} \forall n \in \mathbb{N} : n > N \implies |a_n - a| < \varepsilon$$
> Falls eine Folge gegen einen Grenzwert konvergiert, heißt sie **konvergent**, andernfalls **divergent**. Eine Folge mit Grenzwert $0$ heißt **Nullfolge**.

---

## 1. Kriterien zur Konvergenz

### Vergleichskriterium
Es seien $(a_n)$ und $(b_n)$ konvergente reelle Folgen mit $a = \lim_{n \to \infty} a_n$ und $b = \lim_{n \to \infty} b_n$. 
Gilt $a_n \le b_n$ für **fast alle** $n$ (d.h. für alle $n$ ab einem Index $N$), so folgt:
$$a \le b$$

### Einschließungskriterium ("Sandwich-Theorem")
> [!Theorem] Einschließungssatz
> Gegeben seien drei reelle Folgen $(a_n), (b_n), (c_n)$. Gilt $a_n \le c_n \le b_n$ für fast alle $n$ und haben $(a_n)$ und $(b_n)$ denselben Grenzwert $a$, d.h.:
> $$\lim_{n \to \infty} a_n = a = \lim_{n \to \infty} b_n$$
> Dann konvergiert auch $(c_n)$ und es gilt: $\lim_{n \to \infty} c_n = a$.

### Konvergenzkriterium von Cauchy
Eine Folge $(a_n)$ heißt **Cauchy-Folge**, falls die Glieder "beliebig nahe" zusammenrücken:
$$\forall \varepsilon > 0 \exists N \in \mathbb{R} \forall m, n \in \mathbb{N} : m, n > N \implies |a_m - a_n| < \varepsilon$$
> [!Important] Vollständigkeit
> In $\mathbb{R}$ (und $\mathbb{C}$) gilt: Eine Folge konvergiert genau dann, wenn sie eine Cauchy-Folge ist. Dies ist äquivalent zur **Vollständigkeit** des Zahlenbereichs.

---

## 2. Monotonie und Beschränktheit

### Definitionen
* **Beschränktheit:** * **Nach oben:** $\exists K \in \mathbb{R} \forall n: a_n \le K$ (obere Schranke).
    * **Nach unten:** $\exists k \in \mathbb{R} \forall n: a_n \ge k$ (untere Schranke).
    * **Beschränkt:** Sowohl nach oben als auch nach unten beschränkt. Bei komplexen Folgen: $(|a_n|)$ ist beschränkt.
* **Monotonie:**
    * **Monoton wachsend:** $a_{n+1} \ge a_n$ für alle $n \in \mathbb{N}$.
    * **Monoton fallend:** $a_{n+1} \le a_n$ für alle $n \in \mathbb{N}$.

> [!Theorem] Monotoniekriterium
> Jede monotone und beschränkte reelle Zahlenfolge konvergiert.

---

## 3. Rechenregeln für Grenzwerte
Es seien $\lim_{n \to \infty} a_n = a$ und $\lim_{n \to \infty} b_n = b$. Dann gilt:
* $\lim_{n \to \infty} (a_n \pm b_n) = a \pm b$
* $\lim_{n \to \infty} (a_n \cdot b_n) = a \cdot b$
* $\lim_{n \to \infty} \frac{a_n}{b_n} = \frac{a}{b}$ (für $b \neq 0$ und $b_n \neq 0$ f.f.a.)
* $\lim_{n \to \infty} |a_n| = |a|$
* $\lim_{n \to \infty} (\operatorname{Re} a_n) = \operatorname{Re} a$ und $\lim_{n \to \infty} (\operatorname{Im} a_n) = \operatorname{Im} a$

---

## 4. Häufungspunkte und Teilfolgen

> [!Definition] Teilfolge & Häufungspunkt
> Wählt man eine streng monoton wachsende Folge von Indizes $(n_k)_{k \in \mathbb{N}}$, so heißt $(a_{n_k})_{k \in \mathbb{N}}$ eine **Teilfolge** von $(a_n)$. 
> Ein $a \in \mathbb{C}$ heißt **Häufungspunkt** der Folge $(a_n)$, wenn es eine Teilfolge gibt, die gegen $a$ konvergiert.

### Satz von Bolzano-Weierstraß
> [!Theorem] Bolzano-Weierstraß
> Jede beschränkte Folge in $\mathbb{C}$ besitzt (mindestens) einen Häufungspunkt.

### Limes Superior und Limes Inferior
Für reelle Folgen definiert man:
* **$\limsup_{n \to \infty} a_n$**: Der größte Häufungspunkt (bzw. $+\infty$ bei Unbeschränktheit nach oben).
* **$\liminf_{n \to \infty} a_n$**: Der kleinste Häufungspunkt (bzw. $-\infty$ bei Unbeschränktheit nach unten).

---

## 5. Topologische Aspekte

Eine Menge $A \subset \mathbb{C}$ lässt sich über Folgen charakterisieren:

| Eigenschaft | Charakterisierung über Folgen |
| :--- | :--- |
| **Abgeschlossen** | Für jede konvergente Folge $(a_n)$ mit $a_n \in A$ liegt auch der Grenzwert in $A$. |
| **Kompakt** | Jede Folge $(a_n)$ mit $a_n \in A$ besitzt eine Teilfolge, die gegen ein Element in $A$ konvergiert. |

> [!Note] Korollar
> Eine nichtleere, kompakte Menge $A \subset \mathbb{R}$ besitzt stets ein **Maximum** und ein **Minimum**.