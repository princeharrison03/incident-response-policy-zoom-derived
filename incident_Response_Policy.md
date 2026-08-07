# Incident Response Policy
## Derived from Findings in: Zoom NIST CSF 2.0 Gap Analysis (Project #2)

**Author:** Prince Harrison Eze
**Date:** August 2026
**Framework Basis:** NIST CSF 2.0 (Detect, Respond functions) · NIST SP 800-61 (Incident Handling)
**Status:** Independent policy-drafting exercise / portfolio project — not affiliated with or
commissioned by Zoom Communications.

---

## 1. Purpose and Origin of This Policy

Most incident response policies are written from a generic template, disconnected from any
specific, evidence-based assessment. This one is intentionally different: it is written as the
**direct output** of a prior gap analysis.

In [Project #2 — Zoom NIST CSF 2.0 Gap Analysis](https://github.com/princeharrison03/zoom-nist-csf-gap-analysis), two specific
weaknesses were identified relative to the NIST CSF 2.0 framework:

- **Detect function gap:** publicly available information provided limited visibility into
  real-time abuse/threat detection capability, particularly evident in the 2020 "Zoombombing"
  period, where the fix was largely configuration-based rather than detection-based.
- **Respond function gap (2020 baseline):** the organization's response was reactive rather
  than governed by a pre-defined, structured incident response process.

This policy exists to demonstrate what a governance artifact addressing those exact two gaps
would look like in practice — this is the natural next step in the GRC lifecycle: **assess → find
gaps → write the policy that closes them.** It is written as if for a mid-size technology
organization, using the Zoom case only as the originating evidence base, not as an actual
policy imposed on Zoom.

---

## 2. Scope

This policy applies to:
- All employees, contractors, and third parties with access to organizational systems,
  applications, or data
- All platforms and services in scope of the organization's security program (on-premise,
  cloud, and SaaS)
- All security-relevant events, including confirmed incidents, suspected incidents, and
  near-misses

This policy does **not** cover physical security incidents or HR/personnel conduct matters,
which are addressed under separate policies.

---

## 3. Definitions

| Term | Definition |
|---|---|
| **Event** | Any observable occurrence in a system or network |
| **Security Incident** | An event (or series of events) that violates security policy, or poses an imminent threat to the confidentiality, integrity, or availability of a system or data |
| **Detection** | The capability to identify that a security incident is occurring or has occurred |
| **Response** | The structured process of containing, eradicating, and recovering from a confirmed incident |
| **IRT** | Incident Response Team |

---

## 4. Roles and Responsibilities

| Role | Responsibility |
|---|---|
| **Incident Response Team (IRT) Lead** | Owns this policy; coordinates response activities; final authority on incident severity classification |
| **Security Operations (SecOps) Analysts** | Monitor detection tooling; triage alerts; escalate confirmed incidents to the IRT |
| **System/Application Owners** | Support containment and recovery actions for systems under their ownership; provide technical context during investigation |
| **Communications/Legal Liaison** | Manages internal and external communications, including regulatory notification obligations where applicable |
| **All Personnel** | Required to report suspected incidents promptly through defined channels; no individual is authorized to independently "fix and forget" a suspected incident without reporting it |

---

## 5. Policy Statements

### 5.1 Addressing the Detect Gap

The organization must not rely solely on user-reported issues (the pattern observed in the
Zoom 2020 case, where abuse was largely surfaced through public/user complaints rather than
internal detection) as its primary detection mechanism.

- **5.1.1** Security monitoring capability must be deployed and actively maintained across
  all in-scope systems, with defined alert thresholds reviewed at least quarterly.
- **5.1.2** Detection coverage must be explicitly mapped against known abuse patterns
  relevant to the organization's platform type (e.g., for a communications platform:
  unauthorized access attempts, anomalous session/meeting join patterns, credential
  stuffing indicators).
- **5.1.3** Detection capability must be tested at least annually through simulated
  incidents (tabletop exercises or red-team style testing), not assumed to be effective
  simply because monitoring tools are technically deployed.
- **5.1.4** Any detection gap identified through testing must be logged in a tracked
  remediation register with an assigned owner and target closure date — detection gaps
  may not remain open indefinitely without documented risk acceptance from the IRT Lead.

