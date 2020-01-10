## symbolInstance.tintColor

#### Availability

Adobe Animate.

#### Usage

symbolInstance.tintColor

#### Description

Read-only property; when the Color Effect Property Inspector is using style tint(colorMode == 'tint'), return the color applied to the tint. Otherwise using this property results in an error.

#### Example

The following illustrates use of the tintColor property:

```javascript
var elem = fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements[0]; 
if (elem.colorMode = 'tint') {
    fl.trace(elem.tintColor); 
    fl.trace(elem.tintPercent);
}

```