## filter.blurX

#### Availability

Flash 8.

#### Usage

filter.blurX

#### Description

Property; a float value that specifies the amount to blur in the *x* direction, in pixels. Acceptable values are between 0 and 255. This property is defined for Filter objects with a value of "bevelFilter", "blurFilter", "dropShadowFilter", "glowFilter", "gradientBevelFilter", or "gradientGlowFilter" for the [filter.name](#_bookmark440) property.

#### Example

```javascript
The following example sets the blurX value to 30 and the blurY value to 20 for the Blur filters on the selected object(s):
var myFilters = fl.getDocumentDOM().getFilters(); for(i=0; i \< myFilters.length; i++){
if(myFilters\[i\].name == 'blurFilter'){ myFilters\[i\].blurX = 30;
myFilters\[i\].blurY = 20;
}
}
fl.getDocumentDOM().setFilters(myFilters);

```
#### See also

[document.setFilterProperty()](#_bookmark289), [filter.blurY](#filter.blurY)

<span id="filter.blurY" class="anchor"></span>
