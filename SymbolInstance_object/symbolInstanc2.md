## symbolInstance.backgroundColor

#### Availability

Flash CS5.5 Professional.

#### Usage

symbolInstance.backgroundColor

#### Description

Property; a string that specifies the matte color when 24 bit mode is selected for the instance. This is a string in hexadecimal #rrggbb format or an integer containing the value.

#### Example


The following example assigns the symbol instance a background color of black:
```javascript
var bitmapInstance = fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements[0]; bitmapInstance.backgroundColor = "#000000";

```