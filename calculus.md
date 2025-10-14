# Calculus Problems: Differentiation and Integration

## Part 1: Differentiation

For each of the following functions, calculate $f'(x)$.

### **a) $f(x) = \frac{5}{1-x}$**

Rewrite as $f(x) = 5(1-x)^{-1}$

Using the chain rule:

Let $u = 1-x$, then $\frac{du}{dx} = -1$

So $f(x) = 5u^{-1}$

$\frac{df}{dx} = \frac{df}{du} \cdot \frac{du}{dx}$

$\frac{df}{du} = 5(-1)u^{-2} = -5u^{-2}$

$\frac{du}{dx} = -1$
Therefore:
$f'(x) = (-5u^{-2}) \cdot (-1) = 5u^{-2} = 5(1-x)^{-2} = \boxed{\frac{5}{(1-x)^2}}$

### **b) $f(x) = \frac{1-x}{5}$**

This can be written as $f(x) = \frac{1}{5}(1-x) = \frac{1}{5} - \frac{x}{5}$

Using the power rule:
$$f'(x) = 0 - \frac{1}{5}(1) = \boxed{-\frac{1}{5}}$$

### **c) $f(x) = \sin(2x) + \cos(3x)$**

Using the chain rule for each term:

$\frac{d}{dx}[\sin(2x)] = \cos(2x) \cdot 2 = 2\cos(2x)$

$\frac{d}{dx}[\cos(3x)] = -\sin(3x) \cdot 3 = -3\sin(3x)$

$$f'(x) = \boxed{2\cos(2x) - 3\sin(3x)}$$

### **d) $f(x) = \sin\left(4x + \frac{\pi}{2}\right)$**

Using the chain rule:
$$f'(x) = \cos\left(4x + \frac{\pi}{2}\right) \cdot 4 = \boxed{4\cos\left(4x + \frac{\pi}{2}\right)}$$

### **e) $f(x) = \sin(2x)\cos(3x)$**

Using the product rule: $(uv)' = u'v + uv'$

Let $u = \sin(2x)$, $v = \cos(3x)$

$u' = 2\cos(2x)$
$v' = -3\sin(3x)$

$$f'(x) = [2\cos(2x)][\cos(3x)] + [\sin(2x)][-3\sin(3x)]$$
$$f'(x) = \boxed{2\cos(2x)\cos(3x) - 3\sin(2x)\sin(3x)}$$

### **f) $f(x) = \sin(2\cos(3x))$**

Using the chain rule twice:
$$f'(x) = \cos(2\cos(3x)) \cdot \frac{d}{dx}[2\cos(3x)]$$
$$f'(x) = \cos(2\cos(3x)) \cdot 2 \cdot (-\sin(3x)) \cdot 3$$
$$f'(x) = \boxed{-6\sin(3x)\cos(2\cos(3x))}$$

---

## Part 2: Integration

For each of the following functions, calculate $\int f(x)dx$.

### **a) $f(x) = x^4 - x^3 + x^2$**

Using the power rule: $\int x^n dx = \frac{x^{n+1}}{n+1} + C$

$$\int (x^4 - x^3 + x^2)dx = \boxed{\frac{x^5}{5} - \frac{x^4}{4} + \frac{x^3}{3} + C}$$

### **b) $f(x) = \frac{3}{x}$**

$$\int \frac{3}{x}dx = 3\int \frac{1}{x}dx = \boxed{3\ln|x| + C}$$

### **c) $f(x) = 2\sin x + 3\cos x$**

$$\int (2\sin x + 3\cos x)dx = 2\int \sin x dx + 3\int \cos x dx = \boxed{-2\cos x + 3\sin x + C}$$

### **d) $f(x) = 5e^x - e$**

$$\int (5e^x - e)dx = 5\int e^x dx - e\int dx = \boxed{5e^x - ex + C}$$

### **e) $f(x) = 2x\sin(4x)$**

This requires integration by parts: $\int u dv = uv - \int v du$

Let $u = 2x$, $dv = \sin(4x)dx$

Then $du = 2dx$, $v = -\frac{\cos(4x)}{4}$

$$\int 2x\sin(4x)dx = 2x \cdot \left(-\frac{\cos(4x)}{4}\right) - \int \left(-\frac{\cos(4x)}{4}\right) \cdot 2dx$$

$$= -\frac{x\cos(4x)}{2} + \frac{1}{2}\int \cos(4x)dx$$

$$= -\frac{x\cos(4x)}{2} + \frac{1}{2} \cdot \frac{\sin(4x)}{4}$$

$$= \boxed{-\frac{x\cos(4x)}{2} + \frac{\sin(4x)}{8} + C}$$

### **f) $f(x) = x^2e^x$**

This requires integration by parts twice.

**First application:** Let $u = x^2$, $dv = e^x dx$

Then $du = 2x dx$, $v = e^x$

$$\int x^2 e^x dx = x^2 e^x - \int e^x (2x)dx = x^2 e^x - 2\int xe^x dx$$

**For $\int xe^x dx$, use integration by parts again:**

Let $u = x$, $dv = e^x dx$, then $du = dx$, $v = e^x$

$$\int xe^x dx = xe^x - \int e^x dx = xe^x - e^x$$

**Therefore:**
$$\int x^2 e^x dx = x^2 e^x - 2(xe^x - e^x) = x^2 e^x - 2xe^x + 2e^x$$

$$= \boxed{e^x(x^2 - 2x + 2) + C}$$