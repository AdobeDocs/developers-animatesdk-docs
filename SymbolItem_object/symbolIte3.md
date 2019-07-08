## symbolItem.exportToLibrary()

#### Availability

Flash Pro CS6.

#### Usage

symbolItem.exportToLibrary(frameNumber, bitmapName)

#### Parameters

**frameNumber** An integer indicating the frame within the symbol to be exported.
**bitmapName** A string indicating the name of the new bitmap to be added to the Library.

#### Returns

Nothing.

#### Description

Method; exports a frame from the selected instance of movie clip, graphic, or button symbol on the Stage to a bitmap in Library.

#### Example

```javascript
The following example exports the first frame of the currently selected symbol instance to a new bitmap in the library that will be called "mytestBitmap":
fl.getDocumentDOM().library.item\[0\].exportToLibrary(1, "mytestBitmap");

```