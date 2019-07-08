## symbolInstance.loop

#### Availability

Flash MX 2004.

#### Usage

symbolInstance.loop

#### Description

Property; a string that, for graphic symbols, sets the same property as the Loop pop-up menu in the Property inspector. For other types of symbols, this property is undefined. Acceptable values are "loop", "play once", and "single frame" to set the graphic’s animation accordingly.

#### Example

```javascript
The following example sets the first symbol in the first frame of the first layer in the timeline to single frame (display one specified frame of the graphic timeline), as long as that symbol is a graphic:
fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\].loop = 'single frame';

```