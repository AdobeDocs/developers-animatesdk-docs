## mouseDown()

#### Availability

Flash MX 2004.

#### Usage

function mouseDown( \[ pt \] ) {
// statements
}

#### Parameters

**pt** A point that specifies the location of the mouse when the button is pressed. It is passed to the function when the mouse button is pressed. This parameter is optional.

#### Returns

Nothing.

#### Description

Function; called when the extensible tool is active and the mouse button is pressed while the pointer is over the Stage.

#### Example

```
The following examples show how this function can be used when the extensible tool is active. The first example displays a message in the Output panel that the mouse button was pressed. The second example displays the *x* and *y* coordinates of the mouse’s location when the button was pressed.
function mouseDown() {
fl.trace("Mouse button has been pressed");
}
function mouseDown(pt) {
fl.trace("x = "+ pt.x+" :: y = "+pt.y);
}

```