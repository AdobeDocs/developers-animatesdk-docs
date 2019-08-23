## setCursor()

#### Availability

Flash MX 2004.

#### Usage

function setCursor() {
// statements
}

#### Parameters

None.

#### Returns

Nothing.

#### Description

Function; called when the extensible tool is active and the mouse moves, to allow the script to set custom pointers. The script should call tools.setCursor() to specify the pointer to use. For a list that shows which pointers correspond to which integer values, see [tools.setCursor()](#!AdobeDocs/developers-animatesdk-docs/master/Tools_object/tools8.md).

#### Example

```javascript
function setCursor() { fl.tools.setCursor( 1 );
}

```