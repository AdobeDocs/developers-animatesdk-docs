## document.addNewScene()

#### Availability

Flash MX 2004.

#### Usage

document.addNewScene(\[name\])

#### Parameters

**name** Specifies the name of the scene. If you do not specify a name, a new scene name is generated.

#### Returns

A Boolean value: true if the scene is added successfully; false otherwise.

#### Description

Method; adds a new scene ([Timeline object](#_bookmark1030)) as the next scene after the currently selected scene and makes the new scene the currently selected scene. If the specified scene name already exists, the scene is not added and the method returns an error.

#### Example

```
The following example adds a new scene named myScene after the current scene in the current document. The variable
success will be true when the new scene is created; false otherwise.
var success = fl.getDocumentDOM().addNewScene("myScene");
The following example adds a new scene using the default naming convention. If only one scene exists, the newly created scene is named "Scene 2".
fl.getDocumentDOM().addNewScene();

```