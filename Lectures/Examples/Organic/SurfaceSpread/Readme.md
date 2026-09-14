
Ensure that current network is obj/.

Create geometry node inside obj/ network.

Enter geometry network.

Create Font node:

![](StepByStepGuide/1_font_node.JPG)

* Inside Text field type "H". CTRL + S to save.
* Set vertical alignment to Bottom.

Result:

![](StepByStepGuide/1_font_node_scene.JPG)

Create Poly Bevel node and connect Font node to it:

![](StepByStepGuide/2_PolyExtrudeNode.JPG)

* Set Distance to 0.25
* Set Output Back (Extrusion -> Output Geometry and Group)

Result:

![](StepByStepGuide/2_PolyExtrudeNode_Result.JPG)

Create Remesh To Grid node and connect Poly Extrude node with it:

![](StepByStepGuide/3_RemeshGridNode.JPG)

* Set division Size to 0.01

Result:

![](StepByStepGuide/3_RemeshGridNode_Result.JPG)

Create Group Node and connect Remesh To Grid node with it:

![](StepByStepGuide/4_GroupNodeStartPoints.JPG)

* Set Group type to Points
* Set Group name to "start_points"
* Deselect Base Group
* Select Keep in Bounding Regions
* Position Bounding box to select few points

![](StepByStepGuide/4_GroupNodeStartPoints_Result.JPG)

Create Distancy Along Geometry node and connect Group node with it:

![](StepByStepGuide/5_DistanceAlongGeoNode.JPG)

* In Start Points set "start_points"

Result: 

![](StepByStepGuide/5_DistanceAlongGeoNode_Result.JPG)

Note: dist attribute is visualized, violet are small values, red are large values.

Create Attribute Remap Node and connect Distancy Along Geometry node to it:

![](StepByStepGuide/6_AttrRemapNode.JPG)

* Set original name to "dist"
* Set new name to "dist"
* Click Compute Range
* Set value of 1st ramp point to 0
* Set value of 2nd ramp point to 1
* Animate position of 2nd ramp point

![](StepByStepGuide/6_AttrRemapNode_Result.JPG)

Create Attribute Noise node and Attribute Wrangle node and connect them as follows:

![](StepByStepGuide/7_NoiseAttrWrangleScale.JPG)

Inside Attribute Noise node:
* Set Attribute names to Float and noise
* Adjust Amplitude
* Adjust Element size

Inside Attribute Wrangle node:
* type: f@pscale = @dist * @noise;

![](StepByStepGuide/7_NoiseAttrWrangleScale_Result.JPG)

Create Scatter Node, Normal Node and Attribute transfer node and connect as follows:

![](StepByStepGuide/8_ScatterNormalAttribTransfer.JPG)

Inside Normal node:
* Ensure: Add Normals to Points 

Result:

![](StepByStepGuide/8_ScatterNormalAttribTransfer_Result.JPG)

Create Attribute Randomize node and Attribute Adjust Color Node and connect as follows:

![](StepByStepGuide/9_AttrNormalRandomizeColorNodes.JPG)

Inside Attribute Randomize Node:
* Set Attribute Name to: "N"
* Set Operation to "Add Value"
* Set Distribution to "Inside Sphere"

Inside Attribute Adjust color Node:
* Set Attribute name to "Cd"
* Set Pattern Type to "Noise"
* Set desired colors in Color Ramp

Result: 

![](StepByStepGuide/9_AttrNormalRandomizeColorNodes_Result.JPG)

Create GLTF Node, PolyReduce Node, Transform Node and Copy to points Node and connect them as follows:

![](StepByStepGuide/10_CopyToPointsNode.JPG)

Inside GLTF Node:
* Set desired File Name
* Set Load by Mesh
* Select desired Mesh ID
* Set points merge distance to 0

Inside Poly Reduce node:
* Set percent to keep to 10%

Inside Transform Node:
* Set X Rotation 90deg

Create Merge Node and connect as follows:

![](StepByStepGuide/11_MergeNode.JPG)

Result:

![](StepByStepGuide/11_MergeNode_Result.JPG)

Create VDB From Polygons, Scatter, Connect Adjecent Pieces and Attribute Adjust color as follows:

![](StepByStepGuide/12_VDBScatterConnectPointsNodes.JPG)

Inside VDB From Polygons Node:
* Deselect Distance VDB
* Select Fog VDB

Inside Connect Adjecent Pieces Node:
* Set Connection Type to Adjecent Points
* Set Max Search Points to 4

Inside Attribute Adjust Color:
* Set Attribute name to "Cd"
* Set Pattern Type to "Noise"
* Set desired colors in Color Ramp

Result:

![](StepByStepGuide/12_VDBScatterConnectPointsNodes_Result.JPG)

Additional masks are created similarly and used for instancing:

![](StepByStepGuide/13_AdditionalMaskInstances.JPG)

Note similar setup except:
* Here we are using Distance From Geometry with animated sphere as reference geometry

Result:

![](StepByStepGuide/13_AdditionalMaskInstances_Result.JPG)