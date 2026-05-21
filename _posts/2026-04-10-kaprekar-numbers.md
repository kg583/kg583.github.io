---
title: "Teensy Problems: Kaprekar Numbers"
date: 2026-04-10
categories:
  - teensy-problems
tags:
  - math
  - problem
---

Dr. Kaprekar has stumbled upon an interesting class of numbers. A number N is called a "Kaprekar number" if $N^2$, written in base 10, can be split into two parts, $A$ and $B$, such that $N = A + B$. Here are some examples:
```
   9² =       81 →   8 +     1 =    9
  45² =     2025 →  20 +    25 =   45
4879² = 23804641 → 238 + 04641 = 4879
```
Notice that the parts do not have to be equal in size and can include leading zeros; the only restriction is that neither part is totally zero. Let's help Dr. Kaprekar understand more about his numbers.

1. Prove that $N^2 - N$ being divisible by $10^n - 1$ for some n is a necessary condition for $N$ to be Kaprekar.

2. Show that $N^2 - N \equiv 0 \pmod{10^n - 1}$ and $N < 10^n$ is a sufficient condition for $N$ to be Kaprekar (with an obvious exception).

3. Show that $N^2 - N \equiv 0 \pmod{q}$ has exactly two solutions for any prime power $q$. (Just like normal quadratic equations!) What are they?

4. Why does 3. fail in the case of a modulus divisible by two different primes?

5. Show that every solution to $N^2 - N \equiv 0 \pmod{10^n - 1}$ can be assembled from the solutions to $N^2 - N \equiv 0 \pmod{q}$ for every prime power $q$ dividing $10^n - 1$.

6. Putting these pieces together, describe for Dr. Kaprekar a procedure or program to find all Kaprekar numbers up to some limit $M$ that is "faster" than checking every value up to $M$.

7. Your procedure, though an improvement on bruteforce checking, is still "slow". Why?

8. Wait a second, is $1$ a Kaprekar number?

9. Ponder if and how any of the above arguments change in other bases.


### Hints

<details>
<summary>1. </summary>
State the definition of Kaprekar numbers more "mathematically"
</details>

<details>
<summary>2. </summary>
Appeal again to a "rigorous" definition
</details>

<details>
<summary>5. </summary>
This is tricky to prove rigorously, but I think you can assemble the main idea using the previous parts
</details>
