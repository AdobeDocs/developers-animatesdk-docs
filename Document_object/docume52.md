## document.docClass

#### Availability

Flash CS3 Professional.

#### Usage

document.docClass

#### Description

Property; a string that specifies the top-level ActionScript 3.0 class associated with the document. If the document isn’t configured to use ActionScript 3.0, this property is ignored.

#### Example

```javascript
The following example specifies that the ActionScript 3.0 class associated with the document is com.mycompany.ManagerClass, which is defined in com/mycompany/ManagerClass.as:
var myDocument = fl.getDocumentDOM();
// set the property
myDocument.docClass = "com.mycompany.ManagerClass";
// get the property
fl.outputPanel.trace("document.docClass has been set to " + myDocument.docClass);

```
#### See also

[item.linkageBaseClass](#!AdobeDocs/developers-animatesdk-docs/master/Item_object/item5.md)
