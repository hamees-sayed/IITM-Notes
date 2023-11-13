For week 4, refer to Part 3
For week 5 and 6, refer to Part 4

[https://bsc-iitm.github.io/karthikt/notes/linear_algebra/](https://bsc-iitm.github.io/karthikt/notes/linear_algebra/)

## Positive Definite (Not covered in notes)  
A function $f$ that vanishes at (0, 0) and is strictly positive at other points is called positive definite, and is denoted by $f>0$.  

$\rightarrow Conditions:$  
1. If $f>0$, then $a>0$. 
2. If $f>0$, then $c>0$.  

These two conditions are not enough to ensure $f>0$.  
e.g $\rightarrow f(x, y) = x^2 - 10xy + y^2$  

$\rightarrow$ Extra condition to infer $f>0$.  
$f(x, y) = ax^2 + 2bxy + cy^2 = a(x + \frac{b}{a}y)^2 + (c-\frac{b^2}{a})y^2 \geq 0$ 

3. If $f>0$, $ac>b^2$ combining all equations, we have:  
$f(x, y) = ax^2 + 2bxy + cy^2$ is positive definite i.e if and only if $a>0$ and $ac >b^2$.  

If $ac = b^2$, then $f(x, y) = ax^2 + 2bxy+by^2$ is $\begin{cases} \text{positive semi definite if} \space a>0 \\
                     \text{negative semi definite if} \space a<0
       \end{cases}$  
       
Saddle Point if $ac < b^2$  

---
## Connection to Linear Algebra  

$ax^2 + 2bxy + cy^2 = \begin{bmatrix}x & y\end{bmatrix}\begin{bmatrix}a & b \\ b & c\end{bmatrix}\begin{bmatrix}x \\ y\end{bmatrix}$  
 
Let $v = \begin{bmatrix}x \\ y\end{bmatrix}$ and $A = \begin{bmatrix}a & b \\ b & c\end{bmatrix}$  

Then $ax^2 + 2bxy + cy^2 = v^TAv$  

## Positive Definite matrices  
$A = \begin{bmatrix}a & b \\ b & c\end{bmatrix}$ is positive definite if $a>0, ac-b^2>0$  

> Note: If $a>0$ and $ac-b^2>0$, then both eigenvalues (say $\lambda_1, \lambda_2$) of $A$ are positive.  
To see this:- $ac - b^2 = det(A) = \lambda_1 \lambda_2 > 0, \space Tr(A) = \lambda_1 + \lambda_2 = a + c > 0$   

$\rightarrow$ A real symmetric matrix $n \times n$ matrix $A$ is positive definite if $v^TAv > 0 \space \forall \space v \in \mathbb{R}^n, \space v \neq 0$  
$\rightarrow$ $A$ is real symmetric then there exists an orthonormal basis of eigenvectors, say $\{x_1, x_2, \dots, x_n\}$