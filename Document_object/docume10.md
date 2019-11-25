## document.addNewRectangle()

#### Availability

Flash MX 2004.

#### Usage

document.addNewRectangle(boundingRectangle, roundness [, bSuppressFill [, bSuppressStroke]])

#### Parameters

**boundingRectangle** A rectangle that specifies the bounds within which the new rectangle is added, in the format
{left:value1,top:value2,right:value3,bottom:value4}. The left and top values specify the location of the upper left corner (e.g., left:0,top:0 represents the upper left corner of the Stage) and the right and bottom values specify the location of the lower-right corner. Therefore, the width of the rectangle is the difference in value between left and right, and the height of the rectangle is the difference in value between top and bottom.
In other words, the rectangle bounds do not all correspond to the values shown in the Property inspector. The left and top values correspond to the X and Y values in the Property inspector, respectively. However, the right and bottom values don’t correspond to the W and H values in the Property inspector. For example, consider a rectangle with the following bounds:
{left:10,top:10,right:50,bottom:100}
This rectangle would display the following values in the Property inspector:
X = 10, Y = 10, W = 40, H = 90
**roundness** An integer value from 0 to 999 that specifies the roundness to use for the corners. The value is specified as number of points. The greater the value, the greater the roundness.
**bSuppressFill** A Boolean value that, if set to true, causes the method to create the shape without a fill. The default value is false. This parameter is optional.
**bSuppressStroke** A Boolean value that, if set to true, causes the method to create the rectangle without a stroke**.** The default value is false. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; adds a new rectangle or rounded rectangle, fitting it into the specified bounds. This method performs the same operation as the Rectangle tool. The method uses the document’s current default stroke and fill attributes and adds the rectangle on the current frame and layer. If both *bSuppressFill* and *bSuppressStroke* are set to true, the method has no effect.

#### Example

```javascript
The following example adds a new rectangle with no rounding on the corners within the specified coordinates; it is 100 pixels in width and in height:
fl.getDocumentDOM().addNewRectangle({left:0,top:0,right:100,bottom:100},0);
The following example adds a new rectangle with no rounding on the corners and without a fill; it is 100 pixels in width and 200 in height:
fl.getDocumentDOM().addNewRectangle({left:10,top:10,right:110,bottom:210},0, true);
The following example adds a new rectangle with no rounding on the corners and without a stroke; it is 200 pixels in width and 100 in height:
fl.getDocumentDOM().addNewRectangle({left:20,top:20,right:220,bottom:120},0, false, true);

```
#### See also

[document.addNewPrimitiveRectangle()](../Document_object/documen8.md)
