## 1. Matrix-Darstellung linearer Abbildungen

Zwischen linearen Abbildungen (auf endlich-dimensionalen Räumen) und Matrizen besteht ein direkter Zusammenhang. Jede lineare Abbildung $f: K^n \to K^m$ lässt sich als Matrix-Vektor-Multiplikation schreiben.

### Konstruktion der Darstellungsmatrix

Wie findet man die Matrix zu einer Abbildung?

> [!important] Die Goldene Regel der Matrix-Konstruktion
> **Die Spalten der Matrix sind die Bilder der Basisvektoren.**
>
> Sei $f: V \to W$ linear und seien $(\vec{v}_1, \dots, \vec{v}_n)$ die Basisvektoren von $V$. Die Darstellungsmatrix $A$ entsteht, indem man die Bilder $f(\vec{v}_i)$ als Spalten in die Matrix schreibt:
> $$A = \begin{pmatrix} | & & | \\ f(\vec{v}_1) & \dots & f(\vec{v}_n) \\ | & & | \end{pmatrix}$$

### Das Kommutative Diagramm

Für abstrakte Vektorräume $V$ (Basis $B$) und $W$ (Basis $B'$) lässt sich eine lineare Abbildung $F: V \to W$ durch eine Matrix $A$ im Koordinatenraum darstellen. Es gilt:
$$A = \Phi_{B'} \circ F \circ \Phi_B^{-1}$$

Das bedeutet:
1.  Übersetze Vektor aus $V$ in Koordinaten ($K^n$).
2.  Berechne im $K^n$ mittels Matrix $A$.
3.  Übersetze das Ergebnis zurück in den Vektorraum $W$ (oder interpretiere es als Koordinaten bzgl. $B'$).

---

## 2. Geometrische Transformationen

Die Matrix-Darstellung erlaubt eine geometrische Interpretation, insbesondere im $\mathbb{R}^2$ und $\mathbb{R}^3$.

### Wichtige Transformationen im $\mathbb{R}^2$

* **Drehung (Ursprung):** Eine Drehung um den Winkel $\alpha$ wird durch die Drehmatrix beschrieben:
    $$R_\alpha = \begin{pmatrix} \cos \alpha & -\sin \alpha \\ \sin \alpha & \cos \alpha \end{pmatrix}$$
    * 1. Spalte: Bild von $\vec{e}_1$ ist $(\cos \alpha, \sin \alpha)^T$.
    * 2. Spalte: Bild von $\vec{e}_2$ ist $(-\sin \alpha, \cos \alpha)^T$.

### Rotationen im $\mathbb{R}^3$

Im 3D-Raum werden Rotationen durch Blockmatrizen dargestellt, wobei die Rotationsachse unverändert bleibt (1 auf der Diagonalen, Nullen in Zeile/Spalte).
* *Beispiel Z-Achse:* Der $2\times2$-Rotationsblock steht oben links.

---

## 4. Koordinatentransformation (Basiswechsel)

Bei einem Basiswechsel betrachtet man einen Vektorraum $V$ mit zwei Basen $A$ (alt) und $B$ (neu). Gesucht ist eine Matrix zur Umrechnung der Koordinaten.

### Transformationsmatrix

Die Matrix ${}_B M_A(id)$ (oft auch $U$ genannt) transformiert Koordinaten bezüglich Basis $A$ in Koordinaten bezüglich Basis $B$. Sie ist die Darstellungsmatrix der Identitätsabbildung.

> [!important] Algorithmus zur Konstruktion
> Um von Basis $A=(\vec{a}_1, ..., \vec{a}_n)$ zu Basis $B$ zu wechseln:
> 1.  Stelle jeden Vektor der *alten* Basis $A$ als Linearkombination der *neuen* Basis $B$ dar.
> 2.  Die Koeffizienten bilden die **Spalten** der Transformationsmatrix.

### Verknüpfung und Inverse

* **Inverse Transformation:** Der Wechsel von $B$ zurück nach $A$ entspricht der inversen Matrix: $({}_B M_A(id))^{-1} = {}_A M_B(id)$.
* **Produkt:** Hin- und Rücktransformation ergeben die Identität:
    $${}_A M_B(id) \cdot {}_B M_A(id) = E_n$$

> [!tip] Interpretation
> Man interpretiert Vektoren links durch die "Brille" der Basis $A$ und rechts durch die "Brille" der Basis $B$.