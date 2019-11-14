## keyDown()

#### Availability

Flash MX 2004.

#### Usage

function keyDown() {
// statements
}

#### Parameters

None.

#### Returns

Nothing.

#### Description

Function; called when the extensible tool is active and the user presses a key. The script should call
[tools.getKeyDown()](../Tools_object/tools4.md) to determine which key was pressed.

#### Example

```javascript
The following example displays information about which key was pressed when the extensible tool is active and the user presses a key.
function keyDown() {
fl.trace("key " + fl.tools.getKeyDown() + " was pressed");
}

```
#### See also

[keyUp()](../Top-Level_Functions_and_Methods/keyUp.md)), [tools.getKeyDown()](../Tools_object/tools4.md)

<span id="keyUp()" class="anchor"></span>
