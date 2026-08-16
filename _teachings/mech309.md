---
layout: course
title: MECH 309 - Numerical Methods in Mechanical Engineering
description: Numerical techniques for problems commonly encountered in Mechanical Engineering including systems of linear equations, eigenvalue problems, least-squares estimation, optimization, ordinary differential equations, and interpolation. The emphasis is on understanding the underlying numerical methods and their application to engineering problems.
instructor: Prof. James Richard Forbes

## year:

## term:

## location:

## time:

course_id: mech-309-numerical-methods

schedule:
- week: 1
  date: Sep/Jan
  topic: Errors and Conditioning
  description: Binary numbers, floating point arithmetic, error analysis, and conditioning.

- week: 2
  date: Sep/Jan
  topic: Linear Algebra Review
  description: $Ax = b$ and the four fundamental subspaces.

- week: 3
  date: Sep/Jan
  topic: Linear Systems of Equations
  description: Conditioning, Gaussian elimination, LU decomposition, and Cholesky factorization, interpolation posed as a $Ax = b$ problem.

- week: 4
  date: Sep/Jan
  topic: Iterative Methods
  description: Gradient descent, steepest descent, and iterative solution methods.

- week: 5
  date: Oct/Feb
  topic: QR Factorization
  description: Orthogonal factorization methods and applications.

- week: 6
  date: Oct/Feb
  topic: Eigenvalue Problems
  description: Eigenvalues, eigenvectors, power iteration, and inverse power iteration.

- week: 7
  date: Oct/Feb
  topic: Singular Value Decomposition
  description: SVD computation and engineering applications.

- week: 8
  date: Oct/Feb
  topic: Linear Least Squares
  description: Problem formulation, normal equations, and weighted least squares.

- week: 9
  date: Nov/Mar
  topic: Nonlinear Least Squares
  description: Gauss-Newton and Levenberg-Marquardt algorithms.

- week: 10
  date: Nov/Mar
  topic: Optimization
  description: Unconstrained and constrained optimization methods.

- week: 11
  date: Nov/Mar
  topic: Ordinary Differential Equations - Initial Value Problems
  description: Euler and Runge-Kutta methods for initial value problems.

- week: 12
  date: Nov/Mar
  topic: Ordinary Differential Equations - Boundary Value Problems
  description: Shooting methods and finite difference methods.
  materials:
      - name: Finite Difference Methods for ODEs
        url: /assets/pdf/mech309/15c_BVP_2026_08_15.pdf

- week: 13
  date: Dec/Apr
  topic: Partial Differential Equations
  description: Finite difference methods.
  materials:
      - name: Review of PDEs
        url: /assets/pdf/mech309/16a_PDE_intro_2026_08_15.pdf
      - name: Finite Difference Methods for PDEs
        url: /assets/pdf/mech309/16b_PDE_FD_2026_08_15.pdf

---

<!--
- week: 13
  date: Dec/Apr
  topic: Interpolation and Approximation
  description: Polynomial interpolation, splines, orthogonal polynomials, and Fourier methods.
-->

### Course Overview

MECH 309 introduces the theory and application of numerical methods, also known as scientific computing. Students learn how to reformulate engineering problems into mathematical forms that can be solved computationally and how to assess the accuracy and reliability of numerical solutions.

Topics include:

- Error analysis and conditioning
- Systems of linear equations
- Eigenvalue problems
- Eigen and Singular value decompositions
- Interpolation and splines
- Linear and nonlinear least squares
- Optimization
- Ordinary differential equations (IVPs and BVPs)
- Partial differential equations


### Prerequisite and Corequisite Courses

Students are expected to be comfortable with:

- Calculus
- Differential equations
- Linear algebra
- Basic Python programming

##### Prerequisite Courses

- MATH 263
- MATH 271
- COMP 208

### Python Resources

The course makes extensive use of Python together with NumPy and SciPy.

Useful resources:

- [Python Tutorial](https://docs.python.org/3/tutorial/)
- [Python Numerical Methods](https://pythonnumericalmethods.berkeley.edu/notebooks/Index.html)
- [NumPy 100 Exercises](https://github.com/rougier/numpy-100)
- [SciPy Lectures](https://scipy-lectures.org/intro/)
- [COMP208](https://d3vp.github.io/comp208-notes)
- [Course Code Repository](https://github.com/jrforbes/mech_309_code)

### Learning Outcomes

By the end of the course, students will be able to:

- Reformulate engineering problems as numerical problems suitable for computation.
- Solve systems of linear equations and eigenvalue problems numerically.
- Formulate and solve linear and nonlinear least-squares problems.
- Apply optimization techniques to engineering problems.
- Numerically solve initial value and boundary value problems.
- Assess the accuracy, conditioning, and reliability of numerical solutions.
- Apply modern scientific-computing tools to engineering analysis and design.

### Textbooks

There is no required textbook. However, lectures are based on the following references.

- M. T. Heath, _Scientific Computing: An Introductory Survey_, 2nd ed. New York, NY: McGraw-Hill, 2002.
- S. Boyd and L. Vandenberghe, _Introduction to Applied Linear Algebra_. Cambridge, UK: Cambridge University Press, 2018. Available [here](https://web.stanford.edu/~boyd/vmls/).
- J. Solomon, _Numerical Algorithms: Methods for Computer Vision, Machine Learning and Graphics_. Boca Raton, FL: CRC Press, 2015.
- T. Sauer, _Numerical Analysis_, 3rd ed. Boston, MA: Pearson, 2018.


### Additional Resources

- P. E. Gill, W. Murray, and M. H. Wright, _Numerical Linear Algebra and Optimization_. Philadelphia, PA: SIAM, 2021.
- P. R. Turner, T. Arildsen, and K. Kavanagh, _Applied Scientific Computing with Python_. Cham, Switzerland: Springer, 2018.
- J. Nocedal and S. J. Wright, _Numerical Optimization_, 2nd ed. New York, NY: Springer, 2006.
- C. D. Meyer, _Matrix Analysis and Applied Linear Algebra_. Philadelphia, PA: SIAM, 2000.
- S. Toledo, _Location Estimation from the Ground Up_. Philadelphia, PA: SIAM, 2020.
- G. Strang and K. Borre, _Linear Algebra, Geodesy, and GPS_. Wellesley, MA: Wellesley-Cambridge Press, 1997.
