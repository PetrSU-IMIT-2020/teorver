# Билет №1.8. Основные соотношения между вероятностями событий
Пусть задано вероятностное пространство $(\Omega, \sigma,	{\displaystyle \mathbb {P}})$

$\Omega$  — произвольное непустое множество, элементы которого называются элементарными событиями, исходами или точками;  
$\sigma$ — сигма-алгебра подмножеств ${\displaystyle \Omega }$ , называемых (случайными) событиями;  
${\displaystyle \mathbb {P} }$  — вероятностная мера или вероятность, то есть сигма-аддитивная конечная мера, такая что ${\displaystyle \mathbb {P} (\Omega )=1}$.

Основные соотношения:
1. $A \in \sigma$  
   $P(\overline{A}) = 1 - P(A)$  
   $A, \overline{A}$ - несовместные, $A + \overline{A} = \Omega$  
   По аксиоме счетной аддитивности $P(A) + P(\overline{A}) = P(\Omega) = 1$ (по аксиоме нормирования)  

2. $A, B \in \sigma  \quad A < B  \quad P(A) \leq P(B)$  
   $B = A \cup (B\ A)$ по аксиоме аддитивности  
   $P(B) = P(A) + P(B\ A)$  
   
3. $P(A) \leq 1$  
   Для любых $A \subset \Omega$ на основании 2-ого свойства $P(A) \leq P(\Omega)$  
   
4. $P(\varnothing) = 0$  
   $\varnothing = \overline{\Omega}$ по свойству 1  
   $P(\varnothing) = 1 - P(\Omega) = 0$  
   
5. $A, B \in \sigma$  
   $P(A\setminus B) = P(A) - P(AB)$  
   $P(B\setminus A) = P(B) - P(AB)$  
   $P(A+B) = P(A) + P(B) - P(AB)$  
   
   $1) A = A \setminus B \cup AB$  
      $P(A) = P(A\setminus B) + P(AB)$  
      $P(A\setminus B) = P(A) - P(AB)$
      
   2) Аналогично 1 
   
   $3) A+B = A\setminus B + B\setminus A + AB$  
      $P(A+B) = P(A\setminus B) + P(B\setminus A) + P(AB)$  
      $P(A+B) = P(A) - P(AB) + P(B) - P(AB) + P(AB)$  
      $P(A+B)= P(A) + P(B) - P(AB)$  
      
6. Пусть $B = \bigcup_{\substack{ i \in I }}A_i   P(B) \leq \sum_{\substack{ i \in I }} P(A_i)$  
   $B = A_1 + A_2\ A_1 + A_3\ A_1 A_2 + ...$  
   $A_2\ A_1 \leq P(A_2)   A_3\ A_1 A_2 \leq P(A_3)$ и тд по свойству 2  
   
7. Пусть если семейство событий $A_1, A_2, ..., A_n$  
   $P_1 = \sum_{\substack{ 1 \leq i \leq n }} P(A_i)$  
   $P_2 = \sum_{\substack{ 1 \leq i \le j \leq n }} P(A_i A_j)$  
   аналогично остальные
   $P_n = P(A_1 A_2 ... A_n)$  
   $\displaystyle P(\sum_{\substack{ 1 \leq i \leq n }} P(A_i)) = P_1 - P_2 + P_3 - ... - (-1)^n * P_n$  
      
---
## Создатель

Автор расписанного билета: Кузнецова Елизавета

Кто проверил:
- Квист Татьяна

## Ресурсы
- Билеты Власовой Алисы.
- Википедия https://ru.wikipedia.org/wiki/%D0%92%D0%B5%D1%80%D0%BE%D1%8F%D1%82%D0%BD%D0%BE%D1%81%D1%82%D0%BD%D0%BE%D0%B5_%D0%BF%D1%80%D0%BE%D1%81%D1%82%D1%80%D0%B0%D0%BD%D1%81%D1%82%D0%B2%D0%BE
