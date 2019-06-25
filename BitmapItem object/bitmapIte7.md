## bitmapItem.originalCompressionType

#### Availability

> Flash CS4 Professional.

#### Usage

> bitmapItem.originalCompressionType

#### Description

> Read-only property; a string that specifies whether the specified item was imported as an jpeg file. Possible values for this property are “photo” (for jpeg files) and “lossless” (for uncompressed file types such as GIF and PNG).

#### Example

> Assuming that the first item in the Library is a bitmap item, the following code displays "photo" if the file was imported into the Library as a jpeg file, or "lossless" if is was not:
>
> var libItem = fl.getDocumentDOM().library.items\[0\];
>
> fl.trace("Imported compression type = "+ libItem.originalCompressionType);

#### See also

> [bitmapItem.compressionType](#_bookmark52)
