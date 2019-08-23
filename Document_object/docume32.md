## document.clipPaste()

#### Availability

Flash MX 2004.

#### Usage

document.clipPaste(\[bInPlace\])

#### Parameters

**bInPlace** A Boolean value that, when set to true, causes the method to perform a paste-in-place operation. The default value is false, which causes the method to perform a paste operation to the center of the document. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; pastes the contents of the Clipboard into the document.

#### Example

```javascript
The following example pastes the Clipboard contents to the center of the document:
fl.getDocumentDOM().clipPaste();
The following example pastes the Clipboard contents in place in the current document:
fl.getDocumentDOM().clipPaste(true);

```
#### See also

[document.clipCopy()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume30.md), [document.clipCut()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume31.md), [fl.clipCopyString()](#!AdobeDocs/developers-animatesdk-docs/test/flash_object_(fl)/fl6.md)/fl6.md)
