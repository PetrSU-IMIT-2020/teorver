# Свойства функции непрерывной случайной величины (тоже самое, что 1.17)
## Определение (из учебника)

***Функцией распределения*** (вероятностей) случайной величины $\xi$ называется 
функция $F(x)$, значение которой в точке 
$x$ равно вероятности события 
{ $\xi < x$ }, то есть события, состоящего из тех и только тех элементарных исходов
$\omega$, для которых 
{ $\xi(\omega) < x$ }

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
    
## Пример нахождения функции распределения из плотности (из 2.12)

СВНТ имеет плотность распределения:

$$f_x(x) =
\begin{cases} 0, \quad & x < 0 \\
2*(1 - x), \quad & 0 \geq x \leq 1 \\
0, \quad & x > 1
\end{cases}
$$

задача - найти функцию распределения
решение:

-$\sphericalangle$ x < 0:
$$F_x(x) = \int_{-\infty}^x f_x(t) \mathrm{d}t = \int_{-\infty}^x 0 \mathrm{d}t = 0 $$

-$\sphericalangle$ 0 < x < 1:

$$F_x(x) = \int_{-\infty}^0 f_x(t) \mathrm{d}t + \int_0^x f_x(t) \mathrm{d}t = 0 + \int_0^x (1-x) \mathrm{d}t $$

$$F_x(x) = 2(x - \dfrac{x^2}{2}) $$

-$\sphericalangle$ x > 1:
$$F_x(x) = \int_{-\infty}^0 f_x(t) \mathrm{d}t +  \int_0^1 f_x(t) \mathrm{d}t +  \int_1^x f_x(t) \mathrm{d}t = 0 + 2(1 - 1/2) + \int_1^x 0 \mathrm{d}t = 1 $$

итог: функция распределения имеет вид:

$$F_x(x) =
\begin{cases} 0, \quad & x < 0 \\
2(x - \dfrac{x^2}{2}), \quad & 0 \geq x \leq 1 \\
1, \quad & x > 1
\end{cases}
$$

## Создатель

Автор расписанного билета: Лисицкий Олег + Алиса Хайдарова

Кто проверил:

## Ресурсы
- лекции
- книга Рогова, стр. 57 https://studizba.com/files/show/pdf/18027-4-4-chast.html
- Электронное хранилище учебных материалов https://edu.tltsu.ru/er/book_view.php?book_id=1cec&page_id=19444
