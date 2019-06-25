## frame.soundLoopMode

#### Availability

> Flash MX 2004.

#### Usage

> frame.soundLoopMode

#### Description

> Property; a string that specifies whether a sound that is attached directly to a frame ([frame.soundLibraryItem](#_bookmark630)) should play a specific number of times or loop indefinitely. Acceptable values are "repeat" and "loop". To specify the number of times the sound should play, set a value for [frame.soundLoop](#_bookmark632).

#### Example

> The following example specifies that a sound should play two times:
>
> fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].soundLoopMode = "repeat"; fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].soundLoop = 2;
