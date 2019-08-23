## bitmapItem.compressionType

#### Availability

Flash MX 2004.

#### Usage

bitmapItem.compressionType

#### Description

Property; a string that determines the type of image compression applied to the bitmap. Acceptable values are "photo" or "lossless". If the value of bitmapItem.useImportedJPEGQuality is false, "photo" corresponds to JPEG with a quality from 0 to 100; if bitmapItem.useImportedJPEGQuality is true, "photo" corresponds to JPEG using the default document quality value. The value "lossless" corresponds to GIF or PNG format (see [bitmapItem.useImportedJPEGQuality](#!AdobeDocs/developers-animatesdk-docs/master/BitmapItem_object/bitmapIt13.md)).

#### Example

```javascript
The following code sets the compressionType property of the first item in the library of the current document to
"photo":
fl.getDocumentDOM().library.items\[0\].compressionType = "photo"; alert(fl.getDocumentDOM().library.items\[0\].compressionType);

```