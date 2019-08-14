## outputPanel.trace()

#### Availability

Flash MX 2004.

#### Usage

outputPanel.trace(message)

#### Parameters

**message** A string that contains the text to add to the Output panel.

#### Returns

Nothing.

#### Description

Method; sends a text string to the Output panel, terminated by a new line, and displays the Output panel if it is not already visible. This method is identical to [fl.trace()](#!AdobeDocs/developers-animatesdk-docs/master/flash_object_(fl)/fl77.md), and works in the same way as the trace() statement in ActionScript.
To send a blank line, use outputPanel.trace("") or outputPanel.trace("\\n"). You can use the latter command inline, making \\n a part of the *message* string.

#### Example

```javascript
The following example displays several lines of text in the Output panel:
fl.outputPanel.clear(); fl.outputPanel.trace("Hello World!!!"); var myPet = "cat";
fl.outputPanel.trace("\\nI have a " + myPet); fl.outputPanel.trace(""); fl.outputPanel.trace("I love my " + myPet);
fl.outputPanel.trace("Do you have a " + myPet +"?");

```