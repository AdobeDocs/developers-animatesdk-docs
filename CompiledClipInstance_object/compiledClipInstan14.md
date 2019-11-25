## compiledClipInstance.colorRedPercent

#### Availability

Adobe Animate.

#### Usage

compiledClipInstance.colorRedPercent

#### Description

Property; an int that reduces or increases the red tint values by a specified percentage. The current values are multiplied by this percentage. Valid values are -100 to 100.
This setting is the same as selecting Color > Advanced in the Instance Property Inspector.

#### Example

```javascript
The following example illustrates use of this property:
//change the colorRedPercent of the first element in the first frame, top layer fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements[0].colorRedPercent = 100;
//change the colorRedPercent of the selected symbol instance fl.getDocumentDOM().selection[0].colorRedPercent = 80;

```