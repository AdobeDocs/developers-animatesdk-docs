## library.selectAll()

#### Availability

> Flash MX 2004.

#### Usage

> library.selectAll(\[bSelectAll\])

#### Parameters

> **bSelectAll** A Boolean value that specifies whether to select or deselect all items in the library. Omit this parameter or use the default value of true to select all the items in the library; false deselects all library items. This parameter is optional.

#### Returns

> Nothing.

#### Description

> Method; selects or deselects all items in the library.

#### Example

> The following examples select all the items in the library:
>
> fl.getDocumentDOM().library.selectAll(); fl.getDocumentDOM().library.selectAll(true);
>
> The following examples deselect all the items in the library:
>
> fl.getDocumentDOM().library.selectAll(false); fl.getDocumentDOM().library.selectNone();
