## symbolItem.lastModifiedDate

#### Availability

> Flash Pro CS6.

#### Usage

> symbolItem.lastModifiedDate

#### Description

> Read-only property; a string that indicates the modification date of the symbol as a hexadecimal value, representing a date and time. This value is incremented every time a symbol's timeline is edited.

#### Example

> The following example returns the hexidecimal modification date of the first symbol in the Library:
>
> var item = fl.getDocumentDOM().library.items\[0\];
>
> fl.trace("name: " + item.name + ", date: " + item.lastModifiedDate);
>
> // name: Symbol 1, date: 4f273915
