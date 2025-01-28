# Question Paper 1-3

Paper 1 for Further Maths (9231), Oct/Nov 2024, tested on ChatGPT-4o vs DeepSeek R1

## Question 1a

The matrix M represents the sequence of two transformations in the x-y plane given by a stretch parallel
to the x-axis, scale factor k ( ) k ! 0 , followed by a shear, x-axis fixed, with (0, 1) mapped to (k, 1).

Show that M = [[k, k], [0, 1]].

### Prompt

The matrix M represents the sequence of two transformations in the x-y plane given by a stretch parallel
to the x-axis, scale factor k ( ) k ! 0 , followed by a shear, x-axis fixed, with (0, 1) mapped to (k, 1).

What is the matrix M?

### ChatGPT Answer

To find the matrix M, we need to determine the effects of each transformation and then combine them.

Step 1: Stretch parallel to the x-axis with scale factor k

A stretch parallel to the x-axis with scale factor k means that the x-coordinate of any point is multiplied by k, while the y-coordinate remains unchanged. The matrix that represents this stretch is:

[[k, 0],
 [0, 1]]

 Step 2: Shear, x-axis fixed, with (0, 1) mapped to (k, 1)
A shear transformation with the x-axis fixed means that the transformation only affects the y-coordinate in terms of the x-coordinate. The point (0, 1) being mapped to (k, 1) means that the x-coordinate of any point is modified by k times its y-coordinate, but the y-coordinate remains unchanged. The matrix for this shear is:

[[1, k],
 [0, 1]]

Step 3: Combine the two transformations
The total transformation is the combination of these two transformations. To apply both, we multiply the two matrices, with the stretch matrix on the left and the shear matrix on the right. This gives us:

[[k, 0],   [[1, k],
 [0, 1]] *  [0, 1]]

Multiplying these matrices:

[[k*1 + 0*0, k*k + 0*1],
 [0*1 + 1*0, 0*k + 1*1]]

= [[k, k^2],
   [0, 1]]

Thus, the matrix M is:

[[k, k^2],
 [0, 1]]

### DeepSeek Thinking

Alright, let's tackle this problem step by step. So, we need to find the matrix M that represents a sequence of two transformations in the x-y plane. The first transformation is a stretch parallel to the x-axis with a scale factor k (and k is not zero). The second transformation is a shear where the x-axis remains fixed, and the point (0, 1) is mapped to (k, 1).

First, let me recall what each of these transformations does individually. A stretch parallel to the x-axis would scale the x-coordinate by factor k while leaving the y-coordinate unchanged. So, the matrix for that should be:

[[k, 0],

[0, 1]]

Right? Because when you multiply this matrix by a vector [x, y], you get [k*x, y]. That makes sense for a stretch along the x-axis.

Now, the second transformation is a shear with the x-axis fixed. In a shear transformation, one coordinate is shifted by an amount proportional to the other coordinate. Since the x-axis is fixed, that means points on the x-axis (where y=0) don't move. The shear should affect the x-coordinate based on the y-coordinate, or the y-coordinate based on the x-coordinate? Wait, in a standard shear where the x-axis is fixed, typically the shear is in the direction of the x-axis. So, each point (x, y) is transformed to (x + m*y, y), where m is the shear factor.

But the problem says that the point (0, 1) is mapped to (k, 1). Let's see. If we apply the shear matrix to the point (0, 1), what do we get? Let's denote the shear matrix as:

[[1, m],

[0, 1]]

Because in a shear with x-axis fixed, the x-coordinate becomes x + m*y, and y remains the same. So applying this matrix to [0, 1] would give [m*1, 1], which should equal [k, 1] according to the problem. Therefore, m must be equal to k. So, the shear matrix is:

[[1, k],

[0, 1]]

