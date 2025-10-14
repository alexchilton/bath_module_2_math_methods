\textbf{1. Sample Space of X}

$\{2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12\}$

\textbf{2. Probabilities P(X = x)}

\begin{align}
P(X=2) &= \frac{1}{36} \\
P(X=3) &= \frac{2}{36} = \frac{1}{18} \\
P(X=4) &= \frac{3}{36} = \frac{1}{12} \\
P(X=5) &= \frac{4}{36} = \frac{1}{9} \\
P(X=6) &= \frac{5}{36} \\
P(X=7) &= \frac{6}{36} = \frac{1}{6} \\
P(X=8) &= \frac{5}{36} \\
P(X=9) &= \frac{4}{36} = \frac{1}{9} \\
P(X=10) &= \frac{3}{36} = \frac{1}{12} \\
P(X=11) &= \frac{2}{36} = \frac{1}{18} \\
P(X=12) &= \frac{1}{36}
\end{align}

\textbf{3. PMF and CDF}

PMF:
$$f(x) = P(X = x) = \begin{cases}
\frac{1}{36} & \text{if } x = 2, 12 \\
\frac{2}{36} & \text{if } x = 3, 11 \\
\frac{3}{36} & \text{if } x = 4, 10 \\
\frac{4}{36} & \text{if } x = 5, 9 \\
\frac{5}{36} & \text{if } x = 6, 8 \\
\frac{6}{36} & \text{if } x = 7 \\
0 & \text{otherwise}
\end{cases}$$

CDF:
$$F(x) = P(X \leq x) = \begin{cases}
0 & \text{if } x < 2 \\
\frac{1}{36} & \text{if } 2 \leq x < 3 \\
\frac{3}{36} & \text{if } 3 \leq x < 4 \\
\frac{6}{36} & \text{if } 4 \leq x < 5 \\
\frac{10}{36} & \text{if } 5 \leq x < 6 \\
\frac{15}{36} & \text{if } 6 \leq x < 7 \\
\frac{21}{36} & \text{if } 7 \leq x < 8 \\
\frac{26}{36} & \text{if } 8 \leq x < 9 \\
\frac{30}{36} & \text{if } 9 \leq x < 10 \\
\frac{33}{36} & \text{if } 10 \leq x < 11 \\
\frac{35}{36} & \text{if } 11 \leq x < 12 \\
1 & \text{if } x \geq 12
\end{cases}$$

\textbf{4. Bernoulli Distribution}

\begin{align}
\text{a. } E(X) &= p \\
\text{b. } E(X^2) &= p \\
\text{c. } \text{Var}(X) &= p(1-p)
\end{align}

\textbf{5. Poisson Distribution}

The smallest integer value of $\lambda$ is $7$.

Working:
\begin{align}
P(X \geq 2) &= 1 - P(X = 0) - P(X = 1) \\
&= 1 - e^{-\lambda} - \lambda e^{-\lambda} \\
&= 1 - e^{-\lambda}(1 + \lambda) > 0.99 \\
\therefore e^{-\lambda}(1 + \lambda) &< 0.01 \\
\text{For } \lambda = 7: e^{-7}(1 + 7) &= 8e^{-7} \approx 0.0073 < 0.01 \checkmark
\end{align}