# Step-by-step guide

Main steps will be explained here, for extended version see .HIP file.

Create a project: File -> New Project.

Save Houdini file (.HIP) file inside the project: File -> Save As.

Ensure that `Build` desktop is selected (default). The following window panes should be visible: `obj/` scene view, `obj/` network view, network parameter view.

Inside `obj/` network create `geometry` network node and name it "geo".

Double click created `geometry` network node `geo/` to enter `obj/geo/` network. Note: scene view will also automatically switch to `obj/geo/` network.

![](Images/Tutorial/Start.JPG)

All the following steps are done in `obj/geo/` network, also known as geometry network with SOP (surface operator) nodes.

### Complete Terrain network

Overview of complete network. Each step is explained below.

![](Images/Tutorial/CompleteNetwork.JPG)

### General terrain geometry

Overview:

![](Images/Tutorial/TerrainGeometry.JPG)

Explanation for each node follows.

Create `Grid` node, select and set parameters:
* Size: 10, 10
* Rows: 2
* Columns: 2

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Grid1.JPG)  |  ![](Images/Tutorial/Grid1Result.JPG)

Create `Remesh` node, select and set parameters:
* Element Sizing -> Target Size: 0.1

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Remesh1.JPG)  |  ![](Images/Tutorial/Remesh1Result.JPG)

Create `Attribute Noise` node, select and set parameters:
* General -> Attribute Names -> Vector -> P
* General -> Check "Noise Along Vector"
* Noise Value -> Range Values: Positive
* Noise Value -> Amplitude
* Noise Pattern Type -> Noise Type
* Noise Pattern Type -> Element Size
* Noise Pattern Type -> Fractal -> Fractal Type
* Noise Pattern Type -> Fractal: set other parameters to desired value

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/AttributeNoise1.JPG)  |  ![](Images/Tutorial/AttributeNoise1Result.JPG)

### Terrain groups

Result of final node above (Attribute Noise), connect with following network:

![](Images/Tutorial/TerrainGeometryGroups.JPG)

Explanation for each node follows.

Create `Group` node, select and set parameters:
* Group Name: "sand"
* Base Group: deselect "Enable" checkbox
* Keep in Bounding Regions: select "Enable" checkbox
* Keep in Bounding Regions -> Size X: ch("../grid1/sizex") (Copy parameter from Grid node Size X and use paste relative references)
* Keep in Bounding Regions -> Size Z: ch("../grid1/sizey") (Copy parameter from Grid node Size Y and use paste relative references)
* Keep in Bounding Regions -> Center Y: ch("sizey")/2 (Copy parameter from Bounding Regions -> Size Y and use paste relative references)
* Keep in Bounding Regions -> Size Y: set to desired height, e.g., 0.6, depending on amplitude set in `Attribute Noise` node

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Group1.JPG)  |  ![](Images/Tutorial/Group1Result.JPG)

Create `Group` node, select and set parameters:
* Group Name: "grass"
* Base Group: deselect "Enable" checkbox
* Keep in Bounding Regions: select "Enable" checkbox
* Keep in Bounding Regions -> Size X: ch("../grid1/sizex") (Copy parameter from Grid node Size X and use paste relative references)
* Keep in Bounding Regions -> Size Z: ch("../grid1/sizey") (Copy parameter from Grid node Size Y and use paste relative references)
* Keep in Bounding Regions -> Center Y: ch("sizey")/2 (Copy parameter from Bounding Regions -> Size Y and use paste relative references)
* Keep in Bounding Regions -> Size Y: set to desired height, e.g., 1.2, depending on amplitude set in `Attribute Noise` node

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Group2.JPG)  |  ![](Images/Tutorial/Group2Result.JPG)

Create `Group Combine` node, select and set paramters:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/GroupCombine1.JPG)  |  ![](Images/Tutorial/GroupCombine1Result.JPG)

Create `Group` node, select and set parameters:
* Group Name: "forest"
* Base Group: deselect "Enable" checkbox
* Keep in Bounding Regions: select "Enable" checkbox
* Keep in Bounding Regions -> Size X: ch("../grid1/sizex") (Copy parameter from Grid node Size X and use paste relative references)
* Keep in Bounding Regions -> Size Z: ch("../grid1/sizey") (Copy parameter from Grid node Size Y and use paste relative references)
* Keep in Bounding Regions -> Center Y: ch("sizey")/2 (Copy parameter from Bounding Regions -> Size Y and use paste relative references)
* Keep in Bounding Regions -> Size Y: set to desired height, e.g., 1.7, depending on amplitude set in `Attribute Noise` node

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Group3.JPG)  |  ![](Images/Tutorial/Group3Result.JPG)

