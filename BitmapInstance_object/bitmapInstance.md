## bitmapInstance.getBits()

#### Availability

Flash MX 2004.

#### Usage

bitmapInstance.getBits()

#### Parameters

None.

#### Returns

An object that contains width, height, depth, bits, and, if the bitmap has a color table, cTab properties. The bits element is an array of bytes. The cTab element is an array of color values of the form "\#RRGGBB". The length of the array is the length of the color table.
The byte array is meaningful only when referenced by a DLL or shared library. You typically use it only when creating an extensible tool or effect. For information on creating DLLs for use with Flash JavaScript, see ["C-Level Extensibility"](#_bookmark1165) [on page 591](#_bookmark1165)

#### Description

Method; lets you create bitmap effects by getting the bits out of the bitmap, manipulating them, and then returning them to Flash.

#### Example

```javascript
The following code creates a reference to the currently selected object; tests whether the object is a bitmap; and traces the height, width, and bit depth of the bitmap:
var isBitmap = fl.getDocumentDOM().selection\[0\].instanceType; if(isBitmap == "bitmap"){
var bits = fl.getDocumentDOM().selection\[0\].getBits(); fl.trace("height = " + bits.height);
fl.trace("width = " + bits.width); fl.trace("depth = " + bits.depth);
}

```
#### See also

[bitmapInstance.setBits()](#!AdobeDocs/developers-animatesdk-docs/test/BitmapInstance_object/bitmapInstanc2.md)
