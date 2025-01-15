# Eigenvalues, Eigenvectors, Diagonalization

## Eigenvalue and Eigenvectors

- An eigenvalue is a value \\(\lambda\\) such that given a square matrix \\(A\\), there exist a vector, being the eigenvector, which must be nonzero (otherwise it is trivial), such that:
\\[Av = \lambda v\\]


    - To find an eigenvector (which also corresponds to one eigenvector), it will be easier when we see the problem as the following, given that \\(I\\) is the identity matrix with the same size as \\(A\\):

    \\[(A - \lambda I)v = \vec 0\\]

    - \\(\lambda\\) is an eigenvalue if and only if \\(A - \lambda I\\) has determinant \\(0\\)

    - This is because we want to have a nontrivial \\(v\\) which means \\(\textsf{Nul}(A - \lambda I) \ne \\{0\\}\\)

    - If the eigenvalues of a matrix is found, to find the eigenvectors of a matrix, then find the bases for \\(\textsf{Nul}(A-\lambda I)\\)

- Example

    - Find the eigenvalues and eigenvectors of the following matrix

    \\[A = \begin{bmatrix} 4 & -1 & 6 \\\\ 2 & 1 & 6 \\\\ 2 & -1 & 8 \end{bmatrix}\\]

    - Then \\(A - \lambda I\\):

    \\[A - \lambda I = \begin{bmatrix} 4 - \lambda & -1 & 6 \\\\ 2 & 1 -\lambda & 6 \\\\ 2 & -1 & 8 -\lambda \end{bmatrix}\\]

    - The determinant of the matrix will be:
, this expression is called the characteristic polynomial:
    \\[\textsf{det}(A - \lambda I ) = (4 - \lambda) [(1-\lambda)(8-\lambda)+6] - (-1) [2(8 - \lambda) -12] + 6 [-2 - 2(1-\lambda) ] \\\\ = (\lambda-2)^2 (\lambda - 9)\\]

    - Note: It might be more convenient to use the cofactor expansion method to find the expression for the matrix equation

    - Note that the expression \\((\lambda - 2)\\) appeared as squared, we say that it has algebraic multiplicity \\(2\\) (depends on the number of the power)

    - Here, \\(\lambda = 2\\) and \\(\lambda = 9\\) are both eigenvalues of \\(A\\)

    - The *2-eigenvectors* of the matrix \\(A\\):

        - \\[A - 2I = \begin{bmatrix} 2 & -1 & 6 \\\\ 2 & -1 & 6 \\\\ 2 & -1 & 6 \end{bmatrix} \sim \begin{bmatrix} 2 & -1 & 6 \\\\ 0 & 0 & 0 \\\\ 0 & 0 & 0 \end{bmatrix}\\]     

        - The solution span is \\(\begin{bmatrix}  \frac{1}{2}\\\\ 1 \\\\ 0 \end{bmatrix}x_2 + \begin{bmatrix}   -3 \\\\ 0  \\\\ 1 \end{bmatrix}x_3 \\) 

        - \\(\therefore \textsf{Nul} (A- 2I) = \begin{bmatrix}  \frac{1}{2}\\\\ 1 \\\\ 0 \end{bmatrix} \textsf{ and } \begin{bmatrix}   -3 \\\\ 0  \\\\ 1 \end{bmatrix} = \\) 2-eigenvectors

        - Here, note that it is possible to have two eigenvectors that correlates with one eigenvalue, in this case, we say that it has the geometric multiplicity \\(2\\)

    - The *9-eigenvectors* of the matrix \\(A\\):

        - \\[A - 9I = \begin{bmatrix} -5 & -1 & 6 \\\\ 2 & -8 & 6 \\\\ 2 & -1 & -1 \end{bmatrix} \sim \begin{bmatrix} 1 & 0 & -1 \\\\ 0 & 1 & -1 \\\\ 0 & 0 & 0 \end{bmatrix}\\]

        - The solution span is \\(\begin{bmatrix}  1\\\\ 1 \\\\ 1 \end{bmatrix} x_3 \\) 

        - \\(\therefore \textsf{Nul} (A- 9I) = \begin{bmatrix}  1\\\\ 1 \\\\ 1 \end{bmatrix} = \\) 9-eigenvectors

