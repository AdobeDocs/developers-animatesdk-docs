## stroke.waveLength

#### Availability

Flash MX 2004.

#### Usage

stroke.waveLength

#### Description

Property; a string that specifies the wavelength of a ragged line. This property is available only if the stroke.style property is set to ragged (see [stroke.style](../Stroke_object/stroke20.md)). Acceptable values are "very short", "short", "medium", and "long".

#### Example


The following example sets the waveLength property to short for a stroke style of ragged:
```javascript
var myStroke = fl.getDocumentDOM().getCustomStroke();
myStroke.style = "ragged";
myStroke.pattern = "random"; 
myStroke.waveHeight ="flat"; 
myStroke.waveLength = "short"; 
fl.getDocumentDOM().setCustomStroke(myStroke);

```