Wait, let me verify. The standard shear matrix when x-axis is fixed is usually written as [[1, shear_factor], [0, 1]]. So if we apply this to (0,1), we get (shear_factor*1, 1). Since the problem states that (0,1) maps to (k,1), the shear factor must be k. That makes sense. So the shear matrix is indeed [[1, k], [0, 1]].

Now, the order of transformations is important here. The problem says the stretch is first, followed by the shear. So we need to compose these two transformations by multiplying their matrices in the correct order. Remember that when you apply transformations sequentially, the matrix multiplication is done in reverse order. Wait, no, actually, when you have transformation A followed by transformation B, the combined matrix is B*A. Because the vector is multiplied first by A, then by B. So in terms of matrix multiplication, it's B*A*v.

Therefore, in this case, the stretch is first (matrix S = [[k,0],[0,1]]), followed by the shear (matrix H = [[1,k],[0,1]]). So the total transformation M is H * S.

Let me compute that. So H * S = [[1, k], [0, 1]] * [[k, 0], [0, 1]].

Multiplying these matrices:

First row of H: [1, k] multiplied by first column of S: [k, 0] gives 1*k + k*0 = k.

First row of H: [1, k] multiplied by second column of S: [0, 1] gives 1*0 + k*1 = k.

Second row of H: [0, 1] multiplied by first column of S: [k, 0] gives 0*k +1*0 = 0.

Second row of H: [0, 1] multiplied by second column of S: [0,1] gives 0*0 +1*1 = 1.

Wait, hold on, that seems off. Wait, the first entry of the product matrix should be (1*k + k*0) = k, then the second entry of the first row is (1*0 + k*1) = k. Second row first entry is (0*k +1*0)=0, second row second entry is (0*0 +1*1)=1. So the product matrix H*S is:

[[k, k],

[0, 1]]

Wait, but let me check again. Matrix multiplication: rows of first matrix (H) multiplied by columns of the second matrix (S).

First element: (1)(k) + (k)(0) = k

Second element: (1)(0) + (k)(1) = k

Third element: (0)(k) + (1)(0) = 0

Fourth element: (0)(0) + (1)(1) = 1

Yes, so the resulting matrix is [[k, k], [0, 1]]. That seems correct.

But let me verify by applying the transformations step by step. Suppose we have a point (x, y). First, apply the stretch: (k*x, y). Then apply the shear, which would take (k*x, y) to (k*x + k*y, y). Because the shear adds k times the y-coordinate to the x-coordinate. So indeed, the total transformation is x' = k*x + k*y, y' = y. Which is exactly what the matrix [[k, k], [0, 1]] does.

Alternatively, if we think about the matrices, the stretch first scales x by k, then the shear adds k*y to the x-component. So, combining these operations, the x-component becomes k*x + k*y, and y remains y. So that seems to check out.

Wait, but let me also verify with the given point (0,1). If we apply the stretch first, (0,1) becomes (0*k, 1) = (0,1). Then apply the shear: x becomes 0 + k*1 = k, y remains 1. So (k,1) which matches the problem statement. That's correct.

Another example: take (1,0). Stretch first: (k*1, 0) = (k,0). Then shear: x becomes k + k*0 = k, y remains 0. So (k,0). Which is the same as the original (1,0) stretched along x-axis, as expected. If we had done shear first and then stretch, the result would be different, which is why the order is important.

Therefore, the combined transformation matrix M is H * S = [[k, k], [0, 1]].

But let me just double-check if the shear matrix was correctly determined. Shear with x-axis fixed, mapping (0,1) to (k,1). So shear factor is k. The standard shear matrix in this case is [[1, k], [0, 1]], as we had. So when you multiply this by [0;1], you get [k;1]. Correct. So that's right.

Therefore, multiplying the shear matrix after the stretch matrix gives the correct overall transformation. So the final matrix M is [[k, k], [0, 1]].

### DeepSeek Answer

The matrix M is the product of the shear matrix and the stretch matrix, applied in the given order.

Stretch parallel to the x-axis with scale factor k:

