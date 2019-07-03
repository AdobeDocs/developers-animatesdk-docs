## document.addNewPrimitiveRectangle()

#### Availability

Flash CS4 Professional.

#### Usage

document.addNewPrimitiveRectangle( boundingRectangle, roundness, \[, bSuppressFill \[, bSuppressStroke \]\] ))

#### Parameters

**rect** A rectangle that specifies the bounds within which the new rectangle primitive is added. For information on the format of *boundingRectangle*, see [document.addNewRectangle()](#_bookmark128).
**roundness** An integer between 0 and 999 that represents the number of points used to specify how much the corners should be rounded.
**bSuppressFill** A Boolean value that, if set to true, causes the method to create the rectangle without a fill. The default value is false. This parameter is optional.
**bSuppressStroke** A Boolean value that, if set to true, causes the method to create the rectangle without a stroke**.** The default value is false. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; adds a new rectangle primitive fitting into the specified bounds. This method performs the same operation as the Rectangle Primitive tool. The rectangle primitive uses the document's current default stroke and fill attributes and is added on the current frame and layer. If both *bSuppressFill* and *bSuppressStroke* are set to true, the method has no effect.

#### Example

```
The following example adds rectangle primitives within the specified coordinates, with and without fill and stroke, and with different amounts of roundness:
// Add a rectangle primitive with fill and stroke fl.getDocumentDOM().addNewPrimitiveRectangle({left:0,top:0,right:100,bottom:100}, 0);
// Add a rectangle primitive without a fill fl.getDocumentDOM().addNewPrimitiveRectangle({left:100,top:100,right:200,bottom:200}, 20, true);
// Add a rectangle primitive without a stroke fl.getDocumentDOM().addNewPrimitiveRectangle({left:200,top:200,right:300,bottom:300}, 50,false,true);

```
#### See also

[document.addNewRectangle()](#_bookmark128)
