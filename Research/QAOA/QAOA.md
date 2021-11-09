<!-- <head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head> -->
<link
rel="stylesheet"
href="https://cdn.jsdelivr.net/npm/katex/dist/katex.min.css"
/>
<script
src="https://cdn.jsdelivr.net/combine/npm/katex/dist/katex.min.js,npm/katex/dist/contrib/mathtex-script-type.min.js,npm/katex/dist/contrib/auto-render.min.js"
defer="defer"
onload='renderMathInElement(document.body, { delimiters: [{ left: "$", right: "$", display: false }] })'
></script>

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
