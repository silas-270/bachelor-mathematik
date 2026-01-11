## 1. Standardmethoden

> [!important] Direkter Beweis
>
> Dies ist der geradlinigste Weg. Man zeigt direkt, dass aus einer Voraussetzung $A$ die Behauptung $B$ folgt.
>
> * **Logik:** $A \implies B$ (Wenn $A$, dann $B$).
>    
> * **Durchführung:**
>    
>    1. Gehe davon aus, dass die Voraussetzung $A$ wahr ist.
>        
>    2. Nutze Definitionen, Rechenregeln und bekannte Sätze.
>        
>    3. Leite in einer logischen Kette die Behauptung $B$ ab.
>        
> * **Beispiel:** Beweisen, dass das Quadrat einer geraden Zahl ebenfalls gerade ist ($n = 2k \implies n^2 = 4k^2 = 2(2k^2)$).
    


> [!important] Beweis durch Kontraposition
>
> Statt direkt $A \implies B$ zu beweisen, beweist man die logisch äquivalente Aussage: "Wenn nicht $B$, dann auch nicht $A$".
> 
> * **Logik:** $\neg B \implies \neg A$ ist äquivalent zu $A \implies B$.
>     
> * **Durchführung:**
>    
>    1. Verneine die Behauptung $B$ (Annahme: $B$ ist falsch).
>        
>    2. Zeige durch logische Schlussfolgerungen, dass dann auch die Voraussetzung $A$ falsch sein muss.
>         
> * **Beispiel:** Um zu zeigen „Wenn $n^2$ ungerade ist, dann ist $n$ ungerade“, zeigt man stattdessen: „Wenn $n$ gerade ist, dann ist $n^2$ gerade“.
    


> [!important] Widerspruchsbeweis
>
> Man nimmt das Gegenteil dessen an, was man beweisen will, und führt dies zu einem logischen Fehler.
> 
> * **Logik:** Wenn $(\neg A)$ zu einem Widerspruch (z. B. $1=0$ oder $x \in M$ und $x \notin M$) führt, muss $A$ wahr sein.
>     
> * **Durchführung:**
>    
>    1. Nimm an, die Behauptung sei falsch.
>        
>    2. Leite daraus mit korrekten Schritten eine Aussage ab, die offensichtlich falsch ist oder der Annahme widerspricht.
>        
>    3. Folgere, dass die Annahme falsch war und die ursprüngliche Behauptung daher wahr sein muss.
>        
> * **Beispiel:** Der Beweis, dass $\sqrt{2}$ irrational ist.
    

## 2. Erweiterungen

> [!abstract] Vollständige Induktion
>
> Diese Methode wird oft für Aussagen verwendet, die für alle natürlichen Zahlen $n$ gelten sollen.
> 
> * **Logik:** Dominoprinzip. Wenn der erste Stein fällt und jeder fallende Stein den nächsten umwirft, fallen alle Steine.
>    
> * **Durchführung:**
>    
>    1. **Induktionsanfang:** Zeige, dass die Aussage für die kleinste Zahl (meist $n=1$ oder $n=0$) stimmt.
>        
>    2. **Induktionsvoraussetzung:** Nimm an, dass die Aussage für eine beliebige Zahl $n$ wahr ist.
>        
>    3. **Induktionsschritt:** Zeige unter Verwendung der Voraussetzung, dass die Aussage dann auch für $n+1$ wahr sein muss.
>        
> * **Beispiel:** Summenformeln (wie die Gaußsche Summenformel).
    


> [!abstract] Fallunterscheidung
>
> Man teilt das Problem in mehrere Teilbereiche auf, die zusammen alle Möglichkeiten abdecken.
>
> * **Logik:** Wenn eine Aussage für jeden möglichen Fall einzeln wahr ist, ist sie insgesamt wahr.
>     
> * **Durchführung:**
>    
>    1. Definiere Fälle (z. B. $x > 0$, $x = 0$ und $x < 0$ oder $n$ ist gerade/ungerade).
>        
>    2. Beweise die Behauptung für jeden dieser Fälle separat.
>        
>    3. Stelle sicher, dass kein möglicher Fall vergessen wurde.        

---

## 2. Zusammenfassung der Logik-Strukturen

|**Methode**|**Ziel-Struktur**|**Vorgehensweise**|
|---|---|---|
|**Direkt**|$A \implies B$|Starte bei $A$, ende bei $B$.|
|**Kontraposition**|$\neg B \implies \neg A$|Starte bei "Nicht $B$", lande bei "Nicht $A$".|
|**Widerspruch**|$\neg A \implies \text{Blitz (Widerspruch)}$|Nimm das Gegenteil an und finde einen Fehler.|
|**Induktion**|$\forall n \in \mathbb{N}: P(n)$|Prüfe $n=1$, dann den Schritt $n \to n+1$.|