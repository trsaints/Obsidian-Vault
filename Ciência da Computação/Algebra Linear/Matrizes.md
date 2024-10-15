Uma matriz de ordem m por n é um quadro de `m * n` números, dispostos em `m` linhas e `n` colunas.

Se $$m = n$$, a matriz é retangular.

Se $$m = n$$, a matriz é quadrada.

Cada elemento `a` de uma matriz `A` tem dois índices, i e j.

`a(i,j)` -> i: linha, j: coluna


$$
\begin{matrix}
a_{1,1} & a_{1,2} & a_{1,3} \\
a_{2,1} & a_{2,2} & a_{2,3} \\
a_{3,1} & a_{3,2} & a_{3,3} \\
\end{matrix}
$$
## Dimensões de uma matriz

Se a matriz tem 1 coluna, $$A_{m,1}$$, esta é chamada de matriz-coluna.

Se a matriz tem 1 linha, 
$$A_{1,n}$$, esta é chamada de matriz/vetor-linha.
## Diagonais de matrizes quadradas

Seja a matriz $$A_3$$ Uma matriz de 3 linhas e 3 colunas: 
$$
\begin{matrix}
a_{1,1} & a_{1,2} & a_{1,3} \\
a_{2,1} & a_{2,2} & a_{2,3} \\
a_{3,1} & a_{3,2} & a_{3,3} \\
\end{matrix}
$$

* Diagonal Principal: Elementos da matriz A, $$a_{i,j}$$ em que $$i=j$$Nesse caso, temos que os elementos da diagonal principal são: 
  $$\{a_{1,1},a_{2,2},a_{3,3}\}$$
* Diagonal secundária: Elementos da matriz A,
$$a_{i,j}$$ em que $$i+j=n+1$$Nesse caso, temos que os elementos da diagonal secundária são:
$$\{a_{1,3},a_{2,2},a_{3,1}\}$$
## Matriz diagonal
$$\forall x \in A:i\neq j\implies a_{i,j}\neq 0$$
Exemplo:
$$A_3=
\begin{matrix}
1 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 3 \\
\end{matrix}
$$
## Matriz unidade (ou matriz Identidade)
$$\begin{align} \forall a_{i,j} \in A:i\neq j \implies a_{i,j}=0
\\  i=j \implies a_{i,j}=1 \end{align}$$
Exemplos:
$$
\begin{align}
I_2=\begin{matrix} 1 & 0 \\ 0 & 1 \end{matrix} \\
\\
I_3=\begin{matrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{matrix}
\end{align}
$$
Uma propriedade importante da matriz identidade é: ela é o elemento neutro das matrizes.
Ou seja: $$A*I=I*A=A$$, para as matrizes A e I de mesma ordem.

## Matriz oposta
$$\begin{align}  \exists B=[b_{i,j}]:B=-A, \\ A=[a_{i,j}] \end{align}$$
Exemplo:
$$\begin{align}
A=\begin{matrix} 4 & 1 \\ -3 & 8 \end{matrix}
\implies -A=\begin{matrix} -4 & -1 \\ 3 & -8 \end{matrix} \end{align}$$
## Matriz triangular

Possuem somente zeros acima ou abaixo da diagonal, conforme os dois exemplos abaixo.
### Triangular superior
$$\begin{align}
\forall a_{i,j} \in A=[a_{i,j}]:i>j \implies a_{i,j} = 0 \\ \\ Exemplo:
A = \begin{matrix}
1 & 3 & 4 \\
0 & 2 & -7 \\
0 & 0 & -1
\end{matrix}
\end{align}$$
---
### Triangular inferior
$$\begin{align}
\forall a_{i,j} \in A=[a_{i,j}]:i<j \implies a_{i,j} = 0 \\ \\ Exemplo:
A = \begin{matrix}
2 & 0 & 0 \\
5 & 6 & 0 \\
-3 & -4 & 3
\end{matrix}
\end{align}$$
---
## Igualdade entre matrizes
$$
\begin{align}
A=B \iff a_{i,j}=b_{i,j},
\\ \forall a_{i,j} \in A,
\\ \forall b_{i,j} \in B

\end{align}
$$
## Soma de matrizes (de mesma ordem)
$$
\begin{align}

A=\begin{matrix}
a_{1,1} & a_{1,2} & a_{1,3} \\
a_{2,1} & a_{2,2} & a_{2,3}
\end{matrix} 
,\ \ \ \ B =\begin{matrix}
b_{1,1} & b_{1,2} & b_{1,3} \\
b_{2,1} & b_{2,2} & b_{2,3}
\end{matrix}
\implies
C=\begin{matrix}
a_{1,1} + b_{1,1} & a_{1,2} + b_{1,2} & a_{1,3} + b_{1,3} \\
a_{2,1} + b_{2,1} & a_{2,2} + b_{2,2} & a_{2,3} + b_{2,3}
\end{matrix}
\end{align}
$$
## Diferença de matrizes (de mesma ordem)
$$
\begin{bmatrix} 
4 & -1 \\
-3 & 0
\end{bmatrix}
 -
 \begin{bmatrix} 
5 & -6 \\
7 & -8
\end{bmatrix}
=
 \begin{bmatrix} 
-1 & 5 \\
-10 & 17
\end{bmatrix}
$$
Propriedades notáveis:
 $$
 A+(B+C)=(A+B)+C
 $$
$$A+B=B+A$$
$$A+0=0+A=A$$
$$A+(-A)=-A+A=0$$
## Produto matriz por escalar
$$
\lambda A = B: B=[b_{i,j}], b_{i,j}=\lambda a_{i,j},\forall a_{i,j} \in A
$$
Exemplo:
$$
5 \times 
\begin{bmatrix}
4 & -2 & 1 \\
3 & 5 & -3
\end{bmatrix}
=
\begin{bmatrix}
20 & -10 & 5 \\
15 & 25 & -15
\end{bmatrix}
$$
Propriedades notáveis:
$$(\alpha \times \beta)\times A = \alpha \times (A \times \beta), \forall \alpha,\beta \in \mathbb{R}$$
$$(\alpha + \beta)\times A = \alpha \times A + \beta \times A$$
$$\alpha(A + B)=\alpha A+\alpha B$$
$$1\times A = A$$
## Produto entre matrizes
$$A_{1\times3} \cdot B_{3\times1}=C_{1\times1} $$
C é a soma dos produtos na ordem em que A e B estão dispostos:
$$
A_{m\times n}\cdot B_{p\times q} \iff n = p
$$
Exemplo
$$
\begin{bmatrix}
4 & 2 & 6 \\
2 & 5 & 3
\end{bmatrix}_{2\times3}
\times
\begin{bmatrix}
5 & 2 & 4 & 1 \\
2 & 3 & 1 & 0 \\
1 & 2 & 7 & 6
\end{bmatrix}_{3\times4}
=
\begin{bmatrix}
4\cdot5+2\cdot2+6\cdot1 &
4\cdot2+2\cdot3+6\cdot2 &
4\cdot4+2\cdot1+6\cdot7
\\
2\cdot5+5\cdot2+3\cdot1 &
2\cdot2+5\cdot3+3\cdot2 &
2\cdot4+5\cdot1+3\cdot7
\end{bmatrix}_{2\times4}
$$