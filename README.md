# cyclone-physics (for my own learning)
## @Warning.
## NOTE

 - I modified the cmake file dirty ***only for Windows*** and moved the ***64bit***  
 - If you use visual studio 2019 on window, you can build x64 with cmake. 
- In other cases (linux, ...) I have not tested.

## ParticleForceGenerator

***ParticleGravity*** : ![equation](https://latex.codecogs.com/gif.latex?F%3Dmg)\
***ParticleDrag*** : ![equation](https://latex.codecogs.com/gif.latex?F%3D-p%28%7Bk%7D_%7B1%7D%5Cleft%20%7Cp%5Cright%20%7C&plus;%7Bk%7D_%7B2%7D%7B%5Cleft%20%7Cp%5Cright%20%7C%7D%5E%7B2%7D%29)

```p is the normalized vector of currnet velocity only for the direction, $|p|$ is the magnitude```