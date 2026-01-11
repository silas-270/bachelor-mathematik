## 1. Definition der Ableitung

Wir betrachten Funktionen $f: I \to \mathbb{C}$ auf einem Intervall $I \subset \mathbb{R}$.

> [!important] Definition: Differentialquotient
> Eine Funktion $f$ heißt **differenzierbar** an der Stelle $a \in I$, falls der Grenzwert des Differenzenquotienten existiert:
> $$f'(a) := \lim_{x \to a} \frac{f(x) - f(a)}{x - a}$$
> Man nennt $f'(a)$ die **Ableitung** von $f$ bei $a$ .

> [!note] Geometrische Interpretation
> * **Steigung:** $f'(a)$ entspricht der Steigung der Tangente an den Graphen im Punkt $(a, f(a))$.
> * **Wachstum:** $f'(a)$ beschreibt die lokale Änderungsrate (Wachstum/Fall) der Funktion.

**Elementare Beispiele:**
* **Konstante Funktion:** $f(x) = c \implies f'(x) = 0$ .
* **Identität:** $f(x) = x \implies f'(x) = 1$ .

---

## 2. Die Exponentialfunktion

Die Ableitung der Exponentialfunktion ist zentral, da sie sich selbst reproduziert.

> [!example] Ableitung von $\exp$
> Die Funktion $\exp: \mathbb{R} \to \mathbb{R}$ ist überall differenzierbar mit:
> $$
> \exp'(x) = \exp(x) \quad (\text{bzw. } (e^x)' = e^x)
> $$
> *Herleitung:* Basiert auf $\lim_{h \to 0} \frac{e^h - 1}{h} = 1$ .

**Verallgemeinerungen:**
* **Komplexe Exponenten:** Für $s \in \mathbb{C}$ und $f(x) = e^{sx}$ gilt: $f'(x) = s \cdot e^{sx}$ .
* **Allgemeine Basis:** Für $\lambda > 0$ und $f(x) = \lambda^x$ gilt: $f'(x) = \lambda^x \ln \lambda$.

---

## 3. Lineare Approximation (Weierstraß-Form)

Diese äquivalente Charakterisierung ist oft handlicher für theoretische Beweise als der Grenzwert des Bruchs. Sie besagt, dass $f$ lokal "fast linear" ist.

> [!abstract] Lemma: Weierstraß-Darstellung
> $f$ ist genau dann bei $a$ differenzierbar, wenn sich $f(x)$ schreiben lässt als:
> $$f(x) = f(a) + (f'(a) + \rho(x)) (x - a)$$
> wobei $\rho$ eine "Fehlerfunktion" ist mit $\lim_{x \to a} \rho(x) = 0$ .

> [!note] Landau-Symbol (Klein-o)
> Man schreibt dies oft auch mit dem Landau-Symbol $o(|x-a|)$ für den "superlinearen Rest":
> $$f(x) = f(a) + f'(a)(x - a) + \sigma(x) \quad \text{mit} \quad \lim_{x \to a} \frac{\sigma(x)}{x - a} = 0$$
> Das bedeutet, der Fehler $\sigma(x)$ geht *schneller* gegen 0 als der Abstand $x-a$ .

> [!example] Beispiel: Quadratfunktion
> Für $f(x) = x^2$ gilt $f'(a) = 2a$.
> *Beweis per Weierstraß:* $x^2 - a^2 = (x-a)(x+a) = (x-a)(2a + \underbrace{(x-a)}_{\rho(x)})$. Da $\rho(x) \to 0$, ist die Ableitung $2a$ .

---

## 4. Zusammenhang zur Stetigkeit

Differenzierbarkeit ist eine stärkere Eigenschaft als Stetigkeit ("glatte Kurve" vs. "durchgezogene Linie").

> [!important] Satz
> Ist $f$ an einer Stelle $a$ differenzierbar, so ist $f$ dort auch **stetig**.
> $$\text{Differenzierbarkeit} \implies \text{Stetigkeit}.$$

> [!warning] Achtung: Umkehrung gilt nicht!
> Stetige Funktionen sind nicht zwingend differenzierbar.
> **Standard-Gegenbeispiel:** Die Betragsfunktion $f(x) = |x|$ ist bei $0$ stetig ("kein Sprung"), aber **nicht differenzierbar** ("Knick").
> * Der Differenzenquotient divergiert dort (springt zwischen $-1$ und $1$) .
