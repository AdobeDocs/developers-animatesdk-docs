## frame.hasCustomEase

#### Availability

Flash 8.

#### Usage

*frame.hasCustomEase*

#### Description

Property; a Boolean value. If true, the frame gets its ease information from the custom ease curve. If false, the frame gets its ease information from the ease value.

#### Example

```javascript
The following example specifies that the first frame in the top layer should get its ease information from the ease value rather than the custom ease curve:

var theFrame = fl.getDocumentDOM().getTimeline().layers[0].frames[0] 
theFrame.hasCustomEase = false;

```
#### See also

[frame.getCustomEase()](../Frame_object/frame6.md), [frame.setCustomEase()](../Frame_object/frame24.md), [frame.useSingleEaseCurve](../Frame_object/frame40.md)
