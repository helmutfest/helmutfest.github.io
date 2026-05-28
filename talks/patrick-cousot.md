---
layout: talk
title: "Non Standard Axiomatic Semantics"
permalink: /talks/patrick-cousot/
speaker: "Patrick Cousot"
affiliation: "Courant Institute, New York University"
talk_type: "Scientific Talk"
---

## Abstract

Axiomatic semantics is defined on Wikipedia as follows: "Axiomatic semantics define the meaning of a command in a program by describing its effect on assertions about the program state." The same page states that "It is closely related to Hoare logic." On the "semantics (programming languages)" page, it is stated that "semantics is the rigorous mathematical logic study of the meaning of programming languages." We understand that semantics should not be ambiguous.

We show that the axiomatic semantics/Hoare logic suffers from the same ambiguities as Peano arithmetics, it has nonstandard models. Dedekind solved the problem for naturals by including the second-order induction axiom, requiring that proofs by the recurrence to be sound for any model of the naturals. Then any two models of the naturals are isomorphic. This is not applicable to Hoare logic which as no second order axioms.

We show that, equivalently, fixpoint definitions of the naturals ensures uniqueness up to isomorphism and that the second-order induction axiom follows naturally from this definition by fixpoint induction.

A similar result holds in Hoare logic but is not expressible in the logic itself. Moreover, it does not apply to abstract Hoare logics. We conclude that the axiomatic semantics is inherently ambiguous and can only be understood as an abstraction of a more refined, non-ambiguous semantics.
