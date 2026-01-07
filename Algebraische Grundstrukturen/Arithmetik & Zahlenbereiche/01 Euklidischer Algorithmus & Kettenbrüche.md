## 1. Der Euklidische Algorithmus

> [!summary] Ziel
> Der Algorithmus dient dazu, den **größten gemeinsamen Teiler ($\text{ggT}$)** zweier Elemente effizient zu berechnen, ohne die Primfaktorzerlegung kennen zu müssen.

### A) Für ganze Zahlen
Seien $a, b \in \mathbb{N} \setminus \{0\}$. Man führt wiederholte **Division mit Rest** durch. Das Prinzip ist, dass der Teiler zum neuen Dividenden wird und der Rest zum neuen Teiler.

$$
\begin{align*}
a &= q_1 \cdot b + r_1 \\
b &= q_2 \cdot r_1 + r_2 \\
r_1 &= q_3 \cdot r_2 + r_3 \\
&\vdots \\
r_{n-1} &= q_{n+1} \cdot r_n + 0
\end{align*}
$$

> [!check] Ergebnis
> Der **letzte von Null verschiedene Rest** ($r_n$) ist der gesuchte $\text{ggT}(a, b)$.

### B) Der erweiterte Euklidische Algorithmus

Nach dem **Satz von Bézout** lässt sich der $\text{ggT}$ als Linearkombination der Ausgangszahlen darstellen.

> [!important] Satz von Bézout
> Es existieren $r, s \in \mathbb{Z}$, sodass gilt:
> $$\text{ggT}(a, b) = r \cdot a + s \cdot b$$

**Verfahren:**
Dies wird durch **"Rückwärtseinsetzen"** der Gleichungen aus dem normalen Algorithmus erreicht. Man stellt jede Zeile nach dem Rest um und setzt sie schrittweise in die vorherige ein, bis man bei $a$ und $b$ angelangt ist.

---

## 2. Bestimmung von inversen Elementen

Das ist die wichtigste Anwendung für Klausuren (z.B. in der Kryptografie oder Codierungstheorie).

### Problemstellung
Wir befinden uns im Restklassenring $\mathbb{Z}_p$ ($p$ ist Primzahl).
Gesucht ist zu $a \in \mathbb{Z}_p \setminus \{0\}$ ein Element $a'$, sodass:
$$
a' \cdot a \equiv 1 \pmod p
$$

### Das Verfahren (Rezept)

Da $p$ prim ist, gilt $\text{ggT}(a, p) = 1$. Wir nutzen den erweiterten Euklidischen Algorithmus:

1. **Erweiterter Euklid:** Bestimme $r, s \in \mathbb{Z}$ für die Darstellung der 1:
   $$1 = r \cdot p + s \cdot a$$
2. **Modulo anwenden:** Wir betrachten die Gleichung modulo $p$. Da $r \cdot p$ ein Vielfaches von $p$ ist, wird dieser Term zu 0.
   $$1 \equiv 0 + s \cdot a \pmod p$$
3. **Ergebnis:**
   $$s \equiv a^{-1} \pmod p$$
   *Hinweis: Falls $s$ negativ ist, addiere $p$, um den positiven Repräsentanten zu erhalten.*

---

## 3. Der Euklidische Algorithmus für Polynome

Das Verfahren lässt sich analog auf den Polynomring $K[x]$ anwenden.

**Gegeben:** Zwei Polynome $p(x)$ und $q(x)$ mit $\deg(p) \ge \deg(q) \ge 1$.
**Gesucht:** Der $\text{ggT}(p, q)$.

**Ablauf:**
Man führt eine **Polynomdivision** durch:
1. $p(x) : q(x) = k_1(x)$ mit Rest $r_1(x)$.
2. $q(x) : r_1(x) = k_2(x)$ mit Rest $r_2(x)$.
3. ... bis die Division aufgeht (Rest 0).

> [!info] Normierung
> Der $\text{ggT}(p, q)$ ist der letzte von Null verschiedene Rest.
> Da Polynome nur bis auf einen konstanten Faktor eindeutig sind, wird der ggT meist **auf den Leitkoeffizienten 1 normiert** (geteilt durch den Vorfaktor).

---

## 4. Kettenbrüche

Der Euklidische Algorithmus liefert direkt die Koeffizienten für die Kettenbruchdarstellung einer rationalen Zahl.

### Konstruktion
Ein Bruch $\frac{a}{b}$ lässt sich durch die Quotienten $q_i$ (die ganzen Zahlen vor dem Rest) aus dem Euklidischen Algorithmus darstellen:

$$
\frac{a}{b} = q_1 + \cfrac{1}{q_2 + \cfrac{1}{q_3 + \cfrac{1}{\dots}}}
$$

**Schreibweise:**
Um Platz zu sparen, schreibt man oft:
$$[q_1; q_2, q_3, \dots, q_n]$$

### Anwendung: Approximation

Kettenbrüche eignen sich hervorragend, um "krumme" Zahlen (wie $\pi$ oder $\sqrt{2}$) durch einfache Brüche zu approximieren.

**Vorgehen:**
1. Spalte den ganzzahligen Anteil ab.
2. Bilde den Kehrwert des Nachkommateils.
3. Wiederhole den Schritt.

Bricht man das Verfahren frühzeitig ab, erhält man die **bestmögliche Bruch-Approximation** für einen gegebenen Nenner-Bereich.