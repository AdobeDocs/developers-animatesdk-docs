## shape.contours

#### Availability

Flash MX 2004.

#### Usage

shape.contours

#### Description

Read-only property; an array of Contour objects for the shape (see [Contour object](../Contour_object/contour_summary.md)).

#### Example

```javascript
The following example stores the first contour in the contours array in the *c* variable and then stores the [HalfEdge](#_bookmark644) [object](#_bookmark644) of that contour in the he variable:
var c = fl.getDocumentDOM().selection\[0\].contours\[0\]; var he = c.getHalfEdge();

```