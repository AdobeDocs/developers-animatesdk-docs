## element.setTransformationPoint()

#### Availability

Flash CS3 Professional.

#### Usage

element.setTransformationPoint(transformationPoint)

#### Parameters

**transformationPoint** A point (for example, {x:10, y:20}, where x and y are floating-point numbers) that specifies values for an element’s or group’s transformation point.

-   Shapes: *transformationPoint* is set relative to the document (0,0 is the upper-left corner of the Stage).

-   Symbols: *transformationPoint* is set relative to the symbol’s registration point (0,0 is located at the registration point).

-   Text: *transformationPoint* is set relative to the text field (0,0 is the upper-left corner of the text field).

-   Bitmaps/videos: *transformationPoint* is set relative to the bitmap/video (0,0 is the upper-left corner of the bitmap or video).

-   Drawing objects, primitive objects, and groups: *transformationPoint* is set relative to the stage.

#### Returns

Nothing.

#### Description

Method; sets the position of the element’s transformation point.
This method is almost identical to [document.setTransformationPoint()](#_bookmark317). It is different in the following way:

-   You can set transformation points for elements without first selecting them.

This method moves the transformation point but does not move the element. By contrast, the
[element.transformX](#_bookmark406) and [element.transformY](#_bookmark407) properties move the element.

#### Example

```javascript
The following example sets the transformation point of the third element on the Stage to 100, 200:
fl.getDocumentDOM().getTimeline().layers\[0\].frames\[0\].elements\[2\].setTransformationPoint({x: 100, y:200});

```
#### See also

[document.setTransformationPoint()](#_bookmark317). [element.getTransformationPoint()](#_bookmark381), [element.transformX](#_bookmark406), [element.transformY](#_bookmark407)
