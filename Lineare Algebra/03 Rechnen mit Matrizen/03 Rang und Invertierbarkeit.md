## 1. Invertierbarkeit und Lineare Abbildungen

Wir betrachten ausschließlich quadratische Matrizen ($n \times n$), die eine Abbildung von $K^n$ nach $K^n$ definieren.

> [!important] Definition: Invertierbarkeit
> Eine Matrix $A$ heißt **invertierbar**, wenn die durch sie definierte lineare Abbildung bijektiv ist. Dies ist äquivalent zu folgenden Aussagen:
> * Das Bild der Abbildung ist der volle Raum $K^n$.
> * Der Kern der Abbildung besteht nur aus dem Nullvektor ($\text{Ker}(A) = \{0\}$).
> * Die Spalten von $A$ sind linear unabhängig (bilden eine Basis).

> [!abstract] Satz: Linearität der Umkehrabbildung
> Ist eine lineare Abbildung bijektiv, so ist ihre Umkehrabbildung ebenfalls eine **lineare** Abbildung.

Die darstellende Matrix dieser Umkehrabbildung nennt man die **Inverse** von $A$, bezeichnet als $A^{-1}$.

---

## 2. Die Allgemeine Lineare Gruppe

Die Menge der invertierbaren Matrizen besitzt eine spezielle algebraische Struktur.

> [!important] Definition: $GL(n, K)$
> Die Menge aller invertierbaren $n \times n$-Matrizen über dem Körper $K$ wird als **Allgemeine Lineare Gruppe** (General Linear Group) bezeichnet:
> $$GL(n, K) = \{ A \in K^{n \times n} \mid A \text{ ist invertierbar} \}$$

> [!abstract] Satz: Gruppenstruktur von $GL(n, K)$
> Die Menge $GL(n, K)$ bildet mit der Matrizenmultiplikation als Verknüpfung eine **Gruppe**. Es gelten folgende Eigenschaften:
> * **Abgeschlossenheit:** Das Produkt zweier Bijektionen ist wieder eine Bijektion.
> * **Neutrales Element:** Die Einheitsmatrix $E_n$ (bzw. $I_n$).
> * **Inverses Element:** Existiert per Definition für alle $A \in GL(n, K)$.
> * **Assoziativität:** Gilt für Matrizenmultiplikation allgemein.

> [!tip] Intuition: Links- und Rechtsinverse
> Aufgrund der Gruppenstruktur ist ein rechtsinverses Element automatisch auch linksinvers. Es gilt:
> $$A \cdot A^{-1} = E_n \iff A^{-1} \cdot A = E_n$$
> Es genügt daher, eine der beiden Eigenschaften zu zeigen oder zu berechnen.

---

## 3. Berechnung der Inversen

### Theoretischer Ansatz
Die Berechnung der Inversen entspricht dem Lösen von $n$ linearen Gleichungssystemen der Form $A x_i = e_i$, wobei $e_i$ die Einheitsvektoren sind. Die Lösungsvektoren $x_1, \dots, x_n$ bilden die Spalten der inversen Matrix $A^{-1}$.

### Praktischer Algorithmus (Gauß-Jordan)
Um die Inverse effizient zu berechnen, nutzt man elementare Zeilenumformungen. Jede Zeilenumformung entspricht der Multiplikation mit einer Elementarmatrix $S_k$.

**Verfahren:**
1. Schreibe die Matrix $A$ und die Einheitsmatrix $E_n$ nebeneinander: 
   $$(A \mid E_n)$$
2. Wende elementare Zeilenumformungen auf die gesamte erweiterte Matrix an, um $A$ in die Einheitsmatrix zu überführen.
3. Wenn links die Einheitsmatrix steht, steht rechts die gesuchte Inverse:
   $$(A \mid E_n) \xrightarrow{\text{Zeilenumformungen}} (E_n \mid A^{-1})$$

---

