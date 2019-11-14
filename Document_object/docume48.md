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

[document.addFilter()](../Document_object/documen3.md), [document.changeFilterOrder()](../Document_object/docume29.md), [document.disableAllFilters()](../Document_object/docume46.md), [document.disableFilter()](../Document_object/docume47.md), [document.enableFilter()](../Document_object/docume59.md), [document.getFilters()](../Document_object/docume79.md), [document.removeFilter()](../Document_object/docum270.md), [Filter object](../Filter_object/filter_summary.md)
