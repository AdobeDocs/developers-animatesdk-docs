## element.left

#### Availability

Flash MX 2004.

#### Usage

element.left

#### Description

Read-only property; a float value that represents the left side of the element. The value of element.left is relative to the upper left of the Stage for elements that are in a scene and is relative to the symbol’s registration point (also *origin point* or *zero point*) if the element is stored within a symbol. Use [document.setSelectionBounds()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docu9658.md) or [document.moveSelectionBy()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docum160.md) to set this property.

#### Example

```javascript
The following example illustrates how the value of this property changes when an element is moved:
// Select an element on the Stage and then run this script. var sel = fl.getDocumentDOM().selection\[0\];
fl.trace("Left (before) = " + sel.left); fl.getDocumentDOM().moveSelectionBy({x:100, y:0}); fl.trace("Left (after) = " + sel.left);
See the [element.elementType](#!AdobeDocs/developers-animatesdk-docs/master/Element_object/element1.md) example.

```