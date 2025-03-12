
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



