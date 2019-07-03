## document.addDataToDocument()

#### Availability

Flash MX 2004.

#### Usage

document.addDataToDocument(name, type, data)

#### Parameters

**name** A string that specifies the name of the data to add.
>
**type** A string that defines the type of data to add. Acceptable values are "integer", "integerArray", "double", "doubleArray", "string", and "byteArray".
>
**data** The value to add. Valid types depend on the *type* parameter.

#### Returns

Nothing.

#### Description

Method; stores specified data with a document. Data is written to the FLA file and is available to JavaScript when the file reopens.

#### Example

```
The following example adds an integer value of 12 to the current document:
fl.getDocumentDOM().addDataToDocument("myData", "integer", 12);
The following example returns the value of the data named "myData" and displays the result in the Output panel:
fl.trace(fl.getDocumentDOM().getDataFromDocument("myData"));

```
#### See also

[document.getDataFromDocument()](#_bookmark204), [document.removeDataFromDocument()](#_bookmark253)
