## document.exportInstanceToLibrary()

#### Availability

Flash CS6.

#### Usage

document.exportInstanceToLibrary(frameNumber, bitmapName)

#### Parameters

**frameNumber** Integer indicating the frame to be exported.
**bitmapName** A string representing the name of the bitmap to be added to the Library.

#### Returns

Nothing.

#### Description

Method; Exports a selected instance of a movie clip, graphic, or button symbol on the Stage to a bitmap in Library.

#### Example

```javascript
The following example exports the selected item on frame 1 to the library and assigns the new bitmap the name "myTestBitmap":
fl.getDocumentDOM().exportInstanceToLibrary(1, "myTestBitmap");

```