## item.linkageExportForAS

#### Availability

Flash MX 2004.

#### Usage

item.linkageExportForAS

#### Description

Property; a Boolean value. If this property is true, the item is exported for ActionScript. You can also set the
>
[item.linkageExportForRS](#item.linkageExportForRS) and [item.linkageExportInFirstFrame](#_bookmark671) properties to true.
>
If you set this property to true, the [item.linkageImportForRS](#_bookmark673) property must be set to false. Also, you must specify an identifier ([item.linkageIdentifier](#_bookmark672)) and a URL ([item.linkageURL](#_bookmark674)).

#### Example

```
The following example sets this property for the specified library item:
fl.getDocumentDOM().library.items\[0\].linkageExportForAS = true;

<span id="item.linkageExportForRS" class="anchor"></span
```