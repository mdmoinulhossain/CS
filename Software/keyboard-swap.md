### Keyboard swap using regedit



# Step 1: Open Registry Editor

* Press ``` Windows + R ``` to open the Run dialog.
* Type ``` regedit ``` and press Enter. Click Yes if prompted by User Account Control (UAC).


# Step 2: Navigate to the Keyboard Layout Key
(In the Registry Editor, go to the following path:)

``` 
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layout
```


# Step 3: Create or Edit the Scancode Map
(In the right-hand pane, look for an entry called ``` Scancode Map.```)

* If it doesn’t exist, create it: Right-click in the right pane and select New > Binary Value. Name it Scancode Map. Double-click the Scancode Map entry to open it for editing.

# Binary Data Explanation:

```
00 00 00 00  // Header (always the same)
00 00 00 00  // Header (always the same)
XX 00 00 00  // XX = number of remappings + 1
YY YY YY YY  // Mapping data (4 bytes per remap)
00 00 00 00  // Terminator (always the same)

```
Here I swap Y key to Z and Z key to Y.

```
00 00 00 00
00 00 00 00
02 00 00 00
15 00 2C 00
2C 00 15 00
00 00 00 00

```

Then save and restart pc.

#### General Scan Code Reference

```
Key	Scan Code (Hex)
A	1E
B	30
C	2E
D	20
E	12
F	21
G	22
H	23
I	17
J	24
K	25
L	26
M	32
N	31
O	18
P	19
Q	10
R	13
S	1F
T	14
U	16
V	2F
W	11
X	2D
Y	15
Z	2C


Space	39
Enter	1C
Backspace	0E
Tab	0F
Escape	01
Left Arrow	E04B
Right Arrow	E04D
Up Arrow	E048
Down Arrow	E050
Left Ctrl	1D
Left Alt	38
Caps Lock	3A

0	0B
1	02
2	03
3	04
4	05
5	06
6	07
7	08
8	09
9	0A
```