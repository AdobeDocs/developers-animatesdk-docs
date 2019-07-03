## compiledClipInstance.colorAlphaPercent

#### Availability

Adobe Animate.

#### Usage

compiledClipInstance.colorAlphaPercent

#### Description

Property; an int that reduces or increases the tint and alpha values by a specified percentage. The current values are multiplied by this percentage. Valid values are -100 to 100.
This setting is the same as selecting Color \Advanced in the Instance Property Inspector and adjusting the controls on the left of the dialog

#### Example

```
The following example illustrates use of this property:
//change the colorAlphaPercent of the first element in the first frame, top layer fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\].colorAlphaPercent = -100;
//change the colorAlphaPercent of the selected symbol instance fl.getDocumentDOM().selection\[0\].colorAlphaPercent = 90;

```