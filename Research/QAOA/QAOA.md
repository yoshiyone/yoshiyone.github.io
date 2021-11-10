{% include head.html %}
# Introduction to QAOA

## Goal

Combinational optimization problem.

## Protocol

1. Map the problems into an optimization problem which has a cost function $\langle C \rangle$.
2. Construct the ansatz state:

   $$|\gamma,\beta\rangle=U(B,\beta_p)U(C,\gamma_p)\cdots U(B,\beta_1)U(C,\gamma_1)|s\rangle$$

3. Classical-quantum hybrid algorithm.

## Further Problems

- QUBO?

## Reference

1. [A Quantum Approximate Optimization Algorithm](https://arxiv.org/abs/1411.4028v1)

## Back to homepage

Click [here](../../index.md) to go back to homepage.
