{% include head.html %}

# Canonical forms in MPS

## Background

This page is inspired by the paper [Efficient classical simulation of noisy random quantum circuits in one dimension](https://quantum-journal.org/papers/q-2020-09-11-318/). The author mentioned the concept of canonical form of MPO. However, it's tricky to transform a tensor into canonical form. Here I will summerize how to transform a tensor into canonical form with SVD decomposition.

## Protocols

- Goal: $T_1 S_1 T_2 S_2 ... T_{N-1} S_{N-1} T_N$
- Init: a tensor with N legs.
- Reshape the tensor into only 2 legs. Leg 1 is the original leg 1, leg 2 consists of the other legs.
- Do SVD decomposition at the first space between leg 1 and leg 2. Then we get $U_1$, $S_1$ and $V_1$.
- Reshape $U_1$ into $T_1$.
- To get $T_2$, do SVD decomposition to seperate the tensor consists of $S_1 V_1$. We cannot only seperate $V_1$, since $S_1$ is not unitary. Then we get $T_1 U_2 S_2 V_2$.
- $T_1 U_2 S_2 V_2=T_1 S_1 S_1^{-1} U_2 S_2 V_2$, so $T_2=S_1^{-1} U_2$.
- ...
- Done.
