## 1. Stetige Funktionen auf kompakten Mengen

Stetige Funktionen verhalten sich auf kompakten Mengen (in $\mathbb{R}$: abgeschlossen & beschränkt) besonders gut. Dies beruht auf einer zentralen topologischen Eigenschaft.

> [!abstract] Lemma: Bild kompakter Mengen
> Eine stetige Funktion $f: X \to Y$ bildet kompakte Mengen $A \subset X$ in kompakte Mengen $f(A) \subset Y$ ab.

> [!important] Satz vom Minimum und Maximum
> Sei $f: X \to \mathbb{R}$ stetig und $A \subset X$ **kompakt**.
> Dann nimmt $f$ auf $A$ ein globales Maximum und ein globales Minimum an .
> $$\exists x_{\min}, x_{\max} \in A : f(x_{\min}) \le f(x) \le f(x_{\max}) \quad \forall x \in A$$

> [!example] Gegenbeispiel (ohne Kompaktheit)
> $f(x) = \frac{x^2}{1+x^2}$ auf $\mathbb{R}$ (nicht kompakt) besitzt zwar ein Minimum (0), aber **kein** Maximum (nähert sich 1, erreicht es aber nie).

---

## 2. Der Zwischenwertsatz (ZWS)

Der ZWS besagt anschaulich, dass eine stetige Funktion keine Werte "überspringen" kann.

> [!important] Zwischenwertsatz
> Sei $f: [\alpha, \beta] \to \mathbb{R}$ stetig mit $f(\alpha) < f(\beta)$.
> Dann existiert für jeden Wert $y \in (f(\alpha), f(\beta))$ ein $x_y \in [\alpha, \beta]$ mit $f(x_y) = y$.

### Anwendungen des ZWS
1. **Umkehrfunktionen:** Eine stetige, streng monotone Funktion $f: [\alpha, \beta] \to [\xi, \eta]$ ist bijektiv. Die Umkehrfunktion $f^{-1}$ ist **ebenfalls stetig** und streng monoton .
2. **Arcus Sinus:** Einschränkung von $\sin$ auf $[-\frac{\pi}{2}, \frac{\pi}{2}]$ ist bijektiv $\implies$ Existenz von $\arcsin$ .
3. **Polarkoordinaten:** Zu jedem $z \in \mathbb{C}\setminus\{0\}$ existieren eindeutige $r > 0, \phi \in (-\pi, \pi]$ mit $z = r e^{i\phi}$.
4. **Nullstellen:**
 * $\cos(0)=1 > 0$ und $\cos(2) \le -1/3 < 0 \implies \exists$ Nullstelle in $(0,2)$ (Existenz von $\pi$) .
 * $\exp(0)=1$ und $\exp(y) \ge 1+y \implies$ Surjektivität von $\exp$ auf $\mathbb{R}_{>1}$ .

---

## 3. Funktionenfolgen

Betrachtet wird eine Folge von Funktionen $(f_n)_{n \in \mathbb{N}}$ mit $f_n: X \to Y$. Die Art der Konvergenz entscheidet darüber, ob Eigenschaften wie Stetigkeit erhalten bleiben.

### Punktweise vs. Gleichmäßige Konvergenz

> [!definition] Punktweise Konvergenz
> $f_n \to f_*$ punktweise, falls für jedes **fixe** $x$ gilt: $\lim_{n \to \infty} f_n(x) = f_*(x)$.
> * **Quantoren:** $\forall x \in X \; \forall \varepsilon > 0 \; \exists N \in \mathbb{N} \dots$ ($N$ hängt von $x$ ab!).

> [!definition] Gleichmäßige Konvergenz
> $f_n \to f_*$ gleichmäßig, falls der Abstand global klein wird:
> $$\forall \varepsilon > 0 \; \exists N \in \mathbb{N} \; \forall n > N \; \forall x \in X : |f_n(x) - f_*(x)| < \varepsilon$$
> * **Wichtig:** $N$ hängt **nicht** von $x$ ab ("gleichmäßig" für alle $x$) .

> [!warning] Warn-Beispiel (Punktweise reicht nicht!)
> Sei $f_n(x) = x^n$ auf $[0, 1]$.
> * $f_n$ konvergiert punktweise gegen die unstetige Funktion $f_*(x) = \begin{cases} 0 & x < 1 \\ 1 & x = 1 \end{cases}$.
> * Die Konvergenz ist **nicht** gleichmäßig .

### Stetigkeitssatz

> [!important] Satz
> Konvergiert eine Folge **stetiger** Funktionen $f_n$ **gleichmäßig** gegen $f_*$, so ist die Grenzfunktion $f_*$ **stetig**.
> *Implikation:* Ist $f_*$ unstetig (siehe Beispiel $x^n$), kann die Konvergenz nicht gleichmäßig gewesen sein.

### Anwendung: Potenzreihen
Potenzreihen $P_a(z) = \sum a_k z^k$ sind im Inneren ihres Konvergenzkreises stetig.
* **Grund:** Die Partialsummen (Polynome) konvergieren auf jeder kleineren Kreisscheibe $\mathbb{B}_r$ ($r < \rho$) **gleichmäßig** gegen die Potenzreihe .
* Daher sind $\exp, \sin, \cos$ etc. überall stetig.
