## frame.getCustomEase()

#### Availability

Flash 8.

#### Usage

Frame.getCustomEase(\[property\])

#### Parameters

**property** An optional string that specifies the property for which you want to return the custom ease value. Acceptable values are "all", "position", "rotation", "scale", "color", and "filters". The default value is "all".

#### Returns

Returns an array of JavaScript objects, each of which has an *x* and *y* property.

#### Description

Method; returns an array of objects that represent the control points for the cubic Bézier curve that defines the ease curve.

#### Example

```javascript
The following example returns the custom ease value of the position property for the first frame in the top layer:
var theFrame = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\] var easeArray = theFrame.getCustomEase("position");

```
#### See also

[frame.hasCustomEase](#!AdobeDocs/developers-animatesdk-docs/master/Frame_object/frame10.md), [frame.setCustomEase()](#!AdobeDocs/developers-animatesdk-docs/master/Frame_object/frame24.md), [frame.useSingleEaseCurve](#!AdobeDocs/developers-animatesdk-docs/master/Frame_object/frame40.md)
