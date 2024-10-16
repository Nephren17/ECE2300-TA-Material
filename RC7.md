# RC 7：  Steady Magnetic Fields

By Mo Yang

## Magnetic Field Intensity, Relative Permeability and Magnetic circuit

Considering the effect of both the internal dipole moment and the induced magnetic moment in a magnetic material, the magnetic field intensity $ H $ is defined as:
$$
 H = \frac{B}{\mu_0} - M 
$$

$$
\nabla \times H = J 
$$
directly relates the magnetic field intensity with the density of free charge. The integral form of which is then,
$$
\oint_C H \cdot dl = I
$$
It is another form of Ampere’s circuital law: the circulation of the magnetic field intensity around any closed path is equal to the free current flowing through the surface bounded by the path.

If the closed path $ C $ is chosen to enclose $ N $ turns of a winding carrying a current $ I $ that excites a magnetic circuit, we have
$$
\oint_C H \cdot dl = NI = V_m
$$
$$ V_m $$ is analogous to electromotive force (emf) and is called magnetomotive force (mmf).

If we define:
$$
M = \chi_m H
$$
 where $ \chi_m $ is magnetic susceptibility, Then
$$
B = \mu_0(1+\chi_m)H = \mu_0 \mu_r H = \mu H
$$

$$
H = \frac{1}{\mu} B
$$

$$
\mu_r = 1 + \chi_m = \frac{\mu}{\mu_0}
$$

where $ \mu_r $ is the relative permeability of the medium. $ \mu = \mu_r \mu_0 $ is the absolute permeability/permeability.

### Exercise

Assume that $ N $ turns of wire are wound around a toroidal core of a ferromagnetic material with permeability $ \mu $. The core has a mean radius $ r_o $, a circular cross section of radius $ a $ ($ a \ll r_o $), and a narrow air gap of length $ l_g $, as shown in the following figure. A steady current $ I_o $ flows in the wire. Determine:

(a) the magnetic flux density, $ B_f $, in the ferromagnetic core;

(b) the magnetic field intensity, $ H_f $, in the core;

(c) the magnetic field intensity, $ H_g $, in the air gap.

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240723160730043.png" alt="image-20240723160730043" style="zoom:50%;" />









![image-20240723163006566](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240723163006566.png)











## Behavior of Magnetic Materials

1. **Diamagnetic**, if $ \mu_r \lesssim 1 $ ($ \chi_m $ is a very small negative number)
2. **Paramagnetic**, if $ \mu_r \gtrsim 1 $ ($ \chi_m $ is a very small positive number)
3. **Ferromagnetic**, if $ \mu_r \gg 1 $ ($ \chi_m $ is a large positive number)

## Boundary Conditions for Magnetostatic Fields

1. The normal component of $ B $ is continuous across an interface,
$$
  B_{1n} = B_{2n}
$$
   which is
$$
  \mu_1 H_{1n} = \mu_2 H_{2n}
$$

2. The tangential component of the $ H $ field is discontinuous across an interface where a free surface current exists.
$$
  \mathbf{a_n} \times (H_1 - H_2) = J_s
$$

When the conductivities of both media are finite, currents are defined by volume current densities and free surface currents do not exist on the interface. Hence $ J_s = 0 $, the tangential component of $ H $ is continuous across the boundary of almost all physical media; it is discontinuous only when an interface with an ideal perfect conductor or a superconductor is assumed.



### Exercise

Two magnetic media with permeabilities $ \mu_1 $ and $ \mu_2 $ have a common boundary, as shown in the following figure. The magnetic field intensity in medium 1 at the point $P_1$ has a magnitude $ H_1 $ and makes an angle $ \alpha_1 $ with the normal. Determine the magnitude and the direction of the magnetic field intensity at point $P_2$ in medium 2.

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240723161013887.png" alt="image-20240723161013887" style="zoom:67%;" />









![image-20240723163024409](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240723163024409.png)



















## Inductances and Inductors

For two loops $ C_1 $, $ C_2 $:

![image-20240723160102319](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240723160102319.png)

