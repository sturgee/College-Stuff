
Truth Table for Full Adder:  

| A   | B   | C   | Sum | Carry |
| --- | --- | --- | --- | ----- |
| 0   | 0   | 0   | 0   | 0     |
| 0   | 0   | 1   | 1   | 0     |
| 0   | 1   | 0   | 1   | 0     |
| 0   | 1   | 1   | 0   | 1     |
| 1   | 0   | 0   | 1   | 0     |
| 1   | 0   | 1   | 0   | 1     |
| 1   | 1   | 0   | 0   | 1     |
| 1   | 1   | 1   | 1   | 1     |

  

### K-Map for full adder:

###### Carry:

| A/BC | 00  | 01  | 11  | 10  |
|----- | --- | --- | --- | --- |
| 0    | 0   | 0   | 1   | 0   |
| 1    | 0   | 1   | 1   | 1   |

###### Sum:

| A/BC | 00  | 01  | 11  | 10  |
| ---- | --- | --- | --- | --- |
| 0    | 0   | 1   | 0   | 1   |
| 1    | 1   | 0   | 1   | 0   |

For Carry:
BC + AB + AC

For Sum:
A ⊕ B ⊕ C

#### Logic diagram:
##### Method 1:
![[full-adder-using-1-xor-3-and.png]]
##### Method 2:
![[full-adder-using-2-xor-2-and-1-or.png]]


#### Apparatus required for Full adder construction:

Breadboard, XOR Gate (IC7486), AND Gate (IC7408), OR Gate (IC7432)
![[full-adder-circuit-diagram.png]]