# Prototyping Graphical Programming Languages 

This repository contains a first attempt to build a tool for reasoning with wiring diagrams.

The diagram language we have chosen is [Graphical Regular Logic](https://arxiv.org/abs/1812.05765). This is an intuitive, graphical way of capturing the 'regular' fragment of first order logic, in which we are allowed free use of AND, TRUE, and THERE EXISTS, and a single use of IMPLIES, and a use of FOR ALL that is scoped over the entire logical expression. We have chosen this fragment as it is powerful enough to be useful (eg. to make [conjunctive queries](https://en.wikipedia.org/wiki/Conjunctive_query)), limited enough for the logic to be decideable, and basic enough to expand in versatile directions (eg. to the logic of abelian categories and cohomology, or to coherent, geometric, and constructive first order logic).

The backend will implement the categorical ideas of [Graphical Regular Logic](https://arxiv.org/abs/1812.05765) and [Hypergraph Categories](https://arxiv.org/abs/1806.08304), based primarily on cospans and lax monoidal functors to Set. This rigorous foundation will ensure the data structures used for the language are fit to act as a foundation for future development.

The frontend will run in-browser, allowing use of the tool without installation of a local copy. Terms in the language may be built by simply dragging and dropping icons, and clicking to connect wires, just as one can might build a circuit diagram. This easy interface will ensure that users can take advantage of the formal language without themselves needing to study category theory and mathematical logic.

As a first application, the graphical language will compile to SQL, allowing the tool to be used to make graphical database queries.

We will also create an easy-to-use, yet sound and complete set of graphical deduction rules, based largely around breaking wires. This will allow the tool to be used not just to create formal logical expressions, but reason about implications between them. In the database semantics this will let us reason about query inclusion. Once they specify predicate symbols (like a symbol for each database table), users will also be able to specify addition axioms that will help them reason about terms in these symbols. These axioms could also be discovered from the database semantics itself.



## Specification

A link to an evolving specification document is [here](https://docs.google.com/document/d/1380RFV-DmQ4hXrc0k3HxqrMjqDoE2XXeK82e5FFI04I/edit?usp=sharing).
