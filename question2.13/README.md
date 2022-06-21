# Функция распределения случайной величины
## Важные определения
- Случайной величиной X называется функция  $X = X(\omega) $, определенная на множестве элементарных исходов  $\Omega $ и такая, что при любом действительном x множество тех  $\omega$, для которых  $X(\omega) < x$, принадлежит алгебре событий для данного эксперимента.
- $\Omega$ - пространство, элементы которого - элементарные события.
- $\omega$ - элементарное событие
- $\sigma$ — сигма-алгебра подмножеств ${\displaystyle \Omega }$ , называемых (случайными) событиями

## определение
***Функцией распределения*** (вероятностей) случайной величины $\xi$ называется 
функция $F(x)$, значение которой в точке 
$x$ равно вероятности события 
{ $\xi < x$ }, то есть события, состоящего из тех и только тех элементарных исходов
$\omega$, для которых 
{ $\xi(\omega) < x$ }

$F_\xi(x) = \mathbb P(\xi(\omega) < x) = \mathbb P(\xi < x)$

- ***для дискретной случайной величины:*** $F_\xi(x) = \displaystyle\sum_{x_i < x} P(\xi = x_i)$

- ***для непрерывной случайной величины:*** $F_\xi(x) = \displaystyle\int\limits_{-\infty}^x P(t)dt$

Функция распределения обладает следующими свойствами(доказательства в 2.14):
- $0 \leq F_\xi(x) \leq 1$
- $\mathbb P(x_1 \leq \xi \leq x_2) = F_\xi(x_2) - F_\xi(x_1)$
- $F_\xi(x)$ - неубывающая : $x_2 \geq x_1 \quad F_\xi(x_2) \geq F_\xi(x_1)$
- $\mathbb P(\xi \geq x) = 1 - F_\xi(x)$
- $\lim\limits_{x \to \infty} F_\xi(x) = 1$
- $\lim\limits_{x \to -\infty} F_\xi(x) = 0$
- Непрерывна слева
## Пример нахождения функции распределения из плотности для непрерывной случайной величины(СВНТ)

СВНТ имеет плотность распределения:

$$f_x(x) =
\begin{cases} 0, \quad & x < 0 \\
2*(1 - x), \quad & 0 \leq x \leq 1 \\
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
2(x - \dfrac{x^2}{2}), \quad & 0 \leq x \leq 1 \\
1, \quad & x > 1
\end{cases}
$$

## Создатель

Автор расписанного билета: Лисицкий Олег + Алиса Хайдарова

Кто проверил:


## Ресурсы
- книга Рогова, стр. 57 https://studizba.com/files/show/pdf/18027-4-4-chast.html
- ТеорВер-Онлайн, интернет-учебник http://new.math.msu.su/department/probab/io/teorver-online/teorver30.html
- Электронное хранилище учебных материалов https://edu.tltsu.ru/er/book_view.php?book_id=1cec&page_id=19444
