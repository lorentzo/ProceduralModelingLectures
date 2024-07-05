

# Structure

The structure of these materials follows:
1. Book: I. kerlow: The Art of 3D Computer Animation and Effects [here](https://www.amazon.de/-/en/Isaac-V-Kerlow/dp/0470084901)
2. Lecture: Computer Graphics: Animation and Simulation (Stanford) [here](http://graphics.stanford.edu/courses/cs348c/)
3. My knowledge and experience :)

The aim of this project: create learning materials for computer animation course.

See [wiki](https://github.com/lorentzo/ComputerAnimation/wiki) for more info.




## Course Schedule

Reading:
* [ARTCOMPANIM] I. kerlow: The Art of 3D Computer Animation and Effects
* [INTROCOMPGRAPH] L. Bosnar: https://github.com/lorentzo/IntroductionToComputerGraphics
* [STANFORDANIM] D. James: http://graphics.stanford.edu/courses/cs348c/
* [PROCMODEL] Ebert: Texturing and modeling: procedural approach
* [BOOKOFSHADERS] https://thebookofshaders.com/
* [SCRATCHAPIXEL] https://www.scratchapixel.com/index.html
* PBRT: https://pbrt.org/
* Real-time rendering book: https://www.realtimerendering.com/

### 1. Animation Pipeline

* 20% of the course time

Goals:
* Introduce animation pipeline as used in:
  * Blender Studio: https://studio.blender.org/pipeline/user-guide/project_tools/project-overview
  * Pixar: https://renderman.pixar.com/stories/pixars-usd-pipeline
* Explain CG concepts in each pipeline module (geometry, materials, lights, cameras, rendering, etc.)
* Result is a small project: project based learning, learning by doing, structuring knowledge

Pipeline:
* Editorial: idea, script, storyboard
* Modeling
  * 3D space and transformations
  * Geometry representations
  * Geometry modeling
* Rigging
* Animation
  * Keyframing: manual and procedural
  * Simulation
* Camera
  * Pinhole camera
  * DOF
* Shading: materials and textures
  * BRDF
  * Textures
* Light
  * light sources
  * Shadow
* Rendering
  * Rendering concept
  * Rasterization and raytracing
* Compositing
  * Imaging pipeline

### 1. Blender Animation Pipeline
* 40% of the course time
* 20% is animation walkthrough 
* 80% is project work with specificities

### 2. Houdini Animation Pipeline
* 40% of the course time
* 20% is animation walkthrough 
* 80% is project work with specificities

# Course Concepts

In this course following concepts are aimed to be introduced.

### 1. Computer Animation Introduction

Description: give examples which show structure and that there is no structure. Everyting that is done and that can be done. Community, software, conferences, books, etc.

Note: although computer animation, this course focuses on methods for motion graphics (aka environment animation, props animation) and brings practical knowledge and skills.

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
* Conferences, software for animation
  * https://www.sidefx.com/learn/talks/
* Course Structure 

### 2. Computer Graphics Concepts

Description: idea is to show how computer graphics concepts can be used to obtain desired shapes, colors and animations. Understanding the concept. Understanding how to use it in Blender/Houdini. Intuitive understanding of implementation.

##### 3D scene modeling -- [INTROCOMPGRAPH]
1. 3D scene, transformations
    * Animating with transformations
    * Importance of local and world space and transformation matrices

2. 3D models: geometry and material -- [ARTCOMPANIM ch 3,4,5]
    * Animating with geometry representations
      * Curves: https://www.youtube.com/watch?v=CSre9wCJoWc&ab_channel=AlbertoCordero
      * Mballs: https://www.youtube.com/watch?v=rIhXHSdMWmc&ab_channel=CGPython and [this](https://www.youtube.com/watch?v=syvhbxPE3zI&t=1s&ab_channel=JoshGambrell)
      * Meshes: subdivision, displacement, boolean, remeshing
    * Animating material
      * Surfaces:
        * metals: highly reflective, colored reflection, surface imperfections
          * specular reflection: colors, roughness and normals animation
        * dielectrics: reflective and refractive; opaque, transmission, SSS
          * diffuse and glossy: Color, refraction, transmission animation
        * emission animation
        * texture animation
      * Volumes: density and emission animation using textures

3. Cameras -- [ARTCOMPANIM ch 7]
    * Animating cameras transformations with curves
    * Animating camera rotations with curves
    * Animating camera shaking
    * Animating camera properties: DOF

4. Lights -- [ARTCOMPANIM ch 8]
    * Animating light transformations
    * Animating light emission (blinking, pulsing, etc.)

##### Rendering -- [INTROCOMPGRAPH]
1. Rendering concepts -- [ARTCOMPANIM ch 6, 9]
    * shadows
    * interreflections
    * transmissions
2. Ray-tracing-based rendering
    * Cycles, denoising
    * noise art
3. Rasterization-based rendering
    * bloom, speed
##### Image, display and post-processing -- [INTROCOMPGRAPH], [ARTCOMPANIM ch 14, 15]

1. Compositing 
    * image processing
    * Colors
2. Video editing

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

Description: idea is to show how physical simulations can help for procedural animation and motion graphics. Understanding the concept of simulation. Understanding parameters of simulation (e.g., mass, viscosity, etc.) Understanding how to use it in Blender/Houdini. Intuitive understanding of implementation. Each simulation is presented through an example. Task for students is to reuse the concept on their own animation idea.

Concept: physics simulation can be seen as constrained movement of environment, a reaction to animated (manual or procedural) movement. For example, if we procedurally code random movement of objects, we would like that they collide and behave as rigid body. Another example is we animate boat movement then we want for water to react to the boat. 

Concept: just like rendering uses material information based on geometric optics for appearance computation, physically-based animation takes material information based on classical dynamics for motion behaviour computation.

Looking into physics books would give better idea of how those methods work: https://www.feynmanlectures.caltech.edu/

Nice paper explaining one approach of implementing unified physics: https://mmacklin.com/uppfrta_preprint.pdf
 
* Rigid body dynamics
  * Example: marble dynamics: https://blenderartists.org/t/3d-marble-race-wooden-miniature-town/1477845 (by analnluk)
* Soft body dynamics
* Cloth dynamics
* Hair dynamics
* Fluid simulation: liquids
* Fluid simulation: gas
  * Example: https://www.youtube.com/watch?v=zyIJQHlFQs0&ab_channel=Polyfjord

Interesting ideas:
* https://www.youtube.com/watch?v=5MHglJHYD50&ab_channel=SouthernShotty
  
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