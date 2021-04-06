# LudiPhys
A physics sandbox game made by LudicrousFun and inspired by Universe Sandbox 2

Game uses particles to simulate planets.

planets are a collection of particles bound together by gravity.

particles exert forces like gravity, collision, friction and 'pressure' forces.

particles have properties and thermodynamics.


# Theory

This game uses an implicit SPH implementation where particles simply apply radial forces to simulate effects. This is good as it only relies on purely emergent behaviour and does not need to be explicitly told what to do, this makes the simulation extremely easy to modify and to create. Pressure and Gravity forces large clumps of particles into a sphere, like what would happen in reality. Roche limits are done completely implicitly and rely on purely physics (difference in gravity from one side of a planet to another). Downsides is that such an SPH implementation is really difficult to optimise and thus is incredibly slow. This implementation also does not scale up to larger scales well in terms of performance.


# To-Dos

- Keybind changing
- Keybind settings
- Radioactive materials
- Compute Shaders

# Default Controls (Newest Version)

left-click and hold RMB to spawn object in specified mode.

while holding left click, scroll to change altitude.



W,S: Move forwards / backwards

A,D: Move sideways

Q,E: Move vertically relative to 'world'

Alpha 1: Reset velocities to zero

Alpha 2: Reset all temperatures to 300K

Alpha 3: Reset global momentum to zero.

Enter / Return: spawns a still particle near camera with material settings if specified.

Right Shift: Reset timestep and camera exposure

'/' : Remove all particles

'Backspace' : Remove laser light

';' and ('): Change laser power

'L' fire laser

space: pause

'Z': Toggle between Position Mode and Velocity Mode.

',' and '.': change timestep; high timesteps result in instability

scrollwheel: change camera speed

'[' and ']': changes simulation accuracy; how many interactions are actually calculated

'P': Change Material types.

'Esc': Settings Menu

'Home': Save Simulation, Saved in PhysicsSandbox1/PhysicsSandbox1Data/saves/savename.phys

'End': Load save.

'[' and ']': Controls camera exposure.


# How to load source code? (Main Branch)

Requirements: Unity 5.2.3f1, Assets, Data

1) Create a main folder for unity project.

2) Extract Asset and UnityProjDet in main folder.

3) Open Unity and open project!


# How to load source code? (Releases)

Requirements: Unity 5.4, Assets, Data

1) Extract source.zip to destination

2) Open Unity and open project!


# Changelog

28th Feb 2021: initial Conception, Just made a particle orbit the origin of the map

1st Mar: Added particle-particle interactions, created bugs and fixing them

... Missing entries ...

3rd Mar: Added thermodynamics (Conduction, shock heating, etc.) and others.

4th Mar: UI, Other settings.

5th Mar: v1.1; Added new materials, Added proper momentum and thermodynamics. 
...

# Notes

1) This is just a personal project made by some random 13 year-old.
2) This is under GNU 3.0 license, do what you want with it.
