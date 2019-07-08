## frame.soundEffect

#### Availability

Flash MX 2004.

#### Usage

frame.soundEffect

#### Description

Property; a string that specifies effects for a sound that is attached directly to a frame ([frame.soundLibraryItem](#frame.soundLibraryItem)). Acceptable values are "none", "left channel", "right channel", "fade left to right", "fade right to left", "fade in", "fade out", and "custom".

#### Example

```javascript
The following example specifies that the sound attached to the first frame should fade in:
fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].soundEffect = "fade in";

<span id="frame.soundLibraryItem" class="anchor"></span
```