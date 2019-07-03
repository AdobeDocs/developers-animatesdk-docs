## filter.angle

#### Availability

Flash 8.

#### Usage

filter.angle

#### Description

Property; a float value that specifies the angle of the shadow or highlight color, in degrees. Acceptable values are between 0 and 360. This property is defined for Filter objects with a value of "bevelFilter", "dropShadowFilter", "gradientBevelFilter", or "gradientGlowFilter" for the [filter.name](#_bookmark440) property.

#### Example

```
The following example sets the angle to 120 for the Bevel filters on the selected object(s):
var myFilters = fl.getDocumentDOM().getFilters(); for(i=0; i \< myFilters.length; i++) {
if(myFilters\[i\].name == 'bevelFilter'){ myFilters\[i\].angle = 120;
}
}
fl.getDocumentDOM().setFilters(myFilters);

```
#### See also

[document.setFilterProperty()](#_bookmark289)
