\textbf{Calculation of Covariance and Correlation}

Given data: $(1,5), (4,18), (3,17), (8,35), (1,6), (3,20)$

\textbf{Step 1: Calculate sample means}

$$\bar{X} = \frac{1 + 4 + 3 + 8 + 1 + 3}{6} = \frac{20}{6} = \frac{10}{3}$$

$$\bar{Y} = \frac{5 + 18 + 17 + 35 + 6 + 20}{6} = \frac{101}{6}$$

\textbf{Step 2: Calculate deviations and required sums}

\begin{align}
\sum_{i=1}^{6} (X_i - \bar{X})(Y_i - \bar{Y}) &= (1-\frac{10}{3})(5-\frac{101}{6}) + (4-\frac{10}{3})(18-\frac{101}{6}) \\
&\quad + (3-\frac{10}{3})(17-\frac{101}{6}) + (8-\frac{10}{3})(35-\frac{101}{6}) \\
&\quad + (1-\frac{10}{3})(6-\frac{101}{6}) + (3-\frac{10}{3})(20-\frac{101}{6})
\end{align}

Converting to common denominators:
$$X_i - \bar{X}: -\frac{7}{3}, \frac{2}{3}, -\frac{1}{3}, \frac{14}{3}, -\frac{7}{3}, -\frac{1}{3}$$

$$Y_i - \bar{Y}: -\frac{71}{6}, \frac{7}{6}, \frac{1}{6}, \frac{109}{6}, -\frac{65}{6}, \frac{19}{6}$$

$$\sum_{i=1}^{6} (X_i - \bar{X})(Y_i - \bar{Y}) = \frac{497}{18} + \frac{14}{18} - \frac{1}{18} + \frac{1526}{18} + \frac{455}{18} - \frac{19}{18} = \frac{2472}{18} = \frac{412}{3}$$

$$\sum_{i=1}^{6} (X_i - \bar{X})^2 = \frac{49}{9} + \frac{4}{9} + \frac{1}{9} + \frac{196}{9} + \frac{49}{9} + \frac{1}{9} = \frac{300}{9} = \frac{100}{3}$$

$$\sum_{i=1}^{6} (Y_i - \bar{Y})^2 = \frac{5041}{36} + \frac{49}{36} + \frac{1}{36} + \frac{11881}{36} + \frac{4225}{36} + \frac{361}{36} = \frac{21558}{36} = \frac{3593}{6}$$

\textbf{a. Sample Covariance}

$$\text{Cov}(X,Y) = \frac{1}{n-1} \sum_{i=1}^{6} (X_i - \bar{X})(Y_i - \bar{Y}) = \frac{1}{5} \cdot \frac{412}{3} = \frac{412}{15}$$

\textbf{b. Sample Correlation Coefficient}

$$s_X = \sqrt{\frac{1}{5} \cdot \frac{100}{3}} = \sqrt{\frac{20}{3}} = \frac{2\sqrt{15}}{3}$$

$$s_Y = \sqrt{\frac{1}{5} \cdot \frac{3593}{6}} = \sqrt{\frac{3593}{30}}$$

$$\rho(X,Y) = \frac{\text{Cov}(X,Y)}{s_X \cdot s_Y} = \frac{\frac{412}{15}}{\frac{2\sqrt{15}}{3} \cdot \sqrt{\frac{3593}{30}}} = \frac{412}{15} \cdot \frac{3}{2\sqrt{15}} \cdot \frac{\sqrt{30}}{\sqrt{3593}}$$

$$\rho(X,Y) = \frac{412 \sqrt{2}}{\sqrt{15 \cdot 3593}} \approx 0.891$$

\textbf{Final Answers:}
$$\text{Cov}(X,Y) = \frac{412}{15} \approx 27.47$$
$$\rho(X,Y) \approx 0.891$$