Create `Group Combine` node, select and set paramters:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/GroupCombine2.JPG)  |  ![](Images/Tutorial/GroupCombine2Result.JPG)

Create `Group` node, select and set parameters:
* Group Name: "stone"
* Base Group: deselect "Enable" checkbox
* Keep in Bounding Regions: select "Enable" checkbox
* Keep in Bounding Regions -> Size X: ch("../grid1/sizex") (Copy parameter from Grid node Size X and use paste relative references)
* Keep in Bounding Regions -> Size Z: ch("../grid1/sizey") (Copy parameter from Grid node Size Y and use paste relative references)
* Keep in Bounding Regions -> Center Y: ch("sizey")/2 (Copy parameter from Bounding Regions -> Size Y and use paste relative references)
* Keep in Bounding Regions -> Size Y: set to desired height, e.g., 3, depending on amplitude set in `Attribute Noise` node

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Group4.JPG)  |  ![](Images/Tutorial/Group4Result.JPG)

Create `Group Combine` node, select and set paramters:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/GroupCombine3.JPG)  |  ![](Images/Tutorial/GroupCombine3Result.JPG)


### Terrain color

Result of final node above (Group combine), connect with following network:

![](Images/Tutorial/TerrainGeometryGroupsColor.JPG)

Explanation for each node follows.

Create `Color` node, select and set paramters:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Color1.JPG)  |  ![](Images/Tutorial/Color1Result.JPG)

Create `Color` node, select and set paramters:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Color2.JPG)  |  ![](Images/Tutorial/Color2Result.JPG)

Create `Color` node, select and set paramters:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Color3.JPG)  |  ![](Images/Tutorial/Color3Result.JPG)

Create `Color` node, select and set paramters:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Color4.JPG)  |  ![](Images/Tutorial/Color4Result.JPG)

Create `Attribute Blur` node, select and set paramters:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/AttributeBlur1.JPG)  |  ![](Images/Tutorial/AttributeBlur1Result.JPG)


### Water plane

Network overview:

![](Images/Tutorial/Water.JPG)

Explanation for each node follows.

Create `Grid` node, select and set paramters:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Grid2.JPG)  |  ![](Images/Tutorial/Grid2Result.JPG)

Create `Transform` node, select and set paramters:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Transform1.JPG)  |  ![](Images/Tutorial/Transform1Result.JPG)

Create `Attribute Noise` node, select and set paramters:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/AttributeNoise2.JPG)  |  ![](Images/Tutorial/AttributeNoise2Result.JPG)

Create `Smooth` node, select and set paramters:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Smooth1.JPG)  |  ![](Images/Tutorial/Smooth1Result.JPG)

Create `Attribute Adjust Color` node, select and set paramters:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/AttributeAdjustColor1.JPG)  |  ![](Images/Tutorial/AttributeAdjustColor1Result.JPG)

Create `Merge` node and connect result of water plane and terrain geometry:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Merge2.JPG)  |  ![](Images/Tutorial/Merge2Result.JPG)


### Instancing

Connect the result of terrain network to scatter node in following network:

![](Images/Tutorial/Instancing.JPG)

Explanation for each node follows.

Create `Scatter` node, select and set paramters:
* Group: forest
* Force Total Count: 500

The result of terrain geometry with groups and colors connect to the input of scatter node.

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Scatter1.JPG)  |  ![](Images/Tutorial/Scatter1Result.JPG)

Create `Attribute Randomize` node, select and set paramters:
* Attribute name: `pscale`
* Distribution -> Min Value: 0.1
* Distribution -> Max Value: 0.2

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/AttributeRandomize1.JPG)  |  ![](Images/Tutorial/Scatter1Result.JPG)

Create `Attribute Randomize` node, select and set paramters:
* Attribute name: `Cd`
* Distribution -> Min Value: 0, 0.1, 0
* Distribution -> Max Value: 0.1, 0.3, 0.1

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/AttributeRandomize2.JPG)  |  ![](Images/Tutorial/Scatter1Result.JPG)

Create `Copy To Points` node, select and set paramters:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/CopyToPoints1.JPG)  |  ![](Images/Tutorial/CopyToPoints1Result.JPG)

Any kind of geometry can be inputted to `Copy To Points` node.

Create `Merge` node and connect result of copy to points node and terrain geometry with water plane:

Parameters             |  Result
:-------------------------:|:-------------------------:
![](Images/Tutorial/Merge3.JPG)  |  ![](Images/Tutorial/Merge3Result.JPG)

Same approach can be used to add different types on trees on different parts of terrain, e.g., on grass group.