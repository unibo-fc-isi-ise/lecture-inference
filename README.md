## Knowledge Representation
with Horn Clauses

### Goals

- Understand basic notions such as:
    * unifiers and substitutions
    * unification and MGU
    * SLD resolution
    * Prolog's reasoning

### Overview
- Two powerful mechanisms:
    * Unification: computes a substitution making two terms/clauses equal
    * Resolution: attempts to prove a goal true or not
    * Both rely on the notion of subtitution
- Substitution:
    * a relation among variables and terms
    * can be empty
    * can be applied to terms, rewriting them (hence producing new terms)
    * as sets, can be merged
    + exercise on the creation / application / merging of substitutions
- Unifier [among 2 terms]: a substitution making 2 terms equal
    * computed via some unification algorithm
    * we're commonly interested in the *most general* unifier (example of non-general unifier)
- Unification: algorithms to compute the most general unifier (MGU) among 2 terms 
    * Unification table
    * Mention the Martelli and Montanari algorithm
- Resolution
    - Goal: decide whether a set of formulae in Skolem form is satisfiable
    - SL resolution algorithm:
        0. remove quantifiers => make the formulae a collection predicates connected by logic connective
        1. exploit equivalence among logic connectives to transform all formulae in CNF
            - i.e. a bunch of positive/negative predicates connected via disjunction
        2. if any two formulae contain 2 opposite literals (w.r.t. to some substitution)
            - remove them both literals, rewriting the 2 formulae without them
            - apply the substitutions to all formulae
        3. if any formula is now empty => stop: the set of formulae is inconsistent
            - otherwise, repeat step 2
    - search space is HUGE
        - which couple of literals should be selected at each step?


