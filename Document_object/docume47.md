## document.disableFilter()

#### Availability

Flash 8.

#### Usage

document.disableFilter(filterIndex)

#### Parameters

**filterIndex** An integer representing the zero-based index of the filter in the Filters list.

#### Returns

Nothing.

#### Description

Method; disables the specified filter in the Filters list.

#### Example

```
The following example disables the first and third filters (index values of 0 and 2) in the Filters list from the selected objects:
fl.getDocumentDOM().disableFilter(0); fl.getDocumentDOM().disableFilter(2);

```
#### See also

[document.addFilter()](#_bookmark121), [document.changeFilterOrder()](#_bookmark149), [document.disableAllFilters()](#_bookmark170), [document.disableOtherFilters()](#document.disableOtherFilters()), [document.enableFilter()](#_bookmark184), [document.getFilters()](#_bookmark207), [document.removeFilter()](#_bookmark255), [Filter object](#_bookmark425)

<span id="document.disableOtherFilters()" class="anchor"></span>
