---
layout: course
title: MECH 642 - Advanced Dynamics
description: Variational methods. Hamilton's principle and equations of motion of engineering systems. Lagrangian formulations for discrete systems. Methods of discretizing continuous systems. Rigid body dynamics. Dynamic behaviour of linear and nonlinear systems. Response of engineering systems to deterministic inputs by classical methods. Stability of linear and nonlinear systems.
instructor: Prof. James Richard Forbes

## year:

## term:

## location:

## time:

course_id: mech-642-advanced-dynamics

schedule:
- week: 1
  date: Sep/Jan
  topic: Kinematics I
  description: Physical vectors, reference frames, and direction cosine matrices (DCMs).

- week: 2
  date: Sep/Jan
  topic: Kinematics II
  description: The Transport Theorem.

- week: 3
  date: Sep/Jan
  topic: Attitude Representations
  description: Axis-angle parameters, Euler angles, and quaternions.

- week: 4
  date: Sep/Jan
  topic: Angular Velocity Kinematics
  description: Poisson's equation. 

- week: 5
  date: Oct/Feb
  topic: Newtonian Dynamics
  description: Single-particle and multi-particle system dynamics.

- week: 6
  date: Oct/Feb
  topic: Rigid-Body Dynamics
  description: Newtonian-Eulerian formulation of rigid-body motion.

- week: 7
  date: Oct/Feb
  topic: System Energy
  description: Kinetic energy, potential energy, and energy methods.

- week: 8
  date: Oct/Feb
  topic: Constraints and Virtual Work
  description: Holonomic and nonholonomic constraints, virtual work, and D'Alembert's principle.

- week: 9
  date: Nov/Mar
  topic: Lagrangian Dynamics
  description: Lagrangian formulation for particle and rigid-body systems.

- week: 10
  date: Nov/Mar
  topic: Constrained Dynamics
  description: Lagrange multipliers and the null-space method.

- week: 11
  date: Nov/Mar
  topic: Calculus of Variations
  description: The brachistochrone problem and variational calculus.
  materials:
      - name: Calculus of Variations
        url: /assets/pdf/mech642/11a_calc_var_2026_08_15.pdf

- week: 12
  date: Nov/Mar
  topic: Hamilton's Principle
  description: Hamilton's principle, Hamilton's extended principle, and discretization methods.

- week: 13
  date: Dec/Apr
  topic: Stability Theory
  description: Lyapunov stability, LaSalle's invariant set theorem, and applications.
---


### Course Overview

MECH 642 introduces advanced kinematics and dynamics in three dimensions. Students will learn how to derive the equations of motion of systems composed of particles and rigid bodies using the Newton-Euler approach, Lagrange's equation, Hamilton's (extended) principle, and the Gibbs-Appell equations.

<!-- Students will learn Newtonian, Eulerian, and Lagrangian formulations of motion and apply variational methods to derive equations of motion for engineering systems. -->

Topics include:

- Three-dimensional kinematics
- Direction cosine matrices (DCMs)
- Euler angles and quaternions
- Transport theorem and Poisson's equation
- Newtonian and Eulerian dynamics
- Rigid-body dynamics
- Energy methods
- Holonomic and nonholonomic constraints
- Virtual work and D'Alembert's principle
- Lagrangian dynamics
- Calculus of variations
- Hamilton's principle
- Stability theory

### Prerequisite and Corequisite Courses

There are no official prerequisite or corequisite courses. However, students are expected to be comfortable with:

- Calculus
- Differential equations
- Linear algebra
- Classical mechanics
- Python programming

### Python Resources

Assignments require computational work in Python.

Useful resources:

- [Python Tutorial](https://docs.python.org/3/tutorial/)
- [Python Numerical Methods](https://pythonnumericalmethods.berkeley.edu/notebooks/Index.html)
- [NumPy 100 Exercises](https://github.com/rougier/numpy-100)
- [SciPy Lectures](https://scipy-lectures.org/intro/)

### Learning Outcomes

By the end of the course, students will be able to:

- Describe the motion of particles and rigid bodies in three dimensions.
- Construct and manipulate direction cosine matrices, Euler angles, and quaternion parameterizations.
- Apply Newtonian, Eulerian, and Lagrangian methods to derive equations of motion.
- Analyze systems subject to holonomic and nonholonomic constraints.
- Use variational methods and Hamilton's principle to formulate dynamic models.
- Assess stability using Lyapunov methods and LaSalle's invariant set theorem.
- Apply computational tools to solve advanced dynamics problems.

### Textbooks

There is no required textbook. However, lectures are based on the following references.

- G. M. T. D'Eleutario and G. R. Heppler, _Newton's Second Law And All That_. (In preparation) Cambridge University Press, 2011.
- D. S. Bernstein, _Geometry, Kinematics, Statics, and Dynamics_. (In preparation) Princeton University Press, 2013.
- P. C. Hughes, _Spacecraft Attitude Dynamics_, 2nd ed. Mineola, NY: Dover, 2004.
- F. L. Markley and J. L. Crassidis, _Fundamentals of Spacecraft Attitude Determination and Control_. New York, NY: Springer, 2014.
- A. H. J. de Ruiter, C. J. Damaren, and J. R. Forbes, _Spacecraft Dynamics and Control: An Introduction_. West Sussex, UK: John Wiley & Sons, Ltd., 2013.

### Additional Resources

- N. J. Kasdin and D. A. Paley, _Engineering Dynamics: A Comprehensive Introduction_. Princeton, NJ: Princeton University Press, 2011.
- D. T. Greenwood, _Advanced Dynamics_. Cambridge University Press, 2003.
- A. V. Rao, _Dynamics of Particles and Rigid Bodies: A Systematic Approach_. New York, NY: Cambridge University Press, 2006.
- L. Meirovitch, _Methods of Analytical Dynamics_. Toronto, ON: McGraw-Hill, 1970.
- H. Schaub and J. L. Junkins, _Analytical Mechanics of Space Systems_, 2nd ed. Reston, VA: AIAA, 2009.