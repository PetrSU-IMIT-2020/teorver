# Билет №1.17. Функция распределения дискретной случайной величины и ее свойства.

## Определение (из учебника)

***Функцией распределения*** (вероятностей) случайной величины $\xi$ называется 
функция  $F(x) $, значение которой в точке  $x $ равно вероятности события  $\{\xi < x\} $, то есть события, состоящего из тех и только тех элементарных исходов  $\omega $, для которых $\{\xi(\omega) < x\}$

$F_\xi(x) = \mathbb P(\xi(\omega) < x) = \mathbb P(\xi < x)$

## Свойства

1. $0 \leq F_\xi(x) \leq 1$
2. $\mathbb P(x_1 \leq \xi \leq x_2) = F_\xi(x_2) - F_\xi(x_1)$

    *Доказательство:*  
    $A = \{\omega : \xi(\omega) < x_1\}$  
    $B = \{\omega : \xi(\omega) < x_2\}$  
    $C = \{\omega : x_1 \leq \xi(\omega) < x_2\}$
    
    $B = A+C$  
    $\mathbb P(B) = \mathbb P(A) + \mathbb P(C)$  
    $\mathbb P(C) = \mathbb P(B) - \mathbb P(A)$
    
3. $F_\xi(x)$ - неубывающая : $x_2 \geq x_1 \quad F_\xi(x_2) \geq F_\xi(x_1)$

    *Доказательство:*  
    $F_\xi(x_2) = F_\xi(x_1) + \mathbb P(x_1 \leq \xi < x_2) \geq F_\xi(x_1)$
    
4. $\mathbb P(\xi \geq x) = 1 - F_\xi(x)$
5. $\lim\limits_{x \to \infty} F_\xi(x) = 1$

    *Доказательство:* $x_1, x_2, x_3, ...$ - возрастающая последовательность : $x_n \xrightarrow[n \to \infty]{} \infty$  
    
    $A_1 = \{\xi < x_1\}$  
    $A_2 = \{x_1 \leq \xi < x_2\}$  
    ...  
    $A_n = \{x_{n-1} \leq \xi < x_n\}$
    
    $A = \{\xi < x_n\} = A_1 + A_2 + ... + A_n$
    
    $\mathbb P(\Omega) = \mathbb P(\displaystyle\bigcup_{i=1}^\infty A_i) = \displaystyle\sum_{i=1}^n \mathbb P(A_i) = \lim\limits_{n \to \infty} \displaystyle\sum_{i=1}^n \mathbb P(A_i) = \lim\limits_{n \to \infty} F_\xi(x_n)$
    
6. $\lim\limits_{x \to -\infty} F_\xi(x) = 0$

    *Доказательство:* $x_1, x_2, x_3, ...$ - возрастающая последовательность : $x_n \xrightarrow[n \to \infty]{} \infty$
    
    $A_1 = \{\xi < x_1\}$  
    ...  
    $A_n = \{x_{n-1} \leq \xi < x_n\}$
    
    $\displaystyle\bigcap_{i=1}^\infty A_i = \varnothing \quad$ => $\quad \lim\limits_{n \to \infty} F_\xi(x_n) = \lim\limits_{n \to \infty} \mathbb P(\displaystyle\bigcap_{i=1}^\infty A_i) = 0$
    
7. Непрерывна слева

    *Доказательство:*
    
    $L_1, L_2, ...\quad:\quad \lim\limits_{n \to \infty} L_n = 0$ и $\forall i \quad L_i \geq 0$
    
    $A_n = \{\omega : x-L_n \leq \xi(\omega) < x\}$
    
    $\lim\limits_{n \to \infty} \mathbb P(A_n) = \varnothing = \lim\limits_{n \to \infty} (F_\xi(x) - F_\xi(x-L_n))$ => $F_\xi(x) = \lim\limits_{n \to \infty} F_\xi(x-L_n)$
    
## Пример

Возьмем правильную монету, которую подбросили. Такой опыт имеет два исхода - выпал орел (0), выпала решка (1), вероятность каждого из которых равна $\frac{1}{2}$.

Закон распределения:  

$$\begin{array}{c|c|c} \xi & 0 & 1 \\ \hline  P_\xi & \frac{1}{2} & \frac{1}{2} \end{array}$$

Функция распределения: $F_\xi(x) = \begin{cases} 0 & \quad x \leq 0 \\ \frac{1}{2}  & \quad 0 < x \leq 1 \\ 1 & \quad x > 1 \end{cases}$

---
## Создатель
``
Автор расписанного билета: Алиса Хайдарова

Кто проверил:
- никто

## Ресурсы
- лекции
- учебник
