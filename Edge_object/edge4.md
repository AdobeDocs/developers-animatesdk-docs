## edge.isLine

#### Availability

> Flash MX 2004.

#### Usage

> edge.isLine

#### Description

> Read-only property; an integer with a value of 0 or 1. A value of 1 indicates that the edge is a straight line. In that case, the middle control point bisects the line joining the two end points.

#### Example

> The following example determines whether the specified edge is a straight line and shows a value of 1 (it is a straight line) or 0 (it isn’t a straight line) in the Output panel:
>
> var shape = fl.getDocumentDOM().selection\[0\]; fl.trace(shape.edges\[0\].isLine);
