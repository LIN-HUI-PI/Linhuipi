# Dynamic Stability Cost Index (DSCI): A Dynamical Instability Marker for Pre-Biomarker State Transition

**Author:** Lin Hui-Pi  
**Affiliation:** NOIRÉA Research (Independent)  
**Version:** 0.1 (Concept Note)  
**Date:** 2026-06-16  
**License:** CC BY 4.0

---

## Abstract

This concept note introduces the **Dynamic Stability Cost Index (DSCI)**, a dynamical marker designed to capture the rising cost of stability maintenance before structural damage or biomarker changes become detectable. DSCI does not measure damage. It measures the hidden computational and metabolic overhead a system incurs in order to preserve normal behavioral output as its internal stability degrades. The core thesis is:

> Structural damage is late. Instability is early. Cost escalation is earlier.

DSCI is grounded in the theoretical framework of Dynamical Structuralism (DS) and is positioned within the Lake Model's Silent Drift phase and the Transient Overlap Membrane (TOM) geometry. Its proposed application spans neurodegenerative disease (Alzheimer's disease, Parkinson's disease), trauma-related conditions (PTSD, chronic fatigue), and complex adaptive systems including AI agents and collective decision systems.

---

## 1. Motivation

Current biomarker-driven approaches to detecting pre-symptomatic system failure follow a reverse detection logic:

```
Symptoms ← Biomarker ← Structural Imaging ← Dynamical Change
```

Measurement begins at the symptomatic end and works backward. By the time biomarkers are detectable, structural change is already established. By the time structural change is established, the underlying dynamical trajectory has been in progress for years.

DSCI proposes a reversal of this detection logic. Rather than asking **"has damage occurred?"**, it asks:

> **"How much does it cost the system to look like damage has not occurred?"**

This reframing identifies the earliest measurable signal: not the presence of damage, but the rising cost of masking its preconditions.

---

## 2. Theoretical Position

### 2.1 Lake Model Mapping

DSCI is positioned within the Lake Model (Lin, 2026) as a marker active during the **Silent Drift** phase — the period in which system behavior remains normal but the underlying attractor landscape is shifting.

| Lake Model Phase             | System State                                 | DSCI Signal                 |
|------------------------------|----------------------------------------------|-----------------------------|
| Pseudo-Calm                  | Fully stable                                 | Baseline                    |
| **Silent Drift**             | **Behavior preserved; internal cost rising** | **DSCI begins to rise**     |
| Fog Emergence                | Functional connectome changes detectable     | DSCI elevated               |
| Pre-Intervention Point (PIP) | Biomarker measurable                         | DSCI high                   |
| Manifestation                | Symptoms present                             | Clinical threshold exceeded |

### 2.2 TOM Geometry

The Transient Overlap Membrane (TOM; Lin, 2026) describes the geometric period during which a system simultaneously occupies two attractor basins. During TOM:

- Behavioral output may remain normal
- Structural imaging may remain normal
- Biomarkers may remain below threshold

However, the cost of maintaining coherent output while navigating dual attractor geometry is measurably elevated.

**DSCI operationalizes TOM as a behavioral cost curve.** Rising DSCI is the measurable behavioral evidence that TOM geometry is active.

### 2.3 Relationship to DS Foundational Principles

Within Dynamical Structuralism, the principle that *all visible phenomena are later than the structural changes that produce them* entails that the earliest detectable signals will always be dynamical rather than structural. DSCI is the operationalization of this principle in the domain of measurable output cost.

---

## 3. Definition

**DSCI** measures the hidden cost required to preserve normal behavioral output under increasing internal instability.

### 3.1 Core Formula

```
DSCI = Control Cost + Recovery Cost + Compensation Cost + Energy Cost − Output Fidelity
```

### 3.2 Component Definitions

| Component            | Definition                                                                   | Measurement Proxy                                        |
|----------------------|------------------------------------------------------------------------------|----------------------------------------------------------|
| **Control Cost**     | Load required to maintain task performance                                   | Response time variance; neural synchronization latency   |
| **Recovery Cost**    | Time and effort to return to stable output after perturbation                | Post-interference recovery slope                         |
| **Compensation Cost**| Degree to which non-primary networks or strategies are prematurely recruited | Off-pathway network activation; task-switching overhead  |
| **Energy Cost**      | Metabolic or computational resources required for equivalent output          | fMRI BOLD signal; computational token cost in AI systems |
| **Output Fidelity**  | Quality, accuracy, consistency, and stability of behavioral output           | Accuracy rate; decision consistency; output variance     |

Output Fidelity is **subtracted** because the defining feature of the Pre-Biomarker Phase is that output remains preserved while costs rise. High fidelity suppresses DSCI; the remaining four components continue to accumulate. The tension between rising costs and preserved output is itself the signal.

---

## 4. Pre-Biomarker Phase

