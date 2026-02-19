# XDR Security Assurance & Gap Analysis  
### NIST CSF 2.0 Aligned Assessment

---

## Executive Summary

This repository documents a simulated Security Assurance engagement evaluating an enterprise XDR deployment aligned to the NIST Cybersecurity Framework (CSF) 2.0.

The assessment focuses on validating detection coverage, response workflows, and security configuration posture across endpoint, identity, and SIEM layers.

Rather than assessing all 100+ CSF subcategories, this engagement scopes to relevant Detect (DE), Protect (PR), and Respond (RS) functions applicable to XDR assurance validation.

---

# Assessment Scope

Technologies in Scope:

- Microsoft Defender for Endpoint (MDE)
- Microsoft Sentinel
- Azure / Entra ID
- Endpoint & Identity Telemetry
- Automated Response Workflows

---

# NIST CSF 2.0 Scoped Alignment

This assessment evaluates the following selected CSF categories:

---

## PROTECT (PR)

| CSF ID | Control Area | Assessment Focus |
|--------|-------------|-----------------|
| PR.AC-1 | Identity Management | Entra ID account governance |
| PR.AC-7 | Multi-Factor Authentication | MFA enforcement coverage |
| PR.PT-1 | Logging & Monitoring | Telemetry ingestion validation |
| PR.IP-1 | Secure Configuration | Defender hardening & ASR rules |

---

## DETECT (DE)

| CSF ID | Control Area | Assessment Focus |
|--------|-------------|-----------------|
| DE.CM-1 | Network Monitoring | Sentinel log ingestion coverage |
| DE.CM-4 | Malicious Code Detection | Endpoint malware detection |
| DE.CM-7 | Monitoring for Unauthorized Activity | Identity attack detection |
| DE.AE-1 | Anomalous Activity Detection | Behavioral alerting effectiveness |
| DE.AE-2 | Event Analysis | Alert correlation & triage quality |

---

## RESPOND (RS)

| CSF ID | Control Area | Assessment Focus |
|--------|-------------|-----------------|
| RS.RP-1 | Response Plan Execution | Automated playbook validation |
| RS.MI-1 | Incident Containment | Endpoint isolation testing |
| RS.MI-2 | Incident Mitigation | Malware remediation workflow |
| RS.AN-1 | Incident Analysis | Investigation workflow efficiency |
| RS.CO-2 | Incident Reporting | Alert notification & SOC escalation |

---

# Assessment Methodology

The engagement follows a structured lifecycle aligned to CSF functions:

1. Configuration & Hardening Review (PR)
2. Telemetry & Monitoring Validation (DE)
3. Detection Testing (DE)
4. Response Workflow Testing (RS)
5. Risk-Based Gap Analysis & Remediation Planning

---

# Section 1 – Protect (Configuration & Hardening Review)

| Component | Current State | Gap Identified | Risk Level |
|------------|--------------|---------------|------------|
| MFA Enforcement |  |  |  |
| Conditional Access Policies |  |  |  |
| Endpoint ASR Rules |  |  |  |
| Logging Retention |  |  |  |
| Role-Based Access Controls |  |  |  |

---

# Section 2 – Detect (Detection Validation)

| Attack Scenario | Detection Result | Gap Observed | CSF Reference |
|-----------------|-----------------|--------------|---------------|
| Phishing Simulation |  |  | DE.CM-4 |
| Credential Spray |  |  | DE.CM-7 |
| Lateral Movement |  |  | DE.AE-2 |
| Ransomware Simulation |  |  | DE.CM-4 |
| Malicious PowerShell |  |  | DE.AE-1 |

---

# Section 3 – Respond (Workflow & Containment Validation)

| Workflow | Current State | Gap Identified | CSF Reference |
|----------|--------------|---------------|---------------|
| Endpoint Isolation |  |  | RS.MI-1 |
| Malware Quarantine |  |  | RS.MI-2 |
| Account Disablement |  |  | RS.MI-1 |
| Sentinel Incident Creation |  |  | RS.AN-1 |
| SOC Notification Timing |  |  | RS.CO-2 |

---

# Risk Prioritization Model

Gaps identified during testing are classified as:

- High Risk – Immediate remediation required
- Medium Risk – Remediation within 30 days
- Low Risk – Improvement recommended

---

# Deliverables

- CSF-Aligned Gap Analysis
- Detection Validation Results
- Response Effectiveness Evaluation
- Risk-Based Remediation Roadmap
- Executive Summary Report
