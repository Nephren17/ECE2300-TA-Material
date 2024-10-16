# RC 2: Static Electric Field

 By Mo Yang

## Before RC

- My office hour: 10:00 a.m - 12:00 a.m. Thursday, Shanghai time.
- Please sent me a message if you want to attend the office hour.

## Review of Vector Calculus

- Stokes' Theorem:

$$
\int_{S} (\nabla \times \mathbf{F}) \cdot d\mathbf{S} = \oint_{\partial S} \mathbf{F} \cdot d\mathbf{r}
$$

- Gauss' Theorem (Divergence Theorem):

$$
\oint_{S} \mathbf{F} \cdot d\mathbf{S} = \int_{V} (\nabla \cdot \mathbf{F}) \, dV
$$



- Generalized Stokes Theorem:
  $$
  \int_{M} d\omega = \int_{\partial M} \omega
  $$
  
- Two useful identities about gradient
  $$
  \nabla \times (\nabla V) \equiv 0 \\
  \nabla \cdot (\nabla \times \mathbf{A}) \equiv 0 \
  $$
  

## Coulomb’s Law

### Point Charge

Force on a Point Charge in the Field of Another Point Charge
$$
\mathbf{F}_{12} = q_2 \mathbf{E}_{12} = \hat{\mathbf{a}}_R \frac{q_1 q_2}{4 \pi \epsilon_0 R^2}
$$
Actually, we define "field" from forces. Getting rid of "force" makes it possible to consider potential without interaction. For a single point charge $ $q$ $ located at the origin, the electric field $ $\mathbf{E}$ $ is given by:
$$
\mathbf{E} = \hat{\mathbf{a}}_R \frac{q}{4 \pi \epsilon_0 R^2} \quad (\text{V/m})
$$


Single Point Charge (Charge Not at the Origin):

