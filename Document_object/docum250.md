## document.removeDataFromDocument()

#### Availability

Flash MX 2004.

#### Usage

document.removeDataFromDocument(name)

#### Parameters

**name** A string that specifies the name of the data to remove.

#### Returns

Nothing.

#### Description

Method; removes persistent data with the specified name that has been attached to the document.

#### Example

```javascript
The following example removes from the document the persistent data named "myData": fl.getDocumentDOM().removeDataFromDocument("myData");

```
#### See also

[document.addDataToDocument()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/documen1.md), [document.documentHasData()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docume53.md), [document.getDataFromDocument()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docume76.md)
