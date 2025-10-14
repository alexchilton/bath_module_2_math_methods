# Set Theory Proofs

## Problem 1: Cardinality of Power Sets

**Question:** How does $|\mathcal{P}(A)|$ relate to $|A|$?

### Small Examples

Let's examine some small sets:

- $A = \emptyset$: $\mathcal{P}(A) = \{\emptyset\}$, so $|\mathcal{P}(A)| = 1 = 2^0 = 2^{|A|}$
- $A = \{1\}$: $\mathcal{P}(A) = \{\emptyset, \{1\}\}$, so $|\mathcal{P}(A)| = 2 = 2^1 = 2^{|A|}$
- $A = \{1,2\}$: $\mathcal{P}(A) = \{\emptyset, \{1\}, \{2\}, \{1,2\}\}$, so $|\mathcal{P}(A)| = 4 = 2^2 = 2^{|A|}$
- $A = \{1,2,3\}$: $\mathcal{P}(A) = \{\emptyset, \{1\}, \{2\}, \{3\}, \{1,2\}, \{1,3\}, \{2,3\}, \{1,2,3\}\}$, so $|\mathcal{P}(A)| = 8 = 2^3 = 2^{|A|}$

**Conjecture:** $|\mathcal{P}(A)| = 2^{|A|}$

**Theorem:** For any finite set $A$, $|\mathcal{P}(A)| = 2^{|A|}$.

**Proof by induction on $|A|$:**

*Base case:* When $|A| = 0$, we have $A = \emptyset$. Then $\mathcal{P}(A) = \{\emptyset\}$, so $|\mathcal{P}(A)| = 1 = 2^0 = 2^{|A|}$.

*Inductive step:* Assume the statement holds for all sets with $n$ elements.
Let $A$ be a set with $n+1$ elements. 

We can write $A = B \cup \{x\}$ 

Then....its a bit tricky :-) work in progress....



## Problem 2: Distributivity of Intersection over Union

**Theorem:** For all sets $A$, $B$, and $C$: $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$

$$A \cap (B \cup C) = \{x \mid x \in A \text{ and } x \in B \cup C\}$$

$$= \{x \mid x \in A \text{ and } (x \in B \text{ or } x \in C)\}$$

$$= \{x \mid x \in A \text{ and } x \in B \text{ or } x \in A \text{ and } x \in C\}$$

$$= \{x \mid x \in A \cap B \text{ or } x \in A \cap C\}$$

$$= (A \cap B) \cup (A \cap C)$$



## Problem 3: Inclusion-Exclusion Principle

**Theorem:** For any finite sets $A$ and $B$: $|A \cup B| = |A| + |B| - |A \cap B|$

**Proof:** We partition the union $A \cup B$ into three sets:
1. $A \setminus B = \{x \in A : x \notin B\}$ (elements only in $A$)
2. $B \setminus A = \{x \in B : x \notin A\}$ (elements only in $B$)
3. $A \cap B$ (elements in both $A$ and $B$)

$$|A \cup B| = |A \setminus B| + |B \setminus A| + |A \cap B|$$

Now we express $|A \setminus B|$ and $|B \setminus A|$ in terms of the given quantities:
- Since $A$ is the union of $A \setminus B$ and $A \cap B$: $|A| = |A \setminus B| + |A \cap B|$
- Since $B$ is the  union of $B \setminus A$ and $A \cap B$: $|B| = |B \setminus A| + |A \cap B|$

Therefore:
- $|A \setminus B| = |A| - |A \cap B|$
- $|B \setminus A| = |B| - |A \cap B|$

Substituting back:
$$|A \cup B| = (|A| - |A \cap B|) + (|B| - |A \cap B|) + |A \cap B|$$
$$= |A| + |B| - |A \cap B| - |A \cap B| + |A \cap B|$$
$$= |A| + |B| - |A \cap B|$$