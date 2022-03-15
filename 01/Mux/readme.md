## Truth Table

| First Input (A) | Second Input (B) | Control Signal (S) | Output |
| :--: | :--: | :--: | :--: |
| 0 | 0  | 0 | 0 |
| 0 | 0  | 1 | 0 |
| 0 | 1  | 0 | 0 |
| 0 | 1  | 1 | 1 |
| 1 | 0  | 0 | 1 |
| 1 | 0  | 1 | 0 |
| 1 | 1  | 0 | 1 |
| 1 | 1  | 1 | 1 |

To find the Boolean expression equivalent to the output values, we will use the concept of minimum terms. That is, we will select only positive outputs (1) and form the expression according to the following rule: 

- Input equals zero ➝ Output complemented, otherwise ➝ output equals one. 

### Expression

> ![](https://latex.codecogs.com/gif.latex?%5Cbar%7BA%7DBS%20&plus;%20A%5Cbar%7BB%7D%5Cbar%7BS%7D%20&plus;%20AB%5Cbar%7BS%7D%20&plus;%20ABS)

### Simplification
> ![](https://latex.codecogs.com/gif.latex?%7B%5Ccolor%7BTeal%7D%5Cbar%7BA%7DBS%7D%20&plus;%20%7B%5Ccolor%7BOrange%7DA%5Cbar%7BB%7D%5Cbar%7BS%7D%7D%20&plus;%20%7B%5Ccolor%7BTeal%7DAB%5Cbar%7BS%7D%7D%20&plus;%20%7B%5Ccolor%7BOrange%7DABS%7D%20%3D)

> ![](https://latex.codecogs.com/gif.latex?BS%28%5Cbar%7BA%7D%20&plus;%20A%29%20&plus;%20%5Cbar%7BS%7D%28A%5Cbar%7BB%7D%20&plus;%20AB%29%20%3D)

> ![](https://latex.codecogs.com/gif.latex?BS%20&plus;%20%5Cbar%7BS%7D%5BA%28%5Cbar%7BB%7D%20&plus;%20B%29%5D%20%3D)

> ![](https://latex.codecogs.com/gif.latex?BS%20&plus;%20%5Cbar%7BS%7D%5BA%281%29%5D%20%3D)

> ![](https://latex.codecogs.com/gif.latex?BS%20&plus;%20%5Cbar%7BS%7DA)

## Creating Digital Circuit with the AND, OR and NOT gates

First, we will use the basic logical operations: AND, OR and NOT.

![](basic_mux.png)

Taking into account the universality of the NAND logic gate, we can convert the logic circuit using just this logic operation. 

![](nand_mux.png)





