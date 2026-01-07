## 1. Spann von Vektoren

### Definitionen

> [!important] Definition: Linearkombination
> Seien $v_1, \dots, v_k$ Vektoren eines Vektorraums $V$. Ein Vektor $u$ heißt **Linearkombination** dieser Vektoren, wenn er sich in der Form
> $$u = \sum_{i=1}^{k} \lambda_i v_i$$
> darstellen lässt, wobei $\lambda_i$ Skalare aus dem zugrunde liegenden Körper sind.

> [!important] Definition: Spann (Erzeugnis)
> Der **Spann** einer Familie von Vektoren $(v_1, \dots, v_k)$, oft notiert als $\text{span}(v_1, \dots, v_k)$ oder $\langle v_1, \dots, v_k \rangle$, ist die Menge aller möglichen Linearkombinationen dieser Vektoren[cite: 203].
> $$\text{span}(v_1, \dots, v_k) = \{ \lambda_1 v_1 + \dots + \lambda_k v_k \mid \lambda_i \in K \}$$

### Eigenschaften

> [!abstract] Satz: Spann als Untervektorraum
> Der Spann einer Familie von Vektoren aus $V$ ist ein **Untervektorraum** von $V$. Es ist der *kleinste* Untervektorraum, der die Vektoren $v_1, \dots, v_k$ enthält.

> [!tip] Intuition
> Man kann sich den Spann als die Menge aller Vektoren vorstellen, die man durch Addition und Skalarmultiplikation aus der ursprünglichen Liste "erzeugen" kann.

---

## 2. Lineare Unabhängigkeit

### Definitionen

> [!important] Definition: Lineare Unabhängigkeit
> Eine Familie von Vektoren $(v_1, \dots, v_k)$ heißt **linear unabhängig**, wenn der Nullvektor $0$ nur auf die triviale Weise als Linearkombination dargestellt werden kann.
> Das heißt:
> $$\sum_{i=1}^{k} \lambda_i v_i = 0 \implies \lambda_1 = \dots = \lambda_k = 0$$

> [!important] Definition: Lineare Abhängigkeit
> Ist die Familie nicht linear unabhängig (d.h. es gibt eine Linearkombination der Null, bei der nicht alle $\lambda_i$ null sind), so heißt sie **linear abhängig**.

### Sätze und Kriterien

> [!abstract] Satz: Nullvektor und Duplikate
> * Enthält eine Familie den Nullvektor, ist sie automatisch linear abhängig.
>* Enthält eine Familie denselben Vektor mehrfach, ist sie automatisch linear abhängig.

> [!abstract] Satz: Eindeutigkeit der Darstellung
> Eine Familie $(v_1, \dots, v_k)$ ist genau dann **linear unabhängig**, wenn sich jeder Vektor im Spann dieser Familie **eindeutig** als Linearkombination darstellen lässt.

> [!abstract] Satz: Charakterisierung linearer Abhängigkeit
> Folgende Aussagen sind für eine Familie $(v_1, \dots, v_k)$ äquivalent:
> 1. Die Familie ist linear abhängig.
> 2. Es gibt einen Index $i$, sodass sich der Spann nicht ändert, wenn man $v_i$ weglässt:
>    $$\text{span}(v_1, \dots, v_k) = \text{span}(v_1, \dots, \hat{v}_i, \dots, v_k)$$
> 3. Es gibt einen Index $i$, sodass $v_i$ im Spann der restlichen Vektoren liegt ($v_i$ ist Linearkombination der anderen).

---

## 3. Basen

### Definitionen

> [!important] Definition: Basis
> Eine Familie von Vektoren $B = (v_1, \dots, v_k)$ ist eine **Basis** eines Vektorraums (oder Unterraums) $U$, wenn zwei Bedingungen erfüllt sind:
> 1. $B$ ist ein **Erzeugendensystem** von $U$ (d.h. $\text{span}(B) = U$).
> 2. $B$ ist **linear unabhängig**.

> [!tip] Intuition
> Eine Basis ist eine "ökonomische" Beschreibung eines Raums: Man hat genügend Vektoren, um alles zu erreichen (Erzeugendensystem), aber keine überflüssigen Vektoren (linear unabhängig).

### Sätze

> [!abstract] Satz: Äquivalente Charakterisierungen einer Basis
> Sei $V$ ein endlich erzeugter Vektorraum und $B = (v_1, \dots, v_k)$ eine Liste von Vektoren aus $V$. Folgende Aussagen sind äquivalent:
> 1. $B$ ist eine **Basis** von $V$.
> 2. $B$ ist ein **unverkürzbares Erzeugendensystem** (Nimmt man einen Vektor weg, ist es kein Erzeugendensystem mehr).
> 3. Jeder Vektor $v \in V$ lässt sich **eindeutig** als Linearkombination der Vektoren in $B$ darstellen.
> 4. $B$ ist **unverlängerbar linear unabhängig** (Fügt man irgendeinen Vektor hinzu, wird die Menge linear abhängig).

> [!abstract] Satz: Existenz von Basen
> Jeder endlich erzeugte Vektorraum besitzt eine Basis.

> [!abstract] Satz: Dimension (Vorgriff)
> Alle Basen eines endlich erzeugten Vektorraums haben die exakt gleiche Anzahl an Elementen. Diese Anzahl nennt man die **Dimension** des Vektorraums.

### Algorithmus

**Algorithmus zur Basisauswahl (Reduktionsverfahren)**
Gegeben sei ein endliches Erzeugendensystem (Spann) $B = (v_1, \dots, v_k)$ eines Vektorraums $V$.

1. **Prüfung:** Ist die Liste $B$ linear unabhängig?
   * **Ja:** $B$ ist eine Basis. STOP.
   * **Nein:** Gehe zu Schritt 2.
1. **Reduktion:** Da die Liste linear abhängig ist, ist sie verkürzbar. Wähle einen Vektor $v_i$, der Linearkombination der anderen ist (oder der den Spann nicht ändert), und entferne ihn aus der Liste.
2. **Iteration:** Wiederhole Schritt 1 mit der verkürzten Liste.
   * Da die Liste endlich ist, terminiert der Algorithmus spätestens bei der leeren Menge oder einer Basis.