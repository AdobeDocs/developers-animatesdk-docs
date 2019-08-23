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

[document.addFilter()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/documen3.md), [document.changeFilterOrder()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume29.md), [document.disableFilter()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume47.md), [document.enableAllFilters()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume58.md), [document.getFilters()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume79.md), [document.removeFilter()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docum270.md), [Filter object](#!AdobeDocs/developers-animatesdk-docs/test/Filter_object/filter_summary.md)
