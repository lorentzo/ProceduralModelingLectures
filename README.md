# Procedural Modeling Lectures

Work in progress!

# About

Lectures in procedural modeling.

Lectures aim:
* Give a structure of the procedural modeling field
* Theoretical and practical tools for procedural modeling
* Conceptual understanding of procedural modeling building blocks

Applications:
* Game development
* Animated films
* VFX
* Motion graphics
* Generative/algorithmical Art
* Botany and plants
* Visualization
* Arhitecture
* Algorithmic design

Approach used in this lectures:
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

Topics:
* Procedural modeling of hard-surface (man made) shapes 
* Mesh-based geometry manipulation
* Tools for geometry manipulation

Covered concepts:
* Geometry: vertices, edges, faces and points
* Procedural mesh manipulation
* Parameterized geometry

My work:
* https://www.artstation.com/artwork/KO1bvG
* https://www.artstation.com/artwork/EvyJoA

R&D:
* https://docs.blender.org/manual/en/latest/modeling/index.html

Practical:
* https://www.sidefx.com/learn/collections/modeling-tools/
* https://www.sidefx.com/tutorials/houdini-modelling-tutorial-175-houdini-hard-surface-modelling-tutorial/
* https://www.sidefx.com/tutorials/foundations-overview/

### Lecture 3: procedural terrains

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
* http://www.cs.princeton.edu/courses/archive/fall16/cos526/papers/smelik14.pdf

Practical:
* https://www.sidefx.com/tutorials/procedurally-generating-and-rendering-lowpoly-terrain/
* https://www.sidefx.com/tutorials/foundations-terrain/

### Lecture 4: procedural buildings

Topics:
* Structure and scattering
* Props placement
* Interactive parameters

Introduced concepts:
* Structured proceduralism
* Parameterized control
* Props blocking and instancing

My work: 
* https://github.com/lorentzo/ProceduralBuildings

R&D: 
* https://graphics.pixar.com/library/ElementalSets/paper.pdf

Practical: 
* https://www.youtube.com/watch?v=uIe97023sDk
* https://www.sidefx.com/tutorials/houdini-sci-fi-buildings/
* extension to cities: https://www.sidefx.com/tutorials/foundations-build-a-city-with-pdg/

### Lecture 5: procedural abstract growth and organic modeling

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

### Lectur 6: procedural plant and branching structures

Topics:
* Natural shapes
* Brancing structures

Introduced concepts:
* SCA
* L-Systems
* DLA

My work: 
* https://www.artstation.com/artwork/8wYyYm
* https://www.artstation.com/artwork/EvNkaK

R&D:
* http://algorithmicbotany.org/papers/colonization.egwnp2007.pdf
* https://graphics.pixar.com/library/ElementalEarth/paper.pdf

Practical:
* https://www.sidefx.com/docs/houdini/nodes/sop/lsystem
* https://www.youtube.com/watch?v=0vE8GiXhOWM
* https://www.youtube.com/watch?v=CgxTCpUqp5Q

### Lecture 7: procedural spread

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

### Lecture 8: procedural vector fields and particles

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
* https://www.artstation.com/artwork/lRdzAJ

R&D:
* 

Practical:
* https://www.sidefx.com/learn/collections/applied-houdini-particles/

### Lecture 9: proceduralism and dynamics: cracking and RBD

Topics:
* Cracking of solid objects
* Motion of solid objects before and after cracking
* Cracking caused by fall or hit

Introduced concepts:
* procedurally guided physically-based dynamics
* Procedural cracking
* RBD solvers

R&D:
* https://docs.blender.org/manual/en/latest/addons/object/cell_fracture.html
* https://dl.acm.org/doi/pdf/10.1145/2556700.2556713?casa_token=9i_sM2Dud3wAAAAA:N5XFUTjcGkPoqWebxFAOwVgOPiLx8l8qJ6QcPNzaGgYC-nmH-8mtR9Z2qF9yTnMn4Tu68DTGvTc

Practical:
* https://www.youtube.com/watch?v=IHYelaEFmr8
* https://www.sidefx.com/tutorials/smashing-wine-glass/

### Lecture 10: proceduralism and dynamics: soft bodies

Topics:
* cloth and soft object manipulation
* procedural vector fields

Introduced concepts:
* Proceduralism as force applied on soft bodies
* Soft bodies solvers.

My work:
* NA

R&D:
* https://matthias-research.github.io/pages/publications/posBasedDyn.pdf

Practicals:
* https://www.sidefx.com/docs/houdini/vellum/index.html

### Lecture 11: proceduralism and dynamics: liquids

Topics:
* water simulation 
* procedural solid body manipulation

Introduced concepts:
* Physically-based liquid solvers
* Proceduralism as force

My work:
* NA

R&D:
* https://mmacklin.com/pbf_sig_preprint.pdf
* https://graphics.pixar.com/library/ElementalWater/paper.pdf

Practicals:
* https://entagma.com/tag/fluid/

### Lecture 12: proceduralism and dynamics: volumes and gases

Topics:
* gas and volume simulation 
* procedural forces

Introduced concepts:
* Physically-based gas solvers
* Proceduralism as force
* Procedural constraints and forces and physically-based solvers

My work:
* NA

R&D:
* https://graphics.pixar.com/library/ElementalAir/paper.pdf

Practicals:
* https://entagma.com/tag/fluid/

### Lecture 13: proceduralism and dynamics: fire and smoke

Topics:
* fire simulation and spread
* procedural forces

Introduced concepts:
* Physically-based fire simulation
* Proceduralism as force

My work:
* NA

R&D:
* https://graphics.pixar.com/library/ElementalFire/paper.pdf

Practicals:
* https://www.youtube.com/watch?v=zyIJQHlFQs0


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
* [PIXAR] https://graphics.pixar.com/library/

