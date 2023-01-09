Date: Oct 13th
Note: There was one lecture on the 11th where she introduced SVMs.

Can be used for regression or classification!

- Linear discriminative approach: Find a line that separates two feature spaces.
- SVM goes beyond this: Maximize the margin around the line!
- Many lines could be used to separate two classes, choose the one where the distance is largest between points.
- This allows for better generalization of data.

What about data that isn't linearly separable?
- SVM will translate it to higher-dimensional space and use a line there...


How do we tell if we did it right?

If $t_n * x_n > 0$, then $x_n$ is correctly classified. If negative, it's not correctly satisfied. If 0, then it's on the line.

**Goal:** $\forall x_n$  maximize distance! Distance defined as:
$$\frac{t_n * y(x_n)}{||w||}$$

# Objective Func. for Hard-Margin SVM
Hard margin means don't allow any misclassifications, assume everything is linearly separable.

Eventually we will get into Soft Margin SVMs which do allow some misclassifications at a penalty.

![[Pasted image 20221013142519.png]]

# Support Vectors
- Points on the margin
- They are the closest to the discriminant function
![[Pasted image 20221013142752.png]]

For SVs, their distance is ?

Normalize w and b such that distance of SVs to discriminant function = 1.
For all data points:
$$
t_n(w^T\phi(x_n)+b) >= 1, \forall n
$$

The Objective Function can be rewritten as:
![[Pasted image 20221013143303.png]]


The inequality constrained optimization problem is solved using lagrange multipliers. Not covered in this course


Note: If the data is not linearly separable, the resulting line will be terrible! This is in contrast to that of a [[Logistic Regression]], which will do sort of better. 