The Pre-Biomarker Phase is formally defined as:

> **Performance preserved. Control cost increased.**

This phase is not detectable by accuracy alone. It requires tracking the *trajectory* of cost components over time. DSCI is therefore a **time-series marker**, not a single-point measurement. What is measured is not a value but the **curvature of a cost trajectory**.

Observable indicators of the Pre-Biomarker Phase include:

- Accuracy remains within normal range
- Response time variability increases
- Neural synchronization latency lengthens
- Interference recovery slows
- Compensation networks activate earlier than expected
- Equivalent task completion requires greater energy expenditure

---

## 5. Distinction: Biomarker vs. Dynamical Marker

DSCI is not a biomarker. The distinction is ontological, not merely temporal.

| Property           | Biomarker                           | DSCI (Dynamical Marker)                               |
|--------------------|-------------------------------------|-------------------------------------------------------|
| What it measures   | State cross-section (is X present?) | Process trajectory (how fast is the system drifting?) |
| Temporal structure | Single-point detectable             | Requires time-series data                             |
| Information type   | Damage evidence                     | Cost escalation evidence                              |
| Detection logic    | Threshold crossing                  | Slope change                                          |

DSCI detects the **rate of departure from a stable attractor**, not the presence of damage at that attractor's location.

---

## 6. Cross-Domain Applicability

The Stability Maintenance Cost framing — rather than "governance cost" — is intentional. It applies to any system with an identifiable stable state and measurable output:

- **Neurodegenerative disease:** Alzheimer's disease, Parkinson's disease (pre-symptomatic dynamical drift)
- **Trauma-related conditions:** PTSD, chronic fatigue syndrome (persistent elevated recovery cost)
- **AI agent systems:** Session-level coherence degradation, identity drift under cross-session adaptive learning. Identity drift under cross-session adaptive learning is formalized as Persistent Identity Modeling (PIM) in the NOIRÉA architecture (Lin, 2026). DSCI provides the pre-failure cost escalation marker that precedes detectable PIM accumulation.
- **Collective decision systems:** Group-level stability maintenance under increasing informational load

The formula structure remains consistent across domains. Measurement proxies vary by system type.

---

## 7. Positioning Within Existing Research

Recent literature provides convergent empirical support for the components of DSCI, though not yet under a unified framework:

- **Dynamic functional connectivity** changes in preclinical Alzheimer's disease have been detected prior to structural atrophy
- **Whole-brain functional connectome** alterations have been linked to amyloid and tau PET signals in preclinical cohorts
- **Response time variability** has been studied as a cognitive risk signal in preclinical stages of neurodegeneration
- **Compensatory network activation** (hyperactivation in early cognitive decline) has been documented in fMRI studies of aging and mild cognitive impairment

DSCI provides a unifying construct that integrates these observations under a single dynamical cost framework.

---

## 8. Research Program

### Core Hypothesis

A measurable dynamical instability marker exists that precedes structural damage, precedes biomarker threshold crossing, and precedes any detectable symptom — identifiable as a rising cost trajectory in behavioral output maintenance.

### Next Steps

1. **Operationalization:** Define measurement protocols for each DSCI component in human neuroimaging + behavioral task paradigms
2. **Validation design:** Longitudinal study design linking DSCI trajectories to eventual biomarker positivity in preclinical cohorts
3. **Cross-domain calibration:** Adapt DSCI measurement for AI agent systems and collective decision contexts
4. **Intervention linkage:** Connect DSCI threshold levels to Pre-Intervention Point (PIP) logic in the LIN System architecture

---

## 9. Summary

DSCI is not a biomarker of damage.  
It is a dynamical marker of rising stability-maintenance cost before damage becomes visible.

The core claim:

> **Structural damage is late.**  
> **Instability is early.**  
> **Cost escalation is earlier.**

---

## References

Lin Hui-Pi (2026). *Dynamical Structuralism: Founding Document v1.1.* Zenodo. https://doi.org/10.5281/zenodo.19607127

Lin Hui-Pi (2026). *Lake Model v1.2.* Zenodo. https://doi.org/10.5281/zenodo.20394394

Lin Hui-Pi (2026). *Transient Overlap Membrane (TOM) Concept Note v1.0.* Zenodo. https://doi.org/10.5281/zenodo.20399636

Lin Hui-Pi (2026). *LIN System Architecture v0.4.* Zenodo. https://doi.org/10.5281/zenodo.20379395

Lin Hui-Pi (2026). *Sentinel Architecture.* Zenodo. https://doi.org/10.5281/zenodo.20388312

Lin Hui-Pi (2026). *NOIRÉA: Session-Bounded Identity Isolation in Adaptive Physical AI Systems.* Zenodo. [DOI pending — uploaded concurrently with this note]

---

*This concept note establishes priority of the DSCI framework. Empirical operationalization and experimental validation are planned for subsequent publications.*
