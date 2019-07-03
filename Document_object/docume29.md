## document.changeFilterOrder()

#### Availability

Flash 8.

#### Usage

document.changeFilterOrder(oldIndex, newIndex)

#### Parameters

**oldIndex** An integer that represents the current zero-based index position of the filter you want to reposition in the Filters list.
>
**newIndex** An integer that represents the new index position of the filter in the list.

#### Returns

Nothing.

#### Description

Method; changes the index of the filter in the Filters list. Any filters above or below *newIndex* are shifted up or down accordingly. For example, using the filters shown below, if you issue the command fl.getDocumentDOM().changeFilterOrder(3, 0), the filters are rearranged as follows:

| **Before**                                               | **After**                                                |
|----------------------------------------------------------|----------------------------------------------------------|
| blurFilterdropShadowFilterglowFiltergradien tBevelFilter | gradientBevelFilterblurFilterdropShadowFilterglo wFilter |

If you then issue the command fl.getDocumentDOM().changeFilterOrder(0, 2), the filters are rearranged as follows:

| **Before**                                               | **After**                                                |
|----------------------------------------------------------|----------------------------------------------------------|
| gradientBevelFilterblurFilterdropShadowFilt erglowFilter | blurFilterdropShadowFiltergradientBevelFilterglo wFilter |

#### Example

```
The following example moves the filter that is currently in the second position in the Filters list to the first position:
fl.getDocumentDOM().changeFilterOrder(1,0);

```
#### See also

[document.addFilter()](#_bookmark121), [document.disableFilter()](#_bookmark171), [document.enableFilter()](#_bookmark184), [document.getFilters()](#_bookmark207), [document.removeFilter()](#_bookmark255), [Filter object](#_bookmark425)
