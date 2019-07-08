## document.removeFilter()

#### Availability

Flash 8.

#### Usage

document.removeFilter(filterIndex)

#### Parameters

**filterIndex** An integer specifying the zero-based index of the filter to remove from the selected objects.

#### Returns

Nothing.

#### Description

Method; removes the specified filter from the Filters list of the selected objects.

#### Example

```javascript
The following example removes the first filter (index value 0) from the Filters list of the selected objects:
fl.getDocumentDOM().removeFilter(0);

```
#### See also

[document.addFilter()](#_bookmark121), [document.changeFilterOrder()](#_bookmark149), [document.disableFilter()](#_bookmark171), [document.getFilters()](#_bookmark207), [document.removeAllFilters()](#_bookmark252), [Filter object](#_bookmark425)
