## frame.setCustomEase()

#### Availability

Flash 8.

#### Usage

frame.setCustomEase(property, easeCurve)

#### Parameters

**property** A string that specifies the property the ease curve should be used for. Acceptable values are "all", "position", "rotation", "scale", "color", and "filters".
**easeCurve** An array of objects that defines the ease curve. Each array element must be a JavaScript object with *x* and
*y* properties.

#### Returns

Nothing.

#### Description

Method; specifies an array of control point and tangent endpoint coordinates that describe a cubic Bézier curve to be used as a custom ease curve. This array is constructed by the horizontal (ordinal: left to right) position of the control points and tangent endpoints.

#### Example

```javascript
The following example sets the ease curve for all properties of the first frame in the first layer to the Bézier curve specified by the easeCurve array:
var theFrame = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\]; var easeCurve = \[ {x:0,y:0}, {x:.3,y:.3}, {x:.7,y:.7}, {x:1,y:1} \]; theFrame.setCustomEase( "all", easeCurve );

```
#### See also

[frame.getCustomEase()](../Frame_object/frame6.md), [frame.hasCustomEase](../Frame_object/frame10.md), [frame.useSingleEaseCurve](../Frame_object/frame40.md)
