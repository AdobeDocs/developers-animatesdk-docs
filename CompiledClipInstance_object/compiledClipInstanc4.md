## compiledClipInstance.brightness

#### Availability

Adobe Animate.

#### Usage

compiledClipInstance.brightness

#### Description

Read-only property; an int that contains the value set in the Color Effect Property Inspector for brightness when colorMode == 'brightness'. Specify a percentage between -100 and 100. Returns an error if colorMode is a different setting.

#### Example

```javascript
The following example illustrates use of this property:
var elem = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\]; if (elem.colorMode == 'brightness') {
fl.trace(elem.brightness);
}

```