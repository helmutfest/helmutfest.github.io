---
layout: talk
title: "Who Guards the Guards? Testing Program Analyzers"
permalink: /talks/anastasia-isychev/
speaker: "Anastasia Isychev"
affiliation: "TU Wien"
talk_type: "Scientific Talk"
---

## Abstract

Program analyzers are critical in guarding software reliability. However, due to their inherent complexity, they are likely to contain bugs themselves. Precise specifications of expected analysis results are often unavailable, which makes both formal verification and testing challenging, and other reliable test oracles are difficult or impossible to obtain. So how do we guard the guards?

This talk will highlight current challenges in testing program analyzers and discuss emerging solutions. As a central example, I will present interrogation testing, a technique that uses analyzer's own results to derive elaborate test oracles, thereby forcing an analyzer into contradiction and uncovering soundness and precision bugs.
