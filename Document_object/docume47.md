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
fl.getDocumentDOM().disableFilter(0); fl.getDocumentDOM().disableFilter(2);

```
#### See also

[document.addFilter()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/documen3.md), [document.changeFilterOrder()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume29.md), [document.disableAllFilters()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume46.md), [document.disableOtherFilters()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume48.md)), [document.enableFilter()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume59.md), [document.getFilters()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume79.md), [document.removeFilter()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docum270.md), [Filter object](#!AdobeDocs/developers-animatesdk-docs/test/Filter_object/filter_summary.md)

<span id="document.disableOtherFilters()" class="anchor"></span>
