# Computer Animation

Work in progres...

## About

Learning material for computer animation:
* Animation for Film
* Animation for Games
* VFX
* Motion graphics/design
* Procedural, generative and math animation
* Environment animation (e.g., non-character animation)
  * foliage animation
  * plants animation
  * animating natural phenomena
* Physically based animation
  * fluid animation
  * rigid body animation
  * soft body animation
* Organic animation
* Traditional animation, e.g, hand-drawing or stop-motion animation
* Stylized modeling, rendering and compositing

The aim of these materials:
* Give a map of computer animation
* Teach theoretical background of animation
* Give practical tools and methods for animating

Currently, it is not the aim to give low-level implementation of data-structures and algorithms for animation, rather conceptual understanding of those and using higher-level tools which implement and provide those as well as understanding their parameters and application.

## Structure

The structure of these materials follows:
1. Book: I. kerlow: The Art of 3D Computer Animation and Effects [here](https://www.amazon.de/-/en/Isaac-V-Kerlow/dp/0470084901)
2. Lecture: Computer Graphics: Animation and Simulation (Stanford) [here](http://graphics.stanford.edu/courses/cs348c/)
3. My knowledge and experience :)

The aim of this project: create learning materials for computer animation course.

See [wiki](https://github.com/lorentzo/ComputerAnimation/wiki) for more info.

## Software

* [Blender](https://www.blender.org/)
* [Houdini](https://www.sidefx.com/)

Using [Obsidian](https://obsidian.md/) for organization.


## Course Schedule

Reading:
* [ARTCOMPANIM] I. kerlow: The Art of 3D Computer Animation and Effects
* [INTROCOMPGRAPH] L. Bosnar: https://github.com/lorentzo/IntroductionToComputerGraphics
* [STANFORDANIM] D. James: http://graphics.stanford.edu/courses/cs348c/
* [PROCMODEL] Ebert: Texturing and modeling: procedural approach
* [BOOKOFSHADERS] https://thebookofshaders.com/
* [SCRATCHAPIXEL] https://www.scratchapixel.com/index.html

### 1. Computer Animation Introduction
* Motivation and Examples -- [ARTCOMPANIM, ch 1], [ARTCOMPANIM ch 13]
  * History
  * Present
  * Future
  * Animated film
  * VFX
  * Animation for games
* Animation Production Pipeline -- [ARTCOMPANIM, ch 2, 10]
  * Pre-production 
    * Storytelling
    * Visual and look dev
    * Characters and environments development
  * Production and creative process
    * Modeling, Lighting, Camera, Animation, Render
  * Post-production
    * Editing, post-processing
* Animation applications
  * How is computer animation applied in: games, VFX, animated film
* Course Structure 

### 2. Computer Graphics Concepts
* 3D scene modeling -- [INTROCOMPGRAPH]
  * 3D scene, transformations
  * 3D models: geometry and material -- [ARTCOMPANIM ch 3,4,5]
  * Cameras -- [ARTCOMPANIM ch 7]
  * Lights -- [ARTCOMPANIM ch 8]
* Rendering -- [INTROCOMPGRAPH]
  * Rendering concepts -- [ARTCOMPANIM ch 6, 9]
  * Ray-tracing-based rendering
  * Rasterization-based rendering
* Image, display and post-processing -- [INTROCOMPGRAPH], [ARTCOMPANIM ch 14, 15]

### 3. Computer Animation Concepts
Reading: [ARTCOMPANIM ch 11, 12]
* Traditional animation
* Principles of animation
* Keyframes and interpolation
* Model, Light and Camera animation
  * Position, orientation, scale and shape animation  

### 4. Procedural Animation
Reading: [ARTCOMPANIM ch 12], [STANFORDANIM]

#### Foundations
* Geometry Transformations: translation, rotation and scaling using forward kinematics and inverse kinematics.
* Geometry Deformation: rotation and translation of vertices.

#### Procedural approaches
* Empirical animation concept: animating what we see, not necessary physically correct
* Procedural noise [PROCMODEL], [BOOKOFSHADERS], [SCRATCHAPIXEL]: concept, code:
  * Value and Perlin/Gradient noise
  * Worley (cellular) noise
  * Fractal noise sum (layering noise concept); fBM; Turbulence
  * Warping
  * Applying color ramp.
  * Animation with coordinate transformation or time input
  * Example as surface texture: color, bump and roughness variation
  * Example as geometry deformation: displacement
* Growth models: 
  * Basic scaling
  * Proportional editing
  * SCA, DLA, Eden model, etc.
* L-systems
* Crowds and flocking
* Stochastic geometry concepts
* Scene graph instancing
* Hybrid animation concept: manual supported by procedural
  * Drawing and generating

### 5. Physically-based animation
* Rigid body dynamics
* Soft body dynamics
* Cloth dynamics
* Hair dynamics
* Fluid simulation: liquids
* Fluid simulation: gas
  
### 6. Motion Graphics Applications
* Cable tool: https://www.sidefx.com/tutorials/project-titan-cable-tool/
* Manual and procedural approaches for motion graphics
  * Curves
  * Modifiers
  * Python API
  * Geometry/simulation nodes
  * Simulation
* Literature:
  * 5 ways to motion graphics: https://www.youtube.com/watch?v=EdNwfKW1umU
  * 7 ways to motion graphics: https://www.youtube.com/watch?v=1aYh0cKi960
  * Blender Studio motion graphics: https://studio.blender.org/training/motion-graphics/chapter/top-motion-graphics/
  * Real-time motion graphics: https://blendermarket.com/products/rtmg/docs
  * Intro to motion graphics: https://blendermarket.com/products/intro-to-motion-graphics-blender-course