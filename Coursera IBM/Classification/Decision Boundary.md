i dont get how but for logistic regression, the decision boundary is when z=0
decision boundaries can be linear and non linear too (higher order poly terms)

![](../../attachments/Pasted%20image%2020250819210020.png)

## Cost function for logistic regression

- squared error cost func is not ideal for log regression
- why? because the cost function is a non convex and GD will keep getting stuck in local minima look:
![](../../attachments/Pasted%20image%2020250819210358.png)

Note:

1/2 is put inside the summation to make math easier later.

![](../../attachments/Pasted%20image%2020250819210811.png)
loss on single training example, loss is equal to half of squared difference
![](../../attachments/Pasted%20image%2020250819211225.png)

We zoomed because that is the valid portion of graph for us, why? because logistic regression output range ie f is from 0-1, so notice x axis, we r cropping from there.
![](../../attachments/Pasted%20image%2020250819211500.png)

with these cost functions, we can use GD.
reminder: cost function is the func of the entire training set and is avg of all the loss func on individual training egs (1/m x sum of all training eg cost)


