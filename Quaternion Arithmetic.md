---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠== You can decompress Drawing data with the command palette: 'Decompress current Excalidraw file'. For more info check in plugin settings under 'Saving'


# Excalidraw Data

## Text Elements
Arithmetic + Properties ^X5svvKOS

Double Cover / Two representations for same rotation:
   q = [w, x, y, z]

   -q = [-w, -x, -y, -z] -> opposite axis of rotation, and rotation by 360 - theta

   this is the "double cover" property -> the space of quaternions covers
   the rotations twice

   w = cos(theta/2)
   -w = -cos(theta/2) = cos((360-theta)/2) -> conjugate angle 

   cos (a-b) = cos(a)cos(b) + sin(a)sin(b)

   cos( 360-theta/2 ) = cos (180 - theta/2 )
                            = cos(180)cos(theta/2) + sin(180)sin(theta/2)
                            = -cos(theta/2)

Conjugate:
   conjugate of a quaternion represents the rotation that undoes the original
   q = [w, x, y, z]
   q* (conjugate) = [w, -x, -y, -z] -> same angle, opposite axis of rotation

Inverse:
   q * q^-1 = 1
   q^-1 = q* (conjugate) / norm(q) ^ 2
   the inverse of a unit quaternion is it's conjugate

Norm:
   norm is x^2 + y^2 + w^2 + z^2

Hamilton product:
   when you multiply two quaternions, you need to follow these rules:
   i² = j² = k² = −1
   ij = k, jk = i, ki = j
   ji = −k, kj = −i, ik = −j


Addition/subtraction:
    this is done component-wise
    q1 = [w1, x1, y1, z1]
    q2 = [w2, x2, y2, z2]
    q1+q2 = [w1 + w2, x1 + x2, y1 + y2, z1 + z2]

Multiplication of quaternions:
    associative, but not commutative
    


Multiplication of a quaternion by a scalar:
    k*q1 = [k*w, k*x, k*y, k*z] -> just multiply through

 ^FhdX3BNd

some representations are [q0, q1, q2, q3] = [w, x, y, z]
others are [q1, q2, q3, q4] -> q4 = w. q1, q2, q3 are the same (vector part) ^FM36qbHU

## Embedded Files
6eb67553473377870ce216d864687b82fb18378e: [[Pasted Image 20260311225200_292.png]]

9da141c6a52d71654de093bf92a57ebe97d298e3: [[Pasted Image 20260311225800_947.png]]

%%
## Drawing
```compressed-json
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=
```
%%