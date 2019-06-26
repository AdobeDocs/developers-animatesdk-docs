## filter.saturation

#### Availability

> Flash 8.

#### Usage

> filter.saturation

#### Description

> Property; a float value that specifies the saturation value of the filter. Acceptable values are from -100 to 100. This property is defined for Filter objects with a value of "adjustColorFilter" for the [filter.name](#_bookmark440) property.

#### Example

> The following example sets the saturation value to -100 (grayscale) for the Adjust Color filters on the selected object(s):
>
> var myFilters = fl.getDocumentDOM().getFilters(); for(i=0; i \< myFilters.length; i++){
>
> if(myFilters\[i\].name == 'adjustColorFilter'){ myFilters\[i\].saturation = 0-100;
>
> }
>
> }
>
> fl.getDocumentDOM().setFilters(myFilters);

#### See also

> [document.setFilterProperty()](#_bookmark289)
