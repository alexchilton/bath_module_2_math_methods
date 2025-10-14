# Logic Questions

## Question 1: Translate the following sentences into propositional logic

### a) The flat is vacant.

Let V = "The flat is vacant"

**Translation: V**

This is straightforward - a simple atomic proposition.

### b) The flat can be let only if it is vacant and has been cleaned.

Let V = "The flat is vacant"

Let C = "The flat has been cleaned"

Let L = "The flat can be let"

The phrase "can be let only if" indicates a conditional relationship. "A only if B" means "if A then B", or A → B.

**Translation: L → (V ∧ C)**

### c) Don't drink and drive!

Let D = "You drink"

Let R = "You drive"

This imperative sentence is commanding someone not to do both actions simultaneously.

**Translation: ¬(D ∧ R)**

## Question 2 [6]: Translate the following sentences into predicate logic

Your formalizations should be as detailed as possible.

### a) Some teachers are strict and others are not.

This sentence asserts two things:

Some teachers are strict

Some teachers are not strict

There exists someone who is a teacher and is strict, and there exists someone who is a teacher and is not strict.

Let Domain: All people

Let T(x) = "x is a teacher"

Let S(x) = "x is strict"

**Translation: ∃x(T(x) ∧ S(x)) ∧ ∃y(T(y) ∧ ¬S(y))**

### b) Some dogs' owners do not collect their dog's litter

There exists a person x and a dog y and x owns y and x does not collect y's litter.

Let Domain: All people and dogs
Let P(x) = "x is a person"
Let D(x) = "x is a dog"
Let O(x,y) = "x owns y"
Let C(x,y) = "x collects the litter of y"

**Translation: ∃x∃y(P(x) ∧ D(y) ∧ O(x,y) ∧ ¬C(x,y))**

### c) All animals are equal.

We interpret this as a universal statement about all pairs of animals.

For all x and y, if x is an animal and y is an animal, then x is equal to y.

Let Domain: All entities
Let A(x) = "x is an animal"
Let E(x,y) = "x is equal to y"

**Translation: ∀x∀y((A(x) ∧ A(y)) → E(x,y))**

## Question 3 [6]: Consider the following formula of propositional logic

**P = ((A ∨ B) ∧ C → (A ∧ B) ∨ C)**

### a) Assume that A is true, and B,C are false. Is P true or false? Briefly explain why.

Given: A = T, B = F, C = F

A ∨ B = T ∨ F = T

(A ∨ B) ∧ C = T ∧ F = F

A ∧ B = T ∧ F = F

(A ∧ B) ∨ C = F ∨ F = F

P = ((A ∨ B) ∧ C) → ((A ∧ B) ∨ C) = F → F = T

**P is true.**

This is because a conditional statement (→) is true whenever the antecedent is false, regardless of the truth value of the consequent.

### b) Which truth values for A,B,C will result in P being false?

For P to be false, we need the antecedent ((A ∨ B) ∧ C) to be true and the consequent ((A ∧ B) ∨ C) to be false.

For the antecedent to be true:

(A ∨ B) must be true, so at least one of A or B must be true

C must be true

For the consequent to be false:

(A ∧ B) must be false, so at least one of A or B must be false

C must be false

However, this creates a contradiction: C cannot be both true (for the antecedent) and false (for the consequent) simultaneously.

Therefore, **P is always true (it's a tautology)** - there are no truth value assignments that make P false.

