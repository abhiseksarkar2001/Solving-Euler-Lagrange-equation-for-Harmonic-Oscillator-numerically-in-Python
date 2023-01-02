# Solving-Euler-Lagrange-equation-for-Harmonic-Oscillator-numerically-in-Python
This repository contains a python script for solving the differential equation for a harmonic oscillator using the Lagrange method and the solve_ivp function from the scipy library.

## Usage
To use the script, make sure you have **numpy**, **matplotlib**, and **scipy** installed. Then, simply run the script using a python interpreter. The script will solve the differential equation for a harmonic oscillator with given mass and spring constant, and print the solution.

## Documentation
The harmonic oscillator is a system that oscillates with a frequency that is proportional to the spring constant of the system. It can be described by the following differential equation:

mx'' + kx = 0
where m is the mass of the oscillator, k is the spring constant, x is the displacement of the oscillator, and x'' is the second derivative of x with respect to time.

To solve this equation using the Lagrange method, we first define the Lagrangian of the system:

L = T - V
where T is the kinetic energy of the system and V is the potential energy of the system.

For a harmonic oscillator, the kinetic energy is given by:

<img src="https://latex.codecogs.com/svg.image?\inline&space;\bg{black}{\color{white}&space;T&space;=&space;\frac{1}{2}mx'^2}&space;" title="https://latex.codecogs.com/svg.image?\inline \bg{black}{\color{white} T = \frac{1}{2}mx'^2} " />
where x' is the first derivative of x with respect to time.

The potential energy is given by:

<img src="https://latex.codecogs.com/svg.image?\inline&space;\bg{black}{\color{white}&space;V&space;=&space;\frac{1}{2}kx^2}&space;" title="https://latex.codecogs.com/svg.image?\inline \bg{black}{\color{white} V = \frac{1}{2}kx^2} " />

Then, we find the Euler-Lagrange equation:

<img src="https://latex.codecogs.com/svg.image?\inline&space;\bg{black}{\color{white}&space;\frac{\partial&space;\mathcal{L}}{\partial&space;x}&space;-&space;\frac{d}{dt}\frac{\partial&space;\mathcal{L}}{\partial&space;\dot{x}}&space;=&space;0&space;" title="https://latex.codecogs.com/svg.image?\inline \bg{black}{\color{white} \frac{\partial \mathcal{L}}{\partial x} - \frac{d}{dt}\frac{\partial \mathcal{L}}{\partial \dot{x}} = 0 " />

Substituting the expressions for T, V, and L, we obtain a second-order differential equation for x'':

<img src="https://latex.codecogs.com/svg.image?\inline&space;\bg{black}{\color{white}&space;x''&space;=&space;-\frac{kx}{m}&space;}&space;" title="https://latex.codecogs.com/svg.image?\inline \bg{black}{\color{white} x'' = -\frac{kx}{m} } " />

To solve this equation, we use the solve_ivp function from the scipy library, which takes in a function representing the system of first-order differential equations and the initial conditions, and returns the solution as an object.

The script also includes options for plotting the solution and finding the oscillation frequency.
