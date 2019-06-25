## frame.getSoundEnvelope()

#### Availability

> Adobe Animate.

#### Usage

> frame.getSoundEnvelope()

#### Parameters

> None

#### Returns

> Returns a Sound object.

#### Description

> Method; Gets the sound envelope data of any frame.

#### Example

> The following example illustrates the use of getSoundEnvelope:
>
> // Add a sound item to the first Frame
>
> // Get the sound Envelope
>
> var soundEnv = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].getSoundEnvelope();
>
> //Assigning the sound 1 in the library to Frame 2 fl.getDocumentDOM().getTimeline().layers\[0\].frames\[1\].soundLibraryItem
>
> =fl.getDocumentDOM().library.items\[1\];
>
> //Set the Sound Envelope fl.getDocumentDOM().getTimeline().layers\[0\].frames\[1\].setSoundEnvelope(soundEnv);

#### See also

> [frame.setSoundEnvelope()](#_bookmark626)
