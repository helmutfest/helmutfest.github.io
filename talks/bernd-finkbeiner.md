---
layout: talk
title: "Hyperproperties beyond k-Hypersafety"
permalink: /talks/bernd-finkbeiner/
speaker: "Bernd Finkbeiner"
affiliation: "CISPA Helmholtz Center for Information Security and Technical University of Munich"
talk_type: "Scientific Talk"
---

## Abstract

System requirements related to concepts like information flow, knowledge, and robustness cannot be judged in terms of individual system executions, but rather require an analysis of the relationship between multiple executions. Such requirements belong to the class of hyperproperties, which generalize classic trace properties to properties of sets of traces.

A key idea in the verification of hyperproperties has been to analyze self-compositions of programs. Hyperproperties that need to hold for all possible combinations of k traces, such as k-hypersafety properties, can be analyzed as standard trace properties of the k-fold self-composition. The implicit universal quantification over the traces is, however, an inherent limitation of this paradigm, which makes it difficult to abstract in an existential manner from phenomena like scheduling in concurrent programs, nondeterministic choice, or speed of execution in asynchronous computations. Alternations between quantifiers are furthermore essential for counterfactual reasoning about causation and blame.

In this talk, we will explore the exciting world of hyperproperties beyond k-hypersafety. I will discuss the decidability and complexity of reasoning about such hyperproperties and present algorithmic techniques for the effective resolution of quantifier alternations. I will also give an overview of recently introduced logics for the specification of hyperproperties beyond k-hypersafety, including logics that combine hyperproperties with reasoning over strategies, and logics for second-order hyperproperties.
