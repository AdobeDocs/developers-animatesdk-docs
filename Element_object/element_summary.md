## element summary

#### Availability

Flash MX 2004.

#### Description

Everything that appears on the Stage is of the type Element. The following code example lets you select an element:
var el = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\];

#### Method summary

The following methods are available for the Element object:

| **Method**                                          | **Description**                                                                            |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------|
| [element.getPersistentData()](#_bookmark379)        | Retrieves the value of the data specified by the ***name*** parameter.                     |
| [element.getPublishPersistentData()](#_bookmark380) | True if the specified persistent data is enable for the specified format; otherwise False. |
| [element.getTransformationPoint()](#_bookmark381)   | Gets the value of the specified element’s transformation point.                            |
| [element.hasPersistentData()](#_bookmark383)        | Determines whether the specified data has been attached to the specified element.          |
| [element.removePersistentData()](#_bookmark393)     | Removes any persistent data with the specified name that has been attached to the object.  |
| [element.setPersistentData()](#_bookmark398)        | Stores data with an element.                                                               |
| [element.setPublishPersistentData()](#_bookmark399) | Enables or disables publishing of persistent data for a specified format.                  |
| [element.setTransformationPoint()](#_bookmark400)   | Sets the position of the element’s transformation point.                                   |

#### Property summary

The following properties are available for the Element object:

| **Property**                         | **Description**                                                                                                                                           |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [element.depth](#element.depth)      | Read-only; an integer that has a value greater than 0 for the depth of the object in the view.                                                            |
| [element.elementType](#_bookmark377) | Read-only; a string that represents the type of the specified element.                                                                                    |
| [element.height](#_bookmark384)      | A float value that specifies the height of the element in pixels.                                                                                         |
| [element.layer](#_bookmark385)       | Read-only; represents the [Layer object](#_bookmark679) on which the element is located.                                                                  |
| [element.left](#_bookmark386)        | Read-only; a float value that represents the left side of the element.                                                                                    |
| [element.locked](#_bookmark388)      | A Boolean value: true if the element is locked; false otherwise.                                                                                          |
| [element.matrix](#_bookmark390)      | A [Matrix object](#_bookmark725). The matrix has properties a, b, c, d, tx, and ty. a, b, c, and d are floating- point values; tx and ty are coordinates. |
| [element.name](#_bookmark392)        | A string that specifies the name of the element, normally referred to as the Instance name.                                                               |

| **Property**                        | **Description**                                                                                                                                            |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [element.rotation](#_bookmark394)   | An integer or float value between -180 and 180 that specifies the object’s clockwise rotation, in degrees.                                                 |
| [element.scaleX](#_bookmark395)     | A float value that specifies the *x* scale value of symbols, drawing objects, and primitive rectangles and ovals.                                          |
| [element.scaleY](#_bookmark396)     | A float value that specifies the *y* scale value of symbols, drawing objects, and primitive rectangles and ovals.                                          |
| [element.selected](#_bookmark397)   | A Boolean value that specifies whether the element is selected or not.                                                                                     |
| [element.skewX](#_bookmark402)      | A float value between -180 and 180 that specifies the *x* skew value of symbols, drawing objects, and primitive rectangles and ovals.                      |
| [element.skewY](#_bookmark403)      | A float value between -180 and 180 that specifies the *y* skew value of symbols, drawing objects, and primitive rectangles and ovals.                      |
| [element.top](#_bookmark404)        | Read-only; top side of the element.                                                                                                                        |
| [element.transformX](#_bookmark406) | A floating-point number that specifies the *x* value of the selected element’s transformation point, within the coordinate system of the element's parent. |
| [element.transformY](#_bookmark407) | A floating-point number that specifies the *y* value of the selected element’s transformation point, within the coordinate system of the element's parent. |
| [element.width](#_bookmark408)      | A float value that specifies the width of the element in pixels.                                                                                           |
| [element.x](#_bookmark409)          | A float value that specifies the *x* value of the selected element’s registration point.                                                                   |
| [element.y](#_bookmark410)          | A float value that specifies the *y* value of the selected element’s registration point.                                                                   |

<span id="element.depth" class="anchor"></span>

