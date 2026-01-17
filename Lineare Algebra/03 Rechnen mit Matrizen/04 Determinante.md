## 1. Definition
Die Determinante ist eine Abbildung, die einer quadratischen Matrix einen Skalar aus dem zugrunde liegenden Körper zuordnet. Man kann sie als Funktion der Spaltenvektoren $a_1, \dots, a_n$ auffassen.

> [!important] Definition der Determinante
> Sei $A \in K^{n \times n}$ eine quadratische Matrix über einem Körper $K$. Die Determinante ist definiert als:
> $$\det: \underbrace{K^n \times \dots \times K^n}_{n \text{ Spalten}} \to K, \quad (a_1, \dots, a_n) \mapsto \det(a_1, \dots, a_n)$$


### 2. Die Axiome (Charakterisierung nach Weierstraß)

> [!abstract] 
> Eine Abbildung gilt dann als Determinante, wenn sie die folgenden drei Eigenschaften besitzt:
> 
> 1. Multilinearität
> Die Determinante ist linear in **jeder Spalte**. Für alle $a_i, a_i' \in K^n$ und $\lambda \in K$ gilt:
> - **Additivität:** $$\det(\dots, a_i + a_i', \dots) = \det(\dots, a_i, \dots) + \det(\dots, a_i', \dots)$$
> - **Homogenität:** $$\det(\dots, \lambda \cdot a_i, \dots) = \lambda \cdot \det(\dots, a_i, \dots)$$
>
> 2. Alternierende Eigenschaft (Antisymmetrie)
> Vertauscht man zwei Spalten, ändert sich das Vorzeichen der Determinante:
> $$\det(\dots, a_i, \dots, a_j, \dots) = - \det(\dots, a_j, \dots, a_i, \dots)$$
> **Folge:** Besitzt eine Matrix zwei identische Spalten, ist die Determinante $0$.
>
> 3. Normiertheit
> Die Determinante der Einheitsmatrix $E_n$ ist $1$:
> $$\det(E_n) = \det(e_1, \dots, e_n) = 1$$
> *(Dabei sind $e_k$ die Standard-Einheitsvektoren.)*
> 

### 3. Wichtige Folgerungen für die Berechnung
Aus den Axiomen ergeben sich direkt nützliche Regeln für die Praxis:

| Eigenschaft | Beschreibung |
| :--- | :--- |
| **Lineare Abhängigkeit** | $\det(A) = 0 \iff$ Die Spalten von $A$ sind linear abhängig. |
| **Nullspalten** | Enthält $A$ eine Nullspalte, so ist $\det(A) = 0$. |
| **Transponierte** | Die Determinante bleibt gleich: $\det(A) = \det(A^T)$. |
| **Determinanten-Produktsatz** | $\det(A \cdot B) = \det(A) \cdot \det(B)$. |

---

## Berechnungsmethoden