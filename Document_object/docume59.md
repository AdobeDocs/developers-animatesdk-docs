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


The following example enables the second filter of the selected objects:
```javascript
fl.getDocumentDOM().enableFilter(1);

```
#### See also

[document.addFilter()](../Document_object/documen3.md), [document.changeFilterOrder()](../Document_object/docume29.md), [document.disableFilter()](../Document_object/docume47.md), [document.enableAllFilters()](../Document_object/docume58.md), [document.getFilters()](../Document_object/docume79.md), [document.removeFilter()](../Document_object/docum270.md), [Filter object](../Filter_object/filter_summary.md)