For linear media where permeability does not change with $ I_1 $,
$$
L_{12} = \frac{\Lambda_{12}}{I_1}
$$

where $ \Lambda_{12} $ is the flux linkage, $ L_{12} $ is the mutual inductance between loops $ C_1 $ and $ C_2 $. A more general definition for $ L_{12} $ is then:
$$
L_{12} = \frac{d\Lambda_{12}}{dI_1}
$$
 The total flux linkage with $ C_1 $ caused by $ I_1 $ is calculated as:
$$
\Lambda_{11} = N_1 \Phi_{11} > N_1 \Phi_{12}
$$
 The self-inductance of loop $ C_1 $ could be calculated as:
$$
L_{11} = \frac{\Lambda_{11}}{I_1}
$$
 For linear medium, in general:
$$
L_{11} = \frac{d\Lambda_{11}}{dI_1}
$$
 A conductor arranged in an appropriate shape (e.g., a conducting wire wound as a coil) to supply a certain amount of self-inductance is called an inductor. It can store magnetic energy.

Method to determine the self-inductance of an inductor:
1. Choose an appropriate coordinate system for the given geometry.
2. Assume a current $ I $ in the conducting wire.
3. Find $ B $ from $ I $ by Ampere’s circuital law,
$$
  \oint_C B \cdot dl = \mu_0 I
$$
  if symmetry exists; if not, Biot-Savart law
$$
  B = \frac{\mu_0 I}{4\pi} \oint_{C'} \frac{dl' \times \mathbf{a}_R}{R^2}
$$

   must be used.
4. Find the flux linking with each turn, $ \Phi $, from $ B $ by integration:
$$
   \Phi = \int_S B \cdot ds
$$

  where $ S $ is the area over which $ B $ exists and links with the assumed current.
5. Find the flux linkage $ \Lambda $ by multiplying $ \Phi $ by the number of turns.
6. Find $ L $ by taking the ratio $ L = \frac{\Lambda}{I} $.

To determine the mutual inductance $ L_{12} $ between two circuits, after choosing an appropriate coordinate system, assume $ I_1 $ → Find $ B_1 $ → Find $ \Phi_{12} $ by integrating $ B_1 $ over surface $ S_2 $ → Find flux linkage $ \Lambda_{12} = N_2 \Phi_{12} $ → Find $ L_{12} = \frac{\Lambda_{12}}{I_1} $.

In high-frequency applications, current tends to concentrate in the "skin" of the inner conductor as a surface current, internal self-inductance tends to zero. Neumann formula for mutual inductance:
$$
L_{12} = L_{21} = \frac{\mu_0}{4\pi} \oint_{C_1} \oint_{C_2} \frac{dl_1 \cdot dl_2}{R}
$$


## Magnetic Energy

For a system of $ N $ loops carrying currents,
$$
W_m = \frac{1}{2} \sum_{j=1}^N \sum_{k=1}^N L_{jk} I_j I_k
$$
For a single inductor,
$$
W_m = \frac{1}{2} L I^2
$$

$$
 W_m = \frac{1}{2} \sum_{k=1}^N I_k \Phi_k 
$$



### Magnetic Energy In Terms of Field Quantities

Generally,
$$
 W_m = \frac{1}{2} \int_{V'} \mathbf{A} \cdot \mathbf{J} \, dv' = \frac{1}{2} \int_{V'} \mathbf{H} \cdot \mathbf{B} \, dv' = \frac{1}{2} \int_{V'} \frac{B^2}{\mu} \, dv' = \frac{1}{2} \int_{V'} \mu H^2 \, dv' 
$$
If we define a magnetic energy density $ w_m $ such that
$$
W_m = \int_{V'} w_m \, dv' 
$$
 then
$$
w_m = \frac{1}{2} \mathbf{H} \cdot \mathbf{B} = \frac{B^2}{2\mu} = \frac{1}{2} \mu H^2 
$$
 And we have
$$
L = \frac{2W_m}{I^2}
$$

## Reference

- Fan Hu, RC Slides, VE230
- Nana Liu, Slides, VE230



## Thanks!

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240723162904542.png" alt="image-20240723162904542" style="zoom: 25%;" />