## document.getCustomStroke()

#### Availability

Flash MX 2004.

#### Usage

document.getCustomStroke(\[locationOfStroke\])

#### Parameters

**locationOfStroke** A string that specifies the location of the stroke object. The following values are valid:

-   "toolbar", if set, returns the stroke object of the Tools panel and Property inspector.

-   "selection", if set, returns the stroke object of the selection.

If you omit this parameter, it defaults to "selection". If there is no selection, it returns undefined. This parameter is optional.

#### Returns

The [Stroke object](../Stroke_object/stroke_summary.md) specified by the *locationOfStroke* parameter, if successful; otherwise, it returns undefined.

#### Description

Returns the stroke object of the selected shape or, if specified, of the Tools panel and Property inspector.

#### Example

```javascript
The following example returns the current stroke settings of the selection and changes the stroke thickness to 2:
var stroke = fl.getDocumentDOM().getCustomStroke("selection"); stroke.thickness = 2; fl.getDocumentDOM().setCustomStroke(stroke);
The following example returns the current stroke settings of the Tools panel and Property inspector and sets the stroke color to red:
var stroke = fl.getDocumentDOM().getCustomStroke("toolbar"); stroke.color = "\#FF0000"; fl.getDocumentDOM().setCustomStroke(stroke);

```
#### See also

[document.setCustomStroke()](../Document_object/docum480.md)
