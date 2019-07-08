## frame.convertToFrameByFrameAnimation()

#### Availability

Adobe Animate.

#### Usage

frame.convertToFrameByFrameAnimation()

#### Returns

Returns boolean. Returns true if the frame contains animation that can be converted to frame by frame animation. For example: return true for Motion Tween frame or Classic Tween frame; return false for other type of frame such as static.

#### Description

Method; Converts the current frame to Frame-by-Frame Animation.

#### Example

```javascript
The following example converts the frame 0 to Frame-by-Frame Animation:
var result = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].convertToFrameByFrameAnimation(); fl.trace(result);

```