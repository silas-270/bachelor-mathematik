## 4. Darstellungen und Umrechnungen in $\mathbb{C}$

### Die Eulersche Formel
Die zentrale Brücke zwischen der trigonometrischen Darstellung und der Exponentialform ist die **Eulersche Formel**:
$$
e^{i\varphi} = \cos(\varphi) + i \sin(\varphi)
$$

---

### Darstellungsformen im Überblick

Eine komplexe Zahl $z \in \mathbb{C}$ kann auf drei Arten beschrieben werden:

1. **Kartesische Form (Normalform):**
   $$z = a + bi$$
   (mit Realteil $a = \operatorname{Re}(z)$ und Imaginärteil $b = \operatorname{Im}(z)$)

2. **Trigonometrische Form:**
   $$z = r \cdot (\cos \varphi + i \sin \varphi)$$

3. **Exponentialform (Polarform):**
   $$z = r \cdot e^{i\varphi}$$
   (mit Betrag $r = |z|$ und Argument/Winkel $\varphi = \arg(z)$)

---

### Umrechnungsregeln

#### Von Kartesisch $(a, b)$ zu Polar $(r, \varphi)$
* **Betrag:**
  $$r = \sqrt{a^2 + b^2}$$
* **Winkel (Argument):**
  $$\varphi = \operatorname{atan2}(b, a) = 
  \begin{cases} 
  \arctan(\frac{b}{a}) & \text{falls } a > 0 \\
  \arctan(\frac{b}{a}) + \pi & \text{falls } a < 0, b \ge 0 \\
  \arctan(\frac{b}{a}) - \pi & \text{falls } a < 0, b < 0 
  \end{cases}$$

#### Von Polar $(r, \varphi)$ zu Kartesisch $(a, b)$
* **Realteil:**
  $$a = r \cdot \cos(\varphi)$$
* **Imaginärteil:**
  $$b = r \cdot \sin(\varphi)$$

---

### Rechnen in Polarform
Die Exponentialform eignet sich besonders gut für Multiplikation und Potenzieren:
* **Multiplikation:** $z_1 \cdot z_2 = (r_1 \cdot r_2) \cdot e^{i(\varphi_1 + \varphi_2)}$
* **Potenzieren (Satz von de Moivre):** $z^n = r^n \cdot e^{in\varphi} = r^n (\cos(n\varphi) + i \sin(n\varphi))$