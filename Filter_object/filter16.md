## filter.shadowColor

#### Availability

Flash 8.

#### Usage

filter.shadowColor

#### Description

Property; the color of the shadow, in one of the following formats:

-   A string in the format "\#RRGGBB" or "\#RRGGBBAA"

-   A hexadecimal number in the format 0xRRGGBB

-   An integer that represents the decimal equivalent of a hexadecimal number

This property is defined for Filter objects with a value of "bevelFilter" for the [filter.name](#_bookmark440) property.

#### Example

```
The following example sets the shadow color to "\#ff00003e" for the Bevel filters on the selected object(s):
var myFilters = fl.getDocumentDOM().getFilters(); for(i=0; i \< myFilters.length; i++){
if(myFilters\[i\].name == 'bevelFilter'){ myFilters\[i\].shadowColor = '\#ff00003e';
}
}
fl.getDocumentDOM().setFilters(myFilters);

```
#### See also

[document.setFilterProperty()](#_bookmark289)
