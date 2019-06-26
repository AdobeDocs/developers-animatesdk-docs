## filter.quality

#### Availability

> Flash 8.

#### Usage

> filter.quality

#### Description

> Property; a string that specifies the blur quality. Acceptable values are "low", "medium", and "high" ("high" is similar to a Gaussian blur). This property is defined for Filter objects with a value of "bevelFilter", "blurFilter", "dropShadowFilter", "glowFilter", "gradientGlowFilter", or "gradientBevelFilter" for the [filter.name](#_bookmark440) property.

#### Example

> The following example sets the blur quality to "medium" for the Glow filters on the selected object(s):
>
> var myFilters = fl.getDocumentDOM().getFilters(); for(i=0; i \< myFilters.length; i++){
>
> if(myFilters\[i\].name == 'glowFilter'){ myFilters\[i\].quality = 'medium';
>
> }
>
> }
>
> fl.getDocumentDOM().setFilters(myFilters);

#### See also

> [document.setFilterProperty()](#_bookmark289)
