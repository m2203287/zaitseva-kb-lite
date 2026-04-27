# Examples From Photos

This file captures the key task statements and practical solution patterns from the uploaded screenshots.

## Task 9.30 (single-element domain)

Show that each interpretation on a one-element domain makes the formulas true:
- `P(x) -> P(y)`
- `P(x) <-> P(y)`
- `(exists x P(x)) -> P(y)`
- `(exists x P(x)) -> (forall x P(x))`
- `P(x) v not P(y)`
- `(forall x)(forall y)(P(x) v not P(y))`
- `P(x) -> (P(x) and P(y))`
- `(P(x) v P(y)) -> P(x)`
- `P(y) -> (forall x P(x))`

### Pattern used
- Let domain be `M={a}`.
- Only two unary predicates exist on `M`: always-false and always-true.
- Check each formula by direct substitution (`x=a`, `y=a`) and truth tables.

## Task 9.35 (satisfiable vs unsatisfiable)

Determine which formulas are satisfiable and which are identically false.

### Visible sample conclusions from photo
- `(exists x)(exists y)(P(x) and not P(y))` is satisfiable.
- `not P(x) and (forall y)(P(y))` is unsatisfiable.

### Pattern used
- For satisfiability, build one model where formula is true.
- For unsatisfiability, assume truth and derive contradiction.

## Task 9.38 (non-equivalence pairs)

Prove formulas in each pair are not equivalent.

### Pattern used
- Choose a concrete domain `M`.
- Assign concrete predicates.
- Show one formula is true and the other is false under same interpretation.

### Example from photo
For pair `(exists x)(P(x) -> Q(x))` and `(exists x P(x)) -> (exists x Q(x))`:
- Let `M={1,2}`.
- Let `P(x): x<3`, `Q(x): x<3`.
- First formula can be forced false/true differently than the implication form under chosen interpretation, establishing non-equivalence.

## Task 9.43 (tautologies of predicate logic)

Prove listed formulas are tautologies.

### Pattern used
- Use known quantifier equivalences.
- Use propositional tautologies lifted to predicate formulas.
- If needed, use proof by contradiction: assume formula false and derive impossible valuation pattern.

### Practical note
For formulas where a predicate variable does not contain a subject variable, treat it as a fixed predicate symbol and reduce the target statement to a known quantifier law.

## Table-style check pattern (from photo with truth table)

For closed formulas with predicate variables only:
1. Enumerate predicate valuations (`A0`, `A1`).
2. Evaluate each subformula column.
3. Compare columns of target formulas.
4. Equal columns imply equivalence; mismatch implies non-equivalence.
