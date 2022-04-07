# Particle-swarm-optimizer-and-its-use-in-gravitational-wave-data-analysis
In this project I am investigating the use of particle swarm optimizer algorithm for detection of gravitational wave signal from  compact binary coalescences(black hole and neutron star mergers) and estimating various parameters associated with it.

![giphy (1)](https://user-images.githubusercontent.com/84566016/162309747-3e78fda7-ea8c-459b-80cf-147970caefab.gif)


### Particle swarm optimization algorithm 
PSO alogrithm tries to find the optimum(minimum or maximum) for any given function in given parameter space.
Initially all the particles are distributed all around the parameter space and thy are assigned random valocities. Then the value of given function is calculated at the position of all the particles.Then the velocities of all the particles changes in all the dimentions after 1 unit of time according to the following formula.

    v(t+1) = w*v(t) + c1*r1*(pBest -x(t)) + c2*r2*(gBest - x(t))

- Here v(t+1) is updated velocity of particle.
- x(t) and v(t) are current position and velocity respectively
- w is factor of inertia.(Inertia is tendency of particle to continue it's movement in it's current direction)
- pBest (Personal best) is best  location explored by particle itself,where value of given function was optimum.
- gBest (Global best) is best  location explored by any particle among all the particles in the swarm,where value of given function was optimum.
- The factors r1 and r2 are stochastic factors which determine at any given instance of time the instinct to move towards the pBest and gBest respectively. Their value varies between 0 to 1 in every iteration.

### Using PSO for gravitational wave data analysis
- I have used PyCBC package in this project extensively. From this package one can download data of previously recorded mergers, generate wave templates with various parameters, can do signal processing and much more.
- The function which is to be maximized in this case is called signal to noise ratio(SNR).Which is calculated by doing matched filtering operation on sample data and template.
- Until now I have found masses of object 1 and mass of object 2 in Merger event "GW150914" using particle swarm optimizer algorithm. Plot of the real data and template generated with mass 1 and mass 2(which are found using PSO) can be seen below.
![PSO1](https://user-images.githubusercontent.com/84566016/162335616-cdd56169-09a2-46cf-a673-aa0848fd2137.png)
