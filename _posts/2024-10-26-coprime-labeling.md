---
title: 'KG's Teensy Math Problems: Coprime Labeling'
date: 2024-10-26
categories:
  - teensy-problems
tags:
  - math
  - problem
---

Let $G$ be a graph with $n$ vertices. We say a graph is *coprimely labeled* if its vertices are labeled using all the integers from 1 to $n$ in such a way where, if any two vertices have an edge between them, their labels are coprime; that is, they share no common factors.

For example, the graph depicted below is coprimely labeled. Note that we do not need every edge between vertices with coprime labels to be present (e.g. an edge connecting 2 & 3), but we *cannot* have any edges which connect vertices whose labels share a common factor (e.g. an edge connecting 2 & 4).

Prove that any graph with more than $\binom{n}{2} - \binom{\lfloor n/2 \rfloor}{2}$ edges cannot be coprimely labeled.

I recommend trying to build your way up to this result yourself (and, perhaps, actually prove a stronger condition!), but I won't kid about it being a veritable exercise. If you want some prior scaffolding, here's one approach:

<details>
<summary>Step 1</summary>
We'll construct a sequence $H_n$ of "nearly complete" graphs: graphs on $n$ vertices which are coprimely labeled and have as many edges as possible. Show that $H_3$ is $K_3$, the complete graph on 3 vertices, but $H_4$ is $K_4$ less one edge (which edge?).
</details>

<details>
<summary>Step 2</summary>
In general, we can make $H_n$ by deleting "bad" edges from $K_n$. However, try to find a way to produce $H_{n+1}$ *directly* from $H_{n}$; that is, without deleting any edges.
</details>

<details>
<summary>Step 3</summary>
Find an upper bound for the number of edges you add to $H_n$ to get $H_{n+1}$ based on the parity of $n$. *(Bonus: find an exact formula using Euler's totient function.)*
</details>

<details>
<summary>Step 4</summary>
Show that you can add edges to *any* coprimely labeled graph on $n$ vertices to obtain $H_n$. That is, all coprimely labeled graphs on $n$ vertices are *minors* of $H_n$.
</details>

<details>
<summary>Step 5</summary>
Combine Steps 3 & 4 to obtain the condition we're after. *(Bonus: find a stronger condition using the exact formula.)*
</details>
