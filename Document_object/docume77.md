## document.getElementProperty()

#### Availability

Flash MX 2004.

#### Usage

document.getElementProperty(propertyName)

#### Parameters

**propertyName** A string that specifies the name of the Element property for which to retrieve the value.

#### Returns

The value of the specified property. Returns null if the property is an indeterminate state, as when multiple elements are selected with different property values. Returns undefined if the property is not a valid property of the selected element.

#### Description

Method; gets the specified Element property for the current selection. For a list of acceptable values, see the Property summary table for the [Element object](#_bookmark374).

#### Example

```javascript
The following example gets the name of the Element property for the current selection:
// elementName = the instance name of the selected object.
var elementName = fl.getDocumentDOM().getElementProperty("name");

```
#### See also

[document.setElementProperty()](#_bookmark283)