$$
\mathbf{E}_p = \frac{q (\mathbf{R} - \mathbf{R'})}{4 \pi \epsilon_0 |\mathbf{R} - \mathbf{R'}|^3} \quad (\text{V/m})
$$

Several Point Charges:

$$
\mathbf{E} = \frac{1}{4 \pi \epsilon_0} \sum_{k=1}^n \frac{q_k (\mathbf{R} - \mathbf{R'}_k)}{|\mathbf{R} - \mathbf{R'}_k|^3} 
$$
Note that all the things are inversely proportional to the square of distance.



#### Exercise 1:

 A total charge $Q$ is uniformly put on a thin spherical shell of radius $R$. Determine the electric field intensity at an arbitrary point inside the shell.



















### Dipole

Why we need dipole? A model of physics when external electric field appears.

![image-20240529015439648](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240529015439648.png)

The electric field $ \mathbf{E} $ due to an electric dipole is given by: 
$$
 \mathbf{E} = \frac{q}{4 \pi \epsilon_0} \left( \frac{\mathbf{R} - \frac{\mathbf{d}}{2}}{|\mathbf{R} - \frac{\mathbf{d}}{2}|^3} - \frac{\mathbf{R} + \frac{\mathbf{d}}{2}}{|\mathbf{R} + \frac{\mathbf{d}}{2}|^3} \right) 
$$


Approximation for $ d \ll R $:
$$
\mathbf{E} \approx \frac{q}{4 \pi \epsilon_0 R^3} \left( 3 \frac{\mathbf{R} \cdot \mathbf{d}}{R^2} \mathbf{R} - \mathbf{d} \right) 
$$

### Exercise 2:

Derive the electric field $E$ for the dipole.































Electric Dipole Moment Definition: 
$$
p = qd
$$
where $q$ is the charge, vector $d$ goes from $−q$ to $+q$. 
$$
p = a_zp = p (a_R \cos θ − a_θ \sin θ)
$$


Electric Field: (spherical coordinate) 
$$
E = \frac{p}{ 4π\epsilon_0 R^3} (2a_R  \cos θ + a_θ \sin θ)
$$


### Fundamental Conclusions of Electrostatics

Differential form (of Maxwell Equations):
$$
\nabla \cdot \mathbf{E} = \frac{\rho}{\epsilon_0} \quad \text{(divergence)} \\
\nabla \times \mathbf{E} = 0 \quad \text{(curl)}\\
$$
Integral form:
$$
\oint_{S} \mathbf{E} \cdot d\mathbf{s} = \frac{Q}{\epsilon_0}\\
\oint_{C} \mathbf{E} \cdot d\ell = 0
$$


## Gauss's Theorem

The total outward flux of the electric over any closed surface in free space is equal to the total charge enclosed in the surface divided by $\epsilon_0$. (Note that we can choose an arbitrary surface $ S $ for our convenience.) 
$$
\oint_{S} \mathbf{E} \cdot d\mathbf{s} = \frac{Q}{\epsilon_0}
$$


### Some useful models

(Put them on your CTPP!)

| Model (Uniformly Charged)                             | Electric Field $ E $ (Magnitude)                             |
| ----------------------------------------------------- | ------------------------------------------------------------ |
| Infinitely Long, Line Charge                          | $ E = \frac{\rho_l}{2 \pi r \epsilon_0} $                    |
| Infinite Planar Charge                                | $ E = \frac{\rho_s}{2 \epsilon_0} $                          |
| Uniform Spherical Surface Charge with Radius $ R $    | $\begin{cases} E = 0 & \text{if } r < R \\ E = \frac{Q}{4 \pi r^2 \epsilon_0} & \text{if } r > R \end{cases}$ |
| Uniform Sphere Charge with Radius $ R $               | $\begin{cases} E = \frac{Qr}{4 \pi R^3 \epsilon_0} & \text{if } r < R \\ E = \frac{Q}{4 \pi r^2 \epsilon_0} & \text{if } r > R \end{cases}$ |
| Infinitely Long, Cylindrical Charge with Radius $ R $ | $\begin{cases} E = \frac{\rho_v r}{2 \epsilon_0} & \text{if } r < R \\ E = \frac{\rho_v R^2}{2 r \epsilon_0} & \text{if } r > R \end{cases}$ |

### Exercise 3:

Derive the conclusions above with Gauss's theorem.























### Exercise 4:

Three metal plates with uniform thickness $ d $, length $ L $, and width $ W $ are arranged in the thickness direction with equal spacing. The length and width of the metal plates are much larger than the distance between the plates.The known charges on the metal plates are $ Q_1 $, $ Q_2 $, and $ Q_3 $. Without considering edge effects, find the charges on both sides of the plates: $ q_1, q_2, q_3, q_4, q_5, q_6 $.

![image-20240529022213255](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240529022213255.png)



















## Electrical Potential

The potential of an electric field can be defined as follows:
$$
\mathbf{E} = -\nabla V,
$$

$$
V_2 - V_1 = - \int_{P_1}^{P_2} \mathbf{E} \cdot d\ell.
$$

| Charge Distribution | Electric Potential $ V $                                     |
| ------------------- | ------------------------------------------------------------ |
| Point Charge        | $ V = \frac{q}{4 \pi \epsilon_0 R} $                         |
| Line Charge         | $ V = \frac{1}{4 \pi \epsilon_0} \int_{L'} \frac{\rho_\ell}{R} d\ell' $ |
| Surface Charge      | $ V = \frac{1}{4 \pi \epsilon_0} \int_{S'} \frac{\rho_s}{R} ds' $ |
| Volume Charge       | $ V = \frac{1}{4 \pi \epsilon_0} \int_{V'} \frac{\rho}{R} dv' $ |

If there are $ n $ point charges $ q_1, q_2, \ldots, q_n $ located at positions $ \mathbf{r}_1, \mathbf{r}_2, \ldots, \mathbf{r}_n $, respectively, the total electric potential $ V $ at a point $ \mathbf{r} $ is given by: 
$$
V(\mathbf{r}) = \sum_{i=1}^{n} V_i(\mathbf{r}) = \sum_{i=1}^{n} \frac{k q_i}{|\mathbf{r} - \mathbf{r}_i|}
$$




### Exercise 5:

For a uniformly charged sphere with radius $ R $ and total charge $ Q $, find the electric potential $ U_0 $ at the center of the sphere.















Thanks!

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240529023601614.png" alt="image-20240529023601614" style="zoom:25%;" />