### Staff login from different countries within 3 hours

#### Description:
This KQL query detects successful logins from multiple distinct countries for non-student user accounts within a specified timeframe.

#### Severity:
- **High**: Indicates potential account compromise due to successful logins from multiple countries.

#### Detection:
- **Triggered by**: Detection rule based on the provided KQL query.
- **Alert name**: "Multiple Successful Logins from Different Countries"
- **Description**: An alert triggered when a user account has successful logins from multiple distinct countries within the specified timeframe.

#### Collection:
- **Logs to be collected**:
  - Authentication logs (`imAuthentication`).
  - Network logs, firewall logs, and VPN logs for additional context.
- **Artifacts**:
  - Details of the successful logins, including timestamps, IP addresses, and geolocation data.
  - User activity logs.
  - Device and session information.

#### Analysis:
1. **Verify the Alert**:
   - Confirm the accuracy by cross-referencing with raw log data and verifying distinct geolocations of logon attempts.

2. **Investigate User Activity**:
   - Review recent activities of the affected user account for any unusual or unauthorized actions.
   - Examine the sequence of logons and actions taken by the user post-logon.

3. **Contextual Information**:
   - Gather additional contextual information, such as usual login patterns of the user.
   - Cross-reference source IP addresses with threat intelligence databases.

#### Containment and Eradication:
1. **Immediate Containment**:
   - Temporarily disable the user account to prevent further unauthorized access.
   - Enforce a password reset for the affected user account.

2. **Eradication**:
   - Block identified malicious IP addresses.
   - Remove any malware or backdoors from compromised devices.
   - Revoke suspicious sessions and tokens associated with the user account.

#### Recovery:
1. **Restore Access**:
   - Re-enable the user account after securing it.
   - Ensure the user sets a strong, unique password.
   - Implement multi-factor authentication (MFA) if not already enabled.

2. **Monitor**:
   - Increase monitoring of the user account for further suspicious activities.
   - Regularly review login attempts and geolocation data for anomalies.

3. **Review and Update**:
   - Review and update security policies and incident response procedures based on the incident.
   - Enhance detection rules and preventive measures to avoid similar incidents.

#### Approvals:
- **Incident Commander**:
  - Oversees the incident response process and approves containment and eradication measures.

- **IT Security Manager**:
  - Approves recovery steps and ensures system and network security before restoring access.

- **Compliance Officer**:
  - Reviews the incident for compliance-related implications and approves the final incident report.