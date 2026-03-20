$q$ - current orientation
$\omega$ - instantaneous rotation rates about body frame / global frame axes: [0, yaw, pitch, roll]
$\dot{q}$ - rate of change of orientation

Gyroscope is measuring rotation rates about body frame

Can use this to integrate gyro data over time:
- Know initial orientation ($q$)
- Know axis of rotation: $\hat{\omega}$, know angle of rotation $\omega \cdot \Delta t$
- Infinitesimal rotation is: $$q_{\Delta} = \left[cos\frac{\omega \Delta t}{2}, \hat{\omega}sin\frac{\omega \Delta t}{2}\right]$$
- Next timestep is: $$q_{k+1} = q_{k} \cdot q_{\Delta}$$
	- Right multiply because gyro is measuring rotation rates about body frame, not global frame

