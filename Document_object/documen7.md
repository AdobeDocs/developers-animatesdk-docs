## document.addNewPrimitiveOval()

#### Availability

Flash CS4 Professional.

#### Usage

document.addNewPrimitiveOval( boundingRectangle \[, bSpupressFill \[, bSuppressStroke \]\] ))

#### Parameters

**boundingRectangle** A rectangle that specifies the bounds within which the new oval primitive is added. For information on the format of *boundingRectangle*, see [document.addNewRectangle()](#_bookmark128).
**bSuppressFill** A Boolean value that, if set to true, causes the method to create the oval without a fill. The default value is false. This parameter is optional.
**bSuppressStroke** A Boolean value that, if set to true, causes the method to create the oval without a stroke**.** The default value is false. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; adds a new oval primitive fitting into the specified bounds. This method performs the same operation as the Oval Primitive tool. The oval primitive uses the document's current default stroke and fill attributes and is added on the current frame and layer. If both *bSuppressFill* and *bSuppressStroke* are set to true, the method has no effect.

#### Example

```
The following example adds oval primitives within the specified coordinates, with and without fill and stroke:
// Add an oval primitive with fill and stroke fl.getDocumentDOM().addNewPrimitiveOval({left:0,top:0,right:100,bottom:100});
// Add an oval primitive without a fill fl.getDocumentDOM().addNewPrimitiveOval({left:100,top:100,right:200,bottom:200}, true);
// Add an oval primitive without a stroke fl.getDocumentDOM().addNewPrimitiveOval({left:200,top:200,right:300,bottom:300},false,true);

```
#### See also

[document.addNewOval()](#_bookmark124)
