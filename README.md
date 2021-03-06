# Recurrent Neural Networks for Simulating Dynamical Systems

# Abstract
Systems in Hamiltonian dynamics are governed by ordinary differential equations, expressed through Hamilton's equations. As analytical solutions are not always possible for complex systems, simulations are required to gain intuition on these systems' behaviour. These simulated trajectories are typically generated using numerical methods, including integrators like Euler and Verlet. We explore the application of Neural Network based machine learning for the task of simulation. Applying deep, recurrent and Hamiltonian neural networks to simple and chaotic systems, we demonstrate the capability of these networks to produce fast, accurate results, that obey physical laws of conservation, in multiple example systems. 

# Contents of this Repository
This repository contains all the python code and notebooks used and referenced in my Masters project. 

The code present allows us to construct and train neural networks of dense, recurrent and Hamiltonian architecture, using training data generated by a range of known integration schema, and in the case of the simple harmonic oscillator, data from the analytical solution.

The notebooks present allow us to train our neural networks and assess their performance on a range of dynamical systems, generating plots of the position and velocity error versus the baseline training integrator, the L2-Norm of position and velocity errors, the energy drift and the statespace diagram for a range of simulation timespans.

In addition to the dynamical systems discussed in the paper, this repository also contains the code necessary to run the experiments on the 1D Lennard-Jones Oscillator and the 3D three-body chaotic system. It also contains the symplectic Euler integration scheme, alongside the symplectic Verlet, RK4 and Euler schema detailed in the paper.

# Structure of this repository

The directory 'Code' in this repository consists of all the .py files containing all code for constructing and testing neural networks, defining dynamical systems and formulating integration schema. 

Notebooks in all directories are numbered in a loosely chronological order, to reflect their relative appearances in the paper and to mirror development steps in improving and testing the neural networks.

The directory "Integration Generated Visualisations" contains statespace and energy drift visualisations of all dynamical systems, generated by all available integration schema; these serve to illustrate the performance of the differing schema as discussed in Chapter 3 of the paper.

The directory 'Report Diagrams' contains notebooks used to generate visualisations used in the paper itself.

The directories 'DNN / LSTM / HNN Hyperparameters' contain notebooks showing the steps taken in optimising the hyperparameters of the three network types investigated.

The directories '1D Oscillators' and 'Henon-Heiles' contain notebooks assessing the performance of the final network types identified through hyperparameter optimisation, applied to the one-dimensional oscillators (simple harmonic oscillator, double-well oscillator and rugged oscillator) and chaotic Henon-Heiles system.

The directory 'X Only' contains experiments performed using the LSTM integrator, simulating only the position time-evolution of the SHO system.

The directory 'Additional Experiments' contains notebooks performing investigations into specific behaviours of the final networks.

# Example Results for the DW System

Neural Network

![NN DW 128 Statespace](https://user-images.githubusercontent.com/93135270/159294713-39fc3dbd-ac1d-4a5c-bc32-916e46cfe7a8.png)

LSTM Recurrent Network

![LSTM DW 512 Statespace](https://user-images.githubusercontent.com/93135270/159295074-fe6417dc-9873-42a4-9743-3490dc6266d5.png)

Hamiltonian Neural Network

![HNN DW 128 Statespace](https://user-images.githubusercontent.com/93135270/159294644-71cd75b5-e541-4f67-8113-3ba6d18ed2d2.png)

