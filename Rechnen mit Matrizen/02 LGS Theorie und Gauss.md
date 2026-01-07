## 1. Grundlegende Struktur und Sichtweisen

Wir betrachten lineare Gleichungssysteme (LGS) über einem Körper $K$. Statt der klassischen Zeilen-Schreibweise wird in der Linearen Algebra primär die Matrix-Vektor-Schreibweise verwendet.

> [!important] Definition: Matrix-Form eines LGS
> Ein lineares Gleichungssystem mit $m$ Gleichungen und $n$ Unbekannten wird geschrieben als:
> $$A \cdot x = b$$
> * $A \in K^{m \times n}$ (Koeffizientenmatrix)
> * $x \in K^n$ (Vektor der Unbekannten)
> * $b \in K^m$ (Ergebnisvektor / Inhomogenität)

### Interpretation als Lineare Abbildung
Das LGS kann mittels der zur Matrix $A$ gehörigen linearen Abbildung $f_A: K^n \to K^m$ mit $x \mapsto Ax$ interpretiert werden.

> [!tip] Intuition
> Die Lösungsmenge des LGS ist die Menge aller Urbilder von $b$ unter der Abbildung $f_A$:
> $$L = \{x \in K^n \mid f_A(x) = b\} = f_A^{-1}(\{b\})$$

---

## 2. Homogene LGS

Ein System der Form $A \cdot \vec{v} = \vec{0}$.

> [!important] Definition
> Die Lösung eines homogenen LGS ist der **Kern** der durch die Matrix $A$ gegebenen linearen Abbildung $f_A$.

### Lösungsmenge
Ein homogenes LGS besitzt entweder:
* **Genau eine Lösung:** Nur die triviale Lösung $\vec{0}$ (wenn der Kern trivial ist).
* **Unendlich viele Lösungen:** Alle Vektoren im Untervektorraum $\text{Kern}(f)$.

---

## 3. Inhomogene LGS

Betrachtet wird ein LGS der Form $A \cdot \vec{v} = \vec{b}$ mit $\vec{b} \neq \vec{0}$.

> [!abstract] Struktur der Lösung
> Die allgemeine Lösung eines inhomogenen LGS setzt sich zusammen aus einer **Speziallösung** $\vec{v}_1$ und der **Lösung des zugehörigen homogenen LGS** (dem Kern).
> $$\text{Lösung}_{\text{inhomogen}} = \vec{v}_1 + \text{Kern}(f_A)$$

> [!tip] Intuition zur Lösungsmenge
> Eine "komplette" Nebenklasse $\vec{v} + \text{Kern}(f_A)$ wird auf dasselbe Element im Bild abgebildet.

### Lösbarkeitskriterien
Die Anzahl der Lösungen hängt von $\vec{b}$ und dem Kern ab:
1. **Keine Lösung:** Wenn $\vec{b} \notin \text{Bild}(f_A)$.
2. **Genau eine Lösung:** Wenn $\vec{b} \in \text{Bild}(f_A)$ **und** $\text{Kern}(f_A) = \{0\}$.
3. **Unendlich viele Lösungen:** Wenn $\vec{b} \in \text{Bild}(f_A)$ **und** $\text{Kern}(f_A) \neq \{0\}$.

### Theoretische Zusammenhänge
Folgende Sätze aus der Theorie linearer Abbildungen sind für das Verständnis der Lösungsstruktur essenziell:

> [!abstract] Lemma zur Eindeutigkeit
> Seien $x, y$ zwei Lösungen des Systems $Ax=b$. Dann gilt für deren Differenz:
> $$x - y \in \text{Ker}(f_A)$$

> [!abstract] Dimensionsformel
> $$\dim(\text{Ker}(f_A)) + \dim(\text{Bild}(f_A)) = n$$
> (wobei $n$ die Anzahl der Spalten / Variablen ist).

---

## 4. Quadratische Matrizen ($n \times n$)

