### Staff login from different countries within 3 hours

### Description

The KQL query identifies user accounts with successful logins from multiple distinct countries within a specified timeframe, excluding certain usernames and IP ranges.

#### Severity:
High: Multiple successful logins from different countries indicate a potential account compromise.

#### Detection:
Triggered by: Detection rule based on the provided KQL query.
Alert name: "Multiple Successful Logins from Different Countries"
Description: An alert is triggered when a user account has successful logins from multiple distinct countries within the specified timeframe, indicating potential malicious activity.

#### Collection:
Logs to be collected:
- Authentication logs (imAuthentication).
- Network logs, firewall logs, and VPN logs for additional context.
Artifacts:
- Details of the successful logins, including timestamps, IP addresses, and geolocation data.
- User activity logs.
- Device and session information.

#### Analysis:
Verify the Alert:
- Confirm the accuracy by cross-referencing with raw log data and verifying distinct geolocations of logon attempts.

Investigate User Activity:
- Review recent activities of the affected user account for any unusual or unauthorized actions.
- Examine the sequence of logons and actions taken by the user post-logon.

Contextual Information:
- Gather additional contextual information, such as usual login patterns of the user.
- Cross-reference source IP addresses with threat intelligence databases.

#### Containment and Eradication:
Immediate Containment:
- Temporarily disable the user account to prevent further unauthorized access.
- Enforce a password reset for the affected user account.

Eradication:
- Block identified malicious IP addresses.
- Remove any malware or backdoors from compromised devices.
- Revoke suspicious sessions and tokens associated with the user account.

#### Recovery:
Restore Access:
- Re-enable the user account after securing it.
- Ensure the user sets a strong, unique password.
- Implement multi-factor authentication (MFA) if not already enabled.

Monitor:
- Increase monitoring of the user account for further suspicious activities.
- Regularly review login attempts and geolocation data for anomalies.

Review and Update:
- Review and update security policies and incident response procedures based on the incident.
- Enhance detection rules and preventive measures to avoid similar incidents.

#### Approvals:
Incident Commander:
- Oversees the incident response process and approves containment and eradication measures.

IT Security Manager:
- Approves recovery steps and ensures system and network security before restoring access.

Compliance Officer:
- Reviews the incident for compliance-related implications and approves the final incident report.