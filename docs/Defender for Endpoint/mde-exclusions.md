# Automatic Exclusions

Automatic Exclusions apply to real-time detections only and do not apply to on-demand scans.

These exclusions are described on the following URL:

<https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/configure-server-exclusions-microsoft-defender-antivirus?view=o365-worldwide>

---

# Scheduled Scans

Exclusions for scheduled scans (full / quick / custom) must be explicitly defined in the AMP policy.

---

# Sense EDR

Exclusions for Sense EDR must be defined using Custom Indicators in the Microsoft 365 Defender portal.

Due to limitations with Custom Indicators (file hash / domain / IP / cert supported only) a ticket must be raised with Microsoft Support to implement any additional Indicators which are not supported in the portal. Microsoft can then implement these on a per-Tenant basis.