<!-- Extra headers for rendering pseudocodes BEGIN -->

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

<!-- Extra headers for rendering pseudocodes END -->
# Merge Sort

Merge Sort is a $\Theta(n \log n)$ algorithm to sort an array.

It works as such:
<pre id="mergeSort">
    \begin{algorithm}
        \caption{MergeSort}
        \begin{algorithmic}
            \procedure{MergeSort}{$A, begin, end$}
                \State $mid \gets \lfloor {(begin + end)}/{2}\rfloor$ 
                \State MergeSort($A, begin, mid$)
                \State MergeSort($A, mid, end$)
                \State Merge($A, begin, end$)
            \endprocedure
            \procedure{Merge}{$A, begin, end$}
                \State $i \gets 3$
            \endprocedure
        \end{algorithmic}
    \end{algorithm}
</pre>


Anyway, testing done for now

<!-- Extra scripts for rendering pseudocodes BEGIN -->
<script>
    pseudocode.renderElement(document.getElementById("mergeSort"));
</script>

<script>
    pseudocode.renderClass("pseudocode");
</script>

<!-- Extra scripts for rendering pseudocodes END -->
