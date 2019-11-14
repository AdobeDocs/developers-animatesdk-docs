## document.setCustomFill()

#### Availability

Flash MX 2004.

#### Usage

document.setCustomFill(fill)

#### Parameters

**fill** A Fill object that specifies the fill settings to be used. See [Fill object](../Fill_object/fill_summary.md).

#### Returns

Nothing.

#### Description

Method; sets the fill settings for the Tools panel, Property inspector, and any selected shapes. This allows a script to set the fill settings before drawing the object, rather than drawing the object, selecting it, and changing the fill settings. It also lets a script change the Tools panel and Property inspector fill settings.

#### Example

```javascript
The following example changes the color of the fill color swatch in the Tools panel, Property inspector, and any selected shapes to white:
var fill = fl.getDocumentDOM().getCustomFill(); fill.color = '\#FFFFFF';
fill.style = "solid"; fl.getDocumentDOM().setCustomFill(fill);

```
#### See also

[document.getCustomFill()](../Document_object/docume74.md)
