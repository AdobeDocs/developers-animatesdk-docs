## document.disableOtherFilters()

#### Availability

Flash 8.

#### Usage

document.disableOtherFilters(enabledFilterIndex)

#### Parameters

**enabledFilterIndex** An integer representing the zero-based index of the filter that should remain enabled after other filters are disabled.

#### Returns

Nothing.

#### Description

Method; disables all filters except the one at the specified position in the Filters list.

#### Example

```javascript
The following example disables all filters except the second filter in the list (index value of 1):
fl.getDocumentDom().disableOtherFilters(1);

```
#### See also

[document.addFilter()](#_bookmark121), [document.changeFilterOrder()](#_bookmark149), [document.disableAllFilters()](#_bookmark170), [document.disableFilter()](#_bookmark171), [document.enableFilter()](#_bookmark184), [document.getFilters()](#_bookmark207), [document.removeFilter()](#_bookmark255), [Filter object](#_bookmark425)
