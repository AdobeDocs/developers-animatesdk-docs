## stroke.color

#### Availability

> Flash MX 2004. In Flash 8 and later, this property is deprecated in favor of stroke.shapeFill.color.

#### Usage

> stroke.color

#### Description

> Property; the color of the stroke, in one of the following formats:

-   A string in the format "\#RRGGBB" or "\#RRGGBBAA"

-   A hexadecimal number in the format 0xRRGGBB

-   An integer that represents the decimal equivalent of a hexadecimal number

#### Example

> The following example sets the stroke color:
>
> var myStroke = fl.getDocumentDOM().getCustomStroke(); myStroke.color = "\#000000"; fl.getDocumentDOM().setCustomStroke(myStroke);

#### See also

> [stroke.shapeFill](#_bookmark895)
