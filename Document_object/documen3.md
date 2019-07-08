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

[document.changeFilterOrder()](#_bookmark149), [document.disableFilter()](#_bookmark171), [document.enableFilter()](#_bookmark184), [document.getFilters()](#_bookmark207), [document.removeFilter()](#_bookmark255), [document.setBlendMode()](#_bookmark278), [document.setFilterProperty()](#_bookmark288)
