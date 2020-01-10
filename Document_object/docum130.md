## document.mouseClick()

#### Availability

Flash MX 2004.

#### Usage

document.mouseClick(position, bToggleSel, bShiftSel)

#### Parameters

**position** A pair of floating-point values that specify the *x* and *y* coordinates of the click in pixels.
**bToggleSel** A Boolean value that specifies the state of the Shift key: true for pressed; false for not pressed.
**bShiftSel** A Boolean value that specifies the state of the application preference Shift select: true for on; false for off.

#### Returns

Nothing.

#### Description

Method; performs a mouse click from the Selection tool.

#### Example


The following example performs a mouse click at the specified location:
```javascript
fl.getDocumentDOM().mouseClick({x:300, y:200}, false, false);

```
#### See also

[document.mouseDblClk()](../Document_object/docum140.md)

<span id="document.mouseDblClk()" class="anchor"></span>
