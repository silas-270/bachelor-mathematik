## 1. Kern und Bild linearer Abbildungen

### Definitionen

> [!important] Definition: Kern und Bild
> Seien $V, W$ zwei $K$-Vektorräume und $f: V \to W$ eine lineare Abbildung.
> * **Bild von $f$ ($\text{Im}(f)$):** Die Menge aller Vektoren in $W$, auf die abgebildet wird.
>   $$\text{Bild}(f) = \{ f(v) \in W \mid v \in V \} \subseteq W$$
>   *Alternativ:* $\{\vec{w} \in W \mid \exists \vec{v} \in V: f(\vec{v}) = \vec{w}\}$
> * **Kern von $f$ ($\text{Ker}(f)$):** Die Menge aller Vektoren in $V$, die auf den Nullvektor in $W$ abgebildet werden.
>   $$\text{Kern}(f) = \{ v \in V \mid f(v) = 0_W \} \subseteq V$$

### Eigenschaften und Struktur

> [!abstract] Satz: Unterraum-Eigenschaft
> * $\text{Kern}(f)$ ist ein **Untervektorraum** von $V$.
> * $\text{Bild}(f)$ ist ein **Untervektorraum** von $W$.

> [!tip] Intuition: Zusammenhang zu Gleichungssystemen
> * Der **Kern** entspricht der Lösungsmenge des homogenen linearen Gleichungssystems $Ax = 0$.
> * Das **Bild** entspricht der Menge der Vektoren $b$, für die das Gleichungssystem $Ax = b$ lösbar ist.

> [!abstract] Hilfssatz (Lemma)
> Für zwei Vektoren $v, w \in V$ gilt:
> $$f(v) = f(w) \iff v - w \in \text{Kern}(f)$$
> *Dies impliziert, dass Vektoren mit demselben Bild sich nur um ein Element aus dem Kern unterscheiden.*

#### Zusammenhang mit Injektivität und Surjektivität

Aus der Vorlesung ergeben sich wichtige Kriterien zur Überprüfung der Eigenschaften von Abbildungen :

* **Surjektivität:** $f$ ist surjektiv $\iff \text{Bild}(f) = W$ .
    *(Das bedeutet, jeder Vektor in $W$ wird getroffen).*
* **Injektivität:** $f$ ist injektiv $\iff \text{Kern}(f) = \{ 0_V \}$ .

## 2. Der Dimensionssatz

Dieser Satz verknüpft die Dimensionen von Definitionsbereich, Kern und Bild und ist zentral für die Lineare Algebra.

> [!abstract] Dimensionssatz (Rang-Satz)
> Sei $V$ ein **endlich erzeugter** $K$-Vektorraum und $f: V \to W$ eine lineare Abbildung. Dann gilt:
> $$\dim(V) = \dim(\text{Kern}(f)) + \dim(\text{Bild}(f))$$

> [!tip] Interpretation
> Die Dimension des ursprünglichen Raums $V$ teilt sich auf. Wichtig ist: Die Summe ergibt $\dim(V)$, **nicht** zwingend $\dim(W)$.

#### Spezialfall: Endomorphismen ($V \to V$)

Ist $V$ ein endlicher Vektorraum und $f: V \to V$ eine lineare Abbildung (Definitions- und Zielbereich identisch), gilt folgende Äquivalenz :

$$f \text{ injektiv} \iff f \text{ surjektiv}$$

*Begründung:* Ist $f$ surjektiv, gilt $\dim(\text{Bild}(f)) = \dim(V)$. Nach dem Dimensionssatz muss dann $\dim(\text{Kern}(f)) = 0$ sein, also ist der Kern $\{0_V\}$ und $f$ somit injektiv.

### Bestimmung von Kern und Bild (Algorithmus & Beispiele)

Gegeben sei eine lineare Abbildung $f: K^n \to K^m$, dargestellt durch eine Matrix $A \in K^{m \times n}$.

* **Bestimmung des Bildes ($\text{Bild}(f)$):**
	* Das Bild ist der **Spann der Spaltenvektoren** der Matrix $A$.
	* *Verfahren:* Schreibe die Spalten von $A$ in eine Matrix und bringe sie in Stufenform, um eine Basis aus den linear unabhängigen Spalten zu identifizieren.
* **Bestimmung des Kerns ($\text{Kern}(f)$):**
	* Der Kern ist der **Lösungsraum** des homogenen Gleichungssystems $A x = 0$.
	* *Verfahren:* Löse das LGS $Ax=0$. Die Basisvektoren des Lösungsraums bilden die Basis des Kerns.