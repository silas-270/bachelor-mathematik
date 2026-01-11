## 1. Definition und Konvergenzradius

> [!important] Definition: Potenzreihe
> Sei $(a_k)_{k \in \mathbb{N}}$ eine komplexe Folge. Die Reihe
> $$P_a(z) = \sum_{k=0}^{\infty} a_k z^k$$
> heißt **Potenzreihe** mit Entwicklungspunkt $0$ (allgemeiner: $\sum a_k (z-z_0)^k$).

### Der Konvergenzradius
Potenzreihen konvergieren auf einer Kreisscheibe. Der **Konvergenzradius** $\rho$ ist definiert als:
$$\rho := \sup \{ |z| \in \mathbb{R}_{\ge 0} \mid \sum a_k z^k \text{ konvergiert} \}$$

> [!abstract] Satz (Konvergenzverhalten)
> Sei $\rho$ der Konvergenzradius. Dann gilt:
> 1.  $|z| < \rho \implies$ **absolute Konvergenz**.
> 2.  $|z| > \rho \implies$ **Divergenz**.
> 3.  $|z| = \rho \implies$ **Keine allgemeine Aussage** (Randverhalten muss individuell geprüft werden!).

> [!example] Beispiel: Randverhalten ($\rho = 1$)
> Betrachtet man $\sum_{k=1}^{\infty} \frac{z^k}{k}$ (Radius $\rho=1$):
> * Für $z=1$ divergiert sie (harmonische Reihe).
> * Für $z=-1$ konvergiert sie (alternierende harmonische Reihe).

### Berechnung von $\rho$

> [!tip] Formel von Cauchy-Hadamard (Immer anwendbar)
> $$\rho = \frac{1}{\limsup_{k \to \infty} \sqrt[k]{|a_k|}}$$
> *(Konvention: $1/0 = \infty, 1/\infty = 0$)*.

> [!tip] Formel von Euler (Falls Grenzwert existiert)
> Falls der Grenzwert existiert, gilt einfacher:
> $$\rho = \lim_{k \to \infty} \left| \frac{a_k}{a_{k+1}} \right|$$
> *(Achtung: Kehrwert des Quotientenkriteriums!)*

> [!tip] Rechenregeln
> Sind $P_a$ und $P_b$ Potenzreihen, so gilt für die Summe und das Cauchy-Produkt der Reihen: 
> $$\rho(P_{a+b}) \ge \min(\rho(P_a), \rho(P_b)) \quad \text{und} \quad \rho(P_{a*b}) \ge \min(\rho(P_a), \rho(P_b))$$
> Innerhalb des kleineren Radius dürfen die Reihen gliedweise addiert und multipliziert werden.

---

## 2. Die Exponentialfunktion

Die Exponentialfunktion wird über ihre Potenzreihe definiert, da diese überall konvergiert ($\rho = \infty$).

> [!important] Definition & Eigenschaften
> $$\exp(z) := \sum_{k=0}^{\infty} \frac{z^k}{k!}$$
> * **Funktionalgleichung:** $\exp(z+w) = \exp(z) \cdot \exp(w)$.
> * **Periodizität:** $\exp(z + 2\pi i) = \exp(z)$.
> * **Eulersche Zahl:** $e := \exp(1)$.

### Logarithmus und Potenzen
Da $\exp: \mathbb{R} \to \mathbb{R}_{>0}$ streng monoton wachsend und bijektiv ist, existiert die Umkehrfunktion.
* **Natürlicher Logarithmus:** $\ln: \mathbb{R}_{>0} \to \mathbb{R}$ ist die Umkehrfunktion von $\exp|_{\mathbb{R}}$.
* **Allgemeine Potenz:** Für $a > 0$ und $z \in \mathbb{C}$ definiert man:
    $$a^z := \exp(z \cdot \ln a) = e^{z \ln a}$$

---

## 3. Trigonometrische Funktionen

Sinus und Cosinus werden analytisch über den Real- und Imaginärteil der komplexen Exponentialfunktion definiert.

> [!important] Definitionen
> $$\sin z := \frac{e^{iz} - e^{-iz}}{2i} \quad \text{und} \quad \cos z := \frac{e^{iz} + e^{-iz}}{2}$$
>
> **Eulersche Formel:**
> $$e^{iz} = \cos z + i \sin z$$

### Reihendarstellungen
* **Sinus** (ungerade Potenzen): $\sin z = z - \frac{z^3}{3!} + \frac{z^5}{5!} - \dots$
* **Cosinus** (gerade Potenzen): $\cos z = 1 - \frac{z^2}{2!} + \frac{z^4}{4!} - \dots$

### Analytische Definition von $\pi$
In der Analysis wird $\pi$ nicht geometrisch definiert, sondern über Nullstellen:
> [!abstract] Satz
> Der Cosinus besitzt im Intervall $(0, 2)$ genau eine Nullstelle $\hat{x}$.
> Wir definieren **Pi** als das Doppelte dieser Nullstelle:
> $$\pi := 2 \cdot \hat{x}$$
> Damit gilt: $\cos(\frac{\pi}{2}) = 0$ und $\sin(\frac{\pi}{2}) = 1$.

### Wichtige Identitäten
* **Trigonometrischer Pythagoras:** $\sin^2 z + \cos^2 z = 1$.
* **Additionstheoreme:**
    * $\sin(z+w) = \sin z \cos w + \cos z \sin w$
    * $\cos(z+w) = \cos z \cos w - \sin z \sin w$

---

## 4. Hyperbolische Funktionen

Das "reelle Gegenstück" zu den trigonometrischen Funktionen (ohne $i$).

> [!important] Definitionen
> $$\sinh z := \frac{e^z - e^{-z}}{2} \quad \text{und} \quad \cosh z := \frac{e^z + e^{-z}}{2}$$
>
> **Hyperbolischer Pythagoras:**
> $$\cosh^2 z - \sinh^2 z = 1$$
> *(Man beachte das Minuszeichen!)*