## stroke.waveHeight

#### Availability

Flash MX 2004.

#### Usage

stroke.waveHeight

#### Description

Property; a string that specifies the wave height of a ragged line. This property is available only if the stroke.style
>
property is set to ragged (see [stroke.style](#_bookmark898)). Acceptable values are "flat", "wavy", "very wavy", and "wild".

#### Example

```
The following example sets the waveHeight property to flat for a stroke style of ragged:
var myStroke = fl.getDocumentDOM().getCustomStroke(); myStroke.style = "ragged";
myStroke.pattern = "random"; myStroke.waveHeight = "flat"; myStroke.waveLength = "short"; fl.getDocumentDOM().setCustomStroke(myStroke);

```