### 5.2 Addressing the Respond Gap

The organization's response to a confirmed incident must follow a pre-defined structure,
not an ad hoc, case-by-case reaction (the 2020 baseline pattern this policy is directly
correcting).

- **5.2.1** All confirmed security incidents must be classified by severity (Critical, High,
  Medium, Low) using pre-agreed criteria, within 1 hour of confirmation for Critical/High
  incidents.
- **5.2.2** A designated Incident Response Team must be activated according to severity,
  with defined response time targets (e.g., Critical incidents require IRT activation within
  30 minutes of confirmation).
- **5.2.3** Public or customer-facing communication regarding a confirmed incident must be
  reviewed by the Communications/Legal Liaison before release — reactive, ungoverned
  public statements (as seen in early-stage incident handling generally) are not permitted
  under this policy.
- **5.2.4** Every confirmed incident must produce a post-incident report within 10 business
  days of resolution, including root cause, response timeline, and specific corrective
  actions — feeding back into the Detect requirements in Section 5.1.

### 5.3 Continuous Feedback Loop (Closing the Assess–Remediate Loop)

- **5.3.1** Findings from post-incident reports (5.2.4) must be reviewed against the
  organization's current gap analysis or risk register at least annually, to confirm whether
  previously identified Detect/Respond gaps have actually been closed in practice — not
  just on paper.
- **5.3.2** This policy itself must be reviewed and re-approved annually, or immediately
  following any Critical-severity incident.

---

## 6. Incident Response Lifecycle

This policy adopts the NIST SP 800-61 incident handling lifecycle:

1. **Preparation** — maintaining detection tooling, trained personnel, and this policy itself
2. **Detection and Analysis** — identifying and confirming that an incident has occurred
   (directly governed by Section 5.1)
3. **Containment, Eradication, and Recovery** — limiting damage, removing the threat, and
   restoring normal operations
4. **Post-Incident Activity** — the post-incident report and feedback loop (Section 5.2.4,
   5.3.1)

---

## 7. Reporting and Escalation

- Suspected incidents must be reported immediately through the organization's designated
  reporting channel (e.g., a dedicated security inbox or ticketing category) — not through
  informal channels like direct messages to individual staff.
- No employee, including system owners, may unilaterally decide a suspected incident is
  "not significant enough to report." Triage authority sits with SecOps/IRT, not the reporting
  individual.
- External reporting obligations (regulators, affected customers, law enforcement where
  applicable) are the responsibility of the Communications/Legal Liaison and must follow
  applicable legal timelines (e.g., GDPR's 72-hour breach notification requirement, where in
  scope).

---

## 8. Compliance and Enforcement

Failure to report a suspected incident, or unauthorized independent action taken to conceal
or resolve an incident outside this process, will be treated as a policy violation subject to
disciplinary review, in line with the organization's broader HR and security policies.

---

## 9. Review Cycle

This policy is reviewed **annually**, and additionally following any Critical-severity incident, in
line with Section 5.3.2.

---

## Appendix: Traceability Matrix — Gap Analysis to Policy Clause

This table is the core differentiator of this project: it shows direct, explicit lineage from a
specific finding in Project #2 to a specific clause in this policy, rather than a generic policy
written with no evidentiary basis.

| Gap Analysis Finding (Project #2) | Policy Clause Addressing It |
|---|---|
| Detect function — "limited public evidence of real-time abuse detection capability" (2020) | 5.1.1, 5.1.2 |
| Detect function — reliance on user reports rather than internal detection | 5.1.1 |
| Detect function — no visibility into whether detection is actually tested/effective | 5.1.3, 5.1.4 |
| Respond function — "reactive but fast" characterized 2020 baseline, not a governed process | 5.2.1, 5.2.2 |
| Respond function — public communication handled reactively during crisis | 5.2.3 |
| Recover function — recovery treated as a one-off "event" rather than a structured, repeatable process | 5.2.4, 5.3.1 |

---

*This document is an independent training/portfolio exercise. It is written using the Zoom
NIST CSF 2.0 gap analysis (Project #2) as an illustrative evidence base only, and does not
represent an actual policy adopted by, or imposed on, Zoom Communications.*
