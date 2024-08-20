# Extends C drive
* In Disk Management section, First you need to shrink volume which you want to add with C drive. Then make unalocated this volume and ensure that no ´´healthy backup´´ (researve volume) exit. Otherwise it's make extend volume option remain disable.

## Process to delete and add volume in C
Open cmd with administration mode and follow process
```
C:\Windows\system32>diskpart

Microsoft DiskPart version 10.0.19041.3636

Copyright (C) Microsoft Corporation.
On computer: MMH

DISKPART> list disk

  Disk ###  Status         Size     Free     Dyn  Gpt
  --------  -------------  -------  -------  ---  ---
  Disk 0    Online          238 GB  2048 KB        *

DISKPART> select disk o

The disk you specified is not valid.

There is no disk selected.

DISKPART> select disk 0

Disk 0 is now the selected disk.

DISKPART> list partition

  Partition ###  Type              Size     Offset
  -------------  ----------------  -------  -------
  Partition 1    System             100 MB  1024 KB
  Partition 2    Reserved            16 MB   101 MB
  Partition 3    Primary            101 GB   117 MB
  Partition 4    Recovery           522 MB   102 GB
  Partition 5    Primary            135 GB   102 GB


DISKPART> select partition 5

Partition 5 is now the selected partition.

DISKPART> delete partition override

DiskPart successfully deleted the selected partition.

DISKPART> select partition 4

Partition 4 is now the selected partition.

DISKPART> delete partition override

DiskPart successfully deleted the selected partition.

DISKPART>exit

```
In this case I Delete to add volume from partition 5 as well partition 4 (for egnore disable extend option).