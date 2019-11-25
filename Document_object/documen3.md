## document.addFilter()

#### Availability

Flash 8.
Flash 8

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

[document.changeFilterOrder()](../Document_object/docume29.md), [document.disableFilter()](../Document_object/docume47.md), [document.enableFilter()](../Document_object/docume59.md), [document.getFilters()](../Document_object/docume79.md), [document.removeFilter()](../Document_object/docum270.md), [document.setBlendMode()](../Document_object/docum460.md), [document.setFilterProperty()](../Document_object/docum520.md)
