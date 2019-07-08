## document.swapElement()

#### Availability

Flash MX 2004.

#### Usage

document.swapElement(name)

#### Parameters

**name** A string that specifies the name of the library item to use.

#### Returns

Nothing.

#### Description

Method; swaps the current selection with the specified one. The selection must contain a graphic, button, movie clip, video, or bitmap. This method displays an error message if no object is selected or the given object could not be found.

#### Example

```javascript
The following example swaps the current selection with Symbol 1 from the library:
fl.getDocumentDOM().swapElement('Symbol 1');

```