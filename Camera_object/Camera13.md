## filter.name

#### Availability

Flash 8.

#### Usage

filter.name

#### Parameters

frameIndex:int

#### Return

double

#### Description

Read-only property; a string that specifies the type of filter. The value of this property determines which other properties of the Filter object are available. The value is one of the following: "adjustColorFilter", "bevelFilter", "blurFilter", "dropShadowFilter", "glowFilter", "gradientBevelFilter", or "gradientGlowFilter".

#### Example

The following example displays the filter names and index positions in the Output panel:
```javascript
var myFilters = fl.getDocumentDOM().getFilters();
var traceStr = "";
for(i=0; i < myFilters.length; i++){
traceStr = traceStr + " At index " + i + ": " + myFilters[i].name;
}
fl.trace(traceStr); 

```
#### See also

[document.getFilters()](../Document_object/docume79.md), [document.setFilterProperty()](../Document_object/docum520.md)
