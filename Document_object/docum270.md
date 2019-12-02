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

[document.addFilter()](../Document_object/documen3.md), [document.changeFilterOrder()](../Document_object/docume29.md), [document.disableFilter()](../Document_object/docume47.md), [document.getFilters()](../Document_object/docume79.md), [document.removeAllFilters()](../Document_object/docum240.md), [Filter object](../Filter_object/filter_summary.md)
