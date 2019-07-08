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

[document.save()](#_bookmark266), [fl.saveDocumentAs()](#_bookmark536), [fl.saveDocument()](#_bookmark534), [fl.saveAll()](#_bookmark532)
