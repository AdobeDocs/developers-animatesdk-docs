## Camera Object summary

#### Availability

Animate CC.

#### Description

This object contains all the properties for Camera. It allows to simulate a real-life camera.

Animators can use the following features that are integral to any motion film.

1. Panning with the subject of the frame.

2. Zooming in the object of interest for dramatic effect

3. Zooming out of a frame to remind the viewer of a larger picture

4. Modifying the focal point to shift the attention of the viewer from one subject to another

5. Rotating the camera

6. Using color tint or filters to apply color effects on a scene 

#### Method summary

The following methods can be used with the Camera object:

| **Method**                           | **Description**                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [getZDepth()](../Camera_object/Camera.md)          | Return current Z Depth value of camera.        |
| [getZoom()](../Camera_object/Camera1.md)          | Return the current zoom value of camera. Default is 100%.               |
| [getRotation()](../Camera_object/Camera2.md)          | Return current angle of camera.               |
| [getPosition()](../Camera_object/Camera3.md)     | Return object with x,y, and z properties that specify current location of camera.                                      |
| [getTint()](../Camera_object/Camera4.md)          | Return object with two properties: ‘percent’ & ‘color’.                       |
| [getColorFilter()](../Camera_object/Camera5.md)       | Get camera color filter.                                  |
| [setZDepth()](../Camera_object/Camera6.md)       | Set camera's Z Depth value. |
| [setZoom()](../Camera_object/Camera7.md)        | Zoom camera to absolute value given by input parameter in percentage.                         |
| [setRotation()](../Camera_object/Camera8.md)     | Rotate camera by absolute angle given as input parameters.                              |
| [setTint()](../Camera_object/Camera9.md) | Set camera tint using tint color(RGB) & tint percent (percentage of tint).                    |
| [setColorFilter()](../Camera_object/Camera10.md)            | Set camera color filter using decomposed values of (Brightness,Contrast,saturation,hue).                                             |
| [resetZoom()](../Camera_object/Camera11.md)          | Reset camera zoom to it's default zoom value i.e 100%.                           |
| [resetRotation()](../Camera_object/Camera12.md)       | Reset camera angle to zero.                         |
| [resetPosition()](../Camera_object/Camera13.md)           | Reset camera position to the original position i.e (0,0,0).                                          |
| [resetTint()](../Camera_object/Camera14.md)        | Remove camera tint.                                                       |
| [resetColorFilter()](../Camera_object/Camera15.md)     | Remove color filter.                                |
| [reset()](../Camera_object/Camera16.md)    | Reset all camera properties to default.                       |

#### Property summary

The following properties can be used with the Camera object:

| **Property**                           | **Description**                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [camera.cameraEnabled](../Camera_object/Camera17.md)          |       Enables camera|
| [camera.tintEnabled](../Camera_object/Camera18.md)          |     Enables tint           |
| [camera.colorFilterEnabled](../Camera_object/Camera19.md)          |  Enables camera's color Filter               |




<span id="filter.angle" class="anchor"></span>

