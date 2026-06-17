# Persistent Identity Modeling as a Formation Process: A Research Direction Concept Note

**Author:** Lin Hui-Pi (林慧碧), NOIRÉA Research  
**Version:** v0.1  
**Date:** June 2026  
**Related work:** NOIRÉA architecture (ISSRE 2026 Submission #15); LIN System Layer 1 (Identity Governance Membrane)

---

## Abstract

This concept note records a research direction pivot following peer review of the NOIRÉA architectural framework. Reviewers confirmed that Persistent Identity Modeling (PIM) — the unintended accumulation of identity-correlated representations in adaptive AI systems across deployment sessions — is a timely and original problem. However, they called for empirical evidence from real adaptive systems before the proposed isolation architecture could be evaluated. In response, this note establishes PIM formation as an independent research object: rather than first proposing a defense, we first ask how PIM forms, when it becomes measurable, and whether it is observable in real adaptive systems using publicly available physiological data. This reorientation does not abandon the NOIRÉA governance architecture; it provides the empirical foundation that governance design requires.

---

## 1. Definition of Persistent Identity Modeling (PIM)

Persistent Identity Modeling (PIM) is defined as the process by which an adaptive AI system, while learning to perform a task from human-derived signals across multiple deployment sessions, unintentionally accumulates identity-correlated structure in its learned representations.

PIM is not equivalent to:
- **Subject classification**: the fact that EEG or other physiological signals contain person-specific information is well known. PIM refers specifically to the accumulation of such information *as a byproduct of cross-session task adaptation*, not as an intended learning objective.
- **Personalization**: deliberate adaptation to individual users is a design choice. PIM is unintended and structurally invisible to standard performance metrics.
- **Privacy leakage in a single session**: PIM is a *cross-session, temporal accumulation* phenomenon. It may be undetectable at session boundaries and only becomes measurable as adaptation proceeds.

The core claim of PIM is: **a system can maintain stable or improving task performance while simultaneously accumulating increasing amounts of identity-correlated structure in its representation space.** These two processes are not mutually exclusive, and standard task-level metrics do not reveal the second.

This claim is structurally consistent with the foundational principle of Dynamical Structuralism (DS): *visible phenomena are always later than underlying structural changes*. PIM is a specific instantiation of this principle in machine learning systems — identity structure enters the representation space before it becomes measurable at the output level.

---

## 2. Research Motivation: From Isolation to Formation

The NOIRÉA framework (v0.1) proposed an architectural response to PIM: session-bounded isolation of identity-correlated representations, formalized as four requirements (R1–R4). Peer reviewers at ISSRE 2026 recognized the problem as original and timely, but identified a foundational gap: the framework assumes that identity-correlated and task-correlated representations can be separated, and that PIM accumulation is measurable — but neither assumption was empirically demonstrated in a real adaptive system.

This gap cannot be closed by refining the architecture. It requires a prior empirical question to be answered first:

> **Does PIM, as defined, actually occur in real adaptive systems? If so, how does it form, and when does it become measurable?**

Answering this question is the purpose of the research direction recorded here.

The pivot from *isolation* to *formation* is not a retreat. It is a recognition that a governance architecture requires a natural history of the phenomenon it governs. A defense cannot be evaluated before the threat is characterized. This sequence — characterize formation, then design governance — is the correct scientific order.

---

## 3. The PIM Formation Curve: Experimental Hypothesis and Design

### 3.1 Core Hypothesis

If PIM exists as defined, the following should be observable in a real cross-session adaptive system:

**H1 (Formation):** As cross-session adaptation proceeds, the ability to predict subject identity from learned task representations increases, even when task performance remains stable or improves.

**H2 (Invisibility):** This increase in identity-predictability is not reflected in standard task-level accuracy metrics. The two processes are dissociable.

If H1 and H2 are both confirmed, the result constitutes empirical evidence for PIM as a distinct phenomenon — not reducible to individual differences in raw signals, and not visible through standard evaluation.

### 3.2 Experimental Design

**Dataset:** BCI Competition IV Dataset 2a. Nine subjects, two sessions per subject (Session 1: training; Session 2: adaptation/test). Four-class motor imagery task. Publicly available and widely used as a benchmark in BCI research.

**Decoder:** Common Spatial Pattern (CSP) + Linear Discriminant Analysis (LDA). Standard motor imagery pipeline. CSP output serves as the representation layer under analysis.

**Adaptation step definition:** Adaptation is operationalized as the incremental addition of Session 2 trials to the training set. Step 0 = Session 1 only; Step k = Session 1 + first k × 10 trials from Session 2. The decoder is retrained at each step.

**Probe design:** At each adaptation step, a logistic regression identity probe is trained on CSP features extracted from Session 1 data, using subject ID as the label. The probe is evaluated on held-out Session 2 data. This design ensures the probe measures identity structure *as encoded by the current adapted representation*, not raw EEG individual differences.

**Measurement:** Two curves are tracked across adaptation steps:
- *Task accuracy*: motor imagery classification accuracy on held-out Session 2 trials
- *Identity probe accuracy*: subject ID prediction accuracy from CSP features on held-out Session 2 trials

**PIM formation curve:** The joint trajectory of these two curves. If task accuracy remains stable while identity probe accuracy rises above Session-1 baseline, this constitutes evidence for H1 and H2.

**Chance level:** 1/9 ≈ 11% for identity probe (9 subjects).

**Key distinction from subject classification:** The probe is not measuring whether EEG signals contain identity information (they do, trivially). It is measuring whether the *adapted representation* encodes progressively more identity information as a function of adaptation steps — a temporal, process-level claim.

---

## 4. Research Sequence: Formation Before Governance

The intended research sequence is as follows:

**Stage 1 (this note):** Define PIM as a formation process. Establish the experimental hypothesis and measurement design. Record research direction and priority.

**Stage 2 (in progress):** Implement the PIM formation experiment using BCI Competition IV 2a and MNE-Python. Produce PIM formation curves across subjects. Analyze whether H1 and H2 are supported.

**Stage 3 (subsequent):** If Stage 2 confirms PIM formation, return to the NOIRÉA governance architecture with empirical grounding. Evaluate whether session-boundary reset (R1) disrupts the formation curve. Design NOIRÉA-lite comparison experiment.

This sequence reflects a principle from the LIN System architecture: intervention design requires prior characterization of the failure mode being addressed. HÚPLŃ (the arrest-and-release governance mechanism) was designed after the failure sequence LCS→OTL→SPI→ECI was characterized, not before. The same logic applies here: NOIRÉA's isolation requirements should be evaluated against a characterized formation process, not an assumed one.

---

## 5. Relationship to Adjacent Research Areas

PIM is distinct from, though related to, several existing research areas:

- **Machine unlearning**: unlearning addresses the removal of specific training data influence on request. PIM addresses unintended accumulation during normal operation, prior to any removal request.
- **Continual learning / catastrophic forgetting**: continual learning research focuses on preserving task performance across sessions. PIM concerns a different dimension — what else is being learned alongside the task.
- **Privacy-preserving learning (federated learning, differential privacy)**: these approaches address data-level privacy during training. PIM is a representation-level phenomenon in deployed adaptive systems.
- **Personalization**: personalization is intentional identity-correlated adaptation. PIM is unintentional and structurally invisible.
- **Representation disentanglement**: disentanglement methods aim to separate factors of variation in learned representations. PIM formation research asks whether disentanglement is necessary in the first place — i.e., whether task adaptation inevitably entangles identity.

---

## 6. Open Questions

The following questions are left open for Stage 2 investigation:

1. Does PIM formation rate vary across subjects or task conditions?
2. Is there a detectable threshold — an adaptation step at which identity probe accuracy increases significantly — analogous to the DSCI (Dynamic Stability Cost Index) in the LIN System?
3. Does PIM formation depend on the representation layer? (CSP features vs. deeper learned representations in neural decoders)
4. Is PIM formation reversible — does session-boundary reset reduce identity probe accuracy in subsequent adaptation?

Question 4 connects directly to the NOIRÉA R1 requirement and will be addressed in Stage 3.

---

## Notes

This concept note does not present experimental results. It records a research direction, a defined hypothesis, and a measurement design. Its purpose is to establish the intellectual priority of the PIM formation research question and to document the reasoning behind the pivot from architectural governance to empirical characterization.

The NOIRÉA architecture (R1–R4) remains valid as a governance proposal. This note establishes the empirical work required to evaluate it.
