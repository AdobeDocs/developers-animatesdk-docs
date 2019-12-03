## symbolItem.sourceFilePath

#### Availability

Flash MX 2004.

#### Usage

*symbolItem.sourceFilePath*

#### Description

Property; a string that specifies the path for the source FLA file as a file:/// URI. The path must be an absolute path, not a relative path. This property is used for shared library symbols.

#### Example

The following example shows the value of the sourceFilePath property in the Output panel:

```javascript
fl.trace(fl.getDocumentDOM().library.items[0].sourceFilePath);

```