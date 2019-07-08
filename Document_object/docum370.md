## document.save()

#### Availability

Flash MX 2004.

#### Usage

document.save(\[bOkToSaveAs\])

#### Parameters

**bOkToSaveAs** An optional parameter that, if true or omitted, and the file was never saved, opens the Save As dialog box. If false and the file was never saved, the file is not saved.

#### Returns

A Boolean value: true if the save operation completes successfully; false otherwise.

#### Description

Method; saves the document in its default location. This method is equivalent to selecting File \Save. To specify a name for the file (instead of saving it with the same name), use [fl.saveDocument()](#_bookmark534).
***Note:** If the file is new and has not been modified or saved, or if the file has not been modified since the last time it was saved, this method has no effect and false is returned. To allow an unsaved or unmodified file to be saved, use [fl.saveDocumentAs()](#_bookmark536).*

#### Example

```javascript
The following example saves the current document in its default location:
fl.getDocumentDOM().save();

```
#### See also

[fl.saveAll()](#_bookmark532), [fl.saveDocument()](#_bookmark534), [fl.saveDocumentAs()](#_bookmark536)
