## document.canTestScene()

#### Availability

Flash MX 2004.

#### Usage

document.canTestScene()

#### Parameters

None.

#### Returns

A Boolean value: true if you can use the document.testScene() method successfully; false otherwise.

#### Description

Method; determines whether you can use the [document.testScene()](../Document_object/docu5979.md) method successfully.

#### Example

```javascript
The following example first tests whether fl.getDocumentDOM().testScene() can be used successfully. If so, it calls the method.
if(fl.getDocumentDOM().canTestScene()){ fl.getDocumentDOM().testScene();
}

```
#### See also

[document.canTestMovie()](../Document_object/docume27.md), [document.testMovie()](../Document_object/docu5948.md)
