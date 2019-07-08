## document.enableFilter()

#### Availability

Flash 8.

#### Usage

document.enableFilter(filterIndex)

#### Parameters

**filterIndex** An integer specifying the zero-based index of the filter in the Filters list to enable.

#### Returns

Nothing.

#### Description

Method; enables the specified filter for the selected objects.

#### Example

```javascript
The following example enables the second filter of the selected objects:
fl.getDocumentDOM().enableFilter(1);

```
#### See also

[document.addFilter()](#_bookmark121), [document.changeFilterOrder()](#_bookmark149), [document.disableFilter()](#_bookmark171), [document.enableAllFilters()](#_bookmark183), [document.getFilters()](#_bookmark207), [document.removeFilter()](#_bookmark255), [Filter object](#_bookmark425)