## 4. Anwendung: Lösen von LGS

Die Inverse kann genutzt werden, um lineare Gleichungssysteme der Form $Ax = b$ zu lösen.

> [!abstract] Lösungsformel mittels Inverser
> Ist $A$ invertierbar, so ist die eindeutige Lösung des Systems $Ax = b$ gegeben durch:
> $$x = A^{-1} b$$

> [!tip] Praxis-Hinweis
> Dieses Verfahren lohnt sich besonders dann, wenn man **viele** Gleichungssysteme mit **derselben** Matrix $A$, aber unterschiedlichen Vektoren $b$ lösen muss, da $A^{-1}$ nur einmal berechnet werden muss.

---

## 5. Der Rang einer Matrix

In dieser Vorlesung wird das Konzept des Rangs eingeführt, welches als Kennzahl dient, um den Grad der Degeneriertheit einer Matrix zu beschreiben. Dabei wird die Matrix $A$ ($m \times n$) sowohl aus der Perspektive ihrer Spalten als auch ihrer Zeilen betrachtet.

### Definitionen

> [!tip] Intuition
> Der Rang ist eine natürliche Zahl, die angibt, wie "degeneriert" eine Matrix ist. Je mehr lineare Abhängigkeiten vorhanden sind, desto kleiner ist diese Zahl.

> [!important] Definition: Spaltenrang und Zeilenrang
> Sei $A$ eine Matrix.
> * **Spaltenrang:** Die maximale Anzahl linear unabhängiger Spalten von $A$. Dies entspricht der Dimension des von den Spalten aufgespannten Raums (Spann des Spaltenraums).
> * **Zeilenrang:** Die maximale Anzahl linear unabhängiger Zeilen von $A$. Dies entspricht der Dimension des von den Zeilenvektoren aufgespannten Raums.

### Hauptsatz zum Rang

Obwohl Spalten- und Zeilenrang zunächst unterschiedliche Konzepte zu sein scheinen, sind sie identisch.

> [!abstract] Satz: Gleichheit von Zeilen- und Spaltenrang
> Für jede Matrix $A$ gilt:
> $$\text{Zeilenrang}(A) = \text{Spaltenrang}(A)$$
> Aufgrund dieser Gleichheit spricht man nur noch vom **Rang** der Matrix $A$.
>
> Es gilt zudem der Zusammenhang zur linearen Abbildung $F_A$:
> $$\text{Rang}(A) = \dim(\text{Bild}(F_A))$$

### Berechnung des Rangs

Der Rang lässt sich algorithmisch mittels des Gauß-Verfahrens bestimmen.

* Wird eine Matrix $A$ durch den Gauß-Algorithmus auf **Zeilenstufenform** gebracht, so ändert sich ihr Rang nicht.
* Der Rang der Matrix entspricht genau der **Anzahl der Nicht-Null-Zeilen** in der Zeilenstufenform.

---

## 6. Äquivalenzen für invertierbare Matrizen

Für quadratische $n \times n$-Matrizen erweitern sich die Kriterien für Invertierbarkeit (bzw. Bijektivität der zugehörigen Abbildung $F_A$) durch den Rang-Begriff erheblich.

Folgende Aussagen sind für eine quadratische Matrix $A$ äquivalent:

* $A$ ist invertierbar.
* Die Abbildung $F_A$ ist eine Bijektion.
* $\text{Bild}(F_A) = K^n$.
* $\text{Kern}(F_A) = \{0\}$.
* $\text{Rang}(A) = n$ (Die Matrix hat vollen Rang).
* Die Spalten von $A$ sind linear unabhängig (bilden eine Basis des $K^n$).
* Die Zeilen von $A$ sind linear unabhängig (bilden eine Basis des $K^n$).
* Das lineare Gleichungssystem $Ax = b$ ist eindeutig lösbar.
* $\det(A) \neq 0$ (Ausblick auf Lineare Algebra II).