## mouseMove()

#### Availability

Flash MX 2004.

#### Usage

function mouseMove( [ pt ] ) {
// statements
}

#### Parameters

**pt** A point that specifies the current location of the mouse. It is passed to the function whenever the mouse moves, which tracks the mouse location. If the Stage is in edit or edit-in-place mode, the point coordinates are relative to the object being edited. Otherwise, the point coordinates are relative to the Stage. This parameter is optional.

#### Returns

Nothing.

#### Description

Function; called whenever the extensible tool is active and the mouse moves over a specified point on the Stage. The mouse button can be down or up.

#### Example

The following examples show how this function can be used. The first example displays a message in the Output panel that the mouse is being moved. The second example displays the *x* and *y* coordinates of the mouse’s location as it moves.

```javascript
function mouseMove() { 
        fl.trace("moving");
}
function mouseMove(pt) {
    fl.trace("x = "+ pt.x + " :: y = " + pt.y);
}

```