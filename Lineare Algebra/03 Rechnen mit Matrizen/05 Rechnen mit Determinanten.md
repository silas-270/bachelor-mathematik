## 1. Die allgemeine Leibniz-Formel
Die Leibniz-Formel definiert die Determinante einer $n \times n$-Matrix $A = (a_{ij})$ über alle möglichen Permutationen:

$$\det(A) = \sum_{\pi \in S_n} \operatorname{sgn}(\pi) \prod_{i=1}^n a_{i, \pi(i)}$$

> [!important] Definitionen
> * **$S_n$**: Die symmetrische Gruppe (Menge aller Permutationen von $\{1, \dots, n\}$).
> * **$\pi$**: Eine Permutation, die der Zeile $i$ die Spalte $\pi(i)$ zuordnet.
> * **$\operatorname{sgn}(\pi)$**: Das Signum (Vorzeichen) der Permutation.

**Zeitkomplexität & Anwendungsfall:**
* **Komplexität:** $\mathcal{O}(n \cdot n!)$ – Da es $n!$ Permutationen gibt, wächst der Aufwand extrem schnell.
* **Anwendung:** Fast ausschließlich für theoretische Beweise und Definitionen in der linearen Algebra geeignet. Für praktische Berechnungen ab $n > 3$ unbrauchbar.

---

## 2. Spezialfälle für kleine Matrizen

### Determinante für $2 \times 2$-Matrizen
Die Berechnung erfolgt über das "Über-Kreuz-Multiplizieren":
$$\det \begin{pmatrix} a & b \\ c & d \end{pmatrix} = ad - bc$$

**Zeitkomplexität & Anwendungsfall:**
* **Komplexität:** $\mathcal{O}(1)$ – Konstante Anzahl an Operationen.
* **Anwendung:** Standardverfahren für alle $2 \times 2$ Matrizen.

### Regel von Sarrus ($3 \times 3$)
Die Determinante wird durch die Summe der Produkte der Hauptdiagonalen abzüglich der Produkte der Nebendiagonalen berechnet.



$$\det(A) = a_{11}a_{22}a_{33} + a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32} - a_{13}a_{22}a_{31} - a_{11}a_{23}a_{32} - a_{12}a_{21}a_{33}$$

**Zeitkomplexität & Anwendungsfall:**
* **Komplexität:** $\mathcal{O}(1)$ (feste Anzahl an Multiplikationen).
* **Anwendung:** Nur für $3 \times 3$ Matrizen gültig! Ideal für Klausuren und manuelle Berechnungen kleiner Systeme.

---

## 3. Strukturelle Vereinfachungen

### Dreiecksmatrizen
Für eine obere oder untere Dreiecksmatrix (alle Einträge unter/über der Hauptdiagonale sind $0$) gilt:
$$\det(A) = \prod_{i=1}^n a_{ii}$$

**Zeitkomplexität & Anwendungsfall:**
* **Komplexität:** $\mathcal{O}(n)$.
* **Anwendung:** Extrem effizient, wenn die Matrix bereits in Dreiecksform vorliegt oder durch den Gauß-Algorithmus dorthin transformiert wurde.

### Blockmatrizen
Matrizen in Blockgestalt können zerlegt werden:
$$\det \begin{pmatrix} A & B \\ 0 & D \end{pmatrix} = \det(A) \cdot \det(D)$$

**Zeitkomplexität & Anwendungsfall:**
* **Komplexität:** Abhängig von der Größe der Teilblöcke, reduziert das Problem aber massiv.
* **Anwendung:** Große, dünnbesetzte Matrizen oder partitionierte Systeme.

---

## 4. Berechnungsverfahren für große Matrizen

### Gauß-Elimination (Algorithmus)
Durch elementare Zeilenumformungen wird die Matrix auf Dreiecksgestalt gebracht.

> [!tip] Regeln bei Umformungen
> 1. **Zeilentausch:** Das Vorzeichen der Determinante dreht sich um ($\times -1$).
> 2. **Addition eines Vielfachen:** Der Wert der Determinante bleibt **unverändert**.
> 3. **Skalierung einer Zeile:** Die Determinante skaliert mit demselben Faktor.

**Zeitkomplexität & Anwendungsfall:**
* **Komplexität:** $\mathcal{O}(n^3)$.
* **Anwendung:** Der **Standardweg** für Computerberechnungen und große, volle Matrizen ohne viele Nullen.

### Laplace'scher Entwicklungssatz
Die rekursive Reduktion der Dimension durch Entwicklung nach einer Zeile oder Spalte.

$$\det(A) = \sum_{j=1}^n (-1)^{i+j} \cdot a_{ij} \cdot \det(A_{ij})$$

> [!important] Strategie
> Entwickle immer nach der Zeile oder Spalte mit den **meisten Nullen**, um die Anzahl der Unterdeterminanten zu minimieren.

**Zeitkomplexität & Anwendungsfall:**
* **Komplexität:** $\mathcal{O}(n!)$ im Worst-Case.
* **Anwendung:** Manuelle Berechnung von Matrizen (bis ca. $4 \times 4$ oder $5 \times 5$), die **viele Nulleinträge** enthalten.

---

## 5. Wichtige Eigenschaften im Überblick

* **Transpositionsinvarianz:** $\det(A) = \det(A^T)$. Zeilen und Spalten sind gleichwertig.
* **Determinante & Invertierbarkeit:** Eine Matrix $A$ ist invertierbar $\iff \det(A) \neq 0$.
* **Multiplikationssatz:** $\det(A \cdot B) = \det(A) \cdot \det(B)$.

### Gruppenhomomorphismus
Die Abbildung
$$\det: GL(n, K) \to K^\times, \quad A \mapsto \det(A)$$
ist ein **Gruppenhomomorphismus** von der Gruppe der invertierbaren Matrizen in die multiplikative Gruppe des Körpers $K^\times = K \setminus \{0\}$. Es gilt:
1. $\det(AB) = \det(A)\det(B)$ (Homomorphieeigenschaft).
2. $\det(I_n) = 1$ (Neutrales Element wird auf neutrales Element abgebildet).
3. $\det(A^{-1}) = (\det(A))^{-1}$ (Inverses wird auf Inverses abgebildet).