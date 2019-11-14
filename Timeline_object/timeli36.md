## timeline.pasteMotion()

#### Availability

Flash CS3 Professional.

#### Usage

timeline.pasteMotion()

#### Parameters

None.

#### Returns

Nothing.

#### Description

Method; pastes the range of motion frames retrieved by [timeline.copyMotion()](../Timeline_object/timelin8.md) to the Timeline. If necessary, existing frames are displaced (moved to the right) to make room for the frames being pasted.

#### Example

```javascript
The following example pastes the motion on the clipboard to the currently selected frame or playhead location, displacing that frame to the right of the pasted frames:
fl.getDocumentDOM().getTimeline().pasteMotion();

```
#### See also

[timeline.copyMotion()](../Timeline_object/timelin8.md)
