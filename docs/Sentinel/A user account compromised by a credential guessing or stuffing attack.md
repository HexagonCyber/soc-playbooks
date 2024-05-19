### A user account compromised by a credential guessing or stuffing attack

### Single Line Description
The alert indicates that a user account has been compromised through a credential guessing or stuffing attack, involving an IP address and accessing Microsoft Azure.

#### **Severity**
High: Indicates a potentially severe security breach due to successful credential-based attacks.

#### **Detection**
**Triggered by**: Alert from Microsoft security products such as Sentinel, Defender for Endpoint, or Defender for Office 365.

**Alert name**: "User Account Compromised by Credential Guessing or Stuffing Attack"

**Description**: An alert triggered when a user account is accessed through credential guessing or stuffing attacks, impacting Microsoft Azure.

#### **Collection**
1. **Logs to be collected**:
   - Azure AD sign-in logs.
   - Microsoft Sentinel incident details.
   - Defender for Endpoint alerts and logs.
   - Defender for Office 365 activity logs.
2. **Artifacts**:
   - Impacted user account details.
   - Source IP address of the attack.
   - Cloud application (Microsoft Azure) activity logs.
   - Related security alerts and threat intelligence reports.

#### **Analysis**
1. **Verify the Alert**:
   - Confirm the accuracy of the alert by reviewing sign-in logs and correlating with other security alerts.
   - Validate the source IP address against known malicious IP databases.

2. **Investigate User Activity**:
   - Review recent activities of the impacted user account in Microsoft Azure.
   - Identify any anomalous or unauthorized activities performed post-compromise.

3. **Contextual Information**:
   - Gather additional information about usual login patterns and geolocations of the user.
   - Cross-reference the source IP address with threat intelligence to determine the nature of the attack.

#### **Containment and Eradication**
1. **Immediate Containment**:
   - Temporarily disable the compromised user account to prevent further unauthorized access.
   - Enforce a password reset for the affected user account across all Microsoft services.

2. **Eradication**:
   - Block the malicious IP address on firewalls and endpoint protection solutions.
   - Check for and remove any malware or backdoors if compromised devices are identified.
   - Revoke any active sessions and tokens associated with the compromised account in Microsoft Azure.

#### **Recovery**
1. **Restore Access**:
   - Re-enable the user account after ensuring it is secure.
   - Ensure the user sets a strong, unique password and understands secure password practices.
   - Implement multi-factor authentication (MFA) for the user account if not already enabled.

2. **Monitor**:
   - Increase monitoring of the user account for further suspicious activities.
   - Regularly review login attempts and access patterns to detect any future anomalies.

3. **Review and Update**:
   - Review and update security policies, user education programs, and incident response procedures based on the incident.
   - Enhance detection rules and preventive measures to avoid similar incidents in the future.

#### **Approvals**
**Incident Commander**:
- Oversees the incident response process and approves containment and eradication measures.

**IT Security Manager**:
- Approves recovery steps and ensures that the system and network are secure before restoring access.

**Compliance Officer**:
- Reviews the incident for compliance-related implications and approves the final incident report.