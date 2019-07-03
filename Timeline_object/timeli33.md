## timeline.name

#### Availability

Flash MX 2004.

#### Usage

timeline.name

#### Description

Property; a string that specifies the name of the current timeline. This name is the name of the current scene, screen (slide or form), or symbol that is being edited.

#### Example

```
The following example retrieves the first scene name:
var sceneName = fl.getDocumentDOM().timelines\[0\].name; The following example sets the first scene name to FirstScene: fl.getDocumentDOM().timelines\[0\].name = "FirstScene";

```