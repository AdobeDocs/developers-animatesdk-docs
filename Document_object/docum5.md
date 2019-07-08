## document.skewSelection()

#### Availability

Flash MX 2004.

#### Usage

document.skewSelection(xSkew, ySkew \[, whichEdge\])

#### Parameters

**xSkew** A floating-point number that specifies the amount of *x* by which to skew, measured in degrees.
**ySkew** A floating-point number that specifies the amount of *y* by which to skew, measured in degrees.
**whichEdge** A string that specifies the edge where the transformation occurs; if omitted, skew occurs at the transformation point. Acceptable values are "top center", "right center", "bottom center", and "left center". This parameter is optional.

#### Returns

Nothing.

#### Description

Method; skews the selection by a specified amount. The effect is the same as using the Free Transform tool to skew the object.

#### Example

```javascript
The following examples skew the selected object by 2.0 vertically and 1.5 horizontally. The second example transforms the object at the top center edge:
fl.getDocumentDOM().skewSelection(2.0, 1.5); fl.getDocumentDOM().skewSelection(2.0, 1.5, "top center");

```