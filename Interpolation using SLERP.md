
Basically, let's say you have two orientations: $q_0$, $q_1$

There is a quaternion that represents the rotation between these two orientations. By left-multiplying $q_0$ by this rotation, we get to $q_1$
$$
q \cdot q_0 = q_1
$$
$$
q = q_1 \cdot q_0^{-1}
$$
This quaternion $q$ that represents this rotation, can be interpreted as a combo of the axis of rotation: $\hat{n}$ and the angle of rotation $\theta$ , such that we get
$$
\left(cos\frac{\theta}{2}, sin\frac{\theta}{2} \cdot \hat{n} \right)
$$

We want to make sure this is the shortest angle between these two quaternions, so we can check if the cosine term above is negative, and if so we can negate everything to get the shorter angle about the opposite rotation axis.

To interpolate some percentage of the way through this angle $\theta$, we can just replace $\theta$ with $t \cdot \theta$, to get the following rotation that is part of the way through:

$$
q^t = \left(cos\frac{t\cdot\theta}{2}, sin\frac{t\cdot\theta}{2} \cdot \hat{n} \right)
$$

Then to get our final orientation that is the fraction $t$ of the way to the other orientation, we do the following:

$$
q_{interp} = q^t \cdot q_0
$$


# Alternatively, Geometric SLERP

The other formula for SLERP is:
![[Pasted image 20260318113658.png]]

![[Geometric Slerp Derivation.pdf]]


# Usage

Say you have the following:
- quaternion representing your aircraft attitude relative to the local NED frame at time $t_1$
- quaternion representing your aircraft attitude relative to the local NED frame at time $t_2$
- Desire to get the aircraft attitude relative to the local NED frame at time $t_{meas}$, which is between $t_1$ and $t_2$

You can do the following approach:
![[Pasted image 20260318114250.png]]

The reason you fall back to linear interpolation if the angle is small, is because of numerical instability issues with either formula (Geometric or Quaternion)

[Simple Explanation](https://www.youtube.com/watch?v=x1aCcyD0hqE)

[A little more background](https://www.youtube.com/watch?v=BXajpAy5-UI)

[Wikipedia page](https://en.wikipedia.org/wiki/Spherical_linear_interpolation)

