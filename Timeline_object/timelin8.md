## timeline.copyMotion()

#### Availability

Flash CS3 Professional.

#### Usage

timeline.copyMotion()

#### Parameters

None.

#### Returns

Nothing.

#### Description

Method; copies motion on selected frames, either from a motion tween or from frame-by-frame animation. You can then use [timeline.pasteMotion()](#_bookmark1071) to apply the motion to other frames.
>
To copy motion as text (code) that you can paste into a script, see [timeline.copyMotionAsAS3()](#timeline.copyMotionAsAS3()).

#### Example

```
The following example copies the motion from the selected frame or frames:
fl.getDocumentDOM().getTimeline().copyMotion();

```
#### See also

[timeline.copyMotionAsAS3()](#timeline.copyMotionAsAS3()), [timeline.pasteMotion()](#_bookmark1071)

<span id="timeline.copyMotionAsAS3()" class="anchor"></span>
