## frame.setSoundEnvelope()

#### Availability

Adobe Animate.

#### Usage

frame.setSoundEnvelope(soundEnv)

#### Parameters

**soundEnv** A sound envelope.

#### Returns

Nothing.

#### Description

Method; Sets the sound envelope of any frame with sound file. The soundEnv object is an array and every element of array contains the following properties:

-   mark

-   leftChannel

-   rightChannel

#### Example

```javascript
The following example illustrates the use of setSoundEnvelope:
// Add a sound item to the first Frame
// Get the sound Envelope
var soundEnv = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].getSoundEnvelope();
//Assigning the sound 1 in the library to Frame 2 fl.getDocumentDOM().getTimeline().layers\[0\].frames\[1\].soundLibraryItem
=fl.getDocumentDOM().library.items\[1\];
//Set the Sound Envelope fl.getDocumentDOM().getTimeline().layers\[0\].frames\[1\].setSoundEnvelope(soundEnv);
for (int i=0; i\<soundEnv.length; i++) { fl.trace(soundEnv\[i\].mark);
fl.trace(soundEnv\[i\].leftChannel); fl.trace(soundEnv\[i\].rightChannel);
}

```
#### See also

[frame.getSoundEnvelope()](../Frame_object/frame8.md)
