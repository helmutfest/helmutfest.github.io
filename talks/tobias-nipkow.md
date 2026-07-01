---
layout: talk
title: "Verification of Earley's Algorithm, Including Time Bounds"
permalink: /talks/tobias-nipkow/
speaker: "Tobias Nipkow"
affiliation: "Technical University of Munich"
talk_type: "Scientific Talk"
---

## Abstract

Earley's algorithm is a parsing algorithm for general context-free grammars. The talk will outline a stepwise refinement from an initial specification (which is correct wrt the language defined by the grammar) to executable code. A verified running time analysis is sketched: if arrays are available, the code has the well-known cubic complexity; if lists are used, the complexity is only quartic.
