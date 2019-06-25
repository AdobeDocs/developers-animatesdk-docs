## compiledClipInstance.colorAlphaAmount

#### Availability

> Adobe Animate.

#### Usage

> compiledClipInstance.colorAlphaAmount

#### Description

> Property; an int that reduces or increases the tint and alpha values by a constant amount. This value is added to the current value. This setting is most useful if used in conjunction with colorAlphaPercent. Valid values are -255 to 255.
>
> This setting is the same as selecting Color \> Advanced in the Instance Property Inspector and adjusting the controls on the right of the dialog.

#### Example

> The following example illustrates use of this property:
>
> //change the colorAlphaAmount of the first element in the first frame, top layer fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\].colorAlphaAmount = 100;
>
> //change the colorAlphaAmount of the selected symbol instance fl.getDocumentDOM().selection\[0\].colorAlphaAmount = -100;
