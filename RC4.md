# RC4： Capacitors and Electrostatic Solutions

By Mo Yang

## Capacitors

Definition: The capacitance of isolated conducting body is the electric charge that must be added to the body per unit increase in its electric potential. 
$$
C = \frac{Q}{V}
$$
Components: Two conductors with arbitrary shapes are separated by free space or dielectric medium.

![image-20240611170243478](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240611170243478.png)

Specifically, for the connections of different capacitors, we can have

Series:
$$
\frac{1}{C_{sr}} = \frac{1}{C_{1}} + \frac{1}{C_{2}} + ... + \frac{1}{C_{n}}
$$
Parallel:
$$
C_{pr} = C_1 + C_2 + ... + C_n
$$

### Use of media in capacitor

![平面板电容器 的图像结果](https://th.bing.com/th/id/OIP.enZARXCps23zH4ao62DP7gHaEF?w=308&h=180&c=7&r=0&o=5&dpr=1.1&pid=1.7)

















### Exercise 1

A spherical capacitor consists of an inner conducting sphere of radius $R_i$ and an outer conductor with a sphere inner wall of radius $R_o$. The space in between is filled with a dielectric of permitivity $\epsilon$. Determine the capacitance.

![image-20240611171841469](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240611171841469.png)























## Energy in Capacitors and Electric Fields

The potential energy of N discrete charges at rest:
$$
W_e = \frac{1}{2}\sum^N_{k=1}Q_kV_k
$$
We can also deduce the case for continuous distribution.
$$
W_e = \frac{1}{2}\int_{R^3}\epsilon E^2dV
$$














### Exercise 2

A parallel plate capacitor has a plate area of $ S $ and a plate separation of $ d $. The space between the plates is filled with a dielectric material with a relative permittivity $ \epsilon_r $. Under the following two conditions, determine how much external force $ F $ is needed to completely remove the dielectric from the capacitor:

1. The voltage $ U $ across the capacitor remains constant.
2. The charge $ Q $ on the capacitor remains constant.

![image-20240611171803049](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240611171803049.png)























### Exercise 3

A parallel plate air capacitor is vertically inserted into a liquid dielectric with relative permittivity $\epsilon_r$ and density $\rho$. The capacitor plates have an area $S$ (where $S=ab$), and a separation distance $d$. The voltage $U$ between the two plates is kept constant. Find the height $h$ that the liquid level rises in the capacitor.

![image-20240611174145825](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240611174145825.png)

































## Uniqueness Theorem:

A solution of Poisson's equation $\nabla^2 V = -\frac{\rho_f}{\epsilon}$ that satisfies the given boundary conditions is a unique solution.

### Poisson's equation:
$$
\nabla^2 V = -\frac{\rho_f}{\epsilon} = -\frac{\rho}{\epsilon_0}
$$

where $\rho_f$ is the free charge density, $\epsilon$ is the absolute permittivity, and $\rho$ is the total charge density (free charge density + induced charge density).

### Laplace's equation:
$$
\nabla^2 V = 0
$$

which is a special case of Poisson's equation ($\rho = 0$ everywhere).

We can try to show the proof of the uniqueness theorem.





















## Method of Images

Methods of images is a smart way to solve electrostatics to satisfy certain boundary conditions, utilizing equivalent image charge.(e.g. The voltage potential of a plate is 0 everywhere) The use of image charge is actually based on the uniqueness theorem of electrostatic solution.

Case 1: Point Charge and Grounded Plane Conductor

![image-20240611173810577](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240611173810577.png)



















Case 2: Line Charge and Parallel Conducting Cylinder

![image-20240611173821778](C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240611173821778.png)



























## Reference

Nana Liu, VE 230 slides.

Fan Hu, VE 230 RC slides.

Jiafu Cheng, Electro-megnetics.

Lei Zhou, Electrodynamics.











## Thanks!

<img src="C:\Users\Nephr\AppData\Roaming\Typora\typora-user-images\image-20240611175021373.png" alt="image-20240611175021373" style="zoom:33%;" />