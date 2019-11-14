## compilerErrors.save()

#### Availability

Flash CS3 Professional.

#### Usage

compilerErrors.save(fileURI \[, bAppendToFile \[, bUseSystemEncoding\]\])

#### Parameters

**fileURI** A string, expressed as a file:/// URI, that specifies the filename for the saved file. If *fileURI* already exists, and you haven’t specified a value of true for *bAppendToFile*, *fileURI* is overwritten without warning.
**bAppendToFile** An optional Boolean value that specifies whether the contents of the Compiler Errors panel should be appended to *fileURI* (true) or not (false). The default value is false.
**bUseSystemEncoding** An optional Boolean value that specifies whether to save the Compiler Errors panel text using the system encoding. If this value is false (the default), the Compiler Errors panel text is saved using UTF-8 encoding, with Byte Order Mark characters at the beginning of the text. The default value is false.

#### Returns

Nothing.

#### Description

Method; saves the contents of the Compiler Errors panel to a local text file.

#### Example

```javascript
The following example saves the contents of the Compiler Errors panel to a file named errors.log in the C:\\tests folder:
fl.compilerErrors.save("file:///c\|/tests/errors.log");

```
#### See also

[compilerErrors.clear()](../compilerErrors_object/compilerErrors.md)
