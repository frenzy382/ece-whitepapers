# Designing a Continuous Monitoring Framework for Third-Party Cyber Risk

**Author:** Benjamin Webb  
**Date:** July 2026  
**Category:** Information Security / Third-Party Risk Management

## Abstract

This paper describes the design and initial operationalisation of a continuous monitoring framework for third-party cyber risk within a large UK infrastructure organisation. The work focused on moving from static, point-in-time assessments to an ongoing, risk-based monitoring model using commercial security rating technology, supplemented by internal process design. Key design decisions, challenges encountered, and practical lessons are presented.

## 1. Introduction

Traditional third-party cyber assurance often relies on periodic questionnaires, certificate collection, and infrequent reviews. While useful, these approaches provide limited visibility between assessment cycles and struggle to scale across hundreds of suppliers. 

The organisation in question faced an internal audit finding that highlighted the absence of meaningful ongoing visibility of supplier cyber posture. A programme was established to address this gap. One core workstream was the design of a continuous monitoring capability that could provide near-real-time insight into supplier security ratings, trends, and material changes.

## 2. Design Objectives

The framework needed to satisfy several practical requirements:

- Scale to several hundred suppliers without proportional increases in manual effort
- Differentiate between high-impact and lower-impact suppliers
- Provide actionable signals rather than pure noise
- Integrate with existing procurement and contract management processes
- Remain proportionate and defensible under internal audit scrutiny

The decision was taken to adopt a commercial security rating platform (BitSight) as the primary technical engine, supplemented by internal process design for interpretation, escalation, and response.

## 3. Core Design Decisions

### 3.1 Rating Platform Selection and Configuration

After evaluation of available tools, BitSight was selected for its rating methodology, parent/subsidiary hierarchy support, and questionnaire capabilities. Key configuration decisions included:

- Establishment of a structured onboarding process (certification upload versus full questionnaire depending on tier)
- Definition of impact scoring to prioritise monitoring effort
- Parallel tracking of existing watchlist suppliers that pre-dated the new triage process
- Soft-launch approach with a limited pilot cohort before wider rollout

### 3.2 Continuous Monitoring Logic

A deliberate choice was made to avoid overly rigid “rules of engagement.” Instead, the framework was designed around reporting needs. Weekly rating snapshots were proposed, with a material drop threshold (greater than 20 points within a month) acting as a trigger for manual review. The review would consider trend direction, supplier impact classification, and contextual factors before any outreach.

This approach prioritised useful management information over automated enforcement.

### 3.3 Process Integration

Supporting processes were designed in parallel, including:

- Clear ownership between Information Security and Commercial/Procurement functions for incident and score-related follow-up
- Creation of a supplier cyber incident register to capture and track material events
- Alignment with emerging playbooks that defined Information Security’s role post-award

## 4. Implementation Challenges

Several practical challenges emerged during design and soft launch:

- Technical limitations around lifecycle status handling and due-date automation within the platform
- Low initial response rates during soft launch, partly attributed to email deliverability
- Difficulty categorising legacy watchlist suppliers that had never passed through the new triage process
- Need for clear internal agreement on what constituted a “material” change requiring action

These issues were addressed through iterative configuration, parallel tracking mechanisms, and explicit process design rather than pure tooling changes.

## 5. Lessons Learned

1. **Technology is necessary but not sufficient.** The rating platform provided data; the value came from the surrounding process design and clear accountability.
2. **Start with reporting, not enforcement.** Defining what leadership needed to see first produced a more sustainable monitoring model than attempting to codify every possible response rule upfront.
3. **Pilot ruthlessly.** The soft-launch approach with a small cohort surfaced configuration and process issues before they affected hundreds of suppliers.
4. **Impact classification is critical.** Without a reliable way to distinguish high-impact from lower-impact suppliers, monitoring signals quickly become noise.
5. **Documentation matters for audit.** Maintaining a clear design rationale and decision log proved valuable when explaining the approach to internal stakeholders and auditors.

## 6. Conclusion

The continuous monitoring framework described here represents a pragmatic step from static assurance toward ongoing visibility of third-party cyber risk. By combining a commercial rating platform with deliberate process design, the organisation established a scalable foundation that can evolve as volumes and maturity increase.

The work highlights that successful continuous monitoring is less about perfect tooling and more about clear objectives, proportionate thresholds, and well-defined ownership between security and commercial functions.

## References

- ISO/IEC 27001:2022 – Information security, cybersecurity and privacy protection — Information security management systems — Requirements (particularly Annex A controls related to supplier relationships)
- Internal programme documentation and design decisions (anonymised)

---

*This paper is based on practical experience designing and implementing third-party cyber risk monitoring capabilities. All organisational details have been anonymised.*
