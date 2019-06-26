## item.hasData()

#### Availability

> Flash MX 2004.

#### Usage

> item.hasData(name)

#### Parameters

> **name** A string that specifies the name of the data to check for in the library item.

#### Returns

> A Boolean value: true if the specified data exists; false otherwise.

#### Description

> Method; determines whether the library item has the named data.

#### Example

> The following example shows a message in the Output panel if the first item in the library contains data named myData:
>
> if (fl.getDocumentDOM().library.items\[0\].hasData("myData")){ fl.trace("Yep, it's there!");
>
> }
