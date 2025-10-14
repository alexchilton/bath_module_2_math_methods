\textbf{1. Card Drawing Problems}

\textbf{a. With Replacement}

Let $A$ = "first card is Hearts", $B$ = "second card is Hearts", $C$ = "cards have different suits"

Both cards are Hearts:
$$P(A \cap B) = P(A) \times P(B) = \frac{13}{52} \times \frac{13}{52} = \frac{1}{4} \times \frac{1}{4} = \frac{1}{16}$$

Cards are different suits:
$$P(C) = 1 - P(\text{same suit}) = 1 - 4 \times \left(\frac{1}{4}\right)^2 = 1 - \frac{1}{4} = \frac{3}{4}$$

\textbf{b. Without Replacement}

Let $A$ = "first card is Hearts", $B$ = "second card is Hearts", $C$ = "cards have different suits"

Both cards are Hearts:
$$P(A \cap B) = P(A) \times P(B|A) = \frac{13}{52} \times \frac{12}{51} = \frac{1}{4} \times \frac{4}{17} = \frac{1}{17}$$

Cards are different suits:
$$P(C) = 1 - P(\text{same suit}) = 1 - 4 \times \frac{1}{17} = 1 - \frac{4}{17} = \frac{13}{17}$$

\textbf{2. Bayes' Theorem Problem}

Given:
- $P(\text{Fire}) = 0.005$
- $P(\text{Smoke}) = 0.15$ 
- $P(\text{Smoke}|\text{Fire}) = 0.9$

Using Bayes' Theorem:
$$P(\text{Fire}|\text{Smoke}) = \frac{P(\text{Smoke}|\text{Fire}) \times P(\text{Fire})}{P(\text{Smoke})}$$

$$P(\text{Fire}|\text{Smoke}) = \frac{0.9 \times 0.005}{0.15} = \frac{0.0045}{0.15} = 0.03 = 3\%$$

\textbf{3. Proofs of Probability Space Properties}

\textbf{Property 1:} $P(\Omega \setminus A) = 1 - P(A)$

\textit{Proof:} Since $A$ and $\Omega \setminus A$ are disjoint and $A \cup (\Omega \setminus A) = \Omega$:
$$P(\Omega) = P(A) + P(\Omega \setminus A)$$
$$1 = P(A) + P(\Omega \setminus A)$$
$$\therefore P(\Omega \setminus A) = 1 - P(A)$$

\textbf{Property 2:} If $A \subseteq B$ then $P(B) = P(A) + P(B \setminus A) \geq P(A)$

\textit{Proof:} Since $A \subseteq B$, we can write $B = A \cup (B \setminus A)$ where $A$ and $B \setminus A$ are disjoint:
$$P(B) = P(A) + P(B \setminus A)$$
Since $P(B \setminus A) \geq 0$:
$$P(B) = P(A) + P(B \setminus A) \geq P(A)$$

\textbf{Property 3:} $P(A \cup B) = P(A) + P(B) - P(A \cap B)$

\textit{Proof:} We can decompose $A \cup B$ into disjoint sets:
$$A \cup B = (A \setminus B) \cup (A \cap B) \cup (B \setminus A)$$
$$P(A \cup B) = P(A \setminus B) + P(A \cap B) + P(B \setminus A)$$

Since $A = (A \setminus B) \cup (A \cap B)$ and $B = (B \setminus A) \cup (A \cap B)$:
$$P(A) = P(A \setminus B) + P(A \cap B) \implies P(A \setminus B) = P(A) - P(A \cap B)$$
$$P(B) = P(B \setminus A) + P(A \cap B) \implies P(B \setminus A) = P(B) - P(A \cap B)$$

Substituting:
$$P(A \cup B) = [P(A) - P(A \cap B)] + P(A \cap B) + [P(B) - P(A \cap B)]$$
$$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$