Für quadratische Matrizen $A \in \mathbb{K}^{n \times n}$ und die zugehörige Abbildung $f_A: \mathbb{K}^n \to \mathbb{K}^n$ gelten besondere Eigenschaften.

> [!abstract] Satz: Äquivalenzen der Bijektivität
> Folgende Aussagen sind äquivalent:
> * $f_A$ ist bijektiv.
> * $\text{Bild}(f_A) = \mathbb{K}^n$.
> * Die Spalten der Matrix bilden eine Basis (sind linear unabhängig).
> * $\dim(\text{Bild}(f_A)) = n$.
> * $\text{Kern}(f_A) = \{\vec{0}\}$.

### Matrix-Multiplikation
Die Nacheinanderausführung von Abbildungen entspricht der Matrix-Multiplikation:
$$f_B(f_A(\vec{x})) = (B \cdot A) \cdot \vec{x}$$

---

## 5. Der Gauß-Algorithmus und Elementarmatrizen

Der Gauß-Algorithmus nutzt elementare Zeilenoperationen, um eine Matrix in eine spezifische Form zu bringen, an der die Lösung abgelesen werden kann. Diese prozeduralen Operationen können algebraisch als Multiplikation mit **Elementarmatrizen** aufgefasst werden.

### Zeilenstufenform (ZSF)

> [!important] Definition: Zeilenstufenform
> Eine Matrix befindet sich in ZSF, wenn jede Zeile mehr führende Nullen aufweist als die vorhergehende Zeile.
> * Die ersten Elemente einer Zeile, die ungleich Null sind (Pivots), bilden eine "Treppenstufe".
> * Unterhalb dieser Pivots stehen nur Nullen.

> [!abstract] Satz: Existenz der Zeilenstufenform
> Jede Matrix lässt sich durch elementare Zeilenoperationen in eine Zeilenstufenform bringen.

**Verfahren:**
1. Finde die erste Spalte mit einem Eintrag ungleich Null.
2. Bringe diesen Eintrag durch Zeilenvertauschung (falls nötig) nach oben.
3. Eliminiere alle Einträge unterhalb dieses Pivots durch Addition passender Vielfacher der ersten Zeile.
4. Wiederhole das Verfahren rekursiv für die verbleibende Untermatrix.

### Elementarmatrizen

Es gibt drei Typen von Elementarmatrizen, die den erlaubten Zeilenumformungen entsprechen. Sie entstehen durch Anwendung der jeweiligen Operation auf die Einheitsmatrix.

| Typ | Operation | Matrix-Beschreibung |
| :--- | :--- | :--- |
| **$S_1$ (Addition)** | Addition des $\lambda$-fachen der Zeile $j$ zur Zeile $i$. | Einheitsmatrix mit zusätzlichem Eintrag $\lambda$ an Position $(j, i)$. |
| **$S_2$ (Skalierung)** | Multiplikation einer Zeile $i$ mit Skalar $\lambda \neq 0$. | Einheitsmatrix, bei der ein Diagonalelement durch $\lambda$ ersetzt wurde. |
| **$S_3$ (Vertauschung)** | Vertauschen zweier Zeilen. | Einheitsmatrix, bei der zwei Zeilen vertauscht wurden. |

> [!abstract] Satz: Zeilenoperationen als Matrixmultiplikation
> Das Anwenden einer Zeilenoperation auf eine Matrix $A$ entspricht der Multiplikation mit der zugehörigen Elementarmatrix $S$ von **links**:
> $$A \to S \cdot A$$

> [!tip] Intuition & Invertierbarkeit
> Diese Operationen entsprechen dem Anwenden einer bijektiven Abbildung auf beiden Seiten der Gleichung $Ax = b$.
> * Alle Elementarmatrizen sind **invertierbar** (bijektiv).
> * Da die Multiplikation mit einer invertierbaren Matrix umkehrbar ist, bleibt der Informationsgehalt und damit der Lösungsraum identisch.