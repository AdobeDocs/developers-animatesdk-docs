## document.setFillColor()

#### Availability

Flash MX 2004.

#### Usage

document.setFillColor(color)

#### Parameters

**color** The color of the fill, in one of the following formats:

-   A string in the format "\#RRGGBB" or "\#RRGGBBAA"

-   A hexadecimal number in the format 0xRRGGBB

-   An integer that represents the decimal equivalent of a hexadecimal number

If set to null, no fill color is set, which is the same as setting the Fill color swatch in the user interface to no fill.

#### Returns

Nothing.

#### Description

Method; changes the selection and the tools panel to the specified fill color. For additional information on changing the fill color in the Tools panel and Property inspector, see [document.setCustomFill()](#_bookmark280).

#### Example

```
The first three statements in the following example set the fill color using each of the different formats for specifying color. The fourth statement sets the fill to no fill.
fl.getDocumentDOM().setFillColor("\#cc00cc"); fl.getDocumentDOM().setFillColor(0xcc00cc); fl.getDocumentDOM().setFillColor(120000); fl.getDocumentDOM().setFillColor(null);

```