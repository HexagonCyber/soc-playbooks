### A user account compromised by a credential guessing or stuffing attack

### Single Line Description
The alert indicates that a user account has been compromised through a credential guessing or stuffing attack, involving an IP address and accessing Microsoft Azure.

**Severity:**
High: A compromised user account due to credential guessing or stuffing attack indicates a potential breach and unauthorized access.

**Detection:**
**Triggered by:** Security alert from Microsoft Sentinel.
**Alert name:** "User Account Compromised by Credential Guessing or Stuffing Attack"
**Description:** An alert triggered when a user account is compromised through credential guessing or stuffing, targeting a Microsoft Azure cloud application.

**Collection:**
**Logs to be collected:**
- Authentication logs from Azure AD.
- Logs from Microsoft Sentinel.
- Endpoint data from Microsoft Defender for Endpoint.
- Email activity logs from Microsoft Defender for Office 365.
**Artifacts:**
- Details of the impacted user account.
- Source IP address involved in the attack.
- Specific logs related to the Azure application activity.
- Device information associated with the user account.

**Analysis:**
**Verify the Alert:**
- Cross-reference the alert details with raw log data from Azure AD and Sentinel.
- Confirm the source IP and user activity associated with the compromise.
**Investigate User Activity:**
- Review recent activities of the compromised user account across all connected services.
- Identify any unusual or unauthorized actions performed post-compromise.
**Contextual Information:**
- Gather additional information about the source IP address from threat intelligence sources.
- Analyze the attack patterns to understand the scope and method used in the credential attack.

**Containment and Eradication:**
**Immediate Containment:**
- Disable the compromised user account to prevent further unauthorized access.
- Force a password reset and revoke all active sessions and tokens.
**Eradication:**
- Block the malicious IP address across all relevant platforms.
- Scan the user's endpoint device with Defender for Endpoint to ensure no malware or unauthorized software is present.
- Conduct a thorough review of Azure application configurations and permissions.

**Recovery:**
**Restore Access:**
- Re-enable the user account after ensuring it is secure.
- Enforce the use of a strong, unique password.
- Implement and/or verify multi-factor authentication (MFA) for the user.
**Monitor:**
- Increase monitoring of the user account for any further suspicious activities.
- Set up additional alerting for any anomalies in user logins and activities.
**Review and Update:**
- Review and update security policies and incident response procedures based on findings.
- Enhance detection rules and preventive measures to avoid similar incidents in the future.

**Approvals:**
**Incident Commander:**
- Oversees the incident response process and approves containment and eradication measures.
**IT Security Manager:**
- Approves recovery steps and ensures the system and network are secure before restoring access.
**Compliance Officer:**
- Reviews the incident for compliance-related implications and approves the final incident report.