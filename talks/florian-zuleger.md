---
layout: talk
title: "Automating Amortised Resource Analysis of Self-Adjusting and Probabilistic Data Structures"
permalink: /talks/florian-zuleger/
speaker: "Florian Zuleger"
affiliation: "TU München"
talk_type: "Scientific Talk"
---

## Abstract

Amortised analysis is a key technique for establishing efficient worst-case guarantees for data structures such as splay trees and heaps, but traditional proofs rely on sophisticated potential functions and substantial manual reasoning. This talk presents a line of work on automating amortised resource analysis for functional programs implementing such data structures. Our approach builds on type-based amortised resource analysis, where template potential functions are combined with constraint solving to derive logarithmic amortised bounds.

We illustrate the approach on classical and probabilistic self-adjusting data structures, including splay trees, heaps, skew heaps, and leftist heaps. While the choice of suitable potential templates and analysis heuristics are guided by the user, the resulting analyses can automatically infer tight complexity bounds and recover many classical amortised results.
