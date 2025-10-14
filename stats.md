# Mathematics for AI - Problem Sheet 2 Solutions

## Question 1 [15%]

### a) Three components of a probability space [6]

The three components that define a probability space are:[^1]

**Sample Space (Ω)**: The set of all possible outcomes.
For two dice: Ω = {(1,1), (1,2), (1,3), ..., (6,6)}
Total of 36 possible outcomes

**Event Space (F)**: The collection of all possible events (subsets of the sample space)
For example: "both dice show even numbers" = {(2,2), (2,4), (2,6), (4,2), (4,4), (4,6), (6,2), (6,4), (6,6)}

**Probability Measure (P)**: A function that assigns probabilities to events
For fair dice: P(each outcome) = 1/36
P must satisfy: 0 ≤ P(A) ≤ 1 for any event A, and P(Ω) = 1

### b) Unfair dice [2]

If the dice are not fair, only the **probability measure** changes. The sample space and event space remain the same, but P(each outcome) is no longer 1/36. Some outcomes become more likely than others.

### c) Summing dice values [3]

When we sum the dice values, the sample space changes to:

New sample space: {2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12}

The event space now consists of subsets of these sums

Probabilities are no longer uniform: P(sum = 7) = 6/36 = 1/6, but P(sum = 2) = 1/36

### d) Thousand dice [4] 


With 1000 dice, the probability distribution of the sum would approach a **normal distribution** due to the Central Limit Theorem.[^2]

Expected value: E(sum) = 1000 × 3.5 = 3500

The distribution becomes bell-shaped and symmetric around 3500

Most values cluster near the mean, with very low probability of extreme values

This happens because we're adding many independent random variables

## Question 2 [15%]

**Setup**: 4 red, 3 blue, 1 green ball (8 total). **With replacement** initially.

### a) P(BG) [3]

P(BG) = P(Blue first) × P(Green second)

= (3/8) × (1/8) = 3/64

### b) P(G) [3]

P(G) = P(Green on first draw OR Green on second draw)

= P(G₁) + P(G₂) - P(G₁ ∩ G₂)

= (1/8) + (1/8) - (1/8 × 1/8)

= 1/8 + 1/8 - 1/64 = 8/64 + 8/64 - 1/64 = 15/64

### c) P(R₂|B₁) [3]

Since we replace the ball, the second draw is independent of the first.

P(R₂|B₁) = P(R₂) = 4/8 = 1/2

### d) Without replacement [6]

#### i) P(BG) [2]
P(BG) = P(Blue first) × P(Green second | Blue first)
= (3/8) × (1/7) = 3/56

#### ii) P(G) [2]
P(G) = P(G₁) + P(G₂|not G₁)
= (1/8) + (7/8) × (1/7) = 1/8 + 1/8 = 1/4

#### iii) P(R₂|B₁) [2]
P(R₂|B₁) = 4/7 (since after removing a blue ball, 7 balls remain, 4 of which are red)

## Question 3 [15%]

**Given**:

P(STEM) = 0.3, so P(non-STEM) = 0.7

P(Pass|STEM) = 0.8

P(Pass|non-STEM) = 0.6

**Find**: P(STEM|Pass)

Using Bayes' theorem:

P(STEM|Pass) = P(Pass|STEM) × P(STEM) / P(Pass)

First, find P(Pass):
P(Pass) = P(Pass|STEM) × P(STEM) + P(Pass|non-STEM) × P(non-STEM)
= 0.8 × 0.3 + 0.6 × 0.7 = 0.24 + 0.42 = 0.66

Therefore:
P(STEM|Pass) = (0.8 × 0.3) / 0.66 = 0.24 / 0.66 = 4/11 ≈ 0.364

**Answer**: 36.4%

## Question 4 [15%]

**Given**: Average of 2 calls every 5 minutes, Poisson distribution  
**Find**: Minimum agents needed so calls are on hold ≤ 1% of time

For a Poisson distribution with λ = 2:[^3]

We need P(X > n) ≤ 0.01, where n is the number of agents available and X is the number of calls arriving.

### Poisson Probability Calculations

For a Poisson distribution with parameter λ = 2:

**Individual probability formula:**
$$P(X = k) = \frac{e^{-2} \cdot 2^k}{k!}$$

Where e^(-2) ≈ 0.1353

**Individual probabilities:**

P(X = 0) = (0.1353 × 2^0) / 0! = 0.1353

P(X = 1) = (0.1353 × 2^1) / 1! = 0.2706  

P(X = 2) = (0.1353 × 2^2) / 2! = 0.2706

P(X = 3) = (0.1353 × 2^3) / 3! = 0.1804

P(X = 4) = (0.1353 × 2^4) / 4! = 0.0902

P(X = 5) = (0.1353 × 2^5) / 5! = 0.0361

P(X = 6) = (0.1353 × 2^6) / 6! = 0.0120

**Cumulative probabilities:**

P(X ≤ 4) = 0.1353 + 0.2706 + 0.2706 + 0.1804 + 0.0902 = 0.9471

P(X ≤ 5) = 0.9471 + 0.0361 = 0.9832

P(X ≤ 6) = 0.9832 + 0.0120 = 0.9952

### Analysis

We need P(X > n) ≤ 0.01:

With 6 agents: P(X > 6) = 1 - P(X ≤ 6) = 1 - 0.9952 = 0.0048 

With 5 agents: P(X > 5) = 1 - P(X ≤ 5) = 1 - 0.9832 = 0.0168 

Since P(X > 6) = 0.0048 < 0.01, we need enough agents to handle up to 6 calls without anyone being placed on hold.

**Answer**: 7 agents are needed

## Question 5 [10%]

descriptive statistics, covariance and sample and population sizes[^4]

