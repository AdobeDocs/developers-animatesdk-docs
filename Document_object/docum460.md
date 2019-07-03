## document.setBlendMode()

#### Availability

Flash 8.

#### Usage

document.setBlendMode(mode)

#### Parameters

**mode** A string that represents the desired blending mode for the selected objects. Acceptable values are "normal", "layer", "multiply", "screen", "overlay", "hardlight", "lighten", "darken", "difference", "add", "subtract", "invert", "alpha", and "erase".

#### Returns

Nothing.

#### Description

Method; sets the blending mode for the selected objects.

#### Example

```
The following example sets the blending mode for the selected object to "add". fl.getDocumentDOM().setBlendMode("add");

```
#### See also

[document.addFilter()](#_bookmark121), [document.setFilterProperty()](#_bookmark288), [symbolInstance.blendMode](#_bookmark922)
