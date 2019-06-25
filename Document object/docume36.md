## document.convertToSymbol()

#### Availability

> Flash MX 2004.

#### Usage

> document.convertToSymbol(type, name, registrationPoint)

#### Parameters

> **type** A string that specifies the type of symbol to create. Acceptable values are "movie clip", "button", and
>
> "graphic".
>
> **name** A string that specifies the name for the new symbol, which must be unique. You can submit an empty string to have this method create a unique symbol name for you.
>
> **registration point** Specifies the point that represents the 0,0 location for the symbol. Acceptable values are: "top left", "top center", "top right", "center left", "center", "center right", "bottom left", "bottom center", and "bottom right".

#### Returns

> An object for the newly created symbol, or null if it cannot create the symbol.

#### Description

> Method; converts the selected Stage item(s) to a new symbol. For information on defining linkage and shared asset properties for a symbol, see [Item object](#_bookmark658).

#### Example

> The following examples create a movie clip symbol with a specified name, a button symbol with a specified name, and a movie clip symbol with a default name:
>
> newMc = fl.getDocumentDOM().convertToSymbol("movie clip", "mcSymbolName", "top left"); newButton = fl.getDocumentDOM().convertToSymbol("button", "btnSymbolName", "bottom right"); newClipWithDefaultName = fl.getDocumentDOM().convertToSymbol("movie clip", "", "top left");
