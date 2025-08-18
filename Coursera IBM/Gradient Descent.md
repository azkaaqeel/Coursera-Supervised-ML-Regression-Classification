Used to minimize cost of any function like linear reg

start with random values, check for diff values of w and b

linear reg, with sq error cost f, u always end up with a bow or hammock
different starting point --> different minimum found

Implementation
$$
w = w - a (d/dw) J(w,b)
$$

$$
b = b - a (d/db) J(w,b)
$$
alpha = learning rate, range between 0-1, size of step

Small alpha -> Small steps

Simultaneously update w and b.
Repeat until convergence

w will always be smaller after update

Choosing alpha
1. Too small
Baby step, so happens slowly, more steps needed to reach min

2. Too large
Possibility of missing the min first and reaching a point such that cost is greater, GD may overshoot and keep going further, may never reach minimum. Fail to converge --> Diverge

![[Pasted image 20241215160800.png]]

What if starting point = minimum?

If you are already at a local minimum, derivate will be 0, GD will leave w unchanged.

As we are approaching minimum, GD takes very small steps as the derivative gets smaller, thus a smaller value is deducted.

![[Pasted image 20241215140822.png]]

![[Pasted image 20241215141045.png]]

When using a squared error cost function with LR, the cost function will have SINGLE GLOBAL MINIMUM, not multiple local minima.

WHY?
1. Bowl Shape:
![[Pasted image 20241215144912.png]]
The cost function is a convex function.
Convex function have no other local minimum other than the global minimum.
As long as the alpha is chosen correctlty, GD will always converge to global minimum for Convex functions.

#### Batch Gradient Descent
each step of GD uses all training examples and not just a subset

## Implement Gradient Descent

You will implement gradient descent algorithm for one feature. You will need three functions.

- `compute_gradient` implementing equation (4) and (5) above
- `compute_cost` implementing equation (2) above (code from previous lab)
- `gradient_descent`, utilizing compute_gradient and compute_cost

