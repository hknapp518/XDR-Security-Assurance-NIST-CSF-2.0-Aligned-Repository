# Conditional Access Policy Review

## 1. Environment Overview

**Tenant Name:** Cyber Range Lab  
**Total Users Observed:** 2,179  
**Review Date:** 2026-02-19  
**Reviewer:** Harrison Knapp



---

## 2. Conditional Access Policies Observed

- The Conditional Access configuration interface was accessible, confirming CA capability is provisioned.
- Direct review of Conditional Access policies was limited due to role restrictions within the shared cyber range environment.
- Architecture documentation indicates MFA enforcement via Security Defaults for all tenant users.
  <img width="755" height="97" alt="3" src="https://github.com/user-attachments/assets/1901467d-8156-4d38-b45d-4f7a41a1621d" />
- The Conditional Access configuration interface was accessible, confirming CA capability is provisioned.

**Policies Enforcing MFA:**  
- Cyber range architecture specifies MFA enabled via Security Defaults.  
- Through a KQL query, the Conditional Access policy was visible; however, many users did not have the policy applied due to limited permissions and lack of elevated privileges.  
- Evidence from SigninLogs confirms MFA can succeed when the policy applies.
  <img width="1427" height="599" alt="5" src="https://github.com/user-attachments/assets/3a4256a2-bec2-4d2e-a0c7-c5d680af4460" />


Policies Targeting Admin Roles:
- Unable to confirm due to role restrictions


---

## 3. Identity Protection Status

**Sign-in Risk Policy:** Enabled (observed in SigninLogs)  
<img width="768" height="582" alt="4" src="https://github.com/user-attachments/assets/e47599cc-2656-42c9-b894-b52d124de618" />

**User Risk Policy:** Enabled (observed in SigninLogs)  
<img width="808" height="468" alt="6" src="https://github.com/user-attachments/assets/6b811553-8d5a-417c-9703-5519c3d408e5" />

**Protection Mode:** Report-only / Active (as per cyber range defaults)  
**Failed Sign-in Events Logged:** Yes (confirmed via SigninLogs query)  
**Risk-based Sign-in Events Logged:** Yes (confirmed via SigninLogs query)  
**Telemetry Ingestion into Sentinel:** Verified  
**Observations / Notes:** Identity telemetry is flowing correctly and supports DE.CM-7 and DE.AE-1 detection categories
<img width="1482" height="487" alt="7" src="https://github.com/user-attachments/assets/25696a82-5f27-4189-8bfb-bcc16a601e56" />

---

## 4. Observed Gaps / Risks

- Conditional Access Enforcement Gap
Analysis of 1,030 sign-in events revealed that 0 events had Conditional Access applied and 0 were in report-only mode, while 1,039 events returned ConditionalAccessStatus = notApplied. This suggests that Conditional Access policies are not actively evaluating or enforcing controls for observed sign-in activity during the review window.

- Risk Signals Without Automated Remediation
84 risky sign-in events and 2 aggregated risky users were detected during the evaluation period. However, no Conditional Access enforcement was triggered in response to these risk signals. This represents a potential exposure where elevated identity risk is identified but not automatically mitigated (e.g., MFA challenge or access block).

- Authentication Failure Volume
183 failed sign-in attempts were observed (~18% of total sign-ins). While expected in most environments, absence of Conditional Access enforcement increases the risk of brute-force or password spray attempts succeeding under certain conditions.


## 5. NIST CSF 2.0 Mapping

Relevant Functions:
- Protect (PR.AA – Identity Management & Access Control)
- Detect (DE.CM – Continuous Monitoring)

Control Effectiveness:
- PR.AA (Identity & Access Control): Partially Effective
Identity protection signals are operational; however, absence of Conditional Access enforcement reduces preventative control effectiveness.

- DE.CM (Continuous Monitoring): Effective
Sign-in telemetry ingestion and risk detection capabilities are functioning as expected.

- DE.AE (Anomalies & Events): Effective
Risk-based sign-in and user-level risk signals were successfully generated and logged.
