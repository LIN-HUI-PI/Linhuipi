# NOIRÉA: Session-Bounded Identity Isolation in Adaptive Physical AI Systems
## Zenodo Upload Note

**Author:** Lin Hui-Pi (林慧碧)  
**Affiliation:** NOIRÉA Research (Independent)  
**Version:** Submission v1.0 (Post-Review Release)  
**Date:** June 2026  
**License:** CC BY 4.0

---

## Note on This Upload

This document is the de-anonymized release of a paper submitted to the ISSRE 2026 Research Track (Submission #15) under double-blind review. The submitted version carried the author field "Anonymous Author(s)" in compliance with double-blind review requirements. This Zenodo upload restores the author attribution to Lin Hui-Pi, NOIRÉA Research.

The paper was reviewed by three reviewers and one meta-reviewer. Reviewers recognized PIM as a timely and original problem and identified the need for empirical validation on real adaptive Physical AI systems as the primary direction for future work. The paper was not accepted at ISSRE 2026.

This release establishes public priority for the NOIRÉA architectural framework and the PIM problem formalization. Subsequent empirical work is in progress; see the companion concept note *PIM Formation as a Research Direction* (uploaded concurrently) for the next research stage.

---

## Abstract

Physical AI systems increasingly operate in sustained interaction with human users across multiple deployment sessions, adapting their internal models based on human-derived signals. While this adaptive capability improves task performance, it introduces a previously unaddressed structural risk: the unintended accumulation of persistent, identity-relevant representations across session boundaries. We formalize this phenomenon as **Persistent Identity Modeling (PIM)**, a structural risk class arising from unconstrained cross-session adaptive state persistence.

This paper introduces **NOIRÉA**, a structural constraint architecture that addresses PIM through four domain-agnostic architectural requirements enforcing session-bounded isolation of identity-correlated model state:

- **R1** — Session-Bounded Identity Isolation
- **R2** — Controlled Cross-Session Persistence
- **R3** — Bounded Identity Influence
- **R4** — Revocable Identity State Reset

Empirical observability of PIM is demonstrated through a synthetic experiment. Architectural instantiation is illustrated through an adaptive Brain–Computer Interface case study.

---

## Related Works (Zenodo)

- LIN System Architecture v0.4: https://doi.org/10.5281/zenodo.20379395
- Dynamical Structuralism v1.1: https://doi.org/10.5281/zenodo.19607127
- DSCI Concept Note v0.1: [DOI pending — uploaded concurrently]
- PIM Formation Concept Note v0.1: [DOI pending — uploaded concurrently]

---

## Keywords

Adaptive systems, Physical AI, Persistent Identity Modeling, representation lifecycle, session boundaries, identity isolation, dependable systems, Brain-Computer Interface, human-AI interaction
