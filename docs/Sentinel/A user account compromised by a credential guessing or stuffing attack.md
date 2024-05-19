### A user account compromised by a credential guessing or stuffing attack

### Single Line Description
The alert indicates that a user account has been compromised through a credential guessing or stuffing attack, involving an IP address and accessing Microsoft Azure.

#### Severity:
High: Credential compromise poses a significant risk to sensitive data and services.

#### Detection:
Triggered by: Detection rule based on failed and successful login attempts indicative of credential guessing or stuffing.
Alert name: "User Account Compromised by Credential Guessing or Stuffing Attack"
Description: This alert is triggered when a user account shows signs of being compromised via credential guessing or stuffing, targeting a cloud application in Microsoft Azure.

#### Collection:
Logs to be collected:
- Authentication logs from Microsoft Azure.
- Sign-in logs from Microsoft Sentinel.
- Endpoint logs from Microsoft Defender for Endpoint.
- Email activity logs from Microsoft Defender for Office 365.
- Network logs, firewall logs, and VPN logs for additional context.
Artifacts:
- Details of login attempts, including timestamps, IP addresses, and geolocation data.
- User activity logs.
- Device and session information.

#### Analysis:
Verify the Alert:
- Confirm the accuracy by reviewing the login attempt patterns and correlating with raw log data.
- Check for multiple failed attempts followed by successful logins from the same IP address.

Investigate User Activity:
- Review recent activities of the affected user account for any unauthorized actions or anomalies.
- Examine the sequence of logons and actions taken by the user post-login.

Contextual Information:
- Gather additional contextual information, such as usual login patterns of the user.
- Cross-reference the IP address with threat intelligence databases to identify known malicious sources.

#### Containment and Eradication:
Immediate Containment:
- Temporarily disable the user account to prevent further unauthorized access.
- Enforce a password reset for the affected user account.

Eradication:
- Block the malicious IP address identified in the alert.
- Check and remove any detected malware or backdoors from compromised devices.
- Revoke any suspicious sessions and tokens associated with the user account.
- Update firewall and endpoint protection rules to prevent similar attacks.

#### Recovery:
Restore Access:
- Re-enable the user account after ensuring it is secure.
- Require the user to set a strong, unique password.
- Implement multi-factor authentication (MFA) for the affected user account and others if not already enabled.

Monitor:
- Increase monitoring of the user account for further suspicious activities.
- Regularly review login attempts and geolocation data for anomalies.

Review and Update:
- Review and update security policies and incident response procedures based on the incident.
- Enhance detection rules and preventive measures in Sentinel, Defender for Endpoint, and Defender for Office 365 to avoid similar incidents.

#### Approvals:
Incident Commander:
- Oversees the incident response process and approves containment and eradication measures.

IT Security Manager:
- Approves recovery steps and ensures system and network security before restoring access.

Compliance Officer:
- Reviews the incident for compliance-related implications and approves the final incident report.