# STIG-Implementations

The asset 10.0.0.62 initially failed the audit for STIG ID WN10-AU-000510, which requires the System event log size to be at least 32,768 KB.

To remediate this, I applied the following fix:

Configured the registry setting at HKLM:\SOFTWARE\Policies\Microsoft\Windows\EventLog\System
Set the MaxSize value to 32,768 KB (0x8000 in hex)
After applying the fix and re-scanning, the system now meets the required policy value, passing the audit.
<img width="1543" alt="WN10-AU-000510- Failed first scan" src="https://github.com/user-attachments/assets/3a165d64-3b59-4cc0-8c1d-4dace5c853cc" />

Second scan remediated after using powershell to 
<img width="1642" alt="WN10-AU-000510- Passed After remediation" src="https://github.com/user-attachments/assets/c6c50cad-b1a6-40e7-af19-6038f70495e1" />

