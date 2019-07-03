## fill.color

#### Availability

Flash MX 2004.

#### Usage

fill.color

#### Description

Property; the color of the fill, in one of the following formats:

-   A string in the format "\#RRGGBB" or "\#RRGGBBAA"

-   A hexadecimal number in the format 0xRRGGBB

-   An integer that represents the decimal equivalent of a hexadecimal number

#### Example

```
The following example sets the fill color of the current selection:
var fill = fl.getDocumentDOM().getCustomFill(); fill.color = "\#FFFFFF"; fl.getDocumentDOM().setCustomFill( fill );

```