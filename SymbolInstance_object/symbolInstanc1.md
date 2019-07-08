## symbolInstance.actionScript - dropped

#### Availability

Flash MX 2004. *Dropped in Adobe Animate*.

#### Usage

symbolInstance.actionScript

#### Description

*Dropped in Adobe Animate.*
Property; a string that specifies the actions assigned to the symbol. This applies only to movie clip and button instances. For a graphic symbol instance, the value returns undefined.

#### Example

```javascript
The following example assigns an onClipEvent action to the first item in the first frame of the first layer in the timeline:
fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\].actionScript
= "onClipEvent(enterFrame) {trace('movie clip enterFrame');}";

```