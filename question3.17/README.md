# Билет №3.17. Неравенство Маркова.

<!-- **Краткое определение:** бла-бла-бла    -->
<!-- **Длинное определение:** бла-бла-бла -->

## Основные термины и обозначения

- $\Omega$  — произвольное непустое множество, элементы которого называются элементарными событиями;  
- $\sigma$ — сигма-алгебра подмножеств ${\displaystyle \Omega }$ , называемых (случайными) событиями;  
- ${\displaystyle \mathbb {P} }$  — вероятностная мера или вероятность, такая что ${\displaystyle \mathbb {P} (\Omega )=1}$.

## Введение в билет

## Неравенство Маркова
Пусть дано вероятностное пространство $(F, \sigma, \Omega)$ 
и случайная величина $\xi: \Omega \to R^+$. 
Математическое ожидание $M_\xi$ этой случайной величины конечно. 

Тогда для любого $\displaystyle \epsilon > 0\ верно\ равенство\ \displaystyle P(\xi \geq \epsilon) \leq \frac{M_\xi}{\epsilon}$

## Доказательство 

Введем событие $A = \lbrace \xi \geq \varepsilon \rbrace$ 

$$I_A(\omega) = 
\begin{cases} 0, & \quad \omega \notin A \\
1, & \quad \omega \in A 
\end{cases}$$

По определению $\varepsilon \leq \xi$ и 
так как максимальное значение $I_A(\omega)$ 
это единица, то $\xi I_A \leq \xi$   
$$\varepsilon I_A \leq \xi I_A \leq \xi$$


Найдём математическое ожидание каждого из выражений  
$$\varepsilon M[I_A] = \varepsilon\mathbb P(A) \leq M[\xi I_A] \leq M_\xi \quad \Longrightarrow \quad \mathbb P(A) \leq \frac{M_\xi}{\varepsilon}$$

## Следствия
### Следствие 1
Для любого $\varepsilon$

$\displaystyle \mathbb P(|\xi|\geq \varepsilon) \leq \frac{M[|\xi|]}{\varepsilon}$

$\displaystyle \mathbb P(|\xi|\geq \varepsilon) \leq \frac{M[|\xi|^k]}{\varepsilon^k}, \quad k \in \mathbb N$

---

### Следствие 2

$\displaystyle \mathbb P(|\xi| < \varepsilon) > 1-\frac{M[|\xi|]}{\varepsilon}$

## Пример

В среднем опаздывает студент на 3 минуты. Найти вероятность, что очередной студент опоздает на 15 и более минут.

**Решение:** $\mathbb P(\xi\geq 15) \leq \frac{3}{15} = 0.2$

---
## Создатель

Автор расписанного билета: Квист Татьяна

Кто проверил:
- ...

## Ресурсы
- [Лекция каких-то чуваков](https://eduardgorbunov.github.io/assets/files/Seminar10_675_with_solutions.pdf)
