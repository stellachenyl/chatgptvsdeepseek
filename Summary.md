# Summary

## Question 1

Question 1a Summary: The problem required finding the matrix M representing a stretch parallel to the x-axis (scale factor k) followed by a shear keeping the x-axis fixed. ChatGPT incorrectly multiplied the stretch and shear matrices, resulting in a matrix with k squared. DeepSeek correctly identified the stretch matrix (k, 0 in the first row; 0, 1 in the second row) and shear matrix (1, k in the first row; 0, 1 in the second row), then multiplied them in the correct order (shear after stretch) to get M as a matrix with first row k, k and second row 0, 1. DeepSeek earned full marks.

Question 1b Summary: The task was to find the line of invariant points under M. Using its incorrect matrix from 1a, ChatGPT derived an equation involving k squared. DeepSeek used the correct matrix and solved the invariance condition, leading to the line equation y equals (1 minus k divided by k) times x. DeepSeek earned full marks, while ChatGPT received none.

Question 1c Summary: The question requires finding the matrix that transforms the parallelogram P back onto the unit square S, given the transformation matrix M. Both ChatGPT and DeepSeek correctly identify that finding the inverse of M is the key to solving this. ChatGPT calculates the inverse using the standard formula for a 2x2 matrix and arrives at the wrong inverse matrix: [[1/k, -k], [0, k]]. DeepSeek correctly computes the inverse matrix and verifies the result by multiplying M with its inverse to confirm it gives the identity matrix. DeepSeek’s solution is clearer, with a more thorough explanation and verification steps, ultimately providing the final result: [[1/k, -1], [0, 1]].

Question 1d Summary: This question asks for the possible values of k given that the area of the parallelogram P is 3k^2. Both ChatGPT and DeepSeek correctly identify that the area of P is related to the determinant of matrix M. ChatGPT finds the determinant of M and sets up the equation |k| = 3k^2 to solve for k. It solves the equation and provides k = 0, 1/3, and -1/3 as possible values. However, ChatGPT does not explain why k ≠ 0, which could lead to some ambiguity. DeepSeek, in contrast, goes into more detail, explaining both cases (k ≥ 0 and k < 0) and verifies the solutions. It provides the same values for k (1/3 and -1/3) and clarifies that both values are valid since the problem does not explicitly rule out negative k. DeepSeek provides a clearer and more detailed solution overall.

Marks so far: ChatGPT 1, DeepSeek 10

## Question 2

