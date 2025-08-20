Data only has inputs x, no output labels y. 
Thus, algorithms seeks to find structure in the data.

We use Ordinary Least Squares method is used to fit the Linear Model.

Clustering: Groups similar data points
Anomaly Detection: Finds unusual data points. e.g. Fraud detection

Dimensiolatity Reduction: Compressing data using fewer numbers.

Jupyter Notebooks

#### Regression
Models predict numbers

1) Linear Regression:
	1) Trying to fit data on a straight line
	2) Predicts numbers

#### Terminology

x = input
ŷ = target
m = number of training samples
( x, y ) = single training example
![](Pasted%20image%2020241025215108.png)

#### Linear Regression
$$
F w,b (x) = wx + b
$$

w, b: parameters, weights, coefficients

These are adjusted to improve accuracy.

Cases
1. w=0, output constant

##### Cost Function: Squared Error Cost Function

$$
 (1/2m)Ei=1 (ŷ - y)^2
$$
$$
ŷ^i = f w, b(x^i)
$$
$$
J(w,b) = (1/2m)E ( f w,b(x^i) -(y^i))^2
$$
**Goal: Minimize the value of this function.**

1. Setting b = 0
2. Now goal is to find a value of w such that function value is minimum.

![](Pasted%20image%2020241027010357.png)

3. The **function f** depends on input x, function of x
4. The **cost function** depends on the value of w, function of w ie a parameter


![](Pasted%20image%2020241107223314.png)

**Visualing Cost Function**
In the case where we do not set b to 0, we have a 3d graph.

![](Pasted%20image%2020241109131128.png)
Multiple pairs of w and b such that they have the same value of cost function:
![](Pasted%20image%2020241109131512.png)
Minimum is the peak basically:
![](Pasted%20image%2020241109131744.png)


