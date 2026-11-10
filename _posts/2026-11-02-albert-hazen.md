---
title: "Albert Hazen"
date: 2026-11-02
categories:
  - teensy-problems
tags:
  - math
  - problem
---

Albert Hazen, a good friend of Finn Factor, is also interested in computing prime numbers. He's always been a fan of Wilson's theorem, which states that $(n - 1)! \equiv -1 \pmod{n}$ if and only if $n$ is prime. The modular equivalence takes a bit of knack to prove, though Albert realized we can forego modular arithmetic and still arrive at useful claims for prime-finding.

Let $f \colon \mathbb{N} \to \mathbb{N}$ be an arbitrary function (where it doesn't matter if you think $0 \in \mathbb{N}$ or not), and then define the _Albert function_ $A_f(n) = \mathrm{gcd}(n, f(n)!)$, where $\mathrm{gcd}(a,b)$ is the _greatest common divisor_ of $a$ and $b$ and $n!$ is the usual factorial.

We also let $f^i = f \overbrace{\circ \cdots \circ}^{i \text{ times}} f$ denote function iteration.

1. Let $g(n) = n - 1$. Describe and prove the correctness of a primality test that uses $A_g$. How is it related to Wilson's theorem?

2. Let $h(n) = \lfloor n^{1/2} \rfloor$. Show that $A_h$ may be used in place of $A_g$ in your primality test.

3. Prove that $1/2$ is the smallest possible exponent in $h(n)$ that yields a correct primality test for all $n > 1$.

4. Likewise, prove that the exponent must be strictly less than $1$.

5. Show that, for $n > 30$, $A_h^2(n) = 1$ if and only if $n$ is prime or semiprime (i.e. has exactly two prime factors). What goes wrong for small $n$?

6. Does the analogous claim hold for $A_h^3(n)$?

7. What does it mean for $A_h(n) = n$?
