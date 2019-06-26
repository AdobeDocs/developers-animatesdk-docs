## compiledClipInstance.filters

#### Availability

> Adobe Animate.

#### Usage

> compiledClipInstance.filters

#### Description

> Property; an array of Filter objects. The properties of Filter object in the filters array can be read but cannot be written directly by accessing the filters array. To set the properties of the filter objects in the filters array, first retrieve the array, set the properties, set it back to the filters array.

#### Example

> The following example illustrates use of this property:
>
> //trace the name of the filter at index 0, if == glow filter, set its blurX to 100 var filterName = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\].filters\[0\].name; fl.trace(filterName);
>
> var filterArray = fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\].filters; if (filterName == 'glowFilter'){
>
> filterArray\[0\].blurX = 100;
>
> }
>
> fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\].filters = filterArray;
