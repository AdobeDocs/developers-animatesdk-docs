## document.renameScene()

#### Availability

Flash MX 2004.

#### Usage

document.renameScene(name)

#### Parameters

**name** A string that specifies the new name of the scene.

#### Returns

A Boolean value: true if the name is changed successfully; false otherwise. If the new name is not unique, for example, the method returns false.

#### Description

Method; renames the currently selected scene in the Scenes panel. The new name for the selected scene must be unique.

#### Example

```javascript
The following example renames the current scene to "new name":
var success = fl.getDocumentDOM().renameScene("new name");

```