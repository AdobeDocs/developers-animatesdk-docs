## mouseUp()

#### Availability

Flash MX 2004.

#### Usage

function mouseUp() {
// statements
}

#### Parameters

None.

#### Returns

Nothing.

#### Description

Function; called whenever the extensible tool is active and the mouse button is released after being pressed on the Stage.

#### Example

The following example displays a message in the Output panel when the extensible tool is active and the mouse button is released.

```javascript
function mouseUp() { 
    fl.trace("mouse is up");
}

```