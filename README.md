This repository contains benchmarking instances for the aircraft deconfliction problem via subliminal speed regulation (SRADP) in 3 dimensions, presented here https://doi.org/10.1007/s10898-021-00997-1.
Given a set of aircraft sharing the same airspace, the SRADP consists of minimizing the total speed changes (within specific control bounds) needed to satisfy a minimum safety distance for each pair of aircraft in a given time horizon. An important assumption is that changes occur instantaneously and that the new speeds remain constant in the time horizon. Specifically, given a constant speed for every aircraft, new optimal constant speeds satisfying the safety constraints are decided. 

The SRADP is often formulated in two-dimensional space, assuming that aircraft fly within a fixed altitude layer. For instances of SRADP in two dimension see https://github.com/ReyHijazi/Conflict_Resolution .

This repository includes the instances for SRADP in 3 dimensions (dim=3) in AMPL format.
The so called "sphere instances" are the ones in which n aircraft are placed on a sphere of given radius, with initial speed v_i and a trajectory defined by the two angles phi1 and phi2 such that aircraft fly towards the center of the sphere.
The so called "non-sphere instances" are the ones in which n aircraft move along straight trajectories with initial speed v_i, intersecting in several conflict points. 

In each .dat file :
- dim := 3 is the number of dimensions considered 
- A is the set of aircraft
- n is the number of aircraft
- radius is the radius of the sphere where the aircraft are placed (defined just for sphere instances)
- v[i] is the initial speed of aircraft i
- phi[i,1] is the initial heading angle of aircraft i with the k1-axis
- phi[i,2] is the initial heading angle of aircraft i with the k3-axis
- u[i,k] is the kth component of the initial velocity vector of aircraft i
- x0[i,k] is the kth coordinate of the initial position of aircraft i (for sphere instances defined as: -radius*u[i,k] )


