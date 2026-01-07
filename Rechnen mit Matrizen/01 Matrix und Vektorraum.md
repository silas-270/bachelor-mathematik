## 1. Lineare Abbildungen als Matrizen

Lineare Abbildungen zwischen endlichdimensionalen Räumen ($K^n \to K^m$) lassen sich effizient durch Matrizen darstellen.

* **Korrespondenz:** Eine Abbildung von $K^n$ (Eingabe) nach $K^m$ (Ausgabe) entspricht einer Matrix $A$ mit $m$ Zeilen und $n$ Spalten ($m \times n$-Matrix).
* **Anwendung:** Die Abbildung wird operativ als Matrix-Vektor-Multiplikation geschrieben: $w = A \cdot v$.

---

## 2. Matrix-Vektor-Multiplikation

### Algorithmus (Zeile mal Spalte)
Sei $A \in K^{m \times n}$ und $v \in K^n$. Der Ergebnisvektor $w \in K^m$ berechnet sich komponentenweise. Für den $j$-ten Eintrag gilt:

$$w_j = \sum_{i=1}^n A_{ji} \cdot v_i$$

* **Vorgehen:** Man multipliziert die Einträge der entsprechenden **Zeile** der Matrix paarweise mit den Einträgen des **Vektors** und summiert die Ergebnisse auf.

### Bild der Einheitsvektoren
Ein fundamentales Konzept zum Verständnis linearer Abbildungen.

> [!abstract] Satz: Spalten als Bilder
> Sei $e_i$ der $i$-te Einheitsvektor (Eintrag 1 an Stelle $i$, sonst 0).
> Das Produkt einer Matrix $A$ mit dem Einheitsvektor $e_i$ ergibt exakt die $i$-te Spalte der Matrix $A$.
>
> $$A \cdot e_i = \text{i-te Spalte von A}$$
>
> **Interpretation:** Die Spalten der Matrix sind die Bilder der Einheitsvektoren unter der zugehörigen linearen Abbildung.

---

## 3. Matrixmultiplikation

Die Multiplikation von zwei Matrizen modelliert die **Hintereinanderausführung (Komposition)** von linearen Abbildungen.

> [!tip] Intuition
> Seien $f_A: K^n \to K^m$ und $f_B: K^r \to K^n$ lineare Abbildungen (Matrizen $A$ und $B$).
> Die Komposition $f_A \circ f_B$ entspricht der Matrixmultiplikation $A \cdot B$.
>
> $$(m \times n) \cdot (n \times r) \to (m \times r)$$

> [!important] Definition: Matrixmultiplikation
> Das Produkt einer Matrix $A$ ($m$ Zeilen, $n$ Spalten) und einer Matrix $B$ ($n$ Zeilen, $r$ Spalten) ergibt eine Matrix $C = A \cdot B$ mit $m$ Zeilen und $r$ Spalten.
>
> **Berechnungsverfahren:**
> 1.  **Spaltenbild (Konzeptionell):** Die Spalten der Ergebnismatrix sind die Bilder der Spalten von $B$ unter der Matrix $A$. Man multipliziert $A$ mit jeder einzelnen Spalte von $B$.
> 2.  **Zeile mal Spalte (Rechnerisch):** Der Eintrag $c_{ij}$ ist das Skalarprodukt der $i$-ten Zeile von $A$ mit der $j$-ten Spalte von $B$.

---

## 4. Vektorraumstruktur von Matrizen

Matrizen gleicher Größe bilden selbst einen Vektorraum.

> [!important] Definition: Matrixaddition
> Seien $A, B \in K^{m \times n}$. Die Summe $A+B$ ist die komponentenweise Addition der Einträge.
> * **Voraussetzung:** Die Matrizen müssen exakt die gleiche Form (Zeilen- und Spaltenanzahl) haben.

> [!abstract] Satz: Vektorraum der Matrizen
> Die Menge der Matrizen mit $m$ Zeilen und $n$ Spalten bildet einen Vektorraum der Dimension $m \cdot n$.
> * Schreibweise: $K^{m \times n}$.

---

## 5. Zusammenfassung der Rechenregeln

Für die oben definierten Operationen (Addition und Multiplikation) gelten folgende Gesetze, sofern die Dimensionen kompatibel sind:

* **Assoziativität:** $(A \cdot B) \cdot C = A \cdot (B \cdot C)$ (gilt auch für die Addition).
* **Distributivität:** $A \cdot (B + C) = A \cdot B + A \cdot C$.
* **Inverse des Produkts:** $(A \cdot B)^{-1} = B^{-1} \cdot A^{-1}$ (Reihenfolge kehrt sich um!).

> [!failure] Warnung: Keine Kommutativität
> Die Matrixmultiplikation ist im Allgemeinen **nicht** kommutativ.
>
> $$A \cdot B \neq B \cdot A$$
>
> Dies ist der entscheidende Unterschied zum Rechnen mit reellen Zahlen.

---

## 6. Transposition

> [!important] Definition: Transponierte Matrix
> Die Transposition $A^T$ entsteht durch das Vertauschen von Zeilen und Spalten.
> * Aus einer $n \times m$-Matrix wird eine $m \times n$-Matrix.
> * Der $k$-te Spaltenvektor von $A$ wird zum $k$-ten Zeilenvektor von $A^T$.

> [!abstract] Rechenregeln der Transposition
> * **Doppelte Transposition:** $(A^T)^T = A$
> * **Transposition eines Produkts:** $(A \cdot B)^T = B^T \cdot A^T$ (Reihenfolge kehrt sich um!)

---

## 7. Quadratische Matrizen und Invertierbarkeit

Für quadratische Matrizen ($n \times n$) – also Matrizen mit gleicher Anzahl an Zeilen und Spalten – gelten besondere algebraische Strukturen.

> [!important] Definition: Einheitsmatrix $I_n$
> Eine Matrix mit Einsen auf der Hauptdiagonalen und Nullen sonst. Sie ist das neutrale Element der Multiplikation.
>
> $$A \cdot I = A \quad \text{und} \quad I \cdot A = A$$

> [!important] Definition: Allgemeine Lineare Gruppe ($GL(n, K)$)
> Die Menge der invertierbaren $n \times n$-Matrizen bildet bezüglich der Multiplikation eine Gruppe, genannt *General Linear Group*.
> * **Inverses Element:** Wenn die zugehörige Abbildung bijektiv ist, existiert eine Inverse $A^{-1}$, sodass $A \cdot A^{-1} = I$.