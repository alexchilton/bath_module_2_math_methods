\textbf{1. Expectation for Uniform Distribution on [a,b]}

For a uniform distribution on $[a,b]$, the probability density function is:
$$f(x) = \begin{cases}
\frac{1}{b-a} & \text{if } a \leq x \leq b \\
0 & \text{otherwise}
\end{cases}$$

The expectation is:
$$E[X] = \int_{-\infty}^{\infty} x f(x) \, dx = \int_{a}^{b} x \cdot \frac{1}{b-a} \, dx$$

$$E[X] = \frac{1}{b-a} \int_{a}^{b} x \, dx = \frac{1}{b-a} \left[ \frac{x^2}{2} \right]_{a}^{b}$$

$$E[X] = \frac{1}{b-a} \cdot \frac{1}{2}(b^2 - a^2) = \frac{1}{b-a} \cdot \frac{1}{2}(b-a)(b+a)$$

$$E[X] = \frac{b+a}{2}$$

\textbf{2. Distribution Function for Exponential Distribution with Parameter λ}

For an exponential distribution with parameter $\lambda > 0$, the probability density function is:
$$f(x) = \begin{cases}
\lambda e^{-\lambda x} & \text{if } x \geq 0 \\
0 & \text{if } x < 0
\end{cases}$$

The cumulative distribution function (CDF) is:
$$F(x) = P(X \leq x) = \int_{-\infty}^{x} f(t) \, dt$$

For $x < 0$: $F(x) = 0$

For $x \geq 0$:
$$F(x) = \int_{0}^{x} \lambda e^{-\lambda t} \, dt$$

$$F(x) = \lambda \left[ \frac{e^{-\lambda t}}{-\lambda} \right]_{0}^{x} = \lambda \cdot \frac{1}{-\lambda}(e^{-\lambda x} - e^{0})$$

$$F(x) = -(e^{-\lambda x} - 1) = 1 - e^{-\lambda x}$$

Therefore, the distribution function is:
$$F(x) = \begin{cases}
0 & \text{if } x < 0 \\
1 - e^{-\lambda x} & \text{if } x \geq 0
\end{cases}$$