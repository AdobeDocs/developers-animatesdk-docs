## frame.getSoundEnvelopeLimits()

#### Availability

Adobe Animate.

#### Usage

frame.getSoundEnvelopeLmits()

#### Parameters

None

#### Returns

Returns a structure that contain start and end fields.

#### Description

Method; Gets the limits (start, end) for a custom Sound envelope that is applied to the frame sound.

#### Example

```javascript
The following example illustrates the use of getSoundEnvelopeLimits:
var limits = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].getSoundEnvelopeLimits(); fl.trace(limits.start);
fl.trace(limits.end);

```
#### See also

[frame.setSoundEnvelopeLimits()](#_bookmark627)
