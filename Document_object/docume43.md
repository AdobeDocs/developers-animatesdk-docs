## document.deleteScene()

#### Availability

Flash MX 2004.

#### Usage

document.deleteScene()

#### Parameters

None.

#### Returns

A Boolean value: true if the scene is successfully deleted; false otherwise.

#### Description

Method; deletes the current scene ([Timeline object](#!AdobeDocs/developers-animatesdk-docs/test/Timeline_object/timeline_summary.md)) and, if the deleted scene was not the last one, sets the next scene as the current Timeline object. If the deleted scene was the last one, it sets the first object as the current Timeline object. If only one Timeline object (scene) exists, it returns the value false.

#### Example

```javascript
Assuming there are three scenes (Scene0, Scene1, and Scene2) in the current document, the following example makes Scene2 the current scene and then deletes it:
fl.getDocumentDOM().editScene(2);
var success = fl.getDocumentDOM().deleteScene();

```