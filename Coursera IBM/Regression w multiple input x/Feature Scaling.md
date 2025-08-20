### Normalization
1. max
2. mean

#### Z-score Normalizaton
![](../../attachments/Pasted%20image%2020250819114852.png)

For scaling, check if range is too small or too large, in both conditions, one must consider rescaling
too large--> gradient descent runs v slowly

### **How to check if gradient descent is converging?**

Reminder, objective of GD is to minimize the cost function J.

Implementation
$$
w = w - a (d/dw) J(w,b)
$$

$$
b = b - a (d/db) J(w,b)
$$
alpha = learning rate, range between 0-1, size of step

Key choices --> alpha

Learning curve:

![](../../attachments/Pasted%20image%2020250819115844.png)
If cost increases after an iteration, indicates:
1. bug in code
2. poor choice of alpha
#### Automatic convergence test

i.e. setting an epsilon, if cost decreases <= epsilon, declare convergence.

#### Choosing learning rate

![](../../attachments/Pasted%20image%2020250819120424.png)





 