## item.linkageExportForRS

#### Availability

Flash MX 2004.

#### Usage

item.linkageExportForRS

#### Description

Property; a Boolean value. If this property is true, the item is exported for run-time sharing. You can also set the
[item.linkageExportForAS](../Item_object/item7.md) and [item.linkageExportInFirstFrame](../Item_object/item9.md) properties to true.
If you set this property to true, the [item.linkageImportForRS](../Item_object/item11.md) property must be set to false. Also, you must specify an identifier ([item.linkageIdentifier](../Item_object/item10.md)) and a URL ([item.linkageURL](../Item_object/item12.md)).

#### Example

```javascript
The following example sets this property for the specified library item:
fl.getDocumentDOM().library.items\[0\].linkageExportForRS = true;

<span id="item.linkageExportInFirstFrame" class="anchor"></span
```