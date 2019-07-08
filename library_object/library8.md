## library.getSelectedItems()

#### Availability

Flash MX 2004.

#### Parameters

None.

#### Returns

An array of values for all currently selected items in the library.

#### Description

Method; gets the array of all currently selected items in the library.

#### Example

```javascript
The following example stores the array of currently selected library items (in this case, several audio files) in the
selItems variable and then changes the sampleRate property of the first audio file in the array to 11 kHz:
var selItems = fl.getDocumentDOM().library.getSelectedItems(); selItems\[0\].sampleRate = "11 kHz";

```