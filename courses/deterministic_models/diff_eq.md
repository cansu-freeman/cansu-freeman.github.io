  # Differential Equations

A **differential equation** is simply an equation which involves an unknown function and one or more of its derivatives. For example: *y' = x + 4y -12*.

### First Order Linear Differential Equations
---------------------------------------------

A first-order linear differential equation is one with which can be written in the standard form: ![firstorder](https://latex.codecogs.com/gif.latex?\frac{dy}{dt}&space;&plus;a(t)y&space;=&space;b(t)), where a(t) and b(t) are continuous. If b(t) = 0, we call this a **homogenous** first-order lienar differential equation.

**Theorem:** The general solution of the first order linear homogenous equation is:  ![1stOLIDE](https://latex.codecogs.com/gif.latex?y&space;=&space;ce^{-\int&space;a(t)dt})

**Example:** Find the general solution of dy/dt + ycos(t) = 0.

*First we identify that it is of the form ![firstorder](https://latex.codecogs.com/gif.latex?\frac{dy}{dt}&space;&plus;a(t)y&space;=&space;b(t)), where b(t) = 0. We can classify this as a first order linear homogenous differential equation where a(t) = cos(t). The general solution is as simple as plugging it in:*

Since a(t) = cos(t), the integral of a(t) is sin(t). Thus the solution is ![math](https://latex.codecogs.com/gif.latex?y&space;=&space;ce^{-sin(t)}), for all c. This is considered an explicit solution.

**Example:** Find th e general solution of dy/dt + ysin(t) = 0, given that y(pi) =1.

Similar to the problem above, we can compute that the general solution is ![math](https://latex.codecogs.com/gif.latex?y&space;=&space;ce^{cos(t)}) for all c. But to find the unique solution given by the initial value, we must plug in out value y(pi) = 1. Solved, we get that c = e, so the final unique solution is ![math](https://latex.codecogs.com/gif.latex?y&space;=&space;ce^{cos(t)+1})



Again, a first order **non-homogenous** differential equation is ![firstorder](https://latex.codecogs.com/gif.latex?\frac{dy}{dt}&space;&plus;a(t)y&space;=&space;b(t)), where b(t) is NOT equal to 0. We solve these using the Integrating Factor technique.

Integrating Factors of ![firstorder](https://latex.codecogs.com/gif.latex?\frac{dy}{dt}&space;&plus;a(t)y&space;=&space;b(t)) is defined as ![intfact](https://latex.codecogs.com/gif.latex?\mu&space;=&space;e^{\int&space;a(t)&space;dt}). Pro tip: this is similar to the homogenous solution, but without a minus sign and without a constant, c.

**Lemma:** 

![intfact](https://latex.codecogs.com/gif.latex?\frac{dy}{dt}&space;&plus;a(t)y&space;=&space;b(t)) is defined as ![lemma](https://latex.codecogs.com/gif.latex?\frac{d(\mu&space;y)}{dt}&space;=&space;\frac{dy}{dt}&space;\mu&space;&plus;&space;a(t)y\mu).

 **Pf:** By the chain rule and product rule,
 
![math](https://latex.codecogs.com/gif.latex?\frac{d(\mu&space;y)}{dt}&space;=&space;\frac{d\mu}{dt}&space;y&space;&plus;&space;\mu&space;\frac{dy}{dt})

![math](https://latex.codecogs.com/gif.latex?\frac{d(\mu&space;y)}{dt}&space;=&space;e^{\int&space;a(t)}&space;(\int&space;a(t)dt&space;)'y&space;&plus;&space;\mu&space;\frac{dy}{dt})

![math](https://latex.codecogs.com/gif.latex?\frac{d(\mu&space;y)}{dt}&space;=&space;\mu&space;a(t)y&space;&plus;&space;\mu&space;\frac{dy}{dt})