**Data**: [11, 31], [8, 16], [5, 21], [9, 34], [12, 14], [13, 17]

### a) Covariance calculation [8]

First, find the means:

$\bar{x} = \frac{11 + 8 + 5 + 9 + 12 + 13}{6} = \frac{58}{6} = 9.67$

$\bar{y} = \frac{31 + 16 + 21 + 34 + 14 + 17}{6} = \frac{133}{6} = 22.17$

Sample covariance formula: $s_{xy} = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})$

| $x_i$ | $y_i$ | $x_i - \bar{x}$ | $y_i - \bar{y}$ | $(x_i - \bar{x})(y_i - \bar{y})$ |
|-------|-------|----------------|----------------|----------------------------|
| 11    | 31    | 1.33           | 8.83           | 11.74                     |
| 8     | 16    | -1.67          | -6.17          | 10.30                     |
| 5     | 21    | -4.67          | -1.17          | 5.46                      |
| 9     | 34    | -0.67          | 11.83          | -7.93                     |
| 12    | 14    | 2.33           | -8.17          | -19.04                    |
| 13    | 17    | 3.33           | -5.17          | -17.22                    |

Sum = 11.74 + 10.30 + 5.46 - 7.93 - 19.04 - 17.22 = -16.69

$s_{xy} = \frac{-16.69}{5} = -3.34$

### b) Population vs Sample [2]

If this was the whole population, we would use the population covariance formula with denominator n instead of n-1:

$\sigma_{xy} = \frac{-16.69}{6} = -2.78$

The difference is we divide by n rather than n-1 for population covariance.

## Question 6 [15%]

**Given**: X ~ Uniform(0,1), Y = eˣ

### a) CDF of Y [6]

For Y = eˣ where X ~ Uniform(0,1):

Range of Y: [e⁰, e¹] = [1, e]

For y ∈ [1, e]:
F_Y(y) = P(Y ≤ y) = P(eˣ ≤ y) = P(X ≤ ln(y)) = ln(y)

(since X ~ Uniform(0,1), so F_X(x) = x for x ∈ [0,1])

Therefore:
$$F_Y(y) = \begin{cases} 
0 & \text{if } y < 1 \\
\ln(y) & \text{if } 1 \leq y \leq e \\
1 & \text{if } y > e
\end{cases}$$

### b) PDF of Y [4]

Using the transformation method for continuous random variables:

$$f_Y(y) = f_X(x(y)) \left|\frac{dx}{dy}\right|$$

Where:

$y = e^x \Rightarrow x = \ln(y)$

$\frac{dx}{dy} = \frac{d}{dy}[\ln(y)] = \frac{1}{y}$

$f_X(x) = 1$ for $x \in [0,1]$

Therefore:
$$f_Y(y) = f_X(\ln(y)) \left|\frac{1}{y}\right| = 1 \cdot \frac{1}{y} = \frac{1}{y}$$

for $y \in [1, e]$, and 0 otherwise.

### c) E(Y) [^5]

Using the definition of expected value for continuous random variables:

$$E(Y) = \int_{1}^{e} y \cdot \frac{1}{y} dy = \int_{1}^{e} 1 dy = [y]_{1}^{e} = e - 1$$

**Answer**: E(Y) = e - 1 ≈ 1.718


## Question 7 [15%] 

Using info learnt from Zedstatistics website [4]

**Data**: 1.647, 1.695, 1.703, 1.727, 1.784, 1.651, 1.764, 1.723

### a) Hypotheses [4]

**H₀**: μ = 1.75 (filament meets industry standard)

**H₁**: μ ≠ 1.75 (filament does not meet industry standard)

### b) P-value analysis [6]

Sample statistics:

n = 8

$\bar{x} = \frac{1.647 + 1.695 + 1.703 + 1.727 + 1.784 + 1.651 + 1.764 + 1.723}{8} = 1.712$

$s = 0.048$ (sample standard deviation)

Test statistic: 
$t = \frac{\bar{x} - \mu_0}{s/\sqrt{n}} = \frac{1.712 - 1.75}{0.048/\sqrt{8}} = \frac{-0.038}{0.017} = -2.24$

With df = 7 and α = 0.05 (two-tailed), critical value ≈ ±2.365

Since |t| = 2.24 < 2.365, we **fail to reject H₀**.

The p-value ≈ 0.06 > 0.05, so the filament should be **approved**.

### c) Type of test [2]

This is a **two-tailed test** because we're testing whether the diameter differs from 1.75mm (either too high or too low).

### d) Type I and II Errors [2]

**Type I Error**: Rejecting good filament (saying it's defective when it's actually fine)

Consequence: Wasted materials and production costs

**Type II Error**: Accepting bad filament (saying it's fine when it's actually defective)

Consequence: Poor quality products reach customers, reputation damage

### e) Reducing error risk [1]

**Increase sample size** - taking more measurements would reduce the standard error and make the test more reliable.

REFERENCES:

[^1] Bath University. (2024). Course Materials. Retrieved from 

https://engage.bath.ac.uk/learn/mod/page/view.php?id=289625&forceview=1

[^2] Ross, S. M. (2017). *A First Course in Probability* (10th ed.). Pearson. Chapter 8: Limit Theorems.

[^3] Ross, S. M. (2017). *A First Course in Probability* (10th ed.). Pearson. Chapter 4.7: The Poisson Random Variable.

[^4] Zed Statistics. (2024). Covariance and Descriptive Statistics [Video series]. YouTube. https://www.youtube.com/@zedstatistics

[^5] Ross, S. M. (2017). *A First Course in Probability* (10th ed.). Pearson. Chapter 5 Continuous Random Variables 

Some formatting by copilot inside visual studio code.