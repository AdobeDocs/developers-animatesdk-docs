## timeline.copyMotionAsAS3()

#### Availability

Flash CS3 Professional.

#### Usage

timeline.copyMotionAsAS3()

#### Parameters

None.

#### Returns

Nothing.

#### Description

Method; copies motion on selected frames, either from a motion tween or from frame-by-frame animation, to the clipboard as ActionScript 3.0 code. You can then paste this code into a script.
To copy motion in a format that you can apply to other frames, see [timeline.copyMotion()](#_bookmark1040).

#### Example

```
The following example copies the motion from the selected frame or frames to the clipboard as ActionScript 3.0 code:
fl.getDocumentDOM().getTimeline().copyMotionAsAS3();

```
#### See also

[timeline.copyMotion()](#_bookmark1040)
