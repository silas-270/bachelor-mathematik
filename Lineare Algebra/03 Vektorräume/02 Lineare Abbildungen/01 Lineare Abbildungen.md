## 1. Lineare Abbildungen

Der Übergang von abstrakten Vektorräumen zu konkreten Strukturen wird durch lineare Abbildungen realisiert. Diese sind strukturverträgliche Abbildungen zwischen Vektorräumen.

### Definition und Grundeigenschaften

> [!important] Definition: Lineare Abbildung
> Seien $V$ und $W$ Vektorräume über demselben Körper $\mathbb{K}$ (bzw. $K$). Eine Abbildung $f: V \to W$ heißt **lineare Abbildung** (oder Vektorraum-Homomorphismus), wenn zwei Bedingungen erfüllt sind:
> 1. **Additivität:** Für alle $\vec{v}, \vec{w} \in V$ gilt:
>    $$f(\vec{v} + \vec{w}) = f(\vec{v}) + f(\vec{w})$$
> 2. **Homogenität:** Für alle $\vec{v} \in V$ und $\lambda \in \mathbb{K}$ gilt:
>    $$f(\lambda \cdot \vec{v}) = \lambda \cdot f(\vec{v})$$

> [!tip] Intuition
> Eine lineare Abbildung ist "struktur-erhaltend". Geometrisch kann man sich das Koordinatensystem als Gitter vorstellen: Die lineare Abbildung verzerrt dieses Gitter, wobei der Ursprung fix bleibt und Gitterlinien parallel und im gleichen Abstand bleiben.

### Rechenregeln und Eigenschaften

Ist $f: V \to W$ eine lineare Abbildung, dann gelten folgende Regeln:

* **Nullvektor:** $f(\vec{0}_V) = \vec{0}_W$ (Der Nullvektor wird stets auf den Nullvektor abgebildet).
* **Subtraktion:** $f(\vec{v} - \vec{w}) = f(\vec{v}) - f(\vec{w})$.
* **Linearität bei Linearkombinationen:**
    $$f(\lambda_1 \vec{v}_1 + \dots + \lambda_n \vec{v}_n) = \lambda_1 f(\vec{v}_1) + \dots + \lambda_n f(\vec{v}_n)$$
* **Komposition:** Die Hintereinanderausführung zweier linearer Abbildungen ist wieder linear.

### Überprüfung auf Linearität

Um "Nicht-Linearität" zu zeigen, reicht es, eine der Bedingungen zu widerlegen.

> [!tip] Schnelltest (Notwendige Bedingung)
> Wenn $f(\vec{0}_V) \neq \vec{0}_W$ gilt, dann ist $f$ **nicht** linear.
> *Hinweis:* Die Umkehrung gilt nicht zwingend (d.h. $f(\vec{0}_V) = \vec{0}_W$ ist kein Beweis für Linearität).

---

## 2. Basen und Bestimmung von Abbildungen

Eine der fundamentalsten Eigenschaften linearer Abbildungen ist, dass sie durch ihr Verhalten auf einer Basis vollständig festgelegt sind.

> [!tip] Notation von Basen
> Basen werden oft in runden Klammern (Tupel) notiert (z.B. $B = (\vec{b}_{1},...,\vec{b}_{n})$), da die Reihenfolge der Vektoren für die Koordinatendarstellung entscheidend ist.

### Existenz- und Eindeutigkeitssatz

Sei $(\vec{v}_1, \dots, \vec{v}_n)$ eine Basis von $V$.

* **Eindeutigkeit:** Eine lineare Abbildung $f: V \to W$ ist durch die Bilder der Basisvektoren $f(\vec{v}_1), \dots, f(\vec{v}_n)$ **eindeutig** bestimmt. Für einen beliebigen Vektor $\vec{v} = \sum_{i=1}^n \lambda_i \vec{v}_i$ berechnet sich das Bild als:
    $$f(\vec{v}) = \lambda_1 f(\vec{v}_1) + \dots + \lambda_n f(\vec{v}_n)$$
* **Existenz:** Zu jeder beliebigen Wahl von Vektoren $\vec{w}_1, \dots, \vec{w}_n \in W$ existiert eine lineare Abbildung $f: V \to W$ mit $f(\vec{v}_i) = \vec{w}_i$.

---

## 3. Isomorphismen

Strukturgleiche Vektorräume werden durch Isomorphismen beschrieben.

> [!important] Definition: Isomorphismus
> Zwei Vektorräume $V$ und $W$ heißen **isomorph** ($V \cong W$), wenn es eine lineare Abbildung $f: V \to W$ gibt, die **bijektiv** ist.

Ein Isomorphismus fungiert als "Wörterbuch", das die Vektoren 1-zu-1 übersetzt, wobei die mathematische Struktur vollständig erhalten bleibt. Die Isomorphie ist eine Äquivalenzrelation (Reflexivität, Symmetrie, Transitivität).

> [!abstract] Klassifikation endlich-dimensionaler Vektorräume
> Zwei endlich-dimensionale $K$-Vektorräume sind genau dann isomorph, wenn sie dieselbe Dimension besitzen. Bis auf Isomorphie gibt es für festes $K$ und $n$ nur einen einzigen Vektorraum, nämlich $K^n$.

---

## 4. Von Basen zu Koordinaten

Betrachtet wird ein $K$-Vektorraum $V$ der Dimension $n$ mit einer Basis $B=(\vec{b}_{1},...,\vec{b}_{n})$. Jeder Vektor $\vec{v} \in V$ lässt sich eindeutig als Linearkombination darstellen:
$$\vec{v} = \sum_{i=1}^{n} \lambda_i \vec{b}_i$$

### Koordinatenabbildung

> [!important] Definition: Koordinatenabbildung $\Phi_{B}$
> Die Abbildung, die einem Vektor $\vec{v}$ seine eindeutigen Koeffizienten (Koordinaten) bezüglich der Basis $B$ zuordnet, heißt **Koordinatenabbildung**:
>
> $$\Phi_{B}: V \rightarrow K^{n}, \quad \vec{v} \mapsto \begin{pmatrix} \lambda_{1} \\ \vdots \\ \lambda_{n} \end{pmatrix}$$

> [!abstract] Satz: Isomorphie von $V$ und $K^n$
> Die Koordinatenabbildung $\Phi_{B}$ ist **linear** und **bijektiv**, also ein Isomorphismus zwischen dem Vektorraum $V$ und dem Koordinatenraum $K^n$.

### Die Kanonische Basis im $K^n$

Im Standardraum $K^n$ existiert die **Kanonische Basis (Standardbasis)** $(e_1, \dots, e_n)$, wobei $e_i$ an der $i$-ten Stelle eine $1$ und sonst nur Nullen hat.
*Besonderheit:* Bezüglich der kanonischen Basis stimmen die Komponenten eines Vektors mit seinen Koordinaten überein. Die Koordinatenabbildung ist hier die Identität.

