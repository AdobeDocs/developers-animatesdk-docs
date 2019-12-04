## item.linkageIdentifier

#### Availability

Animate MX 2004.

#### Usage

item.linkageIdentifier

#### Description

Property; a string that specifies the name Animate will use to identify the asset when linking to the destination SWF file. Animate ignores this property if [item.linkageImportForRS](../Item_object/item11.md), [item.linkageExportForAS](../Item_object/item7.md), and [item.linkageExportForRS](../Item_object/item8.md) are set to false. Conversely, this property must be set when any of those properties are set to true.

#### Example

The following example specifies that the string my\_mc will be used to identify the library item when it is linked to the destination SWF file to which it is being exported:

```javascript
fl.getDocumentDOM().library.items[0].linkageIdentifier = "my_mc";
```
#### See also

[item.linkageURL](../Item_object/item12.md)

<span id="item.linkageImportForRS" class="anchor"></span>
