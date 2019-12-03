## item.linkageExportForAS

#### Availability

Flash MX 2004.

#### Usage

item.linkageExportForAS

#### Description

Property; a Boolean value. If this property is true, the item is exported for ActionScript. You can also set the
[item.linkageExportForRS](../Item_object/item8.md) and [item.linkageExportInFirstFrame](../Item_object/item9.md) properties to true.
If you set this property to true, the [item.linkageImportForRS](../Item_object/item11.md) property must be set to false. Also, you must specify an identifier ([item.linkageIdentifier](../Item_object/item10.md)) and a URL ([item.linkageURL](../Item_object/item12.md)).

#### Example

The following example sets this property for the specified library item:

```javascript
fl.getDocumentDOM().library.items[0].linkageExportForAS = true;
```
<span id="item.linkageExportForRS" class="anchor"></span>
