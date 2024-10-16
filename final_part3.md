# VE230 Final RC

By Mo Yang

## Inductances and Magnetic Energy

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









## Faraday’s Law of Electromagnetic Induction

In static case, E and B can exist together (in a conducting medium), but they won’t influence each other. The relationship between induced emf and the negative rate of change of flux linkage:
$$
\nabla \times E = -\frac{\partial B}{\partial t}
$$
$$
\oint_{C} E \cdot d\ell = -\int_{S} \frac{\partial B}{\partial t} \cdot ds
$$



If we define emf
$$
V = \oint_{C} E \cdot d\ell
$$
and magnetic flux
$$
\Phi = \int_{S} B \cdot ds
$$
then Faraday’s law can be rewritten as
$$
V = -\frac{d\Phi}{dt} \quad \text{(Faraday’s law of electromagnetic induction)}
$$
If there are N turns of wire, then the total magnetic flux is $N\Phi$, and we have
$$
V = -N \frac{d\Phi}{dt}
$$
Lenz’s Law: The induced emf will cause a current to flow in the closed loop in such a direction as to oppose the change in the linking magnetic flux.

- Motional EMF:
$$
V_0 = \oint_{C} (u \times B) \cdot d\ell
$$

![image-20240803191332518](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240803191332518.png)

For moving circuit in a time-varying magnetic field

- Lorentz’s Force Equation: 
$$
F = q(E + u \times B)
$$
- Effective Electric Field: If an observer has the same movement with $ q $, Lorentz’s force on $ q $ can be seen as effective electric field
$$
E' = E + u \times B
$$
- General Form of Faraday’s Law:
$$
\oint_{C} E' \cdot d\ell = -\int_{S} \frac{\partial B}{\partial t} \cdot ds + \oint_{C} (u \times B) \cdot d\ell
$$
where the left side talks about emf induced in a moving frame of reference, and on the right side, transformer emf equals to
$$
V_t = -\int_{S} \frac{\partial B}{\partial t} \cdot ds
$$
and motional emf equals to
$$
V_m = \oint_{C} (u \times B) \cdot d\ell
$$


## Potential Function

- Electric field in time-varying field
$$
E = -\nabla V - \frac{\partial A}{\partial t}
$$
where $-\nabla $ comes from charge distribution, and $-\frac{\partial A}{\partial t}$ comes from time-varying current.

- Quasi-static fields
If $ \rho $ and $ J $ vary slowly with time and the range of $ R $ is small in comparison with the wavelength (low frequency, long wavelength), we can use the below 2 equations to find quasi-static fields.
$$
V = \frac{1}{4\pi \epsilon_0} \int_{V'} \frac{\rho}{R} dv'
$$
$$
A = \frac{\mu_0}{4\pi} \int_{V'} \frac{J}{R} dv'
$$

Note:
1. These above equations are solutions of Poisson’s equation in static case.
2. If there are high-frequency sources, we need to consider time-retardation effects, which means as source changes in time, it takes time to change the potential at a certain distance from the source.

- Non-homogeneous wave equation for vector potential
If we choose the divergence of $ A $ such that
$$
\nabla \cdot A + \mu \epsilon \frac{\partial V}{\partial t} = 0
$$
which is called the Lorentz condition/gauge for potentials, we can find the non-homogeneous wave equation for vector potential $ A $ as
$$
\nabla^2 A - \mu \epsilon \frac{\partial^2 A}{\partial t^2} = -\mu J
$$

- Non-homogeneous wave equation for scalar potential
$$
\nabla^2 V - \mu \epsilon \frac{\partial^2 V}{\partial t^2} = -\frac{\rho}{\epsilon}
$$

### Exercise

Substitute equations $ B = \nabla \times A $ and $ E = -\nabla V - \frac{\partial A}{\partial t} $ in Maxwell’s equations to obtain wave equations for scalar potential $ V $ and vector potential $ A $ for a linear, isotropic but inhomogeneous medium. Show that these wave equations reduce to equations $ \nabla^2 V - \mu \epsilon \frac{\partial^2 V}{\partial t^2} = -\frac{\rho}{\epsilon} $ and $ \nabla^2 A - \mu \epsilon \frac{\partial^2 A}{\partial t^2} = -\mu J $ for simple media. (Hint: Use the following gauge condition for potentials in an inhomogeneous medium:
$$
\nabla \cdot (\epsilon A) + \mu \epsilon^2 \frac{\partial V}{\partial t} = 0
$$















### Exercise

Prove by direct substitution that any twice differentiable function of $ (t - R\sqrt{\mu \epsilon}) $ or of $ (t + R\sqrt{\mu \epsilon}) $ is a solution of the homogeneous wave equation.

$$
\frac{\partial^2 U}{\partial R^2} - \mu \epsilon \frac{\partial^2 U}{\partial t^2} = 0.
$$























## Wave Equations and Solutions

For given charge and current distribution $ \rho $ and $ J $, in order to get $ E $ and $ B $, we first need to find solutions for $ V $ and $ A $ in non-homogeneous wave equation.

- Solution for scalar potential:
  $$
  V(R, t) = \frac{1}{4\pi \epsilon} \int_{V'} \frac{\rho(t - R/u)}{R} dv'
  $$

- which is called the retarded scalar potential, indicating that it takes time $ R/u $ for the effect of $ \rho $ to be felt at distance $ R $.


$$

$$
- Solution for vector potential:

$$
A(R, t) = \frac{\mu}{4\pi} \int_{V'} \frac{J(t - R/u)}{R} dv'
$$

For source-free wave equations in simple non-conducting media
- Source-free: $ \rho = 0, J = 0 $.
- Simple non-conducting media: $ \epsilon $ and $ \mu $ are constant, and $ \sigma = 0 $.

- Rewrite the Maxwell’s equations:

$$
\nabla \times E = -\mu \frac{\partial H}{\partial t}
$$

$$
\nabla \times H = \epsilon \frac{\partial E}{\partial t}
$$
$$

$$


$$
\nabla \cdot E = 0
$$
$$

$$
- Obtain wave equations for $ E $ and $ H $:

$$
\nabla^2 E - \frac{1}{u^2} \frac{\partial^2 E}{\partial t^2} = 0
$$

$$
\nabla^2 H - \frac{1}{u^2} \frac{\partial^2 H}{\partial t^2} = 0
$$

where $ u = \frac{1}{\sqrt{\mu \epsilon}} $.





## Thanks for Coming and Good Luck for Exam!

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240803204603425.png" alt="image-20240803204603425" style="zoom: 33%;" />
