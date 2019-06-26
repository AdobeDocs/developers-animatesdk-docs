## document.getDataFromDocument()

#### Availability

> Flash MX 2004.

#### Usage

> document.getDataFromDocument(name)

#### Parameters

> **name** A string that specifies the name of the data to return.

#### Returns

> The specified data.

#### Description

> Method; retrieves the value of the specified data. The type returned depends on the type of data that was stored.

#### Example

> The following example adds an integer value of 12 to the current document and uses this method to display the value in the Output panel:
>
> fl.getDocumentDOM().addDataToDocument("myData", "integer", 12); fl.trace(fl.getDocumentDOM().getDataFromDocument("myData"));

#### See also

> [document.addDataToDocument()](#_bookmark119), [document.documentHasData()](#_bookmark178), [document.removeDataFromDocument()](#_bookmark253)