[[k, 0],
 [0, 1]]

Shear with x-axis fixed, mapping (0, 1) to (k, 1). The shear factor is k, resulting in the matrix:

[[1, k],
 [0, 1]]

Composition (shear applied after stretch):

M = Shear * Stretch = [[1, k], [0, 1]] * [[k, 0], [0, 1]] = [[k, k], [0, 1]]

Matrix M:

[[k, k],
 [0, 1]]

### Verdict

ChatGPT 0, DeepSeek 4

Total Marks so far: ChatGPT 0, DeepSeek 4

## Question 1b

The transformation represented by M has a line of invariant points.
Find, in terms of k, the equation of this line.

### Prompt

The transformation represented by M has a line of invariant points.
Find, in terms of k, the equation of this line.

### ChatGPT Answer

To find the line of invariant points, we need to determine the points that remain unchanged under the transformation represented by the matrix M. For a point (x, y) to be invariant, it must satisfy the equation:

M * [x, y] = [x, y]

This means that multiplying the transformation matrix M by the point [x, y] results in the same point [x, y].

Given the matrix M:

[[k, k^2],
 [0, 1]]

We can set up the following system of equations:

[k * x + k^2 * y, 0 * x + 1 * y] = [x, y]

This leads to two equations:

k * x + k^2 * y = x
y = y
The second equation is trivially true, so we focus on the first equation:

k * x + k^2 * y = x

Rearrange this equation:

k * x - x = -k^2 * y

Factor out x on the left-hand side:

x * (k - 1) = -k^2 * y

Now solve for y:

y = -(x * (k - 1)) / k^2

Thus, the equation of the line of invariant points is:

y = -(k - 1) / k^2 * x

This is the equation of the line of invariant points in terms of k.

### DeepSeek Thinking

Okay, let's tackle this problem. The user wants to find the equation of the line of invariant points under the transformation represented by the matrix M. They mentioned that M is a product of a stretch and a shear, which we already figured out as:

M = [[k, k], [0, 1]]

An invariant point is a point (x, y) that doesn't change after applying the transformation. So, applying M to (x, y) should give back (x, y) itself. Let's write that out mathematically.

So, M multiplied by the vector [x, y] should equal [x, y]. Let's set up the matrix equation:

[[k, k], [0, 1]] * [x, y] = [x, y]

Multiplying the matrix with the vector gives two equations. Let's compute each component:

