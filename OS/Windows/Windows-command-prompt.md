# to check ip:
```
ipconfig
```
```
ipconfig /all
```

$ exit - to exit cmd

# safe mode and others functions
```
msconfig
```

# pc username: 
```
net user
```
# Change username
```
Windows+R, enter lusrmgr.msc
Open Users from left menu
Right mouse click on your account and select Rename
```


# pc Hostname:
$ hostname (To changed this go to "advanced system settings" option)

# Windows version:
```
winver
```

# Pc information:
```
systeminfo
```

# To see add registry file:
```
regedit
```


# scans hard drive for file system errors(For next restart use: $ CHKDSK /f /r):
```
CHKDSK
```


# check and repair if necessary any critical Windows system files:
```
SFC / SCANNOW
```


# S.M.A.R.T. test for windows (ok/Pred Fail):
```
wmic diskdrive get status
```

# RAM Bus speed & Memory type check:
```
wmic memorychip get speed

wmic memorychip get memorytype
```
--------- Power Shell
```
Get-WmiObject Win32_PhysicalMemory | Select-Object Manufacturer, Speed, MemoryType
```


# Cleaning junk files:(Windows + r)
1. $ tree
2. $ temp
3. $ %temp%
4. $ prefetch
5. $ recent
6. $ cleanmgr (- disk cleaner)
--
7. %appdata% - for data of installation app in pc.
8. DISKMGMT.MSC - For disk management


# ShortCut key
1. alt + f4 -> pc restart/shutdown option
2. windows + L -> log off
3. f2 -> rename file
4. ctrl + alt + Delete -> options for pc log off, restart, task manager etc.
5. window + print SysRq -> Screenshot of your pc.
6. ctrl + t -> open new tab in browser and ctrl + w to close.
7. ctrl + shift + t to undo browser and ctrl + shift + w to clone whole browser.(same as file explorer)
8. windows + `+` to zoom in pc screen and `-` to zoom out
9. windows + i to open pc settings



# Credential manager
* windows credentials option saved password of autentication from localhost to remote (ex. github, outlook, virtualapp etc.) 