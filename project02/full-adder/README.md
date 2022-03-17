First, it is necessary to evaluate the half-adder and full-adder truth tables. 

## Full Adder Truth Table

| A | B | Ci | S | Co |
| :--: | :--: | :--: | :--: | :--: |
| 0 | 0  | 0 | 0 | 0 |
| 0 | 0  | 1 | 1 | 0 |
| 0 | 1  | 0 | 1 | 0  |
| 0 | 1  | 1 | 0 | 1  |
| 1 | 0  | 0 | 1 | 0  |
| 1 | 0  | 1 | 0 |  1 |
| 1 | 1  | 0 | 0 |  1 |
| 1 | 1  | 1 | 1 |  1 |

## Full Adder Truth Table

| A | B |  S | Co |
| :--: | :--: | :--: | :--: | 
| 0 | 0  | 0 | 0 | 
| 0 | 1  | 1 | 0 | 
| 1 | 0  | 1 | 0 | 
| 1 | 1  | 1| 1 | 

Performing the calculation of boolean expressions, we have that: 

- For half adder, output is A⊕B and carry is AB. 
- For the full adder, output is A⊕B⊕Ci and carry is AB + BCi + ACi. 

In this way, we can build a full adder from half adders. Looking specifically at the output of the full adder, it appears that it is enough to include a carry input in A⊕B, forming A⊕B⊕Ci. As the output of one half adder is A⊕B, we can connect two half adders in sequence, the output of the second being Ci. Thus: Ci ⊕ (A⊕B). 

![](out_fulladder.png)

Now that we've managed to set the output, let's set the carry. Analyzing the output of the carry of the full adder (AB + BCi + ACi), we can manipulate it in order to try to find some relation with the output of the carrys of the half adders.

> ![](https://latex.codecogs.com/gif.latex?BA%20&plus;%20BCi%20&plus;%20ACi%20%3D%20B%28A%20&plus;%20Ci%29%20&plus;%20ACi%20%3D%20B%28A%20&plus;%20Ci%5Cbar%7BA%7D%29%20&plus;%20ACi%20%3D)

> ![](https://latex.codecogs.com/gif.latex?AB%20&plus;%20ACi%20&plus;%20Ci%5Cbar%7BA%7DB%20%3D%20A%28B%20&plus;%20Ci%29%20&plus;%20Ci%5Cbar%7BA%7DB%20%3D%20A%28B%20&plus;%20Ci%5Cbar%7BB%7D%29%20&plus;%20Ci%5Cbar%7BA%7DB%20%3D)

> ![](https://latex.codecogs.com/gif.latex?AB%20&plus;%20Ci%5Cbar%7BA%7DB%20&plus;%20Ci%5Cbar%7BB%7DA%20%3D%20AB%20&plus;%20Ci%28%5Cbar%7BA%7DB%20&plus;%20%5Cbar%7BB%7DA%29%20%3D%20%7B%5Ccolor%7BDarkGreen%7D%20AB%20&plus;%20Ci%28A%20%5Coplus%20B%29%7D)

With this, we have to perform a logical OR operation between the carry of the first half adder and the second.

![](carry_fulladder.png)

## Creating Digital Circuit
_all circuits were made in [logisim](http://www.cburch.com/logisim/) software, version 2.7.1._

![](fulladder.png)
