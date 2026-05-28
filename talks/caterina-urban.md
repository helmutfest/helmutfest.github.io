---
layout: talk
title: "Termination Resilience Static Analysis"
permalink: /talks/caterina-urban/
speaker: "Caterina Urban"
affiliation: "Inria & ENS | PSL"
talk_type: "Scientific Talk"
---

## Abstract

We present a novel abstract interpretation-based static analysis framework for proving Termination Resilience, the absence of Robust Non-Termination vulnerabilities in software systems. Robust Non-Termination characterizes programs where an untrusted (e.g., externally-controlled) input can force infinite execution, independently of other trusted (e.g., internally-controlled) variables. Our framework is a semantic generalization of Cousot and Cousot's abstract interpretation-based ranking function derivation, and our sound static analysis extends Urban and Miné's decision tree abstract domain in a non-trivial way to manage the distinction between untrusted and trusted program variables. The talk concludes with open challenges in dealing with angelic non-determinism, pointer-manipulating programs, and going beyond termination to program properties expressed in Computational Tree Logic (CTL) or Alternating-Time Temporal Logic (ATL).
