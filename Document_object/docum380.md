## document.saveAndCompact() - dropped

#### Availability

Flash MX 2004. *Dropped in Flash Professional CS6.*

#### Usage

document.saveAndCompact(\[bOkToSaveAs\])

#### Parameters

**bOkToSaveAs** An optional parameter that, if true or omitted and the file was never saved, opens the Save As dialog box. If false and the file was never saved, the file is not saved. The default value is true.

#### Returns

A Boolean value: true if the save-and-compact operation completes successfully; false otherwise.

#### Description

*Dropped in Flash Professional CS6.*

#### Example

```javascript
The following example saves and compacts the current document:
fl.getDocumentDOM().saveAndCompact();

```
#### See also

[document.save()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docum370.md), [fl.saveDocumentAs()](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl65.md)/fl65.md), [fl.saveDocument()](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl64.md)/fl64.md), [fl.saveAll()](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl63.md)/fl63.md)
