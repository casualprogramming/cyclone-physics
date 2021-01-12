# cyclone-physics (for my own learning)
## @Warning.
## NOTE

 - I modified the cmake file dirty ***only for Windows*** and moved the ***64bit***  
 - If you use visual studio 2019 on window, you can build x64 with cmake. 
- In other cases (linux, ...) I have not tested.

## ParticleForceGenerator

***ParticleGravity*** : $F=mg$\
***ParticleDrag*** : $F=-p({k}_{1}\left |p\right |+{k}_{2}{\left |p\right |}^{2})$ \
```p is the normalized vector of currnet velocity only for the direction, $|p|$ is the magnitude```