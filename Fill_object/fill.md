## fill.bitmapIsClipped

#### Availability

Flash CS4 Professional.

#### Usage

fill.bitmapIsClipped

#### Description

Property; a Boolean value that specifies whether the bitmap fill for a shape that is larger than the bitmap is clipped (true) or repeated (false). This property is available only if the value of the [fill.style](../Fill_object/fill9.md) property is "bitmap". If the shape is smaller than the bitmap, this value is false.

#### Example

The following example displays information on whether the bitmap fill is clipped, if appropriate, in the Output panel:

```javascript
var fill = fl.getDocumentDOM().getCustomFill();
if (fill.style == "bitmap")
fl.trace("Fill image is clipped: " + fill.bitmapIsClipped);
```
#### See also

[fill.bitmapPath](../Fill_object/fill1.md)

<span id="fill.bitmapPath" class="anchor"></span>
