## filter.strength

#### Availability

Flash 8.

#### Usage

filter.strength

#### Description

Property; an integer that specifies the percentage strength of the filter. Acceptable values are between 0 and 25,500. This property is defined for Filter objects with a value of "bevelFilter", "dropShadowFilter", "glowFilter", "gradientGlowFilter", or "gradientBevelFilter" for the [filter.name](#!AdobeDocs/developers-animatesdk-docs/test/Filter_object/filter13.md) property.

#### Example

```javascript
The following example sets the strength to 50 for the Glow filters on the selected object(s):
var myFilters = fl.getDocumentDOM().getFilters(); for(i=0; i \< myFilters.length; i++){
if(myFilters\[i\].name == 'glowFilter'){ myFilters\[i\].strength = 50;
}
}
fl.getDocumentDOM().setFilters(myFilters);

```
#### See also

[document.setFilterProperty()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docum520.md)
