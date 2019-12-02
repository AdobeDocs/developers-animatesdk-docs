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

```javascript
The following example disables the first and third filters (index values of 0 and 2) in the Filters list from the selected objects:
fl.getDocumentDOM().disableFilter(0); 
fl.getDocumentDOM().disableFilter(2);

```
#### See also

[document.addFilter()](../Document_object/documen3.md), [document.changeFilterOrder()](../Document_object/docume29.md), [document.disableAllFilters()](../Document_object/docume46.md), [document.disableOtherFilters()](../Document_object/docume48.md), [document.enableFilter()](../Document_object/docume59.md), [document.getFilters()](../Document_object/docume79.md), [document.removeFilter()](../Document_object/docum270.md), [Filter object](../Filter_object/filter_summary.md)

<span id="document.disableOtherFilters()" class="anchor"></span>
