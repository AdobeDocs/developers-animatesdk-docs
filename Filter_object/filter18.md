## filter.type

#### Availability

Flash 8.

#### Usage

filter.type

#### Description

Property; a string that specifies the type of bevel or glow. Acceptable values are "inner", "outer", and "full". This property is defined for Filter objects with a value of "bevelFilter", "gradientGlowFilter", or "gradientBevelFilter" for the [filter.name](../Filter_object/filter13.md) property.

#### Example

```javascript
The following example sets the type to "full" for all Bevel filters on the selected object(s):
var myFilters = fl.getDocumentDOM().getFilters(); for(i=0; i \< myFilters.length; i++){
if(myFilters\[i\].name == 'bevelFilter'){ myFilters\[i\].type = 'full';
}
}
fl.getDocumentDOM().setFilters(myFilters);

```
#### See also

[document.setFilterProperty()](../Document_object/docum520.md)
