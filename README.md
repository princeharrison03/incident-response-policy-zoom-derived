# Incident Response Policy — Derived from a Real Gap Analysis

## Overview
An Incident Response Policy written as the direct output of a prior gap analysis — not a
generic template. This policy explicitly addresses two specific weaknesses identified in
[Project #2: Zoom NIST CSF 2.0 Gap Analysis](https://github.com/princeharrison03/zoom-nist-csf-gap-analysis):
a **Detect** function gap (limited visibility into real-time abuse detection) and a **Respond**
function gap (reactive, ungoverned incident handling during the 2020 baseline period).

This project demonstrates the full GRC lifecycle in practice: **assess → identify gaps → write
the governance artifact that closes them** — rather than treating policy writing as a
standalone, disconnected exercise.

## What's Inside
📄 [`Incident_Response_Policy.md`](./Incident_Response_Policy.md) — the full policy, covering:
- Purpose and origin, explicitly tied to Project #2's findings
- Scope, definitions, and roles/responsibilities (IRT structure)
- Policy statements directly addressing the Detect and Respond gaps
- The NIST SP 800-61 incident response lifecycle
- Reporting, escalation, and enforcement
- **A traceability matrix** mapping each specific gap-analysis finding to the exact policy
  clause written to close it

## Key Differentiator
Most policy-writing portfolio pieces are generic templates with no evidentiary basis. This one
is built backward from real findings — every clause in Section 5 exists because of a specific,
named gap identified in a prior assessment, and the Appendix traceability matrix makes that
lineage explicit and auditable.

## Author
Prince Harrison Eze — building hands-on GRC experience alongside ISC2 CC / Security+
certification prep.

## Related Projects
🔗 [Zoom NIST CSF 2.0 Gap Analysis](https://github.com/princeharrison03/zoom-nist-csf-gap-analysis)
— the assessment this policy was derived from
🔗 [WhatsApp GDPR DPIA](https://github.com/princeharrison03/Whatsapp-GDPR-dpia) — a related
GRC portfolio project applying GDPR to a real, current product feature
