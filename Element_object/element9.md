## element.locked

#### Availability

Flash MX 2004.

#### Usage

element.locked

#### Description

Property; a Boolean value: true if the element is locked; false otherwise. If the value of [element.elementType](#!AdobeDocs/developers-animatesdk-docs/test/Element_object/element1.md) is
"shape", this property is ignored.

#### Example

```javascript
The following example locks the first element in the first frame, top layer:
// Similar to Modify \Arrange \Lock: fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[0\].locked = true;

```