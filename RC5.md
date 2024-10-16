# RC5: Electronic Solutions and Steady Electric Currents

by Mo Yang



## Boundary Value Problem in Cartesian Coordinates

We have Laplace’s equation:
$$
\frac{\partial^2 V}{\partial x^2} + \frac{\partial^2 V}{\partial y^2} + \frac{\partial^2 V}{\partial z^2} = 0
$$

If we assume $ V(x, y, z) = X(x)Y(y)Z(z) $, then we have
$$
\frac{1}{X(x)} \frac{d^2 X(x)}{dx^2} + \frac{1}{Y(y)} \frac{d^2 Y(y)}{dy^2} + \frac{1}{Z(z)} \frac{d^2 Z(z)}{dz^2} = 0 \tag{1}
$$

Let $ f(x) = \frac{1}{X(x)} \frac{d^2 X(x)}{dx^2} $, $ f(y) = \frac{1}{Y(y)} \frac{d^2 Y(y)}{dy^2} $, $ f(z) = \frac{1}{Z(z)} \frac{d^2 Z(z)}{dz^2} $, since $ f(x) $, $ f(y) $, and $ f(z) $ are independent of each other, to make Eq.(1) always exist, $ f(x) $, $ f(y) $, and $ f(z) $ must all be constants. Therefore,
$$
\frac{df(x)}{dx} = 0, \quad \frac{df(y)}{dy} = 0, \quad \frac{df(z)}{dz} = 0
$$

Then after simplifying, we know that
$$
\frac{d^2 X(x)}{dx^2} + k_x^2 X(x) = 0, \quad \frac{d^2 Y(y)}{dy^2} + k_y^2 Y(y) = 0, \quad \frac{d^2 Z(z)}{dz^2} + k_z^2 Z(z) = 0
$$
where $ k_x^2 $, $ k_y^2 $, and $ k_z^2 $ are constants and
$$
k_x^2 + k_y^2 + k_z^2 = 0
$$

Possible solutions of $ X''(x) + k_x^2 X(x) = 0 $:

| $ k_x^2 $ |             $ k_x $             |            $ X(x) $            |
| :-------: | :-----------------------------: | :----------------------------: |
|     0     |                0                |        $ A_0 x + B_0 $         |
|  + $ k $  |  $ A_1 \sin kx + B_1 \cos kx $  | $ C_1 e^{jkx} + D_1 e^{-jkx} $ |
| - $ jk $  | $ A_2 \sinh kx + B_2 \cosh kx $ |  $ C_2 e^{kx} + D_2 e^{-kx} $  |

Where $ k $ is real. And constant $ A $ and $ B $ should be determined by boundary conditions.



### Exercise 1

Two infinite grounded metal plates lie parallel to the xz plane, one at y = 0, the other at y = a. The left end, at x = 0, is closed off with an infinite strip insulated form the two plates and maintained at a specific potential V0(y). Find the potential inside this ”slot”.

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240624184759610.png" alt="image-20240624184759610" style="zoom:70%;" />



























## Boundary Value Problem in Spherical Coordinates

We have Laplace’s equation:
$$
\nabla^2 V = \frac{1}{r^2} \frac{\partial}{\partial r} \left( r^2 \frac{\partial V}{\partial r} \right) + \frac{1}{r^2 \sin \theta} \frac{\partial}{\partial \theta} \left( \sin \theta \frac{\partial V}{\partial \theta} \right) + \frac{1}{r^2 \sin^2 \theta} \frac{\partial^2 V}{\partial \phi^2} = 0
$$

We assume that the solution is independent of $ \phi $, then we have
$$
\nabla^2 V = \frac{1}{r^2} \frac{\partial}{\partial r} \left( r^2 \frac{\partial V}{\partial r} \right) + \frac{1}{r^2 \sin \theta} \frac{\partial}{\partial \theta} \left( \sin \theta \frac{\partial V}{\partial \theta} \right) = 0
$$

Assume $ V(r, \theta) = R(r)\Theta(\theta) $. Putting this into the above equation, and dividing by $ V $,
$$
\frac{1}{R} \frac{d}{dr} \left( r^2 \frac{dR}{dr} \right) + \frac{1}{\Theta \sin \theta} \frac{d}{d\theta} \left( \sin \theta \frac{d\Theta}{d\theta} \right) = 0
$$

Since the first term depends only on $ r $, and the second only on $ \theta $, it follows that each must be a constant:
$$
\frac{1}{R} \frac{d}{dr} \left( r^2 \frac{dR}{dr} \right) = l(l + 1), \quad \frac{1}{\Theta \sin \theta} \frac{d}{d\theta} \left( \sin \theta \frac{d\Theta}{d\theta} \right) = -l(l + 1)
$$

Here $ l(l + 1) $ is just a fancy way of writing the separation constant—you’ll see in a minute why this is convenient.

As always, separation of variables has converted a partial differential equation into ordinary differential equations. The radial equation,
$$
\frac{d}{dr} \left( r^2 \frac{dR}{dr} \right) = l(l + 1)R
$$
has the general solution
$$
R(r) = Ar^l + \frac{B}{r^{l+1}}
$$

$ A $ and $ B $ are the two arbitrary constants to be determined by boundary conditions. The angular equation is:
$$
\frac{d}{d\theta} \left( \sin \theta \frac{d\Theta}{d\theta} \right) = -l(l + 1) \sin \theta \Theta
$$

Its solutions are Legendre polynomials in the variable $ \cos \theta $:
$$
\Theta(\theta) = P_l(\cos \theta)
$$

