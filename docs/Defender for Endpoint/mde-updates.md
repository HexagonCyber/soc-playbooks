# Updating Defender for Endpoint

This document describes how to download and install updates for Microsoft Defender for Endpoint (MDE) components.

---

## Engine and Security Intelligence Updates

### KB

KB2267602 - Installed via WSUS / MECM

### Automatic Updates

The MDE Engine and Signature database components are updated automatically every 8 hours, and prior to a scan being performed.

### 'MpCmdRun.exe'

Updates can also be installed using 'MpCmdRun.exe' commands.

To clear the current cache and trigger an update, run the following commands as an administrator:

```batch
cd "C:\Program Files\Windows Defender"
.\MpCmdRun.exe -removedefinitions -dynamicsignatures
.\MpCmdRun.exe -SignatureUpdate
```

### Installation File

If there are issues occurring with automatic updates, or those triggered using 'MpCmdRun.exe' commands, you can install Engine / Signature updates using an installation file.

1.  Download the relevant 'mpam-fe.exe' package from:

    <https://www.microsoft.com/en-us/wdsi/defenderupdates>

2.  Copy the executable to the affected machine and install.

### Verify update was successful

1.  Enter the following PowerShell command:

```powershell
Get-MpComputerStatus
```

1.  Review the output to ensure the following components have been successfully updated:

```powershell
AMEngineVersion                  : 1.1.19700.3
AntispywareSignatureVersion      : 1.377.21.0
AntivirusSignatureVersion        : 1.377.21.0
NISEngineVersion                 : 1.1.19700.3
NISSignatureVersion              : 1.377.21.0
```

---

## Platform Update

### Manual update

<https://go.microsoft.com/fwlink/?linkid=870379&arch=x64>

---

## Microsoft Defender for Endpoint update for EDR Sensor (MsSense)

### Check installed version:

```powershell
Get-ItemProperty -Path 'Registry::HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Advanced Threat Protection\' -Name "InstallLocation"
```

### KB

KB5005292 - Installed as part of cumulative update

<https://support.microsoft.com/en-us/topic/microsoft-defender-for-endpoint-update-for-edr-sensor-f8f69773-f17f-420f-91f4-a8e5167284ac>

### Manual update

<https://www.catalog.update.microsoft.com/Search.aspx?q=KB5005292>
