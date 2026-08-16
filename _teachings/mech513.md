---
layout: course
title: MECH 513 - Control Systems
description: State-space modelling and related linear algebra. Controllability and observability of linear time-invariant systems and corresponding tests, system realizations. Stability including bounded-Input-Bounded-Output (BIBO), internal, and Lyapunov stability. Linear state feedback control, state observers, optimal control, optimal estimation, and robust control.
instructor: Prof. James Richard Forbes
# year:
# term:
# location:
# time:
course_id: mech-513-control-systems

schedule:
  - week: 1
    date: Sep/Jan
    topic: State-space and Transfer Matrix Representations
    description: State-space and transfer function/matrix forms, linearization, and frequency response.

  - week: 2
    date: Sep/Jan
    topic: Lyapunov Stability Theory
    description: Lyapunov and asymptotic stability.

  - week: 3
    date: Sep/Jan
    topic: Lyapunov Equations
    description: Lyapunov equations and their application to stability analysis.

  - week: 4
    date: Sep/Jan
    topic: Linear Matrix Inequalities
    description: Introduction to LMIs and control-system applications.

  - week: 5
    date: Oct/Feb
    topic: Controllability
    description: Controllability concepts, tests, and implications.

  - week: 6
    date: Oct/Feb
    topic: Observability
    description: Observability concepts, tests, and system realizations.

  - week: 7
    date: Oct/Feb
    topic: State Feedback Control
    description: Static full-state feedback and pole placement.
    materials:
      - name: Static Full-State Feedback
        url: /assets/pdf/mech513/7a_FSF_ctrb_stab_2026_08_15.pdf

  - week: 8
    date: Oct/Feb
    topic: State Observers
    description: Full-order and reduced-order observer design.
    materials:
      - name: Observers
        url: /assets/pdf/mech513/7b_observer_2026_08_15.pdf

  - week: 9
    date: Nov/Mar
    topic: Observer-Based Controllers
    description: Separation principle and output-feedback control.
    materials:
      - name: Observer-Based Controllers
        url: /assets/pdf/mech513/7c_obsv_based_ctrl_2026_08_15.pdf

  - week: 10
    date: Nov/Mar
    topic: The Generalized Plant
    description: Motivation, performance channel, exogenous input channel, examples.

  - week: 11
    date: Nov/Mar
    topic: Optimal Control
    description: Problem formulation, linear quadratic regulator (LQR) design.

  - week: 12
    date: Nov/Mar
    topic: H₂ and H∞ Control
    description: Norms, full-state feedback control, and estimation.
    materials:
      - name: H₂ and H∞ Norms
        url: /assets/pdf/mech513/10_H2_Hinf_sys_norms_2026_08_15.pdf
      - name: H₂ Control via LMIs
        url: /assets/pdf/mech513/11a_H2_LMI_2026_08_15.pdf
      - name: H∞ Control via LMIs
        url: /assets/pdf/mech412/11b_Hinf_LMI_2026_08_15.pdf

  - week: 13
    date: Dec/Apr
    topic: Robust Control
    description: Uncertainty modelling, robust stability, and robust performance.
---

### Course Overview

MECH 513 introduces modern control theory using state-space methods. Students develop mathematical tools for the analysis and synthesis of dynamical systems, with particular emphasis on controllability, observability, stability analysis, state feedback control, state estimation, optimal control, and robust control.

Topics include:

- State-space modelling and system realizations
- Lyapunov stability theory
- Linear matrix inequalities (LMIs)
- Controllability and observability
- State-feedback control and pole placement
- State observers
- Optimal control and estimation
- H₂ and H∞ control
- Robust stability and robust performance

### Prerequisite and Corequisite Courses

Students are expected to be comfortable with:

- Calculus
- Differential equations
- Linear algebra
- Python programming

##### Undergraduate Prerequisite Courses

- MECH 412 or MECH 419

##### Graduate Students

No formal prerequisite.

### Python Resources

The course makes extensive use of Python, the python-control package, and cvxpy.

Useful resources:

- [Python Tutorial](https://docs.python.org/3/tutorial/)
- [Python Numerical Methods](https://pythonnumericalmethods.berkeley.edu/notebooks/Index.html)
- [NumPy 100 Exercises](https://github.com/rougier/numpy-100)
- [SciPy Lectures](https://scipy-lectures.org/intro/)
- [Python Control Library](https://python-control.readthedocs.io/en/0.9.4/)
- [cvxpy](https://www.cvxpy.org/)
- [MECH 412 Code Repository](https://github.com/jrforbes/mech_412_code)
- [MECH 513 Code Repository](https://github.com/jrforbes/mech_513_code)

### Learning Outcomes

By the end of the course, students will be able to:

- Use linear algebra tools to manipulate and analyze linear dynamical systems.
- Assess whether a system is controllable and observable, and understand the implications of such assessments.
- Design state-feedback controllers and state observers using state-space methods.
- Formulate and solve optimal control and estimation problems.
- Analyze uncertainty, robustness, and performance of feedback control systems.
- Apply modern computational tools to control-system analysis and design.

### Textbooks

There is no required textbook. However, lectures are based on the following references.

- S. Skogestad and I. Postlethwaite, _Multivariable Feedback Control: Analysis and Design_, 2nd ed. Hoboken, NJ: John Wiley & Sons, Inc., 2005.
- J. Hespanha, _Linear Systems Theory_. Princeton, NJ: Princeton University Press, 2009.
- R. L. Williams and D. A. Lawrence, _Linear State-Space Control Systems_. Hoboken, NJ: John Wiley & Sons, Inc., 2007.
- K. Zhou and J. C. Doyle, _Essentials of Robust Control_. Upper Saddle River, NJ: Prentice Hall, 1998.

### Additional Resources

- [Randy Beard Control Book](https://github.com/randybeard/controlbook_public)
- [University of Michigan Control Tutorials (CTMS)](http://ctms.engin.umich.edu/CTMS)