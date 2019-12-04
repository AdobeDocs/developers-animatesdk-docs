## document.setElementProperty()

#### Availability

Flash MX 2004.

#### Usage

document.setElementProperty(property, value)

#### Parameters

**property** A string that specifies the name of the Element property to set. For a complete list of properties and values, see the Property summary table for the [Element object](../Element_object/element_summary.md).
You can’t use this method to set values for read-only properties, such as [element.elementType](../Element_object/element1.md), [element.top](../Element_object/elemen22.md), or
[element.left](../Element_object/element8.md).
**value** An integer that specifies the value to set in the specified Element property.

#### Returns

Nothing.

#### Description

Method; sets the specified Element property on selected objects in the document. This method does nothing if there is no selection.

#### Example

The following example sets the width of all selected objects to 100 and the height to 50:

```javascript
fl.getDocumentDOM().setElementProperty("width", 100);
fl.getDocumentDOM().setElementProperty("height", 50);

```