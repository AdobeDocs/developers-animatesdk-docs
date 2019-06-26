## item.linkageImportForRS

#### Availability

> Flash MX 2004.

#### Usage

> item.linkageImportForRS

#### Description

> Property; a Boolean value: if true, the item is imported for run-time sharing. If this property is set to true, both [item.linkageExportForAS](#_bookmark669) and [item.linkageExportForRS](#_bookmark670) must be set to false. Also, you must specify an identifier ([item.linkageIdentifier](#_bookmark672)) and a URL ([item.linkageURL](#item.linkageURL)).

#### Example

> The following example sets this property to true for the specified library item:
>
> fl.getDocumentDOM().library.items\[0\].linkageImportForRS = true;

<span id="item.linkageURL" class="anchor"></span>
