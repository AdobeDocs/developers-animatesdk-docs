## item.linkageClassName

#### Availability

Flash MX 2004.

#### Usage

item.linkageClassName

#### Description

Property; a string that specifies the ActionScript 2.0 class that will be associated with the symbol. (To specify this value for an ActionScript 3.0 class, use [item.linkageBaseClass](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item5.md).)
For this property to be defined, the [item.linkageExportForAS](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item7.md) and/or [item.linkageExportForRS](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item8.md) properties must be set to true, and the [item.linkageImportForRS](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item11.md) property must be set to false.

#### Example

```javascript
The following example specifies that the ActionScript 2.0 class name associated with the first item in the library is
myClass:
fl.getDocumentDOM().library.items\[0\].linkageClassName = "myClass";

<span id="item.linkageExportForAS" class="anchor"></span
```