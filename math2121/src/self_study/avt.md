# Abstract Vector Spaces

- A vector space is a nonempty set \\(V\\) (the elements are called vectors) with two opearation: vector addition (such that \\(u \in V, v \in V \to u + v \in V\\)) and scalar multiplication (such that \\(v \in V \to cv \in V\\)) satisfying the following conditions (axioms of vector space):

    1. \\(u + v = v + u\\) (transitivity)
    2. \\((u + v) + w = u + (v + w)\\) (associativity)
    3. \\(0 \in V: 0 + v = v\\) (zero exists in \\(V\\))
    4. \\(v + (-v) = 0\\) (addition inverse exists)
    5. \\(c(u + v) = cu + cv\\)
    6. \\((c+d)v = cv + dv\\)
    7. \\(c(dv) = (cd)v\\)
    8. \\(1v = v\\)

- Examples

    - \\(\mathbb{R}^n\\) and subspaces of \\(\mathbb{R}^n\\) are subspaces, with addition \\(\gets\\) elementwise addition and multiplication \\(\gets\\) elementwise multiplication
    - The set \\(\mathbb{R}^{m \times n}\\) is a subspace given the same definition for addition and multiplication
    - Therefore the set \\(f: \mathbb{R}^m \to \mathbb{R}^n\\) is also a subspace, with zero being the function \\(f(\vec x) = \vec 0\\)
    - \\(\mathbb{R}^+\\) is a subspace if we define:
        - \\(\oplus : a \oplus b = a \cdot b\\)
        - \\(\odot: c \odot a = a^c\\)
        - \\(0' : 1\\) (the zero vector for this subpsace is the number \\(1\\)) 
            - e.g. \\(7 \oplus \frac{1}{7} = 1\\), \\(7 \odot -2 = \frac{1}{49}\\)
     

- To check if a subset of a vector space is a linear subspace then check for

    1. Closed under addition
    2. Closed under scalar multiplication
    3. Zero exists