## presetItem.isFolder

#### Availability

> Flash CS4 Professional.

#### Usage

> presetItem.isFolder

#### Description

> Read-only property: a Boolean value that specifies whether the item in the Motion Presets panel is a folder (true) or a preset (false).

#### Example

> The following example shows that the first item in the Motion Presets panel is a folder and the second is a preset:
>
> var presetItemArray=fl.presetPanel.items; fl.trace(presetItemArray\[0\].isFolder); fl.trace(presetItemArray\[1\].isFolder);
