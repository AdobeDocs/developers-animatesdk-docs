## filter.distance

#### Availability

Flash 8.

#### Usage

filter.distance

#### Description

Property; a float value that specifies the distance between the filter’s effect and an object, in pixels. Acceptable values are from -255 to 255. This property is defined for Filter objects with a value of "bevelFilter", "dropShadowFilter", "gradientBevelFilter", or "gradientGlowFilter" for the [filter.name](#_bookmark440) property.

#### Example

```javascript
The following example sets the distance to 10 pixels for the Drop Shadow filters on the selected object(s):
var myFilters = fl.getDocumentDOM().getFilters(); for(i=0; i \< myFilters.length; i++){
if(myFilters\[i\].name == 'dropShadowFilter'){ myFilters\[i\].distance = 10;
}
}
fl.getDocumentDOM().setFilters(myFilters);

```
#### See also

[document.setFilterProperty()](#_bookmark289)
