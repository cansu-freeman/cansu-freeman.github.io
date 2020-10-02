# Differential Equations
(in a nutshell)


Please note that this part of the notes are only supposed to be a refresher. They do not include everything that one would typically learn in a differential equation class. There are many theorems that are important and left out for the sake of brevity.

A **differential equation** is simply an equation which involves an unknown function and one or more of its derivatives. For example: *y' = x + 4y -12*.

---------
## 1. First Order Linear Differential Equations

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


q.e.d

This lemma is often a missed middle step when solving differential equations with the integrating factors technique. We use the understanding of this often as you'll see below. Oh by the way, the greet letter: ![mu](https://latex.codecogs.com/gif.latex?\mu).


Below is the framework for how to solve first order linear non-homogenous differential equations using the **integrating factor method** after solving for ![mu](https://latex.codecogs.com/gif.latex?\mu).

1. Multuply both sides by the integrating factor ![mu](https://latex.codecogs.com/gif.latex?\mu) and apply the lemma to rewrite the left-hand side as ![lhs](https://latex.codecogs.com/gif.latex?\frac{d(\mu&space;y)}{dy}).
2. Integrate both sides with respect to t. By the lemma, the left hand side turns into simply ![mu](https://latex.codecogs.com/gif.latex?\mu)y.
3. Solve for y. 

### [Solved Examples of First Order Linear Differential Equations](FirstOrderLinearDE.pdf)

--------
## 2. Seperable Equations

A **seperable** differential equation is one that can be written in the standard form: ![seperable](https://latex.codecogs.com/gif.latex?f(y)&space;\frac{dy}{dt}&space;=&space;g(t)), where f is a function of y. The goal is to *seperate* variables so the y's are on the left and the t's are on the right. 

Below is the framework for solving seperable differential equations:

1. Integrate both sides with respect to t. (This assumes it is already in standard form)
2. Solve for y

### [Solved Examples of Seperable Differential Equations](SeperableDE.pdf)


--------------
## 3. Second Order Linear Differential Equations with Constant Coefficients (homogeneous)

A **second-order linear** differential equation is one that involves have the second derivative within the equation. The simplest type of second order linear homogeneous differential equation are those with **constant coefficiants**. Generally, this looks like ay''+ by' + cy = 0, where a,b,c are constants.

We will seek solutions of the form y = exp(rt), where r is a real number. Let's consider what it means for y = exp(rt) to solve ay''+ by' + cy = 0.
We compute the first and second derivative of y:

![e^rt](https://latex.codecogs.com/gif.latex?y&space;=&space;e^{rt})

![re^rt](https://latex.codecogs.com/gif.latex?y'&space;=&space;re^{rt})

![r^2e^rt](https://latex.codecogs.com/gif.latex?y''&space;=&space;r^{2}e^{rt})

Then if we plug these into ay''+ by' + cy = 0, we have: ![math](https://latex.codecogs.com/gif.latex?a&space;r^{2}y&space;&plus;&space;bry&space;&plus;&space;cy&space;=&space;0). 

Factoring y on the leftside, we have: [chareq](https://latex.codecogs.com/gif.latex?a&space;r^{2}&space;&plus;&space;by&space;&plus;&space;c&space;=&space;0).

Time for a definition. Given the differential equation with constant coefficients, ay''+ by' + cy = 0, the equation ![chareq](https://latex.codecogs.com/gif.latex?a&space;r^{2}&space;&plus;&space;by&space;&plus;&space;c&space;=&space;0) is the **characteristic equation**. A root of the characterstic equation is any number, r, that solves it. 

**Preposition**: A function y = exp(rt) is a solution of ay''+ by' + cy = 0 if and only if r is a root of the characteristic equation. The infamous quadratic 
equation gives the roots to the characteristic equation. 

![quadraticeq](https://latex.codecogs.com/gif.latex?r&space;=&space;\frac{-b&space;\pm&space;\sqrt{b^{2}&space;-4ac}}{2a})

If ![equals0](https://latex.codecogs.com/gif.latex?b^{2}&space;-4ac&space;=&space;0), then there is only one solution.

If ![greater0](https://latex.codecogs.com/gif.latex?b^{2}&space;-4ac&space;>&space;0), then both roots will solve it.

If ![less0](https://latex.codecogs.com/gif.latex?b^{2}&space;-4ac&space;<&space;0), then there will be two solutions with complex roots.

### Case 1: ![greater0](https://latex.codecogs.com/gif.latex?b^{2}&space;-4ac&space;>&space;0)

**Theorem:** Consider the second order linear homogeneous differential equation ay''+ by' + cy = 0. Suppose ![greater0](https://latex.codecogs.com/gif.latex?b^{2}&space;-4ac&space;>&space;0), then ![quadraticeq](https://latex.codecogs.com/gif.latex?r_{1}&space;=&space;\frac{-b&space;-&space;\sqrt{b^{2}&space;-4ac}}{2a}) and ![quadraticeq](https://latex.codecogs.com/gif.latex?r_{2}&space;=&space;\frac{-b&space;plus&space;\sqrt{b^{2}&space;-4ac}}{2a}). Then the general solution is of the form: ![gensol](https://latex.codecogs.com/gif.latex?y&space;=&space;c_{1}e^{r_{1}t}&space;&plus;&space;c_{2}e^{r_{2}t})

### [Solved Examples of Second Order Homogeneous Linear Differential Equations](secondOrderHomog.pdf)


### Case 2: ![less0](https://latex.codecogs.com/gif.latex?b^{2}&space;-4ac&space;<&space;0)

A complex valued function of a real variable ![complexmaping](https://latex.codecogs.com/gif.latex?f:\mathbb{R}\rightarrow&space;\mathbb{C}), which inputs real numbers and outputs complex numbers.

In general, any function ![complexmaping](https://latex.codecogs.com/gif.latex?f:\mathbb{R}\rightarrow&space;\mathbb{C}) can be written as ![complexeq](https://latex.codecogs.com/gif.latex?f&space;=&space;u&space;&plus;&space;iv), where u,v map reals to reals. 

**Def:** ![complexeq](https://latex.codecogs.com/gif.latex?\inline&space;f&space;=&space;u&space;&plus;&space;iv) be a complex valued function. We define the derivative of f to be the complex valued function ![complexeq](https://latex.codecogs.com/gif.latex?\inline&space;f'&space;=&space;u'&space;&plus;&space;iv').

**Def:** The exponential function ![expmapping](https://latex.codecogs.com/gif.latex?\inline&space;e:&space;\mathbb{C}\rightarrow&space;\mathbb{C}) is defined by ![e_x](https://latex.codecogs.com/gif.latex?\inline&space;e^{x}&space;=&space;\sum&space;\frac{x^{n}}{n!}). It turns out that by considering the power-series associated with sin, cos, we can show that ![e_ir](https://latex.codecogs.com/gif.latex?\inline&space;e^{ir}&space;=&space;cosr&space;&plus;isinr,&space;r\in&space;\mathbb{R})

Now consider a +ib, any complex number.  Then, ![exp](https://latex.codecogs.com/gif.latex?\inline&space;e^{a&space;&plus;ib}&space;=&space;e^{a}\cdot&space;e^{ib}&space;=&space;e^{a}(cosb&space;&plus;isinb))

In the Case 1, we had that the solutions to the characteristic equation were a result of finding the roots to the charactersistic equations.![quadeq](https://latex.codecogs.com/gif.latex?\inline&space;r_{1,2}=&space;\frac{-b\pm\sqrt{b^{2}&space;-&space;4ac}}{2a}). In Case 2, we will have the same result, but we will convert the complex root into a real number using the definition above.


**Lemma:** Suppose y = u + iv is a solution to ay''+ by' + cy = 0. Then u, v are also solutions (given that they are real numbers).

For the proof, take the first and second derivative of y = u + iv. Then plug the y values in ay''+ by' + cy = 0.  By factoring and grouping like-terms, we end up with au''+ bu' + cu = 0  AND  av''+ bv' + cv = 0, which implies that u and v solve the differential equation.

The general solution to a complex valued second order differential equation is: ![sol](https://latex.codecogs.com/gif.latex?\inline&space;y&space;=&space;c_1u&space;&plus;&space;c_2v). 


### [Solved Examples of Second Order Complex-Valued Linear Differential Equations](ComplexRootDE.pdf)

### Case 3: ![equals0](https://latex.codecogs.com/gif.latex?b^{2}&space;-4ac&space;=&space;0)

Consider the case where ![equals0](https://latex.codecogs.com/gif.latex?b^{2}&space;-4ac&space;=&space;0). Then r = -b/2a. So ONE solution is y = exp(rt) = exp(-bt/2a). But we need two solutions since we are discussing second order second order differential equations. It turns out that ![sol2](https://latex.codecogs.com/gif.latex?\inline&space;y_2&space;=&space;te^{r_1t}) is also a linearly independent solution.

Without too much detail, as this is a refresher after all, the two solutions ![sol1](https://latex.codecogs.com/gif.latex?\inline&space;y_1&space;=&space;e^{r_1t}) and ![sol2](https://latex.codecogs.com/gif.latex?\inline&space;y_2&space;=&space;te^{r_1t}) are linearly independent because the Wronskian is not equal to 0.

### [Solved Examples of Second Order Repeated Roots Linear Differential Equations](RepeatedRootsDE.pdf)

