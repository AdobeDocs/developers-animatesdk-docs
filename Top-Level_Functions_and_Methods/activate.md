## activate()

#### Availability

Flash MX 2004.

#### Usage

function activate() {
// statements
}

#### Parameters

None.

#### Returns

Nothing.

#### Description

Function; called when the extensible tool becomes active (that is, when the tool is selected in the Tools panel). Use this function to perform any initialization tasks the tool requires.

#### Example

```javascript
The following example sets the value of [tools.activeTool](../Tools_object/tools.md) when the extensible tool is selected in the Tools panel:
function activate() {
var theTool = fl.tools.activeTool
}

```
#### See also

[tools.activeTool](../Tools_object/tools.md)
