## frame.soundSync

#### Availability

Flash MX 2004.

#### Usage

frame.soundSync

#### Description

Property; a string that specifies the sync behavior of a sound that is attached directly to a frame ([frame.soundLibraryItem](#_bookmark630)). Acceptable values are "event", "stop", "start", and "stream".

#### Example

```javascript
The following example specifies that a sound should stream:
fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].soundSync = 'stream';

```