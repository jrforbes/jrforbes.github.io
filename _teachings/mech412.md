---
layout: course
title: MECH 412 - System Dynamics and Control
description: Modelling of physical linear time-invariant systems using transfer functions. Transient and steady-state response specifications. State space representation of systems. Frequency-response characterization. Stability. Feedback control systems. PID controller design. Frequency response design methods. Lead, lag and PID compensators.
instructor: Prof. James Richard Forbes
# year: 2025
# term: Fall
# location: WONG 120
# time: Tuesday & Thursday, 10:05 AM - 11:25 AM
course_id: mech-412-system-dynamics-control

schedule:
  - week: 1
    date: Sep/Jan
    topic: Mathematical Review
    description: ODEs, state-space models, linearization.
    materials:
      - name: ODEs
        url: /assets/pdf/mech412/2_ODEs_2026_08_15.pdf

  - week: 2
    date: Sep/Jan
    topic: Applications of Laplace Transforms
    description: Laplace Transforms, transfer functions, block diagrams.
    materials:
      - name: Laplace Transforms
        url: /assets/pdf/mech412/3_LT_2026_08_15.pdf
      - name: Transfer Functions
        url: /assets/pdf/mech412/4_TF_2026_08_15.pdf
      - name: Block Diagrams
        url: /assets/pdf/mech412/5_block_2026_08_15.pdf

  - week: 3
    date: Sep/Jan
    topic: Physical System Models
    description: Mechanical, electrical, hydraulic, and thermal systems.

  - week: 4
    date: Sep/Jan
    topic: System Identification
    description: Building mathematical models from experimental data.

  - week: 5
    date: Oct/Feb
    topic: Open-Loop System Properties
    description: Stability concepts and the Routh-Hurwitz criterion.

  - week: 6
    date: Oct/Feb
    topic: Time-Domain Analysis
    description: First- and second-order transient response specifications.

  - week: 7
    date: Oct/Feb
    topic: Frequency Response
    description: Bode plots and frequency-domain signal analysis.

  - week: 8
    date: Oct/Feb
    topic: The Control Problem
    description: Feedback systems, well-posedness, and internal stability.

  - week: 9
    date: Nov/Mar
    topic: Classical Controllers
    description: P, PI, PD, PID, lead, lag, and lead-lag compensators.

  - week: 10
    date: Nov/Mar
    topic: Nyquist Analysis
    description: Nyquist stability criterion and robustness analysis.

  - week: 11
    date: Nov/Mar
    topic: Design Margins
    description: Gain margin, phase margin, and vector margin.

  - week: 12
    date: Nov/Mar
    topic: Loop Shaping
    description: Frequency-domain controller design techniques.

  - week: 13
    date: Dec/Apr
    topic: Robust Control
    description: Model uncertainty and robust control methods.

---

### Course Overview

MECH 412 introduces modelling, analysis, and design methods for feedback control systems. Students develop mathematical models of engineering systems, study their dynamic behaviour, and design controllers that meet performance and robustness requirements.

Topics include:

- Transfer functions and state-space models
- Dynamic modelling of physical systems
- System identification
- Time-domain and frequency-domain response
- Feedback control
- PID, lead, and lag compensator design
- Loop shaping and robustness


### Prerequisite and Corequisite Courses

Students are expected to be comfortable with:

- Calculus
- Differential equations
- Linear algebra
- Python programming

#### Prerequiste Courses

- MECH 309
- MECH 315

#### Corequisite Courses

- MECH 331

### Python Resources

The course makes extensive use of Python and the `python-control` package.

Useful resources:

- [Python Tutorial](https://docs.python.org/3/tutorial/)
- [Python Numerical Methods](https://pythonnumericalmethods.berkeley.edu/notebooks/Index.html)
- [NumPy 100 Exercises](https://github.com/rougier/numpy-100)
- [SciPy Lectures](https://scipy-lectures.org/intro/)
- [Python Control Library](https://python-control.readthedocs.io/en/0.9.4/)
- [Course Code Repository](https://github.com/jrforbes/mech_412_code)

### Learning Outcomes

By the end of the course, students will be able to:

- Derive dynamic models suitable for control-system analysis.
- Analyze system behaviour in both the time and frequency domains.
- Design controllers that satisfy performance and robustness specifications.
- Apply mathematics, simulation, and engineering tools to solve control problems.
- Use modern computational tools to support engineering decision making.


### Textbooks

There is no required textbook. However, lectures are based on the following references.

- L. Qiu and K. Zhou, *Introduction to Feedback Control*. Upper Saddle River, NJ: Prentice-Hall, Inc., 2010.
- L. Guzzella, *Analysis and Synthesis of Single-Input Single-Output Control Systems*, 4th ed. ETH Zurich: vdf Hochschulverlag AG, 2019.
- P. Seiler and J. Theis, *An Introduction to Classical Control and Loopshaping*. Ann Arbor, MI: University of Michigan, 2022.
- W. J. Palm, *System Dynamics*, 3rd ed. Toronto, ON: McGraw Hill, 2013.
- K. A. Seeler, *System Dynamics*. New York, NY: Springer, 2014.


### Additional Resources

- [Randy Beard Control Book](https://github.com/randybeard/controlbook_public)
- [University of Michigan Control Tutorials (CTMS)](http://ctms.engin.umich.edu/CTMS)