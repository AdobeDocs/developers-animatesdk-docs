## filter.hue

#### Availability

Flash 8.

#### Usage

filter.hue

#### Parameters

frameIndex:int

#### Return

double

#### Description

Property; a float value that specifies the hue of the filter. Acceptable values are between -180 and 180. This property is defined for Filter objects with a value of "adjustColorFilter" for the [filter.name](../Filter_object/filter13.md) property.

#### Example

The following example sets the hue to 120 for the Adjust Color filters on the selected object(s):
```javascript
var myFilters = fl.getDocumentDOM().getFilters();
for(i=0; i < myFilters.length; i++){
if(myFilters[i].name == 'adjustColorFilter'){
myFilters[i].hue = 120;
}
}
fl.getDocumentDOM().setFilters(myFilters);

```