## 1. Mengenlehre
### Mengenoperationen

Der **Schnitt** von $M$ und $N$:
$$
M \cap N = \{ x : x \in M \land x \in N \}
$$

Die **Vereinigung** von $M$ und $N$:
$$
M \cup N = \{ x : x \in M \lor x \in N \}
$$

Das **relative Komplement** von $N$ in $M$:
$$
M \setminus N = \{ x : x \in M \land x \notin N \}
$$

---

### Eigenschaften von Mengen
* **Disjunkt:** Zwei Mengen $M$ und $N$ heißen disjunkt, falls sie kein einziges Element gemeinsam haben ($M \cap N = \varnothing$).
* **Disjunkte Zerlegung:** Gilt für eine Menge $P$ und zwei Teilmengen $M, N$, dass $P = M \cup N$ mit $M \cap N = \varnothing$, spricht man von einer disjunkten Zerlegung von $P$.

---

## 2. Schranken und Extremwerte
### Maximum und Minimum
Sei $M \subset \mathbb{R}$ eine nichtleere Teilmenge.
* **Minimum:** Eine Zahl $a \in M$ heißt Minimum von $M$, falls $a$ eine untere Schranke von $M$ ist.
* **Maximum:** Eine Zahl $b \in M$ heißt Maximum von $M$, falls $b$ eine obere Schranke von $M$ ist.

### Supremum und Infimum
**Supremumsaxiom:** Jede nach oben beschränkte, nichtleere Teilmenge von $\mathbb{R}$ besitzt ein Supremum in $\mathbb{R}$.

Sei $M \subset \mathbb{R}$ eine nichtleere Teilmenge:
* **Supremum ($\bar{s}$):** Kleinste obere Schranke. $\bar{s}$ ist obere Schranke für $M$ und $\bar{s} \le b$ für alle oberen Schranken $b$.
* **Infimum ($\underline{s}$):** Größte untere Schranke. $\underline{s}$ ist untere Schranke für $M$ und $\underline{s} \ge a$ für alle unteren Schranken $a$.

---

## 3. Topologie von Teilmengen in $\mathbb{R}$
### Beschränktheit
Eine Teilmenge $X \subset \mathbb{R}$ heißt:
* **nach unten beschränkt**, falls gilt: $\exists a \in \mathbb{R} : X \subset [a, \infty)$
* **nach oben beschränkt**, falls gilt: $\exists b \in \mathbb{R} : X \subset (-\infty, b]$
* **beschränkt**, falls $X$ nach oben und unten beschränkt ist.

### Topologische Grundbegriffe
Wir definieren die Epsilon-Umgebung $U_\varepsilon$ um einen Punkt $x \in \mathbb{R}$ als $U_\varepsilon := (x - \varepsilon, x + \varepsilon)$. Eine Teilmenge $X \subset \mathbb{R}$ heißt:

* **offen**, falls gilt: $\forall x \in X \exists \varepsilon > 0 : (x - \varepsilon, x + \varepsilon) \subset X$.
* **abgeschlossen**, falls $\mathbb{R} \setminus X$ offen ist.
* **kompakt**, falls $X$ abgeschlossen und beschränkt ist.

### Innere Punkte, Abschluss und Rand
Für $X \subset \mathbb{R}$ definieren wir:
* **Innere ($\mathring{X}$ oder $\operatorname{int}X$):** $$\mathring{X} = \operatorname{int}X := \{ x \mid x \in \mathbb{R}, \exists \varepsilon > 0 : (x-\varepsilon, x+\varepsilon) \subset X \}$$
* **Abschluss ($\bar{X}$ oder $\operatorname{cl}X$):** $$\bar{X} = \operatorname{cl}X := \mathbb{R} \setminus \operatorname{int}(\mathbb{R} \setminus X)$$
* **Rand ($\partial X$):** $$\partial X := \bar{X} \setminus \mathring{X}$$

---

## 3. Topologie von Teilmengen in $\mathbb{C}$
### Beschränktheit
Eine Teilmenge $X \subset \mathbb{C}$ heißt:
* **beschränkt**, falls es ein $R \in \mathbb{R}_{>0}$ gibt mit $X \subset \mathbb{B}_R(0)$;
(Hinweis: Da $\mathbb{C}$ kein geordneter Körper ist, gibt es hier keine Definition für "nach oben" oder "nach unten" beschränkt.)

### Topologische Grundbegriffe

Für gegebenen Mittelpunkt $\hat{z} \in \mathbb{C}$ und Radius $r \in \mathbb{R}_{>0}$ definieren wir die **(offene) Kreisscheibe** $\mathbb{B}_r := \{z \in \mathbb{C} : |z - \hat{z}| < r \}$.
Eine Teilmenge $X \subset \mathbb{C}$ heißt:

* **($\mathbb{C}$)-offen**, falls zu jedem $z \in X$ ein $\varepsilon > 0$ existiert, so dass $\mathbb{B}_\varepsilon(z) \subset X$;
* **abgeschlossen**, falls $\mathbb{C} \space \backslash \space X$ $\mathbb{C}$-offen ist;
* **kompakt**, falls $X$ abgeschlossen und beschränkt ist.

### Innere Punkte, Abschluss und Rand
Für $X \subset \mathbb{C}$ definieren wir:
* **($\mathbb{C}$)-Innere ($\mathring{X}$ oder $\operatorname{int}X$):** $$
\mathring{X} = \operatorname{int}X := \{ z \in \mathbb{C} \mid \exists \varepsilon > 0 : U_\varepsilon(z) \subset X \}
$$
* **Abschluss ($\bar{X}$ oder $\operatorname{cl}X$):** $$
\bar{X} = \operatorname{cl}X := \mathbb{C} \setminus \operatorname{int}(\mathbb{C} \setminus X)
$$
* **Rand ($\partial X$):** $$
\partial X := \bar{X} \setminus \mathring{X}
$$

## 4. Wichtige Ungleichungen
### Archimedisches Prinzip
Es sei $x \in \mathbb{R}$. Dann gibt es ein $n \in \mathbb{N}$ mit $n > x$.

### Bernoullische Ungleichung
Es seien $x \in \mathbb{R}$ mit $x \ge -1$ und $n \in \mathbb{N}$. Dann gilt:
$$(1+x)^n \ge 1+nx$$

### Dreiecksungleichungen
Es seien $x,y \in \mathbb{R}$. Dann gilt:
1. $|x| \ge 0$, sowie $|x| = 0 \Leftrightarrow x = 0$
2. $|xy| = |x| \cdot |y|$
3. $|x+y| \le |x| + |y|$