## symbolInstance.visible

#### Availability

Flash CS5.5 Professional.

#### Usage

symbolInstance.visible

#### Description

Property; a boolean value that sets the Visible property of an object to on (true) or off (false).

#### Example

The following example sets the visibility of the first item in the first frame of the first layer to false:

```javascript
fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements[0].visible = false;

```