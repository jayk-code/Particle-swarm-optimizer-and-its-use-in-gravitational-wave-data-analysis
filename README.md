# Particle-swarm-optimizer-and-its-use-in-gravitational-wave-data-analysis
In this project I am investigating the use of particle swarm optimizer algorithm for detection of gravitational wave signal from  compact binary coalescences(black hole and neutron star mergers) and estimating various parameters associated with it.

![giphy (1)](https://user-images.githubusercontent.com/84566016/162309747-3e78fda7-ea8c-459b-80cf-147970caefab.gif)


### Particle swarm optimization algorithm 
PSO alogrithm tries to find the optimum(minimum or maximum) for any given function in given parameter space.
Initially all the particles are distributed all around the parameter space and thy are assigned random valocities. Then the value of given function is calculated at the position of all the particles.Then the velocities of all the particles changes according to the following formula.

<h1 align="center">v(t+1) = w*v(t) + c1*r1*(p -x(t)) + c2*r2*(g-x(t))</h1>
