### Asymptotická horní mez ($f$ roste nejvýše tak rychle jako $g$)
- Pro libovolné funkce $f, g: \mathbb{N} \rightarrow \mathbb{N}$ znamená zápis $f \in O(g)$ toto:
  $$
(\exists k \in \mathbb{N})(\exists n_{0} \in \mathbb{N})(\forall n \geq n_{0}):f(n) \leq k \ \cdot \ g(n)
  $$

### Asymptotická oboustranná mez ($f$ roste stejně rychle jako $g$)
- Pro libovolné funkce $f, g: \mathbb{N} \rightarrow \mathbb{N}$ zápis $f \in \Theta(g)$ znamená, že $f \in O(g)$ a $g \in O(f)$

### Asymptotická ostrá horní mez ($f$ roste pomaleji než $g$)
- Pro libovolné funkce $f, g: \mathbb{N} \rightarrow \mathbb{N}$ zápis $f \in o(g)$ znamená, že 
  $$
  (\forall k \in \mathbb{N})(\exists n_{0} \in \mathbb{N})(\forall n \geq n_{0}):k \ \cdot \ f(n) < g(n)
  $$

### Základní pojmy pro porovnání růstu funkcí
- $O(g)$ ... **Asymptotická horní mez**
	- používána se pro popis **horního limitu** růstu funkce
	- $O(g(n)) = \{ f(n) \mid (\exists c \in \mathbb{N}) (\exists n_{0} \in \mathbb{N})(\forall n \geq n_{0}): 0 \leq f(n) \leq c \cdot g(n)\}$ 
	- **Asymptotická horní mez funkce $g(n)$** je množina funkcí $f(n)$, takových, že **existuje** přirozené číslo $c > 0$ a existuje přirozené číslo $n_{0}$ tak, že **pro každé** $n \geq n_{0}$ platí $0 \leq f(n) \leq c \cdot g(n)$

- $\Omega(g)$ ... Asymptotická dolní mez
	- $\Omega (g(n)) = \{ f(n) \mid (\exists c \in \mathbb{N})(\exists n_{0} \in \mathbb{N})(\forall n \geq n_{0}: 0 \leq c \cdot g(n) \leq f(n) \}$
	- **Asymptotická dolní mez funkce $g(n)$** je množina funkcí $f(n)$, takových že **existuje** přirození číslo $c > 0$ a **existuje** přirození číslo $n_{0}$ tak, že **pro každé** $n \geq n_{0}$ platí: $0 \leq c \cdot g(n) \leq f(n)$

- $\theta (g)$ ... **Asymptotická oboustranná mez**
	- popisuje těsnější popis chování funkce
	- $\theta (g(n)) = \{f(n) \mid (\exists c_{1} \in \mathbb{N})(\exists c_{2} \in \mathbb{N})(\exists n_{0} \in \mathbb{N})(\forall n \geq n_{0}): 0 \leq c_{1} \cdot g(n) \leq f(n) \leq c_{2} \cdot g(n)\}$
	- **Asymptotická oboustranná mez funkce $g(n)$** je množina funkcí $f(n$, takových, že **existují** přirozená čísla $c_{1} > 0$ a $c_{2} > 0$ a **existuje** přirozené číslo $n_{0}$ tako, že **pro každé** $n \geq n_{0}$ platí: $0 \leq c_{1} \cdot g(n) \leq f(n) \leq c_{2} \cdot g(n)$
	- Věta: $f(n) \in \theta (g(n))$ právě když $f(n) \in O(g(n))$ a $f(n) \in \Omega (g(n))$

- $o(g)$ ... **Asymptotická ostrá horní mez**
	- $o(g(n)) = \{ f(n) \mid (\forall c \in \mathbb{N})(\exists n_{0} \in \mathbb{N})(\forall n \geq n_{0}): 0 < c \cdot f(n) \cdot g(n) \}$
	- **Asymptotická ostrá horní mez funkce $g(n)$** je množina funkcí $f(n)$, takových, že **pro každé** přirozené číslo $c > 0$ **existuje** přirozené číslo $n_{0}$ tak, že **pro každé** $n \geq n_{0}$ platí: $0 < c \cdot f(n) < g(n)$

- $\omega (g)$ ... Asymptotická ostrá dolní mez
	- $\omega (g(n)) = \{ f(n) \mid (\forall c \in \mathbb{N})(\exists n_{0} \in \mathbb{N})(\forall n \geq n_{0}): 0 < g(n) < c \cdot f(n) \}$
	- **Asymptotická ostrá dolní mez funkce $g(n)$** je množina funkcí $f(n)$, takových, že **pro každé** přirozené číslo $c > 0$ **existuje** přirozené číslo $n_{0}$ tak, že **pro každé** $n \geq n_{0}$ platí: $0 < g(n) < c \cdot f(n)$

### Základní pravidla (vlastnosti)
#### Věta o tranzitivitě odhadů
- Pokud $f = O(g)$ a $g = O(h)$, pak $f = O(h)$.
- Pokud $f = \Omega (g)$ a $g = \Omega (h)$, pak $f = \Omega (h)$.
- Pokud $f = \Theta (g)$ a $g = \Theta (h)$, pak $f = \Theta (h)$.
- Pokud $f = o(g)$ a $g = o(h)$, pak $f = o(h)$.
- Pokud $f = \omega (g)$ a $g = \omega (h)$, pak $f = \omega (h)$.

#### Věta o reflexivitě odhadů
- $f = O(f)$.
- $f = \Omega (f)$.
- $f = \Theta (f)$.

#### Věta o symetrii odhadů
- $f = \Theta (g)$ právě když $g = \Theta (f)$.

#### Věta o symetrii horních a dolních odhadů
- $f = O(g)$ právě když $g = \Omega (f)$.
- $f = o(g)$ právě když $g = \omega (f)$.

## Big-O Complexity chart
![[MacBook-2024-04-29-001106@2x.png]]

<iframe width="690" height="385" src="https://www.youtube.com/embed/__vX2sjlpXU?si=E-RiU8rWlfMJvZvC" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

##### Navigace
Předchozí:  [[Algoritmus, problém, časová složitost algoritmu v nejhorším a průměrném případě]]
Následující: [[Lineární datové struktury - seznam, zásobník, fronta]]
Celý okruh: [[1. Teoretické základy informačních technologií]]