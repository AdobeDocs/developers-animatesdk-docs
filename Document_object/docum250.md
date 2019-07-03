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

```
The following example removes from the document the persistent data named "myData": fl.getDocumentDOM().removeDataFromDocument("myData");

```
#### See also

[document.addDataToDocument()](#_bookmark119), [document.documentHasData()](#_bookmark178), [document.getDataFromDocument()](#_bookmark204)
