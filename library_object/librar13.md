## library.renameItem()

#### Availability

> Flash MX 2004.

#### Usage

> library.renameItem(name)

#### Parameters

> **name** A string that specifies a new name for the library item.

#### Returns

> A Boolean value of true if the name of the item changes successfully, false otherwise. If multiple items are selected, no names are changed, and the return value is false (to match user interface behavior).

#### Description

> Method; renames the currently selected library item in the Library panel.

#### Example

> The following example renames the currently selected library item to new name: fl.getDocumentDOM().library.renameItem("new name");
