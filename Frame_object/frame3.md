## frame.actionScript

#### Availability

Flash MX 2004.

#### Usage

*frame.actionScript*

#### Description

Property; a string that represents ActionScript code. To insert a new line character, use "\n".

#### Example

```javascript
The following example assigns stop() to first frame top layer action:

fl.getDocumentDOM().getTimeline().layers[0].frames[0].actionScript = 'stop();';

```