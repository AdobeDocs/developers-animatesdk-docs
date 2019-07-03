## item.linkageIdentifier

#### Availability

Flash MX 2004.

#### Usage

item.linkageIdentifier

#### Description

Property; a string that specifies the name Flash will use to identify the asset when linking to the destination SWF file. Flash ignores this property if [item.linkageImportForRS](#item.linkageImportForRS), [item.linkageExportForAS](#_bookmark669), and [item.linkageExportForRS](#_bookmark670) are set to false. Conversely, this property must be set when any of those properties are set to true.

#### Example

```
The following example specifies that the string my\_mc will be used to identify the library item when it is linked to the destination SWF file to which it is being exported:
fl.getDocumentDOM().library.items\[0\].linkageIdentifier = "my\_mc";

```
#### See also

[item.linkageURL](#_bookmark674)

<span id="item.linkageImportForRS" class="anchor"></span>
