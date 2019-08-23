## document.mouseDblClk()

#### Availability

Flash MX 2004.

#### Usage

document.mouseDblClk(position, bAltDown, bShiftDown, bShiftSelect)

#### Parameters

**position** A pair of floating-point values that specify the *x* and *y* coordinates of the click in pixels.
**bAltdown** A Boolean value that records whether the Alt key is down at the time of the event: true for pressed; false
for not pressed.
**bShiftDown** A Boolean value that records whether the Shift key was down when the event occurred: true for pressed;
false for not pressed.
**bShiftSelect** A Boolean value that indicates the state of the application preference Shift select: true for on; false
for off.

#### Returns

Nothing.

#### Description

Method; performs a double mouse click from the Selection tool.

#### Example

```javascript
The following example performs a double mouse click at the specified location:
fl.getDocumentDOM().mouseDblClk({x:392.9, y:73}, false, false, true);

```
#### See also

[document.mouseClick()](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docum130.md)
