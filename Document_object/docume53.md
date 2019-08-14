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
The following example checks the document for persistent data with the name "myData": var hasData = fl.getDocumentDOM().documentHasData("myData");

```
#### See also

[document.addDataToDocument()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/documen1.md), [document.getDataFromDocument()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docume76.md), [document.removeDataFromDocument()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docum250.md)
