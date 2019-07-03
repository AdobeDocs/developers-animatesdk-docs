## compiledClipInstance.colorMode

#### Availability

Adobe Animate.

#### Usage

compiledClipInstance.colorMode

#### Description

Property; a string that specifies the color mode, as identified in the Symbol Properties dialog. Valid values are “none”, “brightness”, “tint”, “alpha”, and “advanced”.

#### Example

```
The following example illustrates use of this property:
//change the colorMode of the first element in the first frame, top layer fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\].colorMode = 'advanced';

```