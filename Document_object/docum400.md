## document.scaleSelection()

#### Availability

Flash MX 2004.

#### Usage

document.scaleSelection(xScale, yScale [, whichCorner])

#### Parameters

**xScale** A floating-point value that specifies the amount of *x* by which to scale.
**yScale** A floating-point value that specifies the amount of *y* by which to scale.
**whichCorner** A string value that specifies the edge about which the transformation occurs. If omitted, scaling occurs about the transformation point. Acceptable values are: "bottom left", "bottom right", "top right", "top left", "top center", "right center", "bottom center", and "left center". This parameter is optional.

#### Returns

Nothing.

#### Description

Method; scales the selection by a specified amount. This method is equivalent to using the Free Transform tool to scale the object.

#### Example

```javascript
The following example expands the width of the current selection to double the original width and shrinks the height to half:
fl.getDocumentDOM().scaleSelection(2.0, 0.5); The following example flips the selection vertically: 
fl.getDocumentDOM().scaleSelection(1, -1);

The following example flips the selection horizontally:
fl.getDocumentDOM().scaleSelection(-1, 1);

The following example scales the selection vertically by 1.9 from the top center:
fl.getDocumentDOM().scaleSelection(1, 1.90, 'top center');

```