## Properties of Eigenvalues and Eigenvectors

- The eigenvalue of a triangular matrix is simply the diagonal entries of it

    - \\[ A = \begin{bmatrix} 3 & 4 & 5 \\\\ 0 & 0 & 2 \\\\ 0 & 0 & 1 \end{bmatrix}\\] 

    - The matrix above has eigenvalues \\(\lambda = 3, 0, 1\\)

    - Proof: This is simply because the determinant of a triangular matrix is the multiplication of the diagonal entries, hence \\(\textsf{det}(A - \lambda I) = (d_1 - \lambda)(d_2 - \lambda) ... (d_n - \lambda)\\) given that \\(\\{d_i\\}\\) are the diagonal entries of the triangular matrix \\(A\\)

- Suppose \\(\\{\lambda_i\\}\\) are distinct eigenvalues for \\(A\\) and \\(\\{v_i\\}\\) is the sequence of their corresponding eigenvectors. Then the vectors in \\(\\{v_i\\}\\) are linearly independent

    - Proof: WLOG let the last vector \\(v_n\\) in the sequence be not independent to the others, i.e. there exist \\(\\{c_i\\}\\) such that \\(v_n = c_1v_1 + c_2v_2 + ... + c_nv_n\\)

    - Multiply both side of the equation above by \\(A\\) such that it is \\(Av_n = c_1Av_1 + c_2Av_2 + ... + c_nAv_n\\). Using the fact that \\(Av_i = \lambda_i v_i\\)

    - &lt;complete proof later&gt;

## Diagonalization

- &lt;formal definiton later&gt;

- Similar matrices \\(\to\\) same eigenvalues, but same eigenvalues \\(\not \to\\) similar matrices

- A matrix is diagonalizable if it is similar to a diagonal matrix

- A triangular matrix with all diagonal entries being set to \\(\lambda\\) is not diagonalizable if it is not \\(\lambda I\\)

    - i.e. such matrix is not diagonalizable:

    \\[A = \begin{bmatrix} 3 & 2 & -1 \\\\ 0 & 3 & 0 \\\\ 0 & 0 & 3 \end{bmatrix}\\]

    - Proof: If the triangular matrix \\(A\\) were diagonalizable, then it would be similar to \\(\lambda I\\). However setting \\(A = P\lambda IP^{-1} = \lambda I\\), there are no other possibilities
- Let \\(\\{\lambda_i\\}\\) be the distinct eigenvalues of the matrix \\(A\\), then the matrix \\(A\\) is diagonalizable \\(\leftrightarrow \textsf{dim}\space\textsf{Nul}(A - \lambda_1 I) + \textsf{dim}\space\textsf{Nul}(A - \lambda_2 I) + ... + \textsf{dim}\space\textsf{Nul}(A - \lambda_n I)\\) 

## Complex Numbers

- Let \\(i = \begin{bmatrix} 0 & -1 \\\\ 1 & 0 \end{bmatrix}\\) and \\(1 = \begin{bmatrix} 1 & 0 \\\\ 0 & 1 \end{bmatrix}\\)

- Now, define \\(\mathbb{C} = \\{a + bi: a, b \in \mathbb{R}\\} = \left\\{ \\begin{bmatrix} a & -b \\\\ b & a \end{bmatrix}: a, b \in \mathbb{R}\right\\}\\)

- Addition in \\(\mathbb{C}\\):

    - \\([a + bi] + [c + di] = \begin{bmatrix} a & -b \\\\ b & a \end{bmatrix} + \begin{bmatrix} c & -d \\\\ d & c \end{bmatrix} = \begin{bmatrix} a+c & -b-d \\\\ b+d & a+c \end{bmatrix} = (a+c) + (b+d) i\\)

- Multiplication in \\(\mathbb{C}\\):

    - \\([a + bi] \cdot [c + di] = \begin{bmatrix} a & -b \\\\ b & a \end{bmatrix} \cdot \begin{bmatrix} c & -d \\\\ d & c \end{bmatrix} = \begin{bmatrix} ac-bd & -ad-bc\\\\ ad+bc & ac-bd \end{bmatrix} =  (ac-bd) + (ad+bc) i\\)

- Division in \\(\mathbb{C}\\):

    - In algebraic notation: \\(\frac{a+bi}{c+di} = \frac{(a+bi)(c-di)}{(c+di)(c-di)} = \frac{(ac + bd)  + (bc - ad) i}{c^2 + d^2}\\)

    - Matrix notation: \\([a + bi] \div [c + di] = \begin{bmatrix} a & -b \\\\ b & a \end{bmatrix} \cdot \begin{bmatrix} c & -d \\\\ d & c \end{bmatrix}^{-1} = \begin{bmatrix} a & -b \\\\ b & a \end{bmatrix} \cdot \frac{1}{c^2 + d^2} \begin{bmatrix}  c & d \\\\ -d & c\end{bmatrix} = \frac{(ac + bd)  + (bc - ad) i}{c^2 + d^2}\\)

- Define that the complex number \\(x\\) has the conjugate \\(\bar x\\), in matrices, this means \\(x^\top\\)

    - \\(\overline{a + bi} = \begin{bmatrix} a & -b \\\\ b & a \end{bmatrix}^\top = \begin{bmatrix} a & b \\\\ -b & a \end{bmatrix} = a- bi\\)

    - \\(\overline{xy} = (xy)^\top = y^\top x ^\top\\)

- In the following, we show \\(e^{i x} = \cos x + i \sin x \\)

    - \\(e^{ix} = \frac{1}{0!} + \frac{ix}{1!} + \frac{(ix)^2}{2!} + \frac{(ix)^3}{3!} + ...\\)

    - \\(e^{ix}= \begin{bmatrix}1 & 0 \\\\ 0 & 1\end{bmatrix} + \begin{bmatrix} 0 & -x \\\\ x & 0\end{bmatrix} + \begin{bmatrix} -\frac{x^2}{2} & 0 \\\\ 0 & -\frac{x^2}{2}\end{bmatrix} + \begin{bmatrix} 0 & \frac{x^3}{2\cdot 3}  \\\\ -\frac{x^3}{2\cdot 3} & 0 \end{bmatrix} + \begin{bmatrix} \frac{x^4}{2\cdot 3 \cdot 4}  & 0 \\\\ 0 & \frac{x^4}{2\cdot 3 \cdot 4}\end{bmatrix} + ...\\)

    - \\(\therefore e^{ix}= \begin{bmatrix} 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!}+ ... & -\left(x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + ...\right) \\\\ x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!}+... & 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + ...\end{bmatrix} = \begin{bmatrix}\cos x & -\sin x \\\\ \sin x & \cos x\end{bmatrix}\\)

- Complex number is introduced for the following theorem

- Fundamental theorem of algebra: Define \\(p(x) = a_n x^n + a_{n-1}x^{n-1} + a_{n-2}x^{n-2} + ... + a_2 x^2 + a_1 x + a_0\\). There exists \\(n\\) complex numbers \\(\\{r_i\\}\\), the roots of \\(p(x)\\), (not neccesarily distinct) such that \\(p(x) = a_n(x-r_1)(x-r_2)...(x-r_n)\\)

## Complex Eigenvalues

- We can extend the fundamental theorem of algebra such that we can find complex eigenvalues for some matrix

- We define \\(\overline{A}\\) and \\(\overline{v}\\) to be the matrix and vector given by replacing entries of \\(A \in \mathbb{C}^{n\times m}\\) and \\(v \in \mathbb{C}^n\\) by their complex conjugate

- If we have \\(A\\) be a matrix with all real entries, more formally \\(A = \overline{A}\\). If \\(\lambda \in \mathbb{C}\\) and \\(v \in \mathbb{C}^n\\) be the eigenvalue and eigenvector of \\(A\\), then so is \\(\overline \lambda\\) and \\(\overline v\\)
    
    - Proof: ? Should be because there is no complex element \\(A\\)

- The determinant of a matrix is equal to the product of its eigenvalues, repeated with multiplicity

- The trace of a matrix is equal to the sum of its eigenvalues, repeated with multiplicy