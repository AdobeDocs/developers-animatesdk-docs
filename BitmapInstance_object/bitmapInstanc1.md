## bitmapInstance.hPixels

#### Availability

Flash MX 2004.

#### Usage

bitmapInstance.hPixels

#### Description

Read-only property; an integer that represents the width of the bitmap—that is, the number of pixels in the horizontal dimension.

#### Example

```javascript
The following code retrieves the width of the bitmap in pixels:
// Get the number of pixels in the horizontal dimension. var bmObj = fl.getDocumentDOM().selection\[0\];
var isBitmap = bmObj.instanceType; if(isBitmap == "bitmap"){
var numHorizontalPixels = bmObj.hPixels;
}

```
#### See also

[bitmapInstance.vPixels](#!AdobeDocs/developers-animatesdk-docs/test/BitmapInstance_object/bitmapInstanc3.md)
