## symbolInstance.blendMode

#### Availability

Flash 8.

#### Usage

symbolInstance.blendMode

#### Description

Property; a string that specifies the blending mode to be applied to a movie clip symbol. Acceptable values are "normal", "layer", "multiply", "screen", "overlay", "hardlight", "lighten", "darken", "difference", "add", "subtract", "invert", "alpha", and "erase".

#### Example

```javascript
The following example sets the blending mode for the first movie clip symbol in the first frame on the first level to add:
fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\].blendMode = "add";

```
#### See also

[document.setBlendMode()](#_bookmark279)
