## Troubleshooting - API Communication Issue

### Problem

The Web VM could not access the API running on the API VM.

### Investigation

- Verified API was running successfully.
- Verified Kestrel was listening on `0.0.0.0:5231`.
- Verified Azure NSG rule allowed TCP 5231 from the Web subnet.
- Tested connectivity using `Test-NetConnection`.

### Root Cause

Windows Defender Firewall on the API VM was blocking inbound TCP port 5231.

### Resolution

Created a Windows Firewall rule:

```powershell
New-NetFirewallRule -DisplayName "Allow ASP.NET API 5231" -Direction Inbound -Protocol TCP -LocalPort 5231 -Action Allow
```

### Result

The Web VM successfully communicated with the API over the private Azure VNet.

### special Note

Test-NetConnection 
- If TcpTestSucceeded is False, it's a connectivity problem.
- If it's True but the browser fails, it's probably an application problem.
