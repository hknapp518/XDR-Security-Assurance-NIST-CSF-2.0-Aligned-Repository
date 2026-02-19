# Conditional Access Policy Review

## 1. Environment Overview

**Tenant Name:** Cyber Range Lab  
**Total Users Observed:** 2,179  
**Review Date:** 2026-02-19  
**Reviewer:** Harrison Knapp



---

## 2. Conditional Access Policies Observed

List of Policies:
- Unable to view full CA policies due to role restrictions in shared cyber range
- Cyber range architecture documentation specifies that MFA is enabled for all tenant users (Architecture Ref)
  <img width="755" height="97" alt="3" src="https://github.com/user-attachments/assets/1901467d-8156-4d38-b45d-4f7a41a1621d" />
- Observed Conditional Access interface exists

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
**Protection Mode:** Report-only / Active (as per cyber range defaults)  
**Failed Sign-in Events Logged:** Yes (confirmed via SigninLogs query)  
**Risk-based Sign-in Events Logged:** Yes (confirmed via SigninLogs query)  
**Telemetry Ingestion into Sentinel:** Verified  
**Observations / Notes:** Identity telemetry is flowing correctly and supports DE.CM-7 and DE.AE-1 detection categories

---

## 4. Observed Gaps / Risks

- 
- 
- 

---

## 5. NIST CSF 2.0 Mapping

Relevant Functions:
- Protect (PR.AA – Identity Management & Access Control)
- Detect (DE.CM – Continuous Monitoring)

Control Effectiveness:
