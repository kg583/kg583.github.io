---
title: "Prover Sequence"
date: 2026-09-02
categories:
  - teensy-problems
tags:
  - math
  - problem
---

Recall that a *tree* is an undirected network with no cycles or loops such that any node is reachable from any other. A *labeled* tree is one where we've given each node a unique label, by convention a number between $1$ and $n$ for $n$ the number of nodes in the tree. Two labeled trees are the same if they can be drawn identically, with the same labels and connections.

(More technically, we're considering trees up to *isomorphism*, but fret not if you don't know that term.)

Let $T(n)$ be the number of labeled trees with $n$ nodes. Clearly $T(1) = 1$ (there's just one node labeled $1$) and $T(2) = 1$ (there's two nodes, labeled $1$ and $2$, connected to each other; two nodes with no connection is not a tree).

1. Compute $T(3)$.

2. Compute $T(4)$ (note: tricky).

3. Define the "prover sequence" for a tree in the following way (the name will make sense shortly):
	- Take the node with only one neighbor (called a *leaf*) which has the smallest label, remove it from the tree, and write down the label of its neighbor.
	- Repeat until there are only two nodes left.

4. Given a prover sequence, describe a process for recovering the labeled tree that made it.

5. Show that there is a one-to-one correspondence between labeled trees and prover sequences.

6. How many possible prover sequences are there for labeled trees with $n$ nodes?

7. What do prover sequences then "prove" about $T(n)$?
