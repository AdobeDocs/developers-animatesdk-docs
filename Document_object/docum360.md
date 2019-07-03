## document.rotateSelection()

#### Availability

Flash MX 2004.

#### Usage

document.rotateSelection(angle \[, rotationPoint\])

#### Parameters

**angle** A floating-point value that specifies the angle of the rotation.
>
**rotationPoint** A string that specifies which side of the bounding box to rotate. Acceptable values are "top right", "top left", "bottom right", "bottom left", "top center", "right center", "bottom center", and "left center". If unspecified, the method uses the transformation point. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; rotates the selection by a specified number of degrees. The effect is the same as using the Free Transform tool to rotate the object.

#### Example

```
The following example rotates the selection by 45º around the transformation point:
fl.getDocumentDOM().rotateSelection(45);
The following example rotates the selection by 45º around the lower-left corner:
fl.getDocumentDOM().rotateSelection(45, "bottom left");

```