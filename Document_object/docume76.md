## document.getDataFromDocument()

#### Availability

Flash MX 2004.

#### Usage

document.getDataFromDocument(name)

#### Parameters

**name** A string that specifies the name of the data to return.

#### Returns

The specified data.

#### Description

Method; retrieves the value of the specified data. The type returned depends on the type of data that was stored.

#### Example


The following example adds an integer value of 12 to the current document and uses this method to display the value in the Output panel:

```javascript
fl.getDocumentDOM().addDataToDocument("myData", "integer", 12); 
fl.trace(fl.getDocumentDOM().getDataFromDocument("myData"));

```
#### See also

[document.addDataToDocument()](../Document_object/documen1.md), [document.documentHasData()](../Document_object/docume53.md), [document.removeDataFromDocument()](../Document_object/docum250.md)
