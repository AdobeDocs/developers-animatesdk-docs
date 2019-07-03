## filter.hideObject

#### Availability

Flash 8.

#### Usage

filter.hideObject

#### Description

Property; a Boolean value that specifies whether the source image is hidden (true) or displayed (false). This property is defined for Filter objects with a value of "dropShadowFilter" for the [filter.name](#_bookmark440) property.

#### Example

```
The following example sets the hideObject value to true for the Drop Shadow filters on the selected object(s):
var myFilters = fl.getDocumentDOM().getFilters(); for(i=0; i \< myFilters.length; i++){
if(myFilters\[i\].name == 'dropShadowFilter'){ myFilters\[i\].hideObject = true;
}
}
fl.getDocumentDOM().setFilters(myFilters);

```