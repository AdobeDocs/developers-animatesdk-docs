## document.documentHasData()

#### Availability

Flash MX 2004.

#### Usage

document.documentHasData(name)

#### Parameters

**name** A string that specifies the name of the data to check.

#### Returns

A Boolean value: true if the document has persistent data; false otherwise.

#### Description

Method; checks the document for persistent data with the specified name.

#### Example

```javascript
The following example checks the document for persistent data with the name "myData": 
var hasData = fl.getDocumentDOM().documentHasData("myData");

```
#### See also

[document.addDataToDocument()](../Document_object/documen1.md), [document.getDataFromDocument()](../Document_object/docume76.md), [document.removeDataFromDocument()](../Document_object/docum250.md)
