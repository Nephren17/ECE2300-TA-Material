# Midterm 2 RC Part 2

By Mo Yang

## Poisson Equation Review

$$\nabla^2 V = -\frac{\rho}{\epsilon}$$

- **In Cartesian System:**

  $$\nabla^2 V = \frac{\partial^2 V}{\partial x^2} + \frac{\partial^2 V}{\partial y^2} + \frac{\partial^2 V}{\partial z^2}$$

- **In Cylindrical System:**

  $$\nabla^2 V = \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial V}{\partial r} \right) + \frac{1}{r^2} \frac{\partial^2 V}{\partial \varphi^2} + \frac{\partial^2 V}{\partial z^2}$$

- **In Spherical System:**

  $$\nabla^2 V = \frac{1}{r^2} \frac{\partial}{\partial r} \left( r^2 \frac{\partial V}{\partial r} \right) + \frac{1}{r^2 \sin \theta} \frac{\partial}{\partial \theta} \left( \sin \theta \frac{\partial V}{\partial \theta} \right) + \frac{1}{r^2 \sin^2 \theta} \frac{\partial^2 V}{\partial \varphi^2}$$





## Boundary Value problem in Cartesian Coordinate

1. Laplace’s Equation for $ V $ in Cartesian coordinates is

   $$\frac{\partial^2 V}{\partial x^2} + \frac{\partial^2 V}{\partial y^2} + \frac{\partial^2 V}{\partial z^2} = 0$$

2. To use the Separation of variables and take it into Laplace’s Equation.

   $$\frac{1}{X(x)} \frac{d^2 X(x)}{dx^2} + \frac{1}{Y(y)} \frac{d^2 Y(y)}{dy^2} + \frac{1}{Z(z)} \frac{d^2 Z(z)}{dz^2} = 0$$

3. In order to satisfy all $ x, y, z $ values, these three parts should be constant. Then we can get

   $$\frac{1}{X(x)} \frac{d^2 X(x)}{dx^2} = -k_x^2, \quad \frac{1}{Y(y)} \frac{d^2 Y(y)}{dy^2} = -k_y^2, \quad \frac{1}{Z(z)} \frac{d^2 Z(z)}{dz^2} = -k_z^2$$

   $$k_x^2 + k_y^2 + k_z^2 = 0$$

4. List the boundary conditions we got.

5. The general solution formats for above differential equation $ \frac{d^2 X(x)}{dx^2} + k_x^2 X(x) = 0 $ are:

   | $ k_x $  |            $ X(x) $             |        Exponential Form        |
   | :------: | :-----------------------------: | :----------------------------: |
   |    0     |                0                |        $ A_0 x + B_0 $         |
   | + $ k $  |  $ A_1 \sin kx + B_1 \cos kx $  | $ C_1 e^{jkx} + D_1 e^{-jkx} $ |
   | - $ jk $ | $ A_2 \sinh kx + B_2 \cosh kx $ |  $ C_2 e^{kx} + D_2 e^{-kx} $  |

   We need to choose the proper form of solution given boundary condition.

   - If $ V $ is independent of $ x $, we can see $ X(x) = 1 $.
   
6. Find the coefficients through boundary condition.



### Exercise 1

Two infinite grounded metal plates lie parallel to the xz plane, one at y = 0, the other at y = a. The left end, at x = 0, is closed off with an infinite strip insulated form the two plates and maintained at a specific potential V0(y). Find the potential inside this ”slot”.

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240624184759610.png" alt="image-20240624184759610" style="zoom:70%;" />





































## Boundary-value Problems in Cylindrical Coordinates

1. Laplace Equation:

   $$\frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial V}{\partial r} \right) + \frac{1}{r^2} \frac{\partial^2 V}{\partial \varphi^2} + \frac{\partial^2 V}{\partial z^2} = 0$$

2. General solution: Assuming $ V $ is independent of $ z $.

   $$\frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial V}{\partial r} \right) + \frac{1}{r^2} \frac{\partial^2 V}{\partial \varphi^2} = 0$$

3. Separation of variables: $ V(r, \varphi) = R(r) \Phi(\varphi) $

4. Equations for $ \Phi(\varphi) $:

   $$\frac{d^2 \Phi(\varphi)}{d \varphi^2} + k^2 \Phi(\varphi) = 0$$

   Since the solution should be periodic among $ \varphi $, we can get $ k = n $ and we should use $ k^2 > 0 $ be like

   $$\Phi(\varphi) = A_\varphi \sin n\varphi + B_\varphi \cos n\varphi$$

