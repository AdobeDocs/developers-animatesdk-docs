## frame.useSingleEaseCurve

#### Availability

Flash 8.

#### Usage

frame.useSingleEaseCurve

#### Description

Property; a Boolean value. If true, a single custom ease curve is used for easing information for all properties. If false, each property has its own ease curve.
This property is ignored if the frame doesn’t have custom easing applied.

#### Example

```javascript
The following example specifies that a single custom ease curve should be used for all properties of the first frame on the first layer:
var theFrame = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\] theFrame.useSingleEaseCurve = true;

```
#### See also

[frame.getCustomEase()](#!AdobeDocs/developers-animatesdk-docs/master/Frame_object/frame6.md), [frame.hasCustomEase](#!AdobeDocs/developers-animatesdk-docs/master/Frame_object/frame10.md), [frame.setCustomEase()](#!AdobeDocs/developers-animatesdk-docs/master/Frame_object/frame24.md)
