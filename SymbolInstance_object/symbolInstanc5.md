## symbolInstance.brightness

#### Availability

Adobe Animate.

#### Usage

symbolInstance.brightness

#### Description

Read-only property; returns the value set in the color effect Property Inspector for brightness (percentage between - 100 and 100) when colorMode == 'brightness';. Error if colorMode is a different setting.

#### Example

The following illustrates use of the brightness property:
```javascript
var elem = fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements[0]; 
if (elem.colorMode == 'brightness') {
    fl.trace(elem.brightness);
}

```