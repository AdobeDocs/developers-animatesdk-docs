## document.setFilterProperty()

#### Availability

> Flash 8.

#### Usage

> document.setFilterProperty(property, filterIndex, value)

#### Parameters

> **property** A string specifying the property to be set. Acceptable values are "blurX", "blurY", "quality", angle", "distance", "strength", "knockout", "inner", "bevelType", "color", "shadowColor", and
>
> "highlightColor".
>
> **filterIndex** An integer specifying the zero-based index of the filter in the Filters list.
>
> **value** A number or string specifying the value to be set for the specified filter property. Acceptable values depend on the property and the filter being set.

#### Returns

> Nothing.

#### Description

> Method; sets a specified filter property for the currently selected objects (assuming that the object supports the specified filter).

#### Example

> The following example sets the quality property to 2 for the second filter (index value of 1) in the Filters list of the selected objects and then sets the shadowColor property of the first filter in the Filters list on the selected objects:
>
> fl.getDocumentDOM().setFilterProperty("quality", 1, 2);
>
> fl.getDocumentDOM().setFilterProperty("shadowColor", 0, "\#FF00FF");

#### See also

> [document.addFilter()](#_bookmark121), [document.getFilters()](#_bookmark207), [document.setBlendMode()](#_bookmark278), [document.setFilters()](#document.setFilters()), [Filter](#_bookmark425) [object](#_bookmark425)

<span id="document.setFilters()" class="anchor"></span>
