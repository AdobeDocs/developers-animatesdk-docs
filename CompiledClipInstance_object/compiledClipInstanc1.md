## compiledClipInstance.actionScript - dropped

#### Availability

Flash MX 2004. *Dropped in Adobe Animate*.

#### Usage

compiledClipInstance.actionScript

#### Description

*Dropped in Adobe Animate.*
Property; a string that represents the ActionScript for this instance; equivalent to [symbolInstance.actionScript -](#_bookmark918) [dropped](#_bookmark918).

#### Example

```
The following code assigns ActionScript to specified elements:
// Assign some ActionScript to a specified Button compiled clip instance. fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\]
.actionScript = "on(click) {trace('button is clicked');}";
// Assign some ActionScript to the currently selected Button compiled clip instance. fl.getDocumentDOM().selection\[0\].actionScript =
"on(click) {trace('button is clicked');}";

```