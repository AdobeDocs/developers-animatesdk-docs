## document.addFilter()

#### Availability

Flash 8.

#### Usage

document.addFilter(filterName)

#### Parameters

**filterName** A string specifying the filter to be added to the Filters list and enabled for the selected objects. Acceptable values are "adjustColorFilter", "bevelFilter", "blurFilter", "dropShadowFilter", "glowFilter", "gradientBevelFilter", and "gradientGlowFilter".

#### Returns

Nothing.

#### Description

Method; applies a filter to the selected objects and places the filter at the end of the Filters list.

#### Example

```javascript
The following example applies a glow filter to the selected objects:
fl.getDocumentDOM().addFilter("glowFilter");

```
#### See also

[document.changeFilterOrder()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume29.md), [document.disableFilter()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume47.md), [document.enableFilter()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume59.md), [document.getFilters()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume79.md), [document.removeFilter()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docum270.md), [document.setBlendMode()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docum460.md), [document.setFilterProperty()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docum520.md)
