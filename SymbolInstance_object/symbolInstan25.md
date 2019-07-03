## symbolInstance.symbolType

#### Availability

Flash MX 2004.

#### Usage

symbolInstance.symbolType

#### Description

Property; a string that specifies the type of symbol. This property is equivalent to the value for Behavior in the Create New Symbol and Convert To Symbol dialog boxes. Acceptable values are "button", "movie clip", and "graphic".

#### Example

```
The following example sets the first symbol in the first frame of the first layer in the timeline of the current document to behave as a graphic symbol:
fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\].symbolType = "graphic";

```