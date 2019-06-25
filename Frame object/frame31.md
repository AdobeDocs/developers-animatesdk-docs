## frame.soundLibraryItem

#### Availability

> Flash MX 2004.

#### Usage

> frame.soundLibraryItem

#### Description

> Property; a library item (see [SoundItem object](#_bookmark827)) used to create a sound. The sound is attached directly to the frame.

#### Example

> The following example assigns the first item in the library to the soundLibraryItem property of the first frame:
>
> // The first item in the library must be a sound object. fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].soundLibraryItem
>
> =fl.getDocumentDOM().library.items\[0\];
