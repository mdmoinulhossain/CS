Having trouble connecting your printer on Windows 7, 10, or 11? With the infamous "Windows Cannot Connect to the Printer" error with code 0x0000011b?

In the Registry Editor window, navigate to...
```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Print
```
```
Rename: DWORD value to ‘RpcAuthnLevelPrivacyEnabled’ === value (0)
```
Then go to ```services``` and restart ```Print Spooler```