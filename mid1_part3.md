# VE 230 Midterm RC

By Mo Yang

## Polarization

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240619003951748.png" alt="image-20240619003951748" style="zoom:67%;" />

- Polarization vector, $ \mathbf{P} $:

  $
  \mathbf{P} = \lim_{v \to 0} \frac{1}{v} \sum_{k=1}^n \mathbf{p}_k
  $

  where the numerator represents the vector sum of the induced dipole moment contained in a very small volume $ v $.

- Charge distribution on surface density:

  $
  \rho_{ps} = \mathbf{P} \cdot \mathbf{a}_n
  $

- Volume charge distribution density:

  $
  \rho_p = - \nabla \cdot \mathbf{P}
  $

### Electric Flux Density and Dielectric Constant

Polarization is proportional to external electric field, which is an linear approximation.

Counter example: Iron.

- Electric flux density/electric displacement, $ \mathbf{D} $:

  $
  \mathbf{D} = \epsilon_0 \mathbf{E} + \mathbf{P} \ (C/m^2)
  $

  $
  \nabla \cdot \mathbf{D} = \rho \ (C/m^3)
  $

  where $ \rho $ is the volume density of free charges.

- Another form of Gauss’s law:

  $
  \oint_S \mathbf{D} \cdot d\mathbf{s} = Q_{\text{free}} \ (C)
  $

  The total outward flux of the electric displacement (the total outward electric flux) over any closed surface is equal to the total free charge enclosed in the surface.

- If the dielectric of the medium is linear and isotropic,

  $
  \mathbf{P} = \epsilon_0 \chi_e \mathbf{E}
  $

  $
  \mathbf{D} = \epsilon_0 (1 + \chi_e) \mathbf{E} = \epsilon_0 \epsilon_r \mathbf{E} = \epsilon \mathbf{E}
  $

  where $ \chi_e $ is a dimensionless quantity called electric susceptibility, $ \epsilon_r $ is a dimensionless quantity called the relative permittivity/electric constant of the medium, and $ \epsilon $ is the absolute permittivity/permittivity of the medium (F/m).

- For anisotropic media,

  $
  \begin{pmatrix}
  D_x \\
  D_y \\
  D_z
  \end{pmatrix}
  =
  \begin{pmatrix}
  \epsilon_{11} & \epsilon_{12} & \epsilon_{13} \\
  \epsilon_{21} & \epsilon_{22} & \epsilon_{23} \\
  \epsilon_{31} & \epsilon_{32} & \epsilon_{33}
  \end{pmatrix}
  \begin{pmatrix}
  E_x \\
  E_y \\
  E_z
  \end{pmatrix}
  $

  For bi-axial,

  $
  \begin{pmatrix}
  D_x \\
  D_y \\
  D_z
  \end{pmatrix}
  =
  \begin{pmatrix}
  \epsilon_1 & 0 & 0 \\
  0 & \epsilon_2 & 0 \\
  0 & 0 & \epsilon_3
  \end{pmatrix}
  \begin{pmatrix}
  E_x \\
  E_y \\
  E_z
  \end{pmatrix}
  $

  For uni-axial, $ \epsilon_1 = \epsilon_2 $. For isotropic, $ \epsilon_1 = \epsilon_2 = \epsilon_3 $.

- Dielectric breakdown: Electric field is very strong, causing permanent dislocations and damage in the material.

- Dielectric strength: The maximum electric field intensity that a dielectric material can withstand without breakdown.



### Exercise:

Determine the electric ﬁeld intensity at the center of a small spherical cavity cut out of a large block of dielectric in which a polarization P exists.

































## Boundary Conditions for Electrostatic Fields

- The tangential component of an electric field is continuous across an interface.

  $
  E_{1t} = E_{2t} \ (V/m)
  $

  or

  $
  \frac{D_{1t}}{\epsilon_1} = \frac{D_{2t}}{\epsilon_2}
  $

- The normal component of the displacement field $ \mathbf{D} $ is discontinuous across an interface where a surface charge exists, with the amount of discontinuity being equal to the surface charge density.

  $
  \mathbf{a}_n \cdot (\mathbf{D}_1 - \mathbf{D}_2) = \rho_s
  $

  or

  $
  D_{1n} - D_{2n} = \rho_s \ (C/m^2)
  $





