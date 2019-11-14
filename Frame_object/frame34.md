## frame.soundName

#### Availability

Flash MX 2004.

#### Usage

frame.soundName

#### Description

Property; a string that specifies the name of a sound that is attached directly to a frame ([frame.soundLibraryItem](../Frame_object/frame31.md)), as stored in the library.

#### Example

```javascript
The following example changes the soundName property of the first frame to "song1.mp3"; song1.mp3 must exist in the library:
fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].soundName = "song1.mp3";

```