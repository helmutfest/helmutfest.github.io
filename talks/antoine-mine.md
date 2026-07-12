---
layout: talk
title: "Experience designing a static analyzer by abstract interpretation with MOPSA"
permalink: /talks/antoine-mine/
speaker: "Antoine Miné"
affiliation: "Sorbonne Université"
talk_type: "Scientific Talk"
---

## Abstract

We discuss the design of MOPSA, a platform to build and experiment with
static program analysis by abstract interpretation. MOPSA strives to
achieve a high degree of modularity and extensibility by decomposing
analyses into collections of fine-grained, composable, and reusable
domains which embed various components such as data abstractions and
syntax iterators.

MOPSA has been used to design an analysis for run-time errors in C
programs that participates to the SV-Comp competition. MOPSA also drives
our research to expand the languages supported by static analysis
(introducing support for Python or OCaml, as well as multilanguage
programs) and the properties we infer (such as portability and
non-exploitability analyses).

This talk gives an overview of this work, discusses the specificities
that distinguish MOPSA from other static analyzers by abstract
interpretation. Looking back at a few years of development of MOPSA, we
try to assess what works and what needs work.