First component (x'): k*x + k*y = x

Second component (y'): 0*x + 1*y = y

Looking at the second equation first: y = y. Well, that's always true for any y. So that equation doesn't impose any restrictions. The key equation comes from the first component.

So, from the first equation: kx + ky = x. Let's rearrange this. Subtract x from both sides:

kx + ky - x = 0

Factor x terms:

x(k - 1) + ky = 0

Hmm, let's see. We need to express this as the equation of a line. Let's solve for y in terms of x or vice versa. Maybe solve for y.

Bring the x term to the other side:

ky = -x(k - 1)

Divide both sides by k (assuming k ≠ 0, which is given since k > 0):

y = [- (k - 1)/k] x

Simplify the negative sign:

y = [(1 - k)/k] x

So that's the equation of the line. Let me check if that makes sense. If k is 1, then the line becomes y = 0, which is the x-axis. But wait, if k=1, the original matrix M would be [[1,1],[0,1]], which is a shear. For a shear with factor 1, the invariant points are along the x-axis, which matches. If k is not 1, say k=2, then the line would be y = (-1/2)x. Let's verify with a point on that line. Suppose x=2, y= -1. Applying M:

x' = 2*2 + 2*(-1) = 4 -2 = 2

y' = 0*2 +1*(-1) = -1

So (2, -1) maps to itself. Correct. Another point: x=1, y=(1-2)/2 = -0.5. Apply M:

x' =2*1 +2*(-0.5)= 2 -1=1

y'= -0.5. Correct. So the line y = [(1 -k)/k]x is indeed the invariant line.

Therefore, the equation is y = ((1 - k)/k)x. Alternatively, we can write it as y = (1/k -1)x, but the first form is better. Let me make sure there's no other invariant points. Since the second equation is always true, the entire line defined by the first equation is invariant. So the answer should be y = ((1 - k)/k)x.

### DeepSeek Answer

To find the line of invariant points under the transformation M

[k  k] [x]   = [x]
[0 1] [y]     [y]

From the first row: k*x + k*y = x
Simplify: k*y = x - k*x → y = (1 - k)/k * x

Second row is always satisfied (y = y).

Equation of the line of invariant points:

y = ((1 - k)/k) x

### Verdict

ChatGPT 0, DeepSeek 3

Total Marks so far: ChatGPT 0, DeepSeek 7

## Question 1c

The unit square S in the x-y plane is transformed by M onto the parallelogram P.

Find, in terms of k, a matrix which transforms P onto S.

### Prompt

The unit square S in the x-y plane is transformed by M onto the parallelogram P.

Find, in terms of k, a matrix which transforms P onto S.

### ChatGPT Answer

To find a matrix that transforms the parallelogram P back onto the unit square S, we need to find the inverse of the matrix M, since the transformation from S to P is represented by M. Applying the inverse of M will map P back to S.

The matrix M is:

[[k, k^2],
 [0, 1]]


Step 1: Find the inverse of M
To find the inverse of a 2x2 matrix:

[[a, b],
 [c, d]]

The inverse is given by:

1 / (ad - bc) * [[d, -b],
                 [-c, a]]

For the matrix M:

[[k, k^2],
 [0, 1]]

We have:

a = k, b = k^2, c = 0, d = 1
ad - bc = k * 1 - k^2 * 0 = k
Thus, the inverse of M is:

1 / k * [[1, -k^2],
          [0, k]]


This simplifies to:

[[1/k, -k],
 [0, k]]

Step 2: Conclusion
The matrix that transforms the parallelogram P back onto the unit square S is:

[[1/k, -k],
 [0, k]]

### DeepSeek Thinking

Okay, so I need to find a matrix that transforms the parallelogram P back into the unit square S. The original transformation is matrix M, which is [[k, k], [0, 1]]. So, to reverse this transformation, I probably need to find the inverse of matrix M, right? Because applying the inverse matrix should undo the original transformation.

First, let me recall how to find the inverse of a 2x2 matrix. The inverse of a matrix [[a, b], [c, d]] is (1/(ad - bc)) * [[d, -b], [-c, a]]. But I need to check if the determinant (ad - bc) is not zero. Let me compute the determinant of M first.

For M = [[k, k], [0, 1]], the determinant is (k)(1) - (k)(0) = k. Since k is not zero (given in the original problem that k > 0), the determinant is non-zero, so the inverse exists.

So the inverse matrix should be (1/k) * [[1, -k], [0, k]]. Wait, let me compute that step by step.

Original matrix:

a = k, b = k

c = 0, d = 1

Determinant D = ad - bc = k*1 - k*0 = k

Inverse matrix is (1/D) * [[d, -b], [-c, a]] = (1/k) * [[1, -k], [0, k]]

Wait, but let me verify that. Let's multiply M by its inverse to see if we get the identity matrix.

Original M: [[k, k], [0, 1]]

Proposed inverse: (1/k) * [[1, -k], [0, k]]

Multiplying M * inverse:

First row, first column: k*(1/k) + k*(0) = 1 + 0 = 1

First row, second column: k*(-k/k) + k*(k/k) = -k + k = 0

Second row, first column: 0*(1/k) + 1*0 = 0 + 0 = 0

Second row, second column: 0*(-k/k) + 1*(k/k) = 0 + 1 = 1

Yes, that gives the identity matrix. So the inverse is correct.

Therefore, the matrix that transforms P back to S is the inverse of M, which is:

(1/k) * [[1, -k], [0, k]]

But I should write it as a single matrix. Let's distribute the (1/k) scalar:

First row: (1/k)*1, (1/k)*(-k) → [1/k, -1]

Second row: (1/k)*0, (1/k)*k → [0, 1]

So the inverse matrix is [[1/k, -1], [0, 1]]

Let me double-check by applying this inverse to the transformed parallelogram P. The original transformation M takes the unit square S to P. Applying the inverse should take P back to S.

For example, take a corner of S, say (1,1). Applying M gives:

M * [1, 1] = [k*1 + k*1, 0*1 + 1*1] = [2k, 1]. Now applying the inverse matrix to [2k, 1]:

Inverse matrix is [[1/k, -1], [0, 1]]

So (1/k)*2k + (-1)*1 = 2 -1 = 1

Second component: 0*2k + 1*1 = 1

Which gives (1,1), the original point in S. Similarly, let's check (0,1):

M * [0,1] = [k*0 +k*1, 0*0 +1*1] = [k,1]. Applying inverse:

(1/k)*k + (-1)*1 =1 -1=0

0* k +1*1=1

So (0,1), which is correct.

Another point: (1,0). M*[1,0] = [k*1 +k*0, 0*1 +1*0] = [k,0]. Applying inverse:

(1/k)*k + (-1)*0=1 +0=1

0*k +1*0=0. So (1,0), correct.

Hence, the inverse matrix [[1/k, -1], [0, 1]] transforms P back to S.

Therefore, the answer should be this matrix.

### DeepSeek Answer

To transform the parallelogram P back to the unit square S, we need the inverse of matrix M

Steps:

Compute the determinant of M:
det(M) = k * 1 - k * 0 = k.

Inverse matrix formula:
M⁻¹ = (1/det(M)) * [[1, -k], [0, k]].

Simplify:
Multiply by 1/k to get the final inverse matrix.

Result:
The matrix that transforms P onto S is:

[[1/k, -1],
 [0,   1]]

### Verdict

ChatGPT 0, DeepSeek 1

DeepSeek gave a cleaner answer than the official mark scheme.

Total Marks so far: ChatGPT 0, DeepSeek 8

## Question 1d

Given that the area of P is 3k^2 units^2 , find the possible values of k

### Prompt

Given that the area of P is 3k^2 units^2 , find the possible values of k

### ChatGPT Answer

The area of the parallelogram P is given as 3k^2 square units. To find the possible values of k, we will first use the fact that the area of a transformed shape in the x-y plane can be determined by the absolute value of the determinant of the transformation matrix M.

The matrix M is:

[[k, k^2],
 [0, 1]]

Step 1: Find the determinant of M
The determinant of a 2x2 matrix:

[[a, b],
 [c, d]]

is calculated as:

det(M) = a * d - b * c

For matrix M:

[[k, k^2],
 [0, 1]]

The determinant is:

det(M) = k * 1 - k^2 * 0 = k

Step 2: Use the area formula
The area of the transformed shape (the parallelogram P) is the absolute value of the determinant of M multiplied by the area of the original unit square S, which is 1 unit^2.

So, the area of P is:

|det(M)| * area of S = |k| * 1 = |k|

We are told that the area of P is 3k^2. Therefore, we can equate the area of P to |k|:

|k| = 3k^2

Step 3: Solve for k
Now solve the equation |k| = 3k^2.

Case 1: If k > 0, then |k| = k, so the equation becomes:

k = 3k^2 k - 3k^2 = 0 k(1 - 3k) = 0

So, k = 0 or k = 1/3.

Case 2: If k < 0, then |k| = -k, so the equation becomes:

-k = 3k^2 k + 3k^2 = 0 k(3k + 1) = 0

So, k = 0 or k = -1/3.

Step 4: Conclusion
The possible values of k are:

k = 0, 1/3, -1/3

### DeepSeek Thinking

Alright, let's tackle this problem. So, we have the matrix M which is [[k, k], [0, 1]], and we're told that the area of the parallelogram P, which is the transformed unit square S, is 3k² units². We need to find the possible values of k.

First, I remember that the area scaling factor of a linear transformation represented by a matrix is equal to the absolute value of the determinant of that matrix. Since the original area of the unit square S is 1 (because it's a unit square), the area of the transformed figure P should be |det(M)| times the original area. But here, they say the area of P is 3k². So, I need to set |det(M)| equal to 3k² and solve for k.

Let me compute the determinant of M. The matrix M is:

[[k, k],

[0, 1]]

The determinant of a 2x2 matrix [[a, b], [c, d]] is ad - bc. Applying that here:

det(M) = (k)(1) - (k)(0) = k - 0 = k

So, the determinant is k. The absolute value would be |k|. Since the area scaling factor is |det(M)|, and the original area is 1, the area of P should be |k| * 1 = |k|. But the problem states that the area of P is 3k². So, we have:

|k| = 3k²

Now, solving this equation for k. Let's consider two cases because of the absolute value.

Case 1: k ≥ 0

In this case, |k| = k, so the equation becomes:

k = 3k²

Divide both sides by k (assuming k ≠ 0):

1 = 3k

So, k = 1/3

But we assumed k ≥ 0 and k ≠ 0 here. Since k = 1/3 is positive, this is a valid solution.

Case 2: k < 0

Here, |k| = -k, so the equation becomes:

-k = 3k²

Multiply both sides by -1:

k = -3k²

Bring all terms to one side:

3k² + k = 0

Factor out k:

k(3k + 1) = 0

So, either k = 0 or 3k + 1 = 0. But k < 0 in this case, so k = -1/3.

Wait, but the original problem states that k ≠ 0 (from the first problem description: "scale factor k (k ≠ 0)"). So k = 0 is not allowed, but here in case 2, when k < 0, we get k = -1/3 as a solution.

Therefore, the possible values of k are 1/3 and -1/3. But we need to check if these satisfy the original equation |k| = 3k².

Check for k = 1/3:

Left side: |1/3| = 1/3

Right side: 3*(1/3)² = 3*(1/9) = 1/3

So equality holds.

Check for k = -1/3:

Left side: |-1/3| = 1/3

Right side: 3*(-1/3)² = 3*(1/9) = 1/3

Equality holds here too.

Therefore, both k = 1/3 and k = -1/3 are solutions.

But wait, the problem mentions "the possible values of k". Since k is a scale factor for a stretch, usually scale factors are positive. However, the problem didn't specify that k must be positive, just that k ≠ 0. So, negative k would imply a reflection combined with a stretch. Depending on the context, negative scale factors might be acceptable. Since the problem allows k ≠ 0, both solutions are valid.

So the possible values of k are 1/3 and -1/3.

### DeepSeek Answer

To find the possible values of k given that the area of P is 3k²:

Area scaling factor of transformation M = [[k, k], [0, 1]] is the absolute value of its determinant:
det(M) = k * 1 - k * 0 = k.
Thus, area of P = |k| * (area of unit square) = |k|.

Set this equal to the given area 3k²:
|k| = 3k².

Solve for k:

If k > 0: k = 3k² → 3k² - k = 0 → k(3k - 1) = 0 → k = 1/3 (since k ≠ 0).

If k < 0: -k = 3k² → 3k² + k = 0 → k(3k + 1) = 0 → k = -1/3 (since k ≠ 0).

Possible values of k:

k = 0, 1/3, -1/3

### Verdict

ChatGPT did not figure out at all the 1a, so I cannot expect it to use 1a's answer. DeepSeek figured out 1a immediately and put the result to good use.

ChatGPT 1, DeepSeek 2

Total Marks so far: ChatGPT 1, DeepSeek 10

Next question will be in QP1_2.md