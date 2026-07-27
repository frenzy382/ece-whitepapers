# Practical Lessons in Third-Party Risk Scoring and Triage Tool Design

**Author:** Benjamin Webb  
**Date:** July 2026  
**Category:** Information Security / Third-Party Risk Management

## Abstract

This paper describes the design of a structured triage and risk-scoring approach for third-party cyber risk within a large UK infrastructure organisation. The work involved defining functional requirements for a triage tool, evaluating platform options, and establishing a clear decision process for routing suppliers into different assurance pathways. Key design choices, challenges, and practical lessons are presented.

## 1. Introduction

As organisations increase their reliance on third parties, the volume of suppliers requiring cyber security assessment can quickly overwhelm manual processes. Without a clear triage mechanism, security teams either apply the same level of scrutiny to every supplier (creating bottlenecks) or rely on inconsistent judgement (creating risk).

The organisation in question needed a repeatable way to classify suppliers and route them into appropriate assurance pathways. This paper outlines the approach taken to design both the decision logic and the supporting tool requirements.

## 2. Design Objectives

The triage and scoring approach needed to:

- Provide a consistent method for assessing supplier cyber risk tier
- Support different assurance pathways (light-touch versus detailed review)
- Be explainable to commercial colleagues and auditors
- Integrate with continuous monitoring enrolment decisions
- Remain usable by staff who were not full-time security specialists
- Generate clear outputs that could be handed to procurement teams

## 3. Core Design Elements

### 3.1 Risk Tiering Logic
Suppliers were classified into risk tiers based on a combination of factors, including:

- Nature of the service and data access
- Potential impact on critical operations
- Existing contractual and assurance status
- Other contextual risk indicators

The goal was to create meaningful differentiation rather than a purely mathematical score.

### 3.2 Pathway Design
Distinct pathways were defined:

- Lower-tier suppliers followed a streamlined process with limited manual intervention
- Higher-tier suppliers entered a structured Information Security review with defined outputs
- Continuous monitoring enrolment was linked to tier and residual risk

### 3.3 Tool Requirements
A formal set of functional requirements was developed for a triage support tool. These covered:

- Data capture and scoring inputs
- Workflow routing
- Output generation
- Integration points with existing procurement systems
- Reporting and audit trail capabilities

Both external platform options and an internal build were evaluated against these requirements.

## 4. Key Design Decisions

- **Judgement plus structure** – Purely automated scoring was rejected in favour of a structured but judgement-informed model.
- **Clear outputs** – Every higher-tier review was required to produce a defined set of artefacts for handover.
- **Separation of duties** – Triage decisions and detailed security review activities were deliberately distinguished.
- **Future flexibility** – The requirements were written to allow either an external platform or an internal solution.

## 5. Challenges Encountered

- Balancing consistency with the need for professional judgement
- Aligning security tiering decisions with commercial and procurement processes
- Managing legacy suppliers that had never passed through a formal triage process
- Ensuring the tool requirements remained realistic given organisational constraints

These were addressed through iterative refinement of the requirements, stakeholder workshops, and parallel process design.

## 6. Lessons Learned

1. **Triage is a decision process first, a tool second.** Getting the logic and pathways right matters more than the technology choice.
2. **Explainability is essential.** Stakeholders need to understand why a supplier was placed in a particular tier.
3. **Outputs drive behaviour.** Defining what the process must produce improves consistency more effectively than detailed procedural text alone.
4. **Legacy data is a real constraint.** Any new triage model must include a plan for existing suppliers.
5. **Requirements should enable options.** Writing technology-agnostic requirements preserved flexibility during vendor and build evaluations.

## 7. Conclusion

Designing an effective third-party risk triage and scoring approach requires more than selecting a tool. It demands clear decision logic, well-defined pathways, explicit outputs, and careful alignment with commercial processes. The work described in this paper provided a structured foundation for consistent supplier cyber risk handling and supported the wider continuous monitoring and assurance model.

## References

- ISO/IEC 27001:2022 – Annex A controls related to supplier relationships and risk assessment
- Internal triage requirements and design decisions (anonymised)

---

*This paper is based on practical experience designing triage and risk-scoring approaches for third-party cyber risk. All organisational details have been anonymised.*
