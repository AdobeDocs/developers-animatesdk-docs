## compiledClipInstance.tintColor

#### Availability

Adobe Animate.

#### Usage

compiledClipInstance.tintColor

#### Description

Read-only property; a Color object that, when the Color Effect Property Inspector is using style tint (colorMode == 'tint'), returns the color applied to the tint. Otherwise, using this property results in an error.

#### Example

The following example illustrates use of this property:
```javascript
var elem = fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements[0];
if (elem.colorMode = 'tint') {
fl.trace(elem.tintColor);
fl.trace(elem.tintPercent);
}

```