## document.getCustomFill()

#### Availability

Flash MX 2004.

#### Usage

document.getCustomFill(\[objectToFill\])

#### Parameters

**objectToFill** A string that specifies the location of the fill object. The following values are valid:

-   "toolbar" returns the fill object of the Tools panel and Property inspector.

-   "selection" returns the fill object of the selection.

If you omit this parameter, the default value is "selection". If there is no selection, the method returns
undefined. This parameter is optional.

#### Returns

The [Fill object](#_bookmark412) specified by the *objectToFill* parameter, if successful; otherwise, it returns undefined.

#### Description

Method; retrieves the fill object of the selected shape or, if specified, of the Tools panel and Property inspector.

#### Example

```javascript
The following example gets the fill object of the selection and then changes the selection’s color to white:
var fill = fl.getDocumentDOM().getCustomFill(); fill.color = '\#FFFFFF';
fill.style = "solid"; fl.getDocumentDOM().setCustomFill(fill);
The following example returns the fill object of the Tools panel and Property inspector and then changes the color swatch to a linear gradient:
var fill = fl.getDocumentDOM().getCustomFill("toolbar"); fill.style = "linearGradient";
fill.colorArray = \[ 0x00ff00, 0xff0000, 0x0000ff \]; fill.posArray = \[0, 100, 200\]; fl.getDocumentDOM().setCustomFill( fill );

```
#### See also

[document.setCustomFill()](#_bookmark280)
