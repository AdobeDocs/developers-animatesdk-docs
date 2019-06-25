## textAttrs.fillColor

#### Availability

> Flash MX 2004.

#### Usage

> textAttrs.fillColor

#### Description

> Property; the color of the fill, in one of the following formats:

-   A string in the format "\#RRGGBB" or "\#RRGGBBAA"

-   A hexadecimal number in the format 0xRRGGBB

-   An integer that represents the decimal equivalent of a hexadecimal number

#### Example

> The following example sets the color to red for the selected text field from the character at index 2 up to, but not including, the character at index 8:
>
> fl.getDocumentDOM().selection\[0\].setTextAttr("fillColor", 0xff0000, 2, 8);
