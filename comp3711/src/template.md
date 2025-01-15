<extra-script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/pseudocode@latest/build/pseudocode.min.css">
<script src="https://cdn.jsdelivr.net/npm/pseudocode@latest/build/pseudocode.min.js"></script>
<script>
    MathJax = {
        tex: {
            inlineMath: [['$','$'], ['\\(','\\)']],
            displayMath: [['$$','$$'], ['\\[','\\]']],
            processEscapes: true,
            processEnvironments: true,
        }
    }
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3.2.2/es5/tex-chtml.js"
        integrity="sha256-Cm3tWrvOEzMWWN0jnzQ4Kr0GSSx0txth6MqoES7FX6U="
        crossorigin="anonymous" referrerpolicy="no-referrer">
</script>
</extra-script>

<extra-script>
<script>
    pseudocode.renderElement(document.getElementById("<pre-id-here>"));
    pseudocode.renderClass("pseudocode");
</script>
</extra-script>