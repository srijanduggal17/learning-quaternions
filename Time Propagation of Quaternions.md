$\dot{q} = \frac{1}{2} q \cdot \omega$

$q$ - current orientation
$\omega$ - rate of change of orientation: [0, yaw, pitch, roll]
$\dot{q}$ - rate of change of orientation

Can use this to integrate gyro data over time:
- Know initial orientation ($q$)
- Getting gyro measurements ($\omega$) -> get $\dot{q}$ 
- Multiply by timestep: $q_{next} = q + \dot{q}\cdot \Delta T$