## Capacitors

Definition: The capacitance of isolated conducting body is the electric charge that must be added to the body per unit increase in its electric potential. 
$$
C = \frac{Q}{V}
$$
Components: Two conductors with arbitrary shapes are separated by free space or dielectric medium.

![image-20240611170243478](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240611170243478.png)

**Components**: Two conductors with arbitrary shapes separated by free space or a dielectric medium.

- $ C = \frac{Q}{V_{12}} $

Refer to the textbook for the standard.

- Its capacitance is independent of $ V $ and $ Q $, meaning a capacitor has capacitance even when no voltage is applied and no free charges exist on its conductors.

#### How to Calculate Capacitance:

1. Choose a proper coordinate system.
2. Assume $ +Q $ and $-Q $ on the conductors.
3. Find $ E $ from $ Q $ (e.g., Gauss's law, $ D_n = \epsilon E_n = \rho_s $).
4. Find $ V_{12} = \int_1^2 E \cdot dl $.
5. $ C = \frac{Q}{V_{12}} $.

Specifically, for the connections of different capacitors, we can have

Series:
$$
\frac{1}{C_{sr}} = \frac{1}{C_{1}} + \frac{1}{C_{2}} + ... + \frac{1}{C_{n}}
$$
Parallel:
$$
C_{pr} = C_1 + C_2 + ... + C_n
$$







## Electrostatic Energy and Forces

- **Potential difference between $ P_1 $ and $ P_2 $**:

  
  $$
   W_{12} q = V_{21} = V_2 - V_1 = \int_{P_1}^{P_2} E \cdot dl
  $$
  
- **Self Energy**: Work done to bring a charge $ Q_2 $ from infinitely far away to distance $ R_{12} $ with $ Q_1 $ (initially, $ Q_1 $ is in space):

$$
W = Q_2 V_2 = Q_2 \frac{Q_1}{4 \pi \epsilon_0 R_{12}}
$$



- **Mutual Energy**: Potential energy of a group of $ N $ discrete point charges at rest:

$$
W_e = \frac{1}{2} \sum_{k=1}^N Q_k V_k
$$



where $ V_k = \frac{1}{4 \pi \epsilon_0} \sum_{j=1, j \neq k}^N \frac{Q_j}{R_{jk}} $. Note that $ W_e $ can be negative, e.g., in a 2-point charge system with one positive and one negative charge.

Electrostatic Energy (Volume) Density $ w_e $ defined as:

$$
W_e = \int_{v_0} w_e dv
$$


Electrostatic Energy in terms of Field Quantities:

A continuous charge distribution of density $ \rho $:
$$
W_e = \frac{1}{2} \int_v \rho V dv = \frac{1}{2} \int_{v_0} (\nabla \cdot D) V dv
$$
Another expression:

$$
W_e = \frac{1}{2} \int_{v_0} D \cdot E dv
$$
If it is a simple dielectric:
$$
W_e = \frac{1}{2} \int_{v_0} \epsilon E^2 dv = \frac{1}{2} \int_{v_0} \frac{D^2}{\epsilon} dv
$$


### Electrostatic Forces

Using the principle of virtual displacement to calculate force in two situations:

1. **System of bodies with fixed charges**:
   - Mechanical work is from the reduced stored electrostatic energy:
   
   $ F_Q = \nabla W_e(N) $
   
   - Electric torque rotates one of the bodies by $ d\theta $ (a virtual rotation) about an axis:
   
   $ T_Q = \frac{\partial W_e}{\partial \theta} \ (N \cdot m) $

2. **System of conducting bodies with fixed potentials**:
   - The fixed potential can be retained by connecting with an external source.
   - $ F_v = \nabla W_e $
   - $ T_v = \frac{\partial W_e}{\partial \theta} $



### Exercise：

A parallel plate air capacitor is vertically inserted into a liquid dielectric with relative permittivity $\epsilon_r$ and density $\rho$. The capacitor plates have an area $S$ (where $S=ab$), and a separation distance $d$. The voltage $U$ between the two plates is kept constant. Find the height $h$ that the liquid level rises in the capacitor.

![image-20240611174145825](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240611174145825.png)



























### Thanks for coming!

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240619003301511.png" alt="image-20240619003301511" style="zoom:33%;" />
