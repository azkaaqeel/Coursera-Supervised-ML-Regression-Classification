More than one feaure --? Multiple variables

Can be rewritten as vector:
![](Pasted%20image%2020241215161917.png)

Vectorization Benefits:
1) code shorter, 
2) runs faster efficientlty as Numpy uses parallel hardware capabilities
3) using LA libraries, and GPU

Comparison:

![](Pasted%20image%2020241215162203.png)

**Indexing** means referring to _an element_ of an array by its position within the array.  
**Slicing** means getting a _subset_ of elements from an array based on their indices.
![](Pasted%20image%2020241215170518.png)
![](Pasted%20image%2020241215171250.png)

Alternative to GD:
Normal equation
 1. (works only for linear regression), without iterations.
2. Slow after n>10k
3. Doesnt generalize to other algos.