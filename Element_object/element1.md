## element.elementType

#### Availability

Flash MX 2004.

#### Usage

*element.elementType*

#### Description

Read-only property; a string that represents the type of the specified element. The value is one of the following:

-   "shape"

-   "text"

-   "tlfText" (Flash Pro CS5 and later)

-   "instance"

-   "shapeObj"

#### Example

```javascript
The following example stores the type of the first element in the eType variable:
// In a new file, place a movie clip on first frame top layer, and
// then run this line of script.
var eType = fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements[0].elementType; // eType = instance
The following example displays several properties for all the elements in the current layer or frame:
var tl = fl.getDocumentDOM().getTimeline()
var elts = tl.layers[tl.currentLayer].frames[tl.currentFrame].elements; 
for (var x = 0; x < elts.length; x++) {
    var elt = elts[x];
    fl.trace("Element "+ x +" Name = " + elt.name + " Type = " + elt.elementType + " location
    = " + elt.left + "," + elt.top + " Depth = " + elt.depth);
}

```