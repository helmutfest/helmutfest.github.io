---
layout: page
title: "Incremental Static Analysis for Biological Models"
permalink: /talks/rebecca-ghidini/
speaker: "Rebecca Ghidini"
affiliation: "École Normale Supérieure (Paris)"
talk_type: "Scientific Talk"
---

**Speaker:** Rebecca Ghidini  
**Affiliation:** École Normale Supérieure (Paris)  
**Type:** Scientific Talk

## Abstract

The Kappa language is used for modeling protein-protein interaction networks in the form of rule-based models. To assist the modelers, the static analyzer KaSa automatically infers properties about the models. It computes an over-approximation of the reachable biomolecular species by abstract interpretation.

While efficient, KaSa is sometimes too slow to reason while modifying large models, especially in the user interface that strives to provide real-time feedback. Here, we propose an incremental extension of KaSa that updates the result of the current analysis at each model modification, without having to recompute it from scratch.

Our approach relies on the use of a relational analysis which over-approximates the relationships between the rules of the model and the reachable protein complexes. Once the relational analysis is computed, rules can be efficiently removed by excluding the reachable species that derive only from the removed rules. Adding rules is done classically by resuming the fixpoint iterations of the analysis algorithm.
