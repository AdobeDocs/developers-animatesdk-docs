## document.setCustomStroke()

#### Availability

Flash MX 2004.

#### Usage

document.setCustomStroke(stroke)

#### Parameters

**stroke** A [Stroke object](../Stroke_object/stroke_summary.md).

#### Returns

Nothing.

#### Description

Method; sets the stroke settings for the Tools panel, Property inspector, and any selected shapes. This allows a script to set the stroke settings before drawing the object, rather than drawing the object, selecting it, and changing the stroke settings. It also lets a script change the Tools panel and Property inspector stroke settings.

#### Example

The following example changes the stroke thickness setting in the Tools panel, Property inspector, and any selected shapes:

```javascript

var stroke = fl.getDocumentDOM().getCustomStroke(); stroke.thickness += 2; 
fl.getDocumentDOM().setCustomStroke(stroke);

```
#### See also

[document.getCustomStroke()](../Document_object/docume75.md)
