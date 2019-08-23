## item.linkageImportForRS

#### Availability

Flash MX 2004.

#### Usage

item.linkageImportForRS

#### Description

Property; a Boolean value: if true, the item is imported for run-time sharing. If this property is set to true, both [item.linkageExportForAS](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item7.md) and [item.linkageExportForRS](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item8.md) must be set to false. Also, you must specify an identifier ([item.linkageIdentifier](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item10.md)) and a URL ([item.linkageURL](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item12.md)).

#### Example

```javascript
The following example sets this property to true for the specified library item:
fl.getDocumentDOM().library.items\[0\].linkageImportForRS = true;

<span id="item.linkageURL" class="anchor"></span
```