## bitmapItem.useImportedJPEGQuality

#### Availability

Flash MX 2004.

#### Usage

bitmapItem.useImportedJPEGQuality

#### Description

Property; a Boolean value that specifies whether to use the default imported JPEG quality (true) or not (false). Available only for JPEG compression.

#### Example

```
The following code sets the useImportedJPEGQuality property of the first item in the library of the current document to true:
fl.getDocumentDOM().library.items\[0\].useImportedJPEGQuality = true; alert(fl.getDocumentDOM().library.items\[0\].useImportedJPEGQuality);

```