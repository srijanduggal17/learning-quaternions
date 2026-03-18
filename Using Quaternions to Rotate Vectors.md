![[Pasted image 20260311224017.png]]

https://www.youtube.com/watch?v=zjMuIxRvygQ


Goal: To rotate a vector / point $p$ about an axis by a certain angle

1. Define a unit vector for the rotation axis
2. Define a quaternion ($q$) that represents the rotation about an axis by half of your angle
3. Define the inverse / conjugate of your unit quaternion ($q^{-1}$)
4. Do the sandwich product: $q \cdot p \cdot q^{-1}$
