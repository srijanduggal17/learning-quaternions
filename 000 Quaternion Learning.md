[[General Quaternion Concepts]]

Background stuff:
- [[Quaternion Arithmetic]]
- [[Intrinsic and Extrinsic Rotations in Euler Angles.canvas]]

Applications:
- [[Active vs Passive Rotations]]
	- [[Using Quaternions to Rotate Vectors]]
	- Transforming vectors between reference frames (expressing them in different coordinates), when relationship between reference frames is represented by a quaternion
- [[Rotating Orientations by Rotations in the Body Frame vs Global Frame]]
- [[Time Derivative of Quaternions]]
- [[Numerical Integration of Orientation from Gyro]]

Interpolation:
- [[Interpolation using SLERP]]


Things to test myself in code:
- Active vs passive rotations (rotating a vector vs expressing a vector in a diff frame's coordinates)
- combining single axis rotations into a single multi-axis rotation (both rotation matrices and quaternions)
- Rotating an orientation by rotations in the body frame vs rotations in the global frame
- Numerical integration using gyro data
- Averaging orientations using Markley's Method
- Some sort of state estimation problem w/ gyro and accel data
- Imagine a drone application and a robot application like Kiwi. think of the use cases within those for quaternions
- Calculating attitude error using quaternions
- Using quaternion representation of attitude error to drive controllers
- Attitude rate control w/ time derivative of quaternion?

[[Sources + References]]

