<head>
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        TeX: {
        equationNumbers: {
            autoNumber: "AMS"
        }
        },
        tex2jax: {
        inlineMath: [ ['$', '$'] ],
        displayMath: [ ['$$', '$$'] ],
        processEscapes: true,
    }
    });
    MathJax.Hub.Register.MessageHook("Math Processing Error",function (message) {
        alert("Math Processing Error: "+message[1]);
        });
    MathJax.Hub.Register.MessageHook("TeX Jax - parse error",function (message) {
        alert("Math Processing Error: "+message[1]);
        });
    </script>
    <script type="text/javascript" async
    src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
    </script>
</head>

# Introduction to QAOA

## Goal

Combinational optimization problem.

## Protocol

1. Map the problems into an optimization problem which has a cost function $\langle C \rangle$.
2. Construct the ansatz state:
   $$ |\gamma,\beta\rangle=U(B,\beta_p)U(C,\gamma_p)\cdots U(B,\beta_1)U(C,\gamma_1)|s\rangle $$

3. Classical-quantum hybrid algorithm.

## Further Problems

- QUBO?

## Reference

1. [A Quantum Approximate Optimization Algorithm](https://arxiv.org/abs/1411.4028v1)
