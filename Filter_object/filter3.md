## filter.brightness

#### Availability

Flash 8.

#### Usage

filter.brightness

#### Description

Property; a float value that specifies the brightness of the filter. Acceptable values are between -100 and 100. This property is defined for Filter objects with a value of "adjustColorFilter" for the [filter.name](../Filter_object/filter13.md) property.

#### Example

```javascript
The following example sets the brightness to 30.5 for the Adjust Color filters on the selected object(s):
var myFilters = fl.getDocumentDOM().getFilters(); for(i=0; i < myFilters.length; i++){
if(myFilters[i].name == 'adjustColorFilter'){ myFilters[i].brightness = 30.5;
}
}
fl.getDocumentDOM().setFilters(myFilters);

```