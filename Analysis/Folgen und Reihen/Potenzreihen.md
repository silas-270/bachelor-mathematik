> [!Definition] Potenzreihe
> Sei $(a_k)_{k \in \mathbb{N}}$ eine Folge von Koeffizienten. Die Zuordnung $P_a$ von $z \in \mathbb{C}$ zur Reihe
> $$
> P_a(z) = \sum_{k=0}^{\infty} a_k z^k
> $$
> heißt **Potenzreihe**.

## 1. Konvergenzradius

Potenzreihen haben ein sehr geordnetes Konvergenzverhalten. Es gibt einen Radius, innerhalb dessen sie immer konvergieren und außerhalb dessen sie divergieren.

> [!Definition] Konvergenzradius
> Der Konvergenzradius $\rho(P_a) \in \mathbb{R}_{\ge 0} \cup \{+\infty\}$ ist definiert als:
> $$
> \rho(P_a) := \sup\{r \in \mathbb{R}_{\ge 0} \mid P_a(r) \text{ konvergiert}\}
> $$

> [!Theorem] Konvergenzbereich
> Sei $\rho$ der Konvergenzradius. Dann gilt:
> * Für alle $z \in \mathbb{C}$ mit $|z| < \rho$ ist die Reihe **absolut konvergent**3.
> * Für alle $z \in \mathbb{C}$ mit $|z| > \rho$ ist die Reihe **divergent**4.
> * Für den Randfall $|z| = \rho$ ist keine allgemeine Aussage möglich.

### Berechnung des Konvergenzradius

Um $\rho$ zu bestimmen, nutzt man Varianten des Wurzel- oder Quotientenkriteriums.

> [!Theorem] Formel von Cauchy-Hadamard (Wurzel)
> Sei $q := \limsup_{k \to \infty} \sqrt[k]{|a_k|}$. Dann ist der Konvergenzradius:
> $$
> \rho(P_a) = \frac{1}{q}
> $$
> _(Konvention: $1/0 = \infty$ und $1/\infty = 0$)_.

> [!Theorem] Euler-Formel (Quotient)
> Falls der Grenzwert $q := \lim_{k \to \infty} \left| \frac{a_{k+1}}{a_k} \right|$ existiert, gilt ebenfalls:
> $$
> \rho(P_a) = \frac{1}{q}
> $$.

> [!Note] Rechenregeln
> Sind $P_a$ und $P_b$ Potenzreihen, so gilt für die Summe und das Cauchy-Produkt der Reihen: 
> $$
> \rho(P_{a+b}) \ge \min(\rho(P_a), \rho(P_b)) \quad \text{und} \quad \rho(P_{a*b}) \ge \min(\rho(P_a), \rho(P_b))
> $$
> Innerhalb des kleineren Radius dürfen die Reihen gliedweise addiert und multipliziert werden.

---

## 2. Die Exponentialfunktion

> [!Definition] Exponentialfunktion
> Die Exponentialfunktion $\exp: \mathbb{C} \to \mathbb{C}$ ist definiert durch die Reihe:
> $$
> \exp(z) := \sum_{k=0}^{\infty} \frac{z^k}{k!}
> $$
> Diese Reihe hat den Konvergenzradius $\rho = \infty$ (konvergiert für alle $z \in \mathbb{C}$).
> Die Eulersche Zahl ist definiert als $e := \exp(1)$.

### Logarithmus und allgemeine Potenzen

Da die reelle Exponentialfunktion streng monoton wächst und das Bild $\mathbb{R}_{>0}$ hat, ist sie umkehrbar.

> [!Definition] Natürlicher Logarithmus
> Für $y \in \mathbb{R}_{>0}$ ist der natürliche Logarithmus $\ln(y)$ die eindeutige Lösung $x \in \mathbb{R}$ der Gleichung $e^x = y$.
> Es gilt die Funktionalgleichung: $\ln(xy) = \ln x + \ln y$.

> [!Definition] Allgemeine Potenz
> Für $a \in \mathbb{R}_{>0}$ und beliebiges $z \in \mathbb{C}$ definiert man:
> $$
> a^z := e^{z \ln a}.
> $$

---

## 3. Trigonometrische Funktionen

Sinus und Cosinus werden über die komplexe Exponentialfunktion definiert.

> [!Definition] Sinus und Cosinus
> Für $z \in \mathbb{C}$ sind definiert:
> $$
> \sin z := \frac{e^{iz} - e^{-iz}}{2i} \quad \text{und} \quad \cos z := \frac{e^{iz} + e^{-iz}}{2}.
> $$

### Reihendarstellung

Durch Einsetzen der Exponentialreihe erhält man die Potenzreihen für Sinus und Cosinus (beide $\rho = \infty$):

* **Sinus** (nur ungerade Exponenten, alternierend):
    $$ 
    \sin z = \sum_{k=0}^{\infty} \frac{(-1)^k}{(2k+1)!} z^{2k+1} = z - \frac{z^3}{3!} + \frac{z^5}{5!} - \dots.
    $$
* **Cosinus** (nur gerade Exponenten, alternierend):
    $$ 
    \cos z = \sum_{k=0}^{\infty} \frac{(-1)^k}{(2k)!} z^{2k} = 1 - \frac{z^2}{2!} + \frac{z^4}{4!} - \dots.
    $$

### Wichtige Identitäten

* **Trigonometrischer Pythagoras:** $\sin^2 z + \cos^2 z = 1$.
* **Symmetrie:** $\sin(-z) = -\sin z$ (ungerade) und $\cos(-z) = \cos z$ (gerade).
* **Additionstheoreme:**
    * $\sin(z+w) = \sin z \cos w + \cos z \sin w$.
    * $\cos(z+w) = \cos z \cos w - \sin z \sin w$.

---

## 4. Hyperbolische Funktionen

Analog zu den trigonometrischen Funktionen definiert man die hyperbolischen Funktionen ("Kettenlinie"), jedoch ohne den imaginären Faktor im Exponenten.

> [!Definition] Sinh und Cosh
> Für $z \in \mathbb{C}$ gilt:
> $$
> \sinh z := \frac{e^z - e^{-z}}{2} \quad \text{und} \quad \cosh z := \frac{e^z + e^{-z}}{2}.
> $$

> [!Note] Hyperbolischer Pythagoras
> Im Gegensatz zum trigonometrischen Pythagoras gilt hier ein Minuszeichen:
> $$
> \cosh^2 z - \sinh^2 z = 1.
> $$