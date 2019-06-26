## shape.deleteEdge()

#### Availability

> Flash MX 2004.

#### Usage

> shape.deleteEdge(index)

#### Parameters

> **index** A zero-based index that specifies the edge to delete from the [shape.edges](#shape.edges) array. This method changes the length of the shape.edges array.

#### Returns

> Nothing.

#### Description

> Method; deletes the specified edge. You must call [shape.beginEdit()](#_bookmark807) before using this method.

#### Example

> The following example takes the currently selected shape and removes the first edge in the edge array:
>
> var shape = fl.getDocumentDOM().selection\[0\]; shape.beginEdit();
>
> shape.deleteEdge(0); shape.endEdit();

<span id="shape.edges" class="anchor"></span>
