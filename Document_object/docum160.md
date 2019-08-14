## document.moveSelectionBy()

#### Availability

Flash MX 2004.

#### Usage

document.moveSelectionBy(distanceToMove)

#### Parameters

**distanceToMove** A pair of floating-point values that specify the *x* and *y* coordinate values by which the method moves the selection. For example, passing ({x:1,y:2}) specifies a location one pixel to the right and two pixels down from the current location.

#### Returns

Nothing.

#### Description

Method; moves selected objects by a specified distance.
***Note:** When the user uses the arrow keys to move the item, the History panel combines all presses of the arrow key as one move step. When the user presses the arrow keys repeatedly, rather than taking multiple steps in the History panel, the method performs one step, and the arguments are updated to reflect the repeated arrow keys.*
For information on making a selection, see [document.setSelectionRect()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docu9689.md), [document.mouseClick()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docum130.md), [document.mouseDblClk()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docum140.md), and the [Element object](#!AdobeDocs/developers-animatesdk-docs/master/Element_object/element_summary.md).

#### Example

```javascript
The following example moves the selected item 62 pixels to the right and 84 pixels down:
fl.getDocumentDOM().moveSelectionBy({x:62, y:84});

```