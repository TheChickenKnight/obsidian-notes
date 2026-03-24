Given the basic variables + order, can we find the OS?
Given $\begin{vmatrix}x_1\\x_5\\x_2\end{vmatrix}$ , and the LP

$$\begin{vmatrix}
&x_{1} & x_{2} & x_{3} & x_{4} & x_{5} & z \\  
x_{3}&3&-2&1&0&0&0&5 \\ 
x_{4}&1&1&0&1&0&0&4 \\
x_{5}&1&2&0&0&1&0&6 \\   
&-2&-1&0&0&0&1&0

\end{vmatrix}$$

We already know the columns
$$\begin{vmatrix}
&x_{1} & x_{2} & x_{3} & x_{4} & x_{5} & z \\  
x_{1}&1&0&&&0&0&& \\ 
x_{5}&0&0&&&1&0& \\
x_{2}&0&1&&&0&0& \\
\\
\end{vmatrix}$$

We can find the rest by creating Matrix $B$ from the columns of the original LP that line up with the OS's basic variables.

$$B =\begin{vmatrix} 
3&0&-2\\ 
1&0&1\\
1&1&2

\end{vmatrix}
\begin{vmatrix} 
1&0&0\\ 
0&1&0\\
0&0&1

\end{vmatrix}$$
 finding the inverse,
$$B^{-1} =\begin{vmatrix} 
\frac{1}{5}& \frac{2}{5}&0\\ 
\frac{1}{5}&-\frac{8}{5}&1\\
-\frac{1}{5}& \frac{3}{5}&0
\end{vmatrix}$$
and then using $\vec{x_b}=B^{-1}\vec{b}$ 
$$B^{-1} =\begin{vmatrix} 
\frac{1}{5}& \frac{2}{5}&0\\ 
\frac{1}{5}&-\frac{8}{5}&1\\
-\frac{1}{5}& \frac{3}{5}&0
\end{vmatrix}
\begin{vmatrix}
5 \\
4 \\
6
\end{vmatrix}=
\begin{vmatrix}
\frac{13}{5} \\
\frac{3}{5} \\
\frac{7}{5}
\end{vmatrix}$$

For the objective row, we can use $OR_j-C_j+\vec{C_B}^T\vec{t_j}$, which is row reducing.
$$OR_{3}=-0+2(\frac{1}{5})+0(\frac{1}{5})+1(-\frac{1}{5})$$