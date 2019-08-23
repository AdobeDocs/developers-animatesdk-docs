## document.addNewOval()

#### Availability

Flash MX 2004.

#### Usage

document.addNewOval(boundingRectangle \[, bSuppressFill \[, bSuppressStroke \]\])

#### Parameters

**boundingRectangle** A rectangle that specifies the bounds of the oval to be added. For information on the format of
*boundingRectangle*, see [document.addNewRectangle()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docume10.md).
**bSuppressFill** A Boolean value that, if set to true, causes the method to create the shape without a fill. The default value is false. This parameter is optional.
**bSuppressStroke** A Boolean value that, if set to true, causes the method to create the shape without a stroke. The default value is false. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; adds a new Oval object in the specified bounding rectangle. This method performs the same operation as the Oval tool. The method uses the document’s current default stroke and fill attributes and adds the oval on the current frame and layer. If both *bSuppressFill* and *bSuppressStroke* are set to true, the method has no effect.

#### Example

```javascript
The following example adds a new oval within the specified coordinates; it is 164 pixels in width and 178 pixels in height:
fl.getDocumentDOM().addNewOval({left:72,top:50,right:236,bottom:228});
The following example draws the oval without a fill: fl.getDocumentDOM().addNewOval({left:72,top:50,right:236,bottom:228}, true); The following example draws the oval without a stroke:
fl.getDocumentDOM().addNewOval({left:72,top:50,right:236,bottom:228}, false, true);

```
#### See also

[document.addNewPrimitiveOval()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/documen7.md))

<span id="document.addNewPrimitiveOval()" class="anchor"></span>
