## item.linkageIdentifier

#### Availability

Flash MX 2004.

#### Usage

item.linkageIdentifier

#### Description

Property; a string that specifies the name Flash will use to identify the asset when linking to the destination SWF file. Flash ignores this property if [item.linkageImportForRS](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item11.md), [item.linkageExportForAS](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item7.md), and [item.linkageExportForRS](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item8.md) are set to false. Conversely, this property must be set when any of those properties are set to true.

#### Example

```javascript
The following example specifies that the string my\_mc will be used to identify the library item when it is linked to the destination SWF file to which it is being exported:
fl.getDocumentDOM().library.items\[0\].linkageIdentifier = "my\_mc";

```
#### See also

[item.linkageURL](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item12.md)

<span id="item.linkageImportForRS" class="anchor"></span>
