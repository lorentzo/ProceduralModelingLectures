# Procedural Animation Lectures

Work in progres!

# About

Lectures in procedural modeling.

Lectures aim:
* Give a structure of the procedural modeling field
* Theoretical and practical tools for procedural modeling
* Conceptual understanding of procedural modeling building blocks

Applications:
* Game worlds (environments, foliage, natural phenomena)
* Animation worlds
* VFX
* Motion graphics
* Generative Art
* Botany and plants
* Visualization
* Arhitecture
* Algorithmic design

Lectures approach:
* Learning concepts, approaches and method by doing
* Using Blender (https://www.blender.org/) and Houdini (https://www.sidefx.com/)


# Lecture topics

### Lecture 1: intro

* Start with interactive example!
* Introduction, motivation: why procedural modeling?
* Big picture: procedural modeling, generative art, generative design, algorithmic art, etc.
* Procedural modeling in computer graphics and animation
* Lectures overview

### Lecture 2: procedural hard surface modeling

* Procedural modeling of hard-surface (man made) shapes 

### Lecture 2: procedural terrains

Topics:
* Introducing noise types (Perlin, Worley, flow and other derivations)
* Noise layering (fractal sum, fbm) and warping
* Noise for geometric displacement
* Geometry attributes for instancing
* Instancing

Introduced concepts:
* Noise
* Displacement
* Geometry attributes/data and materials
* Instancing and transformations (rotations, scaling, translation)
* Instancing and masked surface sampling
* Surface and volume generation
* Heightfields

My work:
* https://github.com/lorentzo/HoudiniProceduralTerrain

R&D:
* 

Practical:
* https://www.sidefx.com/tutorials/procedurally-generating-and-rendering-lowpoly-terrain/

### Lecture 3: procedural buildings

Topics:
* Structure and scattering
* Props placement
* Interactive parameters

Introduced concepts:
* Structured proceduralism
* Parameters

My work: 
* https://github.com/lorentzo/ProceduralBuildings

R&D: 
* https://graphics.pixar.com/library/ElementalSets/paper.pdf

Practical: 
* https://www.youtube.com/watch?v=uIe97023sDk

### Lecture 4: procedural abstract growth

Topics:
* Animated noise
* Animated geometry displacement
* Feedback loop and simulation

Introduced concepts:
* Morphing: transformations and generation of geometry
* Animating geometry attributes
* Feedback loop animation
* Iterative proportional mesh extrusions
* Eden model

My work: 
* https://github.com/lorentzo/HoudiniAnimation?tab=readme-ov-file#morph

R&D:
* https://inconvergent.net/2016/shepherding-random-growth/
* Digital morphogenesis: https://en.wikipedia.org/wiki/Digital_morphogenesis
  * Complex shape development
  * Biology, Geology, Geomorphology and arhitecture

Practical:
* https://entagma.com/tag/growth/

### Lectur 5: procedural plant and branching structures

* SCA
* L-Systems
* DLA

### Lecture 5: procedural spread

Topics:
* surface spread
* volume spread
* Plants spread
* particles

Introduced concepts:
* Spread over surface
* Animated geometry spread attributes
* surface particles

My work:
* https://github.com/lorentzo/HoudiniAnimation?tab=readme-ov-file#spreadgrowth

R&D:
* https://docs.blender.org/manual/en/latest/addons/mesh/tissue.html

Practical:
* https://www.youtube.com/watch?v=b-DDdGcvBaI

### Lecture 6: procedural particle motion

Topics:
* noise as vector field
* particles and vector fields
* flying leafs, snow

Introduced concepts:
* Vector fields
* Particle motion
* Guiding particles via vector fields
* instancing on particles

My work: 
* https://github.com/lorentzo/HoudiniAnimation?tab=readme-ov-file#treewind
* https://www.artstation.com/artwork/LRwEoA

R&D:
* 

Practical:
* https://www.sidefx.com/learn/collections/applied-houdini-particles/

### Lecture 7: procedurally guided physically-based dynamics

Topics:
* Cracking and breaking with RBD
* Explosions
* Water splashes
* physically-based natural phenomena

* solids
  * rigid
  * soft
* fluids
  * liquids
  * gases

* Procedural constraints and forces and physically-based solvers

# Covered concepts

Types of modeled phenomena:
* Abstract vs regular/structured
* Nature vs human-made
* Organic vs hard-surface

Procedural animation methods:
* Physically-based approaches
  * classical mechanics, forces and constraints
    * fluids: gases and liquids
    * solids: rigid bodies and soft bodies
* Biological simulation
  * Surface/Volume Growth
  * Surface/Volume Spread modeling
  * Branching (recursion)
    * Trees
    * Roots
  * Reaction, Reaction-diffusion
  * Digital Morphogenesis
  * Phenomenological simulation
* Mathematics:
  * Iterative systems and chaos
  * Cells and automation
* Empirical CG
  * Procedural noise, layering and warping
  * L-Systems
  * Boids 
  * Geometric instancing (including arraying)
  * Particles and force fields

CG methods:
* 3D scene: lights, cameras, materials and shapes (meshes, voxles, curves, etc.)
* Rendering: GPU raster, CPU path-tracing
* Post-processing

Literature:
* [STANFORDANIM] D. James: http://graphics.stanford.edu/courses/cs348c/
* [PROCMODEL] Ebert: Texturing and modeling: procedural approach
* [HORIKAWA] J. Horikawa: https://www.youtube.com/watch?app=desktop&v=rj0dEEVU1Ek&ab_channel=Houdini
  * https://jhorikawa.gumroad.com/l/GOZFw
* [NATUREOFCODE] https://natureofcode.com/

