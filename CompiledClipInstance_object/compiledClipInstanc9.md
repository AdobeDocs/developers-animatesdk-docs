## compiledClipInstance.colorBluePercent

#### Availability

Adobe Animate.

#### Usage

compiledClipInstance.colorBluePercent

#### Description

Property; an int that reduces or increases the blue tint values by a specified percentage. The current values are multiplied by this percentage. Valid values are -100 to 100.

This setting is the same as selecting Color > Advanced in the Instance Property Inspector.

#### Example

The following example illustrates use of this property:
```javascript
//change the colorBluePercent of the first element in the first frame, top layer
fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements[0].colorBluePercent = 100;
//change the colorBluePercent of the selected symbol instance
fl.getDocumentDOM().selection[0].colorBluePercent = 80;
```