$ P_l(x) $ is most conveniently defined by the Rodrigues formula:
$$
P_l(x) \equiv \frac{1}{2^l l!} \left( \frac{d}{dx} \right)^l(x^2-1)^l
$$

The first few Legendre polynomials are listed below:
$$
\begin{aligned}
P_0(x) &= 1 \\
P_1(x) &= x \\
P_2(x) &= \frac{3x^2 - 1}{2} \\
P_3(x) &= \frac{5x^3 - 3x}{2} \\
P_4(x) &= \frac{35x^4 - 30x^2 + 3}{8} \\
P_5(x) &= \frac{63x^5 - 70x^3 + 15x}{8}
\end{aligned}
$$

In the case of azimuthal symmetry, then, the most general separable solution to Laplace’s equation, consistent with minimal physical requirements, is
$$
V(r, \theta) = \left( A_l r^l + \frac{B_l}{r^{l+1}} \right) P_l(\cos \theta)
$$

As before, separation of variables yields an infinite set of solutions, one for each $ l $. The general solution is the linear combination of separable solutions:
$$
V(r, \theta) = \sum_{l=0}^{\infty} \left( A_l r^l + \frac{B_l}{r^{l+1}} \right) P_l(\cos \theta)
$$



### Exercise 2

A grounded conductor ball of radius R is placed in a uniform outer field $E_0$, find the score of the space field Cloth.

![image-20240624190731644](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240624190731644.png)





































## Boundary Value Problem in Cylindrical Coordinates

### Laplace’s Equation in Cylindrical Coordinates

$$
\frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial V}{\partial r} \right) + \frac{1}{r^2} \frac{\partial^2 V}{\partial \phi^2} + \frac{\partial^2 V}{\partial z^2} = 0
$$

Assuming $ V $ has no $ z $ dependence,

$$
\frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial V}{\partial r} \right) + \frac{1}{r^2} \frac{\partial^2 V}{\partial \phi^2} = 0
$$

Assume

$$
V(r, \phi) = R(r) \Phi(\phi)
$$

$$
\frac{r}{R(r)} \frac{d}{dr} \left( r \frac{dR(r)}{dr} \right) + \frac{1}{\Phi(\phi)} \frac{d^2 \Phi(\phi)}{d\phi^2} = 0
$$

Therefore,

$$
\frac{r}{R(r)} \frac{d}{dr} \left( r \frac{dR(r)}{dr} \right) = k^2
$$

$$
\frac{d^2 \Phi(\phi)}{d\phi^2} + k^2 \Phi(\phi) = 0
$$

has solution

$$
R(r) = A_r r^n + B_r r^{-n}
$$

$$
\Phi(\phi) = A_{\phi} \sin n\phi + B_{\phi} \cos n\phi
$$

Therefore,

$$
V_n(r, \phi) = r^n (A_n \sin n\phi + B_n \cos n\phi) + r^{-n} (A'_n \sin n\phi + B'_n \cos n\phi), \quad n \neq 0
$$

In the special case where $ k = 0 $,

$$
\frac{d^2 \Phi(\phi)}{d\phi^2} = 0
$$

$$
\Phi(\phi) = A_0 \phi + B_0, \quad k = 0
$$

and $ A_0 = 0 $ if there is no circumferential variations. Meanwhile,

$$
\frac{d}{dr} \left( r \frac{dR(r)}{dr} \right) = 0
$$

$$
R(r) = C_0 \ln r + D_0, \quad k = 0
$$

Therefore,

$$
V(r) = C_1 \ln r + C_2
$$

Thus, the general solution is

$$
V(r, \phi) = a_0 + b_0 \ln r + \sum_{k=1}^{\infty} \left( r^k (a_k \cos k\phi + b_k \sin k\phi) + r^{-k} (c_k \cos k\phi + d_k \sin k\phi) \right)
$$







## Steady Electric Currents

### Current Density and Ohm’s Law

$$
I = \int_S \mathbf{J} \cdot d\mathbf{s} \quad (\text{A})
$$

where $ \mathbf{J} $ is the volume current density or current density, defined by

$$
\mathbf{J} = Nqu \quad (\text{A/m}^2)
$$

where $ N $ is the number of charge carriers per unit volume, each of charge $ q $ moves with a velocity $ u $.

Since $ Nq $ is the free charge per unit volume, by $ \rho = Nq $, we have:

$$
\mathbf{J} = \rho u \quad (\text{A/m}^2)
$$

For conduction currents,

$$
\mathbf{J} = \sigma \mathbf{E} \quad (\text{A/m}^2)
$$



### Exercise 3

A thin spherical conductor with radius $ R $ is centered at point $ O $. On the surface of the sphere, there are three points $ A $, $ B $, and $ C $ with semi-diameters $ OA $, $ OB $, and $ OC $ being mutually perpendicular. There are thin conductive wires connected at points $ A $ and $ B $ on the sphere's surface, and these two thin conductive wires are connected to a power source. It is known that an electric current $ I_0 $ flows into the sphere at point $ A $ and flows out of the sphere at point $ B $, as shown in Figure 2-5(a). Determine the current density at point $ C $ (i.e., the current per unit length flowing through the direction of the electric current at point $ C $).

---

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240624192822871.png" alt="image-20240624192822871" style="zoom:50%;" />























## Referece

- Fan Hu, RC Slides, VE230.
- Prof. Nana Liu, Slides, VE230.
- Jiafu Cheng, Electromegnetics.
- Lei Zhou, Electrodynamics.





## Thanks for Attending!

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240624193551339.png" alt="image-20240624193551339" style="zoom: 15%;" />