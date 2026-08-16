---
layout: course
title: MECH 672 - Navigation and Control of Robotic and Aerospace Systems
description: Modeling, navigation, and control of robotic and aerospace systems that rotate and translate in three-dimensional space. Kinematic and dynamic models. Nonlinear state-estimation strategies for navigation. Nonlinear control strategies.
instructor: Prof. James Richard Forbes

### year:

### term:

### location:

### time:

course_id: mech-672-navigation-and-control

schedule:
- week: 1
  date: Sep/Jan
  topic: Linear Algebra Review
  description: Linear systems of equations, least squares, and matrix decompositions.

- week: 2
  date: Sep/Jan
  topic: Probability Theory Review
  description: Probability density functions, marginalization, conditioning, and Bayes rule.
  materials:
      - name: Marginalization, Conditioning, Bayes Rule
        url: /assets/pdf/mech672/04_marg_cond_2026_08_15.pdf
      - name: Derivation of Bayes Rule
        url: /assets/pdf/mech672/05_bayes_opt_2026_08_15.pdf

- week: 3
  date: Sep/Jan
  topic: Linear Systems
  description: Linear state-space models, controllability, observability, and linearization.

- week: 4
  date: Sep/Jan
  topic: Stochastic Processes
  description: White-noise driven systems, uncertainty propagation, and Allan variance analysis.

- week: 5
  date: Oct/Feb
  topic: Kinematics and Dynamics
  description: Kinematic and dynamic models for rigid-body motion in three dimensions.

- week: 6
  date: Oct/Feb
  topic: Matrix Lie Groups
  description: SO(2), SE(2), SO(3), SE(3), and uncertainty representations on Lie groups.

- week: 7
  date: Oct/Feb
  topic: The Kalman Filter
  description: Derivation of the Kalman filter and applications to navigation.

- week: 8
  date: Oct/Feb
  topic: Extended Kalman Filters
  description: EKF-based navigation, multiplicative EKF, invariant EKF, and matrix Lie group EKF formulations.
  materials:
      - name: Invariant EKF (InEKF) Formulation
        url: /assets/pdf/mech672/16_InEKF_2026_08_15.pdf

- week: 9
  date: Nov/Mar
  topic: The Bayes Filter
  description: Bayes filter derivation, Kalman filtering as a special case, and sigma-point approximations.

- week: 10
  date: Nov/Mar
  topic: Batch State Estimation
  description: MAP estimation, solving the MAP problem via Gauss-Newton optimization, the sliding window filter.

- week: 11
  date: Nov/Mar
  topic: Smoothing
  description: Cholesky smoother and RTS smoothing.

- week: 12
  date: Nov/Mar
  topic: Nonlinear Stability Theory
  description: Equilibrium points, Lyapunov stability, LaSalle's invariant set theorem, and Barbalat's lemma.

- week: 13
  date: Dec/Apr
  topic: Nonlinear Control
  description: Nonlinear control design for robotic and aerospace systems.
---


### Course Overview

MECH 672 introduces modern navigation and control methods for robotic and aerospace systems operating in three-dimensional space. The course emphasizes state estimation, navigation, modeling, and nonlinear control techniques that arise in robotics, aerospace engineering, autonomous systems, and related fields.

Topics include:

- Probability theory and stochastic processes
- Kinematic and dynamic system models
- Matrix Lie groups
- Kalman and extended Kalman filtering
- Bayes filtering
- Smoothing methods
- Lyapunov stability theory
- Nonlinear control design

### Prerequisite and Corequisite Courses

There are no official prerequisite or corequisite courses. However, the following courses are beneficial:

- MECH 412
- MECH 513

Students are expected to be comfortable with:

- Calculus
- Differential equations
- Linear algebra
- Probability theory
- Numerical methods


### Python Resources

The course makes extensive use of Python together with NumPy and SciPy.

Useful resources:

- [Python Tutorial](https://docs.python.org/3/tutorial/)
- [Python Numerical Methods](https://pythonnumericalmethods.berkeley.edu/notebooks/Index.html)
- [NumPy 100 Exercises](https://github.com/rougier/numpy-100)
- [SciPy Lectures](https://scipy-lectures.org/intro/)
- [filterpy](https://filterpy.readthedocs.io/)
- [Kalman and Bayesian Filters in Python](https://github.com/rlabbe/Kalman-and-Bayesian-Filters-in-Python)

### Learning Outcomes

By the end of the course, students will be able to:

- Model robotic and aerospace systems that rotate and translate in three dimensions.
- Design and implement Kalman-filter-based navigation systems.
- Formulate and solve a batch state estimation problem.
- Apply nonlinear stability theory to engineering systems.
- Design nonlinear controllers for robotic and aerospace applications.
- Use modern computational tools to solve state-estimation and control problems.

### Textbooks

There is no required textbook. However, lectures are based on the following references.

State Estimation/Navigation:

- T. D. Barfoot, _State Estimation for Robotics_. New York, NY: Cambridge University Press, 2017.
- J. A. Farrell, _Aided Navigation: GPS with High Rate Sensors_. McGraw-Hill Education, 2008.
- Y. Bar-Shalom, X. R. Li, and K. Thiagalingam, _Estimation with Applications to Tracking and Navigation_. Hoboken, NJ: Wiley, 2001.
- S. Särkkä and L. Svensson, _Bayesian Filtering and Smoothing_, 2nd ed. Cambridge, UK: Cambridge University Press, 2023.
- A. J. Haug, _Bayesian Estimation and Tracking: A Practical Guide_. Hoboken, NJ: John Wiley & Sons, Inc., 2012.


Nonlinear Control:

- H. Marquez, _Nonlinear Control Systems_. Hoboken, NJ: John Wiley & Sons, Inc., 2003.
- M. Vidyasagar, _Nonlinear Systems Analysis_, 2nd ed. Englewood Cliffs, NJ: Prentice-Hall, 1993.
- H. K. Khalil, _Nonlinear Systems_, 3rd ed. Pearson Prentice Hall, 2002.

Kinematics and Dynamics:

- A. H. J. de Ruiter, C. J. Damaren, and J. R. Forbes, _Spacecraft Dynamics and Control: An Introduction_. West Sussex, UK: John Wiley & Sons, Ltd., 2013.
- P. C. Hughes, _Spacecraft Attitude Dynamics_, 2nd ed. Mineola, NY: Dover, 2004.


### Additional Resources

- D. Simon, _Optimal State Estimation_. Hoboken, NJ: John Wiley & Sons, Inc., 2006.
- J. L. Crassidis and J. L. Junkins, _Optimal Estimation of Dynamic Systems_, 2nd ed. Boca Raton, FL: CRC Press, 2012.
- R. F. Stengel, _Optimal Control and Estimation_. New York, NY: Dover, 1994.