5. Equations for $ R(r) $: After using separation of variables, we get

   $$\frac{r}{R(r)} \frac{d}{dr} \left( r \frac{dR(r)}{dr} \right) = k^2$$

   Which is a second order differential equation

   $$r^2 \frac{d^2 R(r)}{dr^2} + r \frac{dR(r)}{dr} - n^2 R(r) = 0$$

   And the general solution is

   $$R(r) = A_r r^n + B_r r^{-n}$$

   * If we study the area including $ r = 0 $, $ B_r = 0 $. Otherwise, $ V $ goes to infinity at $ r = 0 $.
   * If we study the area including $ r = \infty $, $ S_r = 0 $.

6. Equations for $ V_n(r, \varphi) $,

   $$V_n(r, \varphi) = r^n \left( A_n \sin n\varphi + B_n \cos n\varphi \right) + r^{-n} \left( A_n' \sin n\varphi + B_n' \cos n\varphi \right), \quad n \neq 0$$

7. Special case: if $ V $ is independent of $ \varphi $, $ k = 0 $. Then we get

   $$\frac{d}{dr} \left( r \frac{dR(r)}{dr} \right) = 0$$

   $$V(r) = C_1 \ln r + C_2$$





## Boundary-value Problem in Spherical Coordinates

1. Since we only consider the situation that $ V $ is independent of $ \varphi $, the Laplace Equation in Spherical coordinates is simplified to

   $$\frac{1}{R^2} \frac{\partial}{\partial R} \left( R^2 \frac{\partial V}{\partial R} \right) + \frac{1}{R^2 \sin \theta} \frac{\partial}{\partial \theta} \left( \sin \theta \frac{\partial V}{\partial \theta} \right) = 0$$

2. By using separation of variables, we assign $ V(R, \theta) = \Gamma(R) \Theta(\theta) $. Then it looks like

   $$\frac{1}{\Gamma(R)} \frac{d}{dR} \left[ R^2 \frac{d\Gamma(R)}{dR} \right] + \frac{1}{\Theta(\theta) \sin \theta} \frac{d}{d\theta} \left[ \sin \theta \frac{d\Theta(\theta)}{d\theta} \right] = 0$$

3. General solutions for $ \Gamma(R) $. Firstly, we assume the part for $ \Gamma(R) $ equals to $ k^2 $:

   $$\frac{1}{\Gamma(R)} \frac{d}{dR} \left[ R^2 \frac{d\Gamma(R)}{dR} \right] = k^2$$

   It is actually a second differential equation:

   $$R^2 \frac{d^2 \Gamma(R)}{dR^2} + 2R \frac{d\Gamma(R)}{dR} - k^2 \Gamma(R) = 0$$

   The solution form is

   $$\Gamma_n(R) = A_n R^n + B_n R^{-(n+1)}, \quad \text{where } k = n(n+1), \, n > 0$$

4. General solutions for $ \Theta $. Similarly, we can get

   $$\frac{1}{\Theta(\theta) \sin \theta} \frac{d}{d\theta} \left[ \sin \theta \frac{d\Theta(\theta)}{d\theta} \right] = -k^2$$

   Since we already know $ n(n+1) = k^2 $, we can get the second differential equation:

   $$\frac{d}{d\theta} \left[ \sin \theta \frac{d\Theta(\theta)}{d\theta} \right] + n(n+1) \Theta(\theta) \sin \theta = 0$$

   It is called Legendre’s equation and for $ \theta \in [0, \pi] $, the solution has special forms called Legendre’s polynomials:

   $$\Theta_n(\theta) = P_n(\cos \theta)$$

   There are some solution forms for usual $ n $:

   | $ n $ | $ P_n(\cos \theta) $                             |
   | ----- | ------------------------------------------------ |
   | 0     | 1                                                |
   | 1     | $ \cos \theta $                                  |
   | 2     | $ \frac{1}{2}(3 \cos^2 \theta - 1) $             |
   | 3     | $ \frac{1}{2}(5 \cos^3 \theta - 3 \cos \theta) $ |

5. By combining them together,

   $$V_n(R, \theta) = \left[ A_n R^n + B_n R^{-(n+1)} \right] P_n(\cos \theta)$$





### Exercise 2

A grounded conductor ball of radius R is placed in a uniform outer field $E_0$, find the score of the space field Cloth.

![image-20240624190731644](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240624190731644.png)





























### Method of Image

Methods of images is a smart way to solve electrostatics to satisfy certain boundary conditions, utilizing equivalent image charge.(e.g. The voltage potential of a plate is 0 everywhere) The use of  image charge is actually based on the uniqueness theorem of electrostatic solution

#### Exercise 3

If there is a conductive sphere with radius $ R $ and a total charge $ Q $, but it is not grounded, and a point charge $ q $ is located outside the sphere at a distance $ d $ from the center of the sphere, how can we solve for the electric field produced by this system outside the sphere and the force experienced by the point charge outside the sphere?

![image-20240717081214632](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240717081214632.png)























### Good luck on your exam!

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240716223416245.png" alt="image-20240716223416245" style="zoom:23%;" />
