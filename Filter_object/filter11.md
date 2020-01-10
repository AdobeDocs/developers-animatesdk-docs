## filter.inner

#### Availability

Flash 8.

#### Usage

filter.inner

#### Description

Property; a Boolean value that specifies whether the shadow is an inner shadow (true) or not (false). This property is defined for Filter objects with a value of "dropShadowFilter" or "glowFilter" for the [filter.name](../Filter_object/filter13.md) property.

#### Example

The following example sets the value of the inner property to true for the Glow filters on the selected object(s):
```javascript
var myFilters = fl.getDocumentDOM().getFilters();
for(i=0; i < myFilters.length; i++){
if(myFilters[i].name == 'glowFilter'){
myFilters[i].inner = true;
}
}
fl.getDocumentDOM().setFilters(myFilters);

```
#### See also

[document.setFilterProperty()](../Document_object/docum520.md)
