## 1. Rechenregeln für Summen und Produkte

> [!abstract] Produkt und Summenoperator
> Für $m \cdot n$ gegebene Zahlen $x_{jk} \in \mathbb{R}$ mit einem Doppelindex, wobei $j \in \{ 1, \dots, m \}$, $k \in \{ 1, \dots, n \}$, hat man
> $$\begin{aligned} 
> \sum_{j=1}^{m} \sum_{k=1}^{n} x_{jk} = \sum_{k=1}^{n} \sum_{j=1}^{m} x_{jk}, \\
> prod_{j=1}^{m} \prod_{k=1}^{n} x_{jk} = \prod_{k=1}^{n} \prod_{j=1}^{m} x_{jk}.
> \end{aligned}$$
> 
> Aus dem Distributivgesetz erhält man außerdem
> 
> $$\left( \sum_{j=1}^{m} x_j \right) \cdot \left( \sum_{k=1}^{n} y_k \right) = \sum_{j=1}^{m} \sum_{k=1}^{n} x_j y_k.$$

> [!abstract] Der Binomische Lehrsatz
>
> Es seien $n \in \mathbb{N}$ und $x, y \in \mathbb{R}$. Dann gilt:
>
> $$(x+y)^n = \sum_{k=0}^{n} \binom{n}{k} x^{n-k} y^k.$$

## 2. Wichtige Ungleichungen

> [!abstract] Bernoullische Ungleichung
> 
> Es seien $x \in \mathbb{R}$ mit $x \ge -1$ und $n \in \mathbb{N}$. Dann gilt
> 
> $$(1+x)^n \ge 1 + nx.$$


> [!abstract] Dreiecksungleichungen
> 
> Seien $x,y \in \mathbb{R}$. Dann gilt:
> 
> * $|x+y| \le |x| + |y| \text,$
> * $|a-b| \ge ||a|-|b||.$


> [!abstract] Archimedisches Prinzip
> 
> Es sei $x \in \mathbb{R}$. Dann gibt es ein $n \in \mathbb{N}$ mit $n > x$.