# Iterative Methods for Solving Linear Systems

This project contains implementations of the Gauss-Seidel and Jacobi iterative methods for solving systems of linear equations of the form Ax = b.

## Description

- **Gauss-Seidel Method:** An iterative technique for solving a square system of n linear equations with unknown x. It is an improvement over the Jacobi method, where it uses the updated values as soon as they are available.

- **Jacobi Method:** An iterative algorithm for determining the solutions of a strictly diagonally dominant system of linear equations. The method relies on an initial guess and iteratively improves the solution.

## Functions

### `gaussSeidel(A, b, tol=0.001, max_iterations=100)`

Solves the system of linear equations Ax = b using the Gauss-Seidel iterative method.

- **Parameters:**
  - `A` (list of list of floats): Coefficient matrix.
  - `b` (list of floats): Constant terms.
  - `tol` (float, optional): Tolerance for the stopping criterion. Defaults to 0.001.
  - `max_iterations` (int, optional): Maximum number of iterations. Defaults to 100.

- **Returns:**
  - `list of floats`: Solution vector x if the method converges within the maximum number of iterations.
  - `None`: If the method does not converge.

### `jacobi(A, b, tol=0.001, max_iterations=100)`

Solves the system of linear equations Ax = b using the Jacobi iterative method.

- **Parameters:**
  - `A` (list of list of floats): Coefficient matrix.
  - `b` (list of floats): Constant terms.
  - `tol` (float, optional): Tolerance for the stopping criterion. Defaults to 0.001.
  - `max_iterations` (int, optional): Maximum number of iterations. Defaults to 100.

- **Returns:**
  - `list of floats`: Solution vector x if the method converges within the maximum number of iterations.
  - `None`: If the method does not converge.

## Usage

To run the methods and see their results, use the `main()` function which tests both methods with a sample system of linear equations.

### Example

```python
def main():
    A = [
        [4, 2, 0],
        [2, 10, 4],
        [0, 4, 5]
    ]
    b = [2, 6, 5]

    print("Solution using the Gauss-Seidel method:")
    solution_gauss_seidel = gaussSeidel(A, b)
    if solution_gauss_seidel is not None:
        print(solution_gauss_seidel)

    print("\nSolution using the Jacobi method:")
    solution_jacobi = jacobi(A, b)
    if solution_jacobi is not None:
        print(solution_jacobi)

if __name__ == "__main__":
    main()
