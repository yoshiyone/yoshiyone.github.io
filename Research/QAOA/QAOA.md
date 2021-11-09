<head>
    <script>
MathJax = {
tex: {
inlineMath: [['$', '$']],
displayMath: [['\\[', '\\]']],
processEnvironments: true,
processRefs: true
},
options: {
skipHtmlTags: ['noscript', 'style', 'textarea', 'pre', 'code'],
ignoreHtmlClass: 'tex2jax_ignore',
renderActions: {
find_script_mathtex: [10, function (doc) {
for (const node of document.querySelectorAll('script[type^="math/tex"]')) {
const display = !!node.type.match(/; *mode=display/);
const math = new doc.options.MathItem(node.textContent, doc.inputJax[0], display);
const text = document.createTextNode('');
node.parentNode.replaceChild(text, node);
math.start = { node: text, delim: '', n: 0 };
math.end = { node: text, delim: '', n: 0 };
doc.math.push(math);
}
}, '']
}
},
svg: {
fontCache: 'global'
}
};
</script>
<script id="MathJax-script" async src="https://cdn.staticfile.org/mathjax/3.0.1/es5/tex-svg.js"></script>
</head>

# Introduction to QAOA

## Goal

Combinational optimization problem.

## Protocol

1. Map the problems into an optimization problem which has a cost function $\langle C \rangle$.
2. Construct the ansatz state:
$$
|\gamma,\beta\rangle=U(B,\beta_p)U(C,\gamma_p)\cdots U(B,\beta_1)U(C,\gamma_1)|s\rangle
$$

3. Classical-quantum hybrid algorithm.

## Further Problems

- QUBO?

## Reference

1. [A Quantum Approximate Optimization Algorithm](https://arxiv.org/abs/1411.4028v1)
