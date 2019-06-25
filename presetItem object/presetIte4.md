## presetItem.open

#### Availability

> Flash CS4 Professional.

#### Usage

> presetItem.open

#### Description

> Read-only property: specifies whether a folder in the Motion Presets panel is currently expanded (true) or not (false).
>
> This property is true if the item is not a folder. To determine if an item is a folder or a preset, use [presetItem.isFolder](#_bookmark773).

#### Example

> The following example displays information on whether folders in the Motion Presets panel are expanded or collapsed:
>
> fl.outputPanel.clear();
>
> var presetItemArray=fl.presetPanel.items; for (i=0;i\<presetItemArray.length; i++){
>
> var presetItem = presetItemArray\[i\]; if (presetItem.isFolder) {
>
> var status = presetItem.open ? "Open" : "Closed"
>
> fl.trace(presetItem.level + "-" + presetItem.name +" folder is " + status);
>
> }
>
> }
