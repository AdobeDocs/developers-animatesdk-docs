## item.linkageURL

#### Availability

Flash MX 2004.

#### Usage

item.linkageURL

#### Description

Property; a string that specifies the URL where the SWF file containing the shared asset is located. Animate ignores this property if [item.linkageImportForRS](../Item_object/item11.md), [item.linkageExportForAS](../Item_object/item7.md), and [item.linkageExportForRS](../Item_object/item8.md) are set to false. Conversely, this property must be set when any of those properties are set to true. You can specify a web URL or a filename in platform-dependent format (that is, forward slashes \[/\] or backward slashes \[\\\], depending on the platform).

#### Example

The following example specifies a linkage URL for the specified library item:

```javascript
fl.getDocumentDOM().library.items[0].linkageURL = "theShareSWF.swf";
```
#### See also

[item.linkageIdentifier](../Item_object/item10.md)
