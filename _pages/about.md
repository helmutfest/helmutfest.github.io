---
layout: about
title: about
permalink: /
subtitle: 2nd edition, Nov 24 2025

profile:
  align: right
  image: smu-computing.jpg
  image_circular: false # crops the image to make it circular

selected_papers: false # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

Welcome to the second SG Programming Languages Summit!
The summit is an informal meeting for everyone interested in programming languages research (broadly construed) that takes place once a year in Singapore.

## time & venue

- Nov 24 2025, 9am-5pm
- Venue: Singapore Management University, Room SR B1-01 (Basement 1)
- Address: [Yong Pung How School of Law,  55 Armenian St, Singapore 179943](https://maps.app.goo.gl/Wznb7x9fUHfq67h68)

## keynote

The summit will feature a keynote by [Krishna S](https://www.cse.iitb.ac.in/~krishnas/) from IIT Bombay.

## call for participation

The SG PL summit is **open to participants at all levels across academia and industry** and attendance is **free-of-charge**. 

**Please sign up at the following link by November 7, 2025:** (Signup now closed)


## schedule at a glance

| | |
|---|---|
| 09:00 - 09:10  | **Welcome and Opening Remarks** |
| 09:10 - 10:10 | Keynote |
| 10:10 - 10:40 | **Coffee break** |
| 10:40 - 12:00 | Session 1: Concurrency & Hardware |
| 12.00 - 13:30  | **Lunch break** (Lunch is not provided) |
| 13:30 - 15:30   | Session 2: AI & Medley I |
| 15:30 - 16:00   | **Coffee break** |
| 16:00 - 17:20   | Session 3: Medley II & Program Logics |


## detailed schedule

### Keynote


**09:10 - 10:10** 

**Title**: Verifying Concurrent Programs under Weak Consistency

**Speaker**: [Krishna S](https://www.cse.iitb.ac.in/~krishnas/), IIT Bombay, India

<details>
<summary>Abstract</summary>
The strongest level of consistency in concurrent/distributed storage systems consists in ensuring that every issued write operation is immediately visible to all processes. However, for performance reasons, storage systems do not guarantee  strong consistency, but they rather implement weaker consistency models where different processes may see different sets of writes along computations, sometimes in different orders. The conditions on the visibility order guaranteed by a system corresponds to its memory consistency model. Weak consistency models admit complex and unintuitive behaviors, making the task of programming applications very hard. This motivates investigating the verification problem 
of checking the correctness of a  program running over a weak consistency model.  Solving this problem  is nontrivial due to the fact that capturing program semantics under weak consistency models requires, in general, reasoning about infinite-state systems,  which in general, threaten decidability. 

In this talk, I will touch upon some popular weak consistency models and some key results related to verifying programs under these. 
</details>

---


### Session 1: Concurrency & Hardware

**10:40-11:00**

**Title**: Enhanced Data Race Prediction Through Modular Reasoning

**Speaker**: Zhendong Ang, National University of Singapore

<details>
<summary>Abstract</summary>
There are two orthogonal methodologies for efficient prediction of data races from concurrent program runs: commutativity and prefix reasoning. There are several instances of each methodology in the literature, with the goal of predicting data races using a streaming algorithm where the required memory does not grow proportional to the length of the observed run, but these instances were mostly created in an ad hoc manner, without much attention to their unifying underlying principles. 
In this paper, we identify and formalize these principles for each category with the ultimate goal of paving the way for combining them into a new algorithm which shares their efficiency characteristics but offers strictly more prediction power. In particular, we formalize three distinct classes of races predictable using commutativity reasoning, and compare them. We identify three different styles of prefix reasoning, and prove that they predict the same class of races, which provably contains all races predictable by any commutativity reasoning technique. 

Our key contribution is combining prefix reasoning and commutativity reasoning in a modular way to introduce a new class of races, granular prefix races, that are predictable in constant-space and linear time, in a streaming fashion. This class of races includes all races predictable using commutativity and prefix reasoning techniques. We present an improved constant-space algorithm for prefix reasoning alone based on the idea of antichains (from language theory). This improved algorithm is the stepping stone that is required to devise an efficient algorithm for prediction of granular prefix races. We present experimental results to demonstrate the expressive power and performance of our new algorithm.</details>

---

**11:00-11:20**

**Title**: Data Race Detection by Digest-Driven Abstract Interpretation  

**Speaker**: [Michael Schwarz](https://michael-schwarz.github.io), National University of Singapore

<details>
<summary>Abstract</summary>
Sound static analysis can prove the absence of data races by establishing that no two conflicting memory accesses can occur at the same time. We repurpose the concept of digests — summaries of computational histories originally introduced to bring tunable concurrency-sensitivity to thread-modular value analysis by abstract interpretation. We extend this idea to race detection and use digests to capture the conditions under which conflicting accesses may not happen in parallel. To formalize this, we give a definition of data races in the thread-modular local trace semantics and show how exclusion criteria for potential conflicts can be expressed as digests. We report on our implementation of digest-driven data race detection in the static analyzer Goblint, and evaluate it on the Sv-Comp benchmark suite. Combining the lockset digest with digests reasoning on thread id s and thread joins increases the number of correctly solved tasks by more than a factor of five compared to lockset reasoning alone.

Based on joint work with Julian Erhard (TU Munich & LMU Munich), accepted to appear at VMCAI '26.</details>


---

**11:20-11:40**

**Title**: Anvil: A General-Purpose Timing-Safe Hardware Description Language  

**Speaker**: [Jason Zhijingcheng Yu](https://www.comp.nus.edu.sg/~yuz1996/), National University of Singapore

<details>
<summary>Abstract</summary>
Expressing hardware designs using hardware description languages (HDLs) routinely involves using stateless signals whose values change according to their underlying registers. Unintended behaviours can arise when the stored values in these underlying registers are mutated while their dependent signals are expected to remain constant across multiple cycles. Such timing hazards are common because existing HDLs lack abstractions for values that remain unchanged over multiple clock cycles, delegating this responsibility to hardware designers. In this talk, I present Anvil, an HDL equipped with a type system that statically guarantees timing safety, i.e., absence of timing hazards, while maintaining expressiveness for cycle-level timing control or dynamic timing behaviours. In particular, I will focus on two main aspects: 1) safety: formal definition of the timing safety property and Anvil's semantics and type system, and 2) expressiveness: empirical evaluation of Anvil's expressiveness in real-world hardware designs.</details>

---

**11:40-12:00**

**Title**: Understanding and Optimizing Hardware Model Checking     

**Speaker**: [Yibo DONG](https://yibodong.tech/), National University of Singapore

<details>
<summary>Abstract</summary>
Hardware model checking has become one of the most successful applications of formal verification, providing automated safety guarantees for complex digital systems. Despite this success, the performance of modern checkers still depends heavily on the interaction between their algorithmic components and the underlying SAT solvers. Understanding and improving this interaction remains a core challenge at the boundary between theory and implementation. In this talk, I will discuss recent efforts to make hardware model checking both more efficient and more explainable. We focus on symbolic model checking algorithms that rely on iterative SAT solving, taking the Complementary Approximate Reachability (CAR) framework as a representative example. I will illustrate how CAR structures its reasoning through sequences of SAT calls and how the characteristics of these calls, such as the order of assumptions and the handling of unsatisfiable cores, can strongly influence performance. Building on this understanding, we introduce several optimizations that improve reasoning efficiency. These insights also shed light on how solver-level behaviors shape verification outcomes, suggesting directions for more transparent and adaptive model checking in the future.</details>

---

### Session 2: AI & Medley I

**13:30-13:50**

**Title**: Towards verifying and enforcing runtime safety for agent systems  

**Speaker**: [Haoyu Wang](https://sites.google.com/view/haoyuwang18/home), Singapore Management University

<details>
<summary>Abstract</summary>
Ensuring the safety of autonomous and intelligent agent systems remains a pressing challenge as they increasingly interact with open, dynamic environments. While formal verification offers rigorous guarantees before deployment, it struggles to handle the scale, uncertainty, and adaptivity of real-world settings. This talk explores a complementary direction—runtime safety verification and enforcement—where agents continuously reason about and regulate their own behavior during execution.

I will introduce a series of techniques that combine formal logic–based specifications with probabilistic runtime models, enabling agents to quantify and monitor safety in real time. Building on these foundations, we develop proactive enforcement mechanisms that intervene before violations occur, leveraging learned probabilistic dynamics and robust semantic scores to guide corrective actions.

The talk will showcase applications across domains such as autonomous driving and embodied household agents, highlighting how runtime monitoring and model-based enforcement can make learning agents both adaptable and verifiably safe. I will conclude by discussing open problems—including integrating symbolic reasoning with LLM-based controllers, balancing safety with performance, and moving toward unified frameworks for trustworthy autonomous behavior.</details>

---

**13:50-14:10**

**Title**: Optimizing and Fortifying AI Software through the Lens of Artifact Synthesis  

**Speaker**: Jieke Shi, Singapore Management University

<details>
<summary>Abstract</summary>
Ensuring the safety and efficiency of AI systems has become increasingly critical as neural networks move from the cloud to the edge, enabling on-device intelligence that controls physical systems, generates code, and interacts with humans in real time. This talk presents advances in engineering AI systems that are safer, more efficient, and greener by design, integrating synthesis-driven techniques across two key dimensions: efficiency and control. The first part focuses on efficiency, presenting techniques to synthesize compact and sustainable language models for code that run in real time on local devices such as laptops, delivering cloud-free deployment with up to hundreds of times lower energy use and minimal accuracy loss. The second part addresses safety, presenting approaches that rely on program synthesis and formal verification to systematically identify safety violations in AI-enabled control systems and to synthesize runtime shields that enforce safe behaviors without retraining. Although the specific challenges and methods differ across these aspects, from efficient deployment to runtime assurance, they share a common goal: bringing trustworthy, responsive, and environmentally responsible AI from the cloud to the device, making autonomous intelligence not only powerful but also reliable, efficient, and sustainable.</details>

---

**14:10-14:30**

**Title**: Certified Robust Accuracy of Neural Networks Are Bounded due to Bayes Errors 

**Speaker**: Ruihan Zhang, Singapore Management University

<details>
<summary>Abstract</summary>
Adversarial examples pose a security threat to many critical systems built on neural networks. While certified training improves robustness, it also decreases accuracy noticeably. Despite various proposals for addressing this issue, the significant accuracy drop remains. More importantly, it is not clear whether there is a certain fundamental limit on achieving robustness whilst maintaining accuracy. In this work, we offer a novel perspective based on Bayes errors. By adopting Bayes error to robustness analysis, we investigate the limit of certified robust accuracy, taking into account data distribution uncertainties. We first show that the accuracy inevitably decreases in the pursuit of robustness due to changed Bayes error in the altered data distribution. Subsequently, we establish an upper bound for certified robust accuracy, considering the distribution of individual classes and their boundaries.</details>

---

**14:30-14:50**

**Title**: Cottontail: LLM-Driven Concolic Execution for Highly Structured Test Input Generation

**Speaker**: [Haoxin Tu](https://haoxintu.github.io/), National University of Singapore

<details>
<summary>Abstract</summary>
How can we perform concolic execution to generate highly structured test inputs for systematically testing parsing programs? Existing concolic execution engines are significantly restricted by (1) input structure-agnostic path constraint selection, leading to the waste of testing effort or missing coverage; (2) limited constraint-solving capability, yielding many syntactically invalid test inputs; (3) reliance on manual acquisition of highly structured seed inputs, resulting in non-continuous testing.
In this talk, we will discuss Cottontail, a new Large Language Model (LLM)-driven concolic execution engine, to mitigate the above limitations. A more complete program path representation, named Expressive Structural Coverage Tree (ESCT), is first constructed to select structure-aware path constraints. Later, an LLM-driven constraint solver based on a Solve-Complete paradigm is designed to solve the path constraints smartly to get test inputs that are not only satisfiable to the constraints but also valid to the input syntax. Finally, a history-guided seed acquisition is employed to obtain new highly structured test inputs either before testing starts or after testing is saturated.
We implemented Cottontail on top of SymCC and evaluated eight extensively tested open-source libraries across four different formats (XML, SQL, JavaScript, and JSON). Cottontail significantly outperforms baseline approaches by 30.73% and 41.32% on average in terms of line and branch coverage. Besides, Cottontail found six previously unknown vulnerabilities (six CVEs assigned). We have reported these issues to developers, and four out of them have been fixed so far.</details>

---

**14:50-15:10**

**Title**: A Direct Reduction from Stochastic Parity Games to Simple Stochastic Games

**Speaker**: Zihan Zhou, National University of Singapore

<details>
<summary>Abstract</summary>
Significant progress has been recently achieved in developing efficient solutions for simple stochastic games (SSGs), focusing on reachability objectives. While reductions from stochastic parity games (SPGs) to SSGs have been presented in the literature through the use of multiple intermediate game models, a direct and simple reduction has been notably absent. This paper introduces a novel and direct polynomial-time reduction from quantitative SPGs to quantitative SSGs. By leveraging a gadget-based transformation that effectively removes the priority function, we construct an SSG that simulates the behavior of a given SPG. We formally establish the correctness of our direct reduction. Furthermore, we demonstrate that under binary encoding this reduction is polynomial, thereby directly corroborating the known NP∩coNP complexity of SPGs and providing new understanding in the relationship between parity and reachability objectives in turn-based stochastic games.</details>

---

**15:10-15:30**

**Title**: Ergonomics for Computational Duality

**Speaker**: Ding Feng & Kyrieal Mortel Abad, National University of Singapore

<details>
<summary>Abstract</summary>
In recent years, programming languages grounded in classical logic and sequent calculus have gained attention for their elegant treatment of control flow via computational dualities. 
However, existing dual language implementations typically extend upon $\lambda$-calculus foundations, and often lacks syntactic sugar. Thus, they either inherits excessive complexities or obscures the fundamental symmetry between data producers and consumers.
In this talk, we present Mini-Mu, a minimalist and ergonomics-oriented dual language. 
It eliminates $\lambda$-abstraction entirely, building computation solely on $\mu\tilde{\mu}$-calculus primitives and pattern matching. Unlike conventional approaches which treat functions as first-class citizens and layer duality onto functional constructs, Mini-Mu directly treats computation as bidirectional data flow between expressions and continuations. Data and codata---including both conventional structures and reified continuations---is treated equally with constructors and $\mu$-abstractions, eliminating the asymmetry in $\lambda$ based systems. Through introducing formal semantics and practical examples for the language, we show that the system maintains expressiveness of full $\lambda\mu\tilde{\mu}$-calculus, while offering readability and writability comparable to traditional programming languages. We will also demonstrate that this purely dual foundation simplifies a number of concepts and techniques for various programming patterns, and the potential of duality-based programming in various fields.</details>

---


### Session 3: Medley II & Program Logics

**16:00-16:20**

**Title**: Exploring Fixed-Point-Oriented Programming        

**Speaker**: [Foo Yong Qi](https://yongqi.foo/), National University of Singapore

<details>
<summary>Abstract</summary>
Many problems, from static analysis, graph algorithms, type checking and beyond, involve fixed-point computations over cyclic or self-referential structures, typically solved via work-queue algorithms. This talk explores Fixed-Point-Oriented Programming (FPOP), an evolving programming paradigm that allows programmers to express work-queue algorithms by simply describing the essence of the fixed-point computation. In this talk, we discuss ongoing directions for extending FPOP languages toward greater efficiency, modularity and expressiveness. First, we describe how facts in work queues can be interpreted as a form of continuation: suspended computations that can be resumed and ordered to control evaluation to enable algorithm-level optimizations. Next, we explore rule composition as a mechanism to allow complex analyses, such as reduced products, to be expressed by composing simpler components. Finally, we further conjecture a unified model bridging bottom-up chaotic iteration and top-down goal-directed reasoning, allowing both styles of computation to co-exist naturally within a single framework. The talk outlines the conceptual foundations of FPOP, illustrates its potential, and invites discussion on ideas and applications for FPOP languages.</details>

---

**16:20-16:40**

**Title**: Engineering a Verified Explicit-State Model Checker in Lean        

**Speaker**: [Qiyuan Zhao](https://zqy1018.top/), National University of Singapore

<details>
<summary>Abstract</summary>
Explicit-state model checkers like TLC are effective tools for exploring the concrete state space of a system. They can systematically find bugs and produce concrete, easy-to-understand counterexamples, which makes them valuable in early stages of system design. However, they provide limited assurance that a system is bug-free. By contrast, symbolic verifiers such as Ivy and Veil rely on SMT solvers to perform bounded or parameterized verification, leading to much stronger guarantees. Yet to keep verification decidable, they often require introducing abstractions into the system model. Consequently, counterexamples are generated for the abstracted system rather than the concrete design, and may therefore be harder to interpret.

In this talk, we present an ongoing effort to build a verified explicit-state model checker integrated into Veil, developed in the Lean theorem prover. The checker can serve as a "front line" for symbolic verification: it allows users to explore bounded instances of parameterized systems and obtain concrete counterexamples that help identify and fix bugs before moving on to full symbolic verification. Inspired by TLC, the tool can also function as a general-purpose model checker for standalone systems. We will discuss the main challenges in making the checker both verified and practical, and conclude with a live demo illustrating its use.</details>

---                                                                              
**16:40-17:00**

**Title**: Engineering a Verified Explicit-State Model Checker in Lean        

**Speaker**: [Thibault Dardinier](https://dardinier.me/), National University of Singapore

<details>
<summary>Abstract</summary>
Hyperproperties relate multiple executions of a program and capture essential correctness and security properties such as determinism, monotonicity, transitivity, reachability, and (generalized) non-interference. Existing program logics for hyperproperties typically reason about a fixed number of states, which limits the kinds of hyperproperties they can express and prove, and hinders the reuse of proofs across different formalisms.

In this talk, I will present Hyper Hoare Logic (HHL), a generalization of Hoare logic that lifts assertions from predicates over individual states to predicates over sets of states. This generalization enables uniform reasoning for a wide range of hyperproperties, including those beyond the reach of existing logics. Despite its expressiveness, HHL admits simple and intuitive inference rules that support key reasoning principles, such as composing different kinds of hyperproperties in the same proof or reasoning about loops where different executions perform different numbers of iterations.
</details>

---        

**17:00-17:20**

**Title**: Type Safety via Hoare Logic with Separation Type      

**Speaker**: Li Wenhua, National University of Singapore

<details>
<summary>Abstract</summary>
Traditionally, type safety for user programs are ensured by
crafted type systems that embrace the motto “well-typed programs cannot
go wrong” at runtime due to type errors. However, we are increasingly
reliant on type systems for more advanced considerations, such as greater
memory safety (e.g., Rust), and the need to support dynamically-typed
languages. In this paper, we show how Hoare logic with separation types
(inspired from separation logic) is able to meet these new demands.
Our new proposal has several benefits. First, we can flexibly handle type
safety for different paradigms, from statically typed languages (such as
ML or Haskell) to dynamically typed languages (such as Python) via
semantic subtyping. Second, we can naturally support path-sensitive and
flow-sensitive type specifications. Lastly, we give a comprehensive set of
error types for different scenarios, (i) Err type to capture runtime errors
as values that can be passed into arguments of method calls; (ii) Abrt
type to denote compile-time errors that would have triggered program
abortions and must be flagged as type errors; and (iii) Exc type that can
be used to support checked and unchecked exceptions that may escape
methods, or be caught and handled by user programs.
</details>

---

## mailing list

All SG PL Summit related communications will be made via the following [mailing list](https://groups.google.com/g/plsg).
To join, please get in touch with [Ilya Sergey](mailto:ilya@nus.edu.sg) or [Yong Kiam Tan](mailto:yongkiam.tan@ntu.edu.sg).

This mailing list has very low traffic. If you are interested in programming languages research in Singapore, we encourage you to sign up.