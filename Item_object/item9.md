## item.linkageExportInFirstFrame

#### Availability

Flash MX 2004.

#### Usage

item.linkageExportInFirstFrame

#### Description

Property; a Boolean value. If true, the item is exported in the first frame; if false, the item is exported in the frame of the first instance. If the item does not appear on the Stage, it isn’t exported.
This property can be set to true only when [item.linkageExportForAS](../Item_object/item7.md) and/or [item.linkageExportForRS](../Item_object/item8.md) are set to true.

#### Example

The following example specifies that the specified library item is exported in the first frame:

```javascript
fl.getDocumentDOM().library.items[0].linkageExportInFirstFrame = true;
```