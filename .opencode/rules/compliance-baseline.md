---
agentic:
  generated_by: agentic
  source: "areas/software/security/rules/compliance-baseline.md"
  repository: "https://github.com/sawrus/agent-guides"
  created_by: "v0.4.0"
  updated_by: "v0.4.0"
---
# Rule: Compliance Baseline

**Priority**: P1 — Required before processing real user data.

## Minimum Controls

| Control | Requirement |
|:---|:---|
| Encryption at rest | All databases and file storage encrypted |
| Encryption in transit | TLS 1.2+ on all endpoints |
| Access logging | All admin actions logged with actor identity |
| Backup & recovery | Data backed up daily; restore tested quarterly |
| Incident response | Defined escalation path and communication plan |
| Vulnerability scanning | Weekly automated scan; critical patched within 7 days |

## PCI DSS (if handling card data)
- Card data never stored post-authorization (use Stripe/Adyen tokens)
- Network segmentation: cardholder data environment isolated

## GDPR/CCPA (if processing EU/CA user data)
- Data processing inventory maintained
- User deletion must complete within 30 days
- Breach notification procedure in place (72-hour window for GDPR)
