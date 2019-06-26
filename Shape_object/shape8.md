## shape.isGroup

#### Availability

> Flash MX 2004.

#### Usage

> shape.isGroup

#### Description

> Read-only property; if true, the shape is a group. A group can contain different types of elements, such as text elements and symbols. However, the group itself is considered a shape, and you can use the shape.isGroup property no matter what types of elements the group contains.

#### Example

> The following example stores the first selected object in the sel variable and then uses the [element.elementType](#_bookmark378) and
>
> shape.isGroup properties to determine if the selected item is a group:
>
> var sel = fl.getDocumentDOM().selection\[0\];
>
> var shapeGroup = (sel.elementType == "shape") && sel.isGroup; fl.trace(shapeGroup);

#### See also

> [shape.isDrawingObject](#_bookmark815)
