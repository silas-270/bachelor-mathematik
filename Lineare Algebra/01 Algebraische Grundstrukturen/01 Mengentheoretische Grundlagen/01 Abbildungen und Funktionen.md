Sei $f: A \to B$ eine Funktion, die Elemente aus der Definitionsmenge $A$ auf die Zielmenge $B$ abbildet.

## 1. Injektivität (Linkseindeutigkeit)

> [!abstract] Definition: Injektivität
> 
> Eine Funktion $f: A \to B$ heißt injektiv, wenn verschiedene Elemente aus $A$ niemals auf dasselbe Element in $B$ abgebildet werden.
> 
> Formal:
> 
> $$\forall a_1, a_2 \in A: f(a_1) = f(a_2) \implies a_1 = a_2$$
> 
> Kontraposition (oft einfacher für Beweise):
> 
> $$a_1 \neq a_2 \implies f(a_1) \neq f(a_2)$$

> [!tip] Anschauung & Merkmale
> 
> - **Pfeil-Logik:** Bei jedem Element in $B$ kommt **höchstens ein** Pfeil an.
>     
> - **Graphen-Test:** Jede horizontale Gerade schneidet den Funktionsgraphen **höchstens einmal**.
>     
> - **Gleichung:** Die Gleichung $f(x) = y$ hat für jedes $y$ entweder **keine** oder **eine** Lösung.
>     
> - **Mächtigkeit:** Dies ist nur möglich, wenn $|A| \le |B|$ (für endliche Mengen).
>     

---

## 2. Surjektivität (Rechtstotalität)

> [!abstract] Definition: Surjektivität
> 
> Eine Funktion $f: A \to B$ heißt surjektiv, wenn jedes Element der Zielmenge $B$ mindestens einmal als Funktionswert vorkommt. Die Bildmenge ist gleich der Zielmenge ($f(A) = B$).
> 
> Formal:
> 
> $$\forall b \in B \ \exists a \in A: f(a) = b$$

> [!tip] Anschauung & Merkmale
> 
> - **Pfeil-Logik:** Bei jedem Element in $B$ kommt **mindestens ein** Pfeil an (kein Element in $B$ bleibt "leer").
>     
> - **Graphen-Test:** Jede horizontale Gerade schneidet den Funktionsgraphen **mindestens einmal** (vorausgesetzt die Gerade liegt im Wertebereich $B$).
>     
> - **Gleichung:** Die Gleichung $f(x) = y$ ist für jedes $y \in B$ **lösbar**.
>     
> - **Mächtigkeit:** Dies ist nur möglich, wenn $|A| \ge |B|$ (für endliche Mengen).
>     

---

## 3. Bijektivität (Eineindeutigkeit)

> [!abstract] Definition: Bijektivität
> 
> Eine Funktion heißt bijektiv, wenn sie sowohl injektiv als auch surjektiv ist. Sie stellt eine 1-zu-1-Korrespondenz zwischen den Mengen her.
> 
> Merkmal: Für jedes $b \in B$ existiert **genau ein** $a \in A$ mit $f(a) = b$.

> [!example] Wichtigste Konsequenz: Umkehrbarkeit
> 
> Genau dann, wenn $f$ bijektiv ist, existiert eine Umkehrfunktion (Inverse) $f^{-1}: B \to A$.
> 
> - Es gilt: $f^{-1}(f(a)) = a$ und $f(f^{-1}(b)) = b$.
>     
> - **Mächtigkeit:** Für endliche Mengen gilt zwingend $|A| = |B|$.
>     

---

## Zusammenfassung / Spickzettel

|**Eigenschaft**|**"Pfeil"-Logik (Zielmenge B)**|**Gleichung f(x)=y**|**Mächtigkeit (endlich)**|
|---|---|---|---|
|**Injektiv**|Max. 1 Pfeil pro $b$|0 oder 1 Lösung|$|
|**Surjektiv**|Min. 1 Pfeil pro $b$|$\ge$ 1 Lösung|$|
|**Bijektiv**|Genau 1 Pfeil pro $b$|Genau 1 Lösung|$|