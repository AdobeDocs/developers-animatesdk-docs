## document.selection

#### Availability

Flash MX 2004.

#### Usage

document.selection

#### Description

Property; an array of the selected objects in the document. If nothing is selected, returns an array of length zero. If no document is open, returns null.
To add objects to the array, you must first select them in one of the following ways:

-   Manually select objects on the Stage.

-   Use one of the selection methods, such as [document.setSelectionRect()](../Document_object/docu9689.md), [document.setSelectionBounds()](../Document_object/docu9658.md), [document.mouseClick()](../Document_object/docum130.md), [document.mouseDblClk()](../Document_object/docum140.md), or [document.selectAll()](../Document_object/docum420.md).

-   Manually select a frame or frames.

-   Use one of the methods of the [Timeline object](../Timeline_object/timeline_summary.md) to select a frame or frames, such as

[timeline.getSelectedFrames()](../Timeline_object/timeli25.md), [timeline.setSelectedFrames()](../Timeline_object/timeli46.md), or [timeline.selectAllFrames()](../Timeline_object/timeli42.md).

-   Specify all the elements in a particular frame (see [Element object](../Element_object/element_summary.md)). See the first example below.

-   Create an array of one or more elements and then assign that array to the document.selection array. See the third example below.

#### Example

```javascript
The following example assigns all elements on Frame 11 to the current selection (remember that index values are different from frame number values):
fl.getDocumentDOM().getTimeline().currentFrame = 10; fl.getDocumentDOM().selection = fl.getDocumentDOM().getTimeline().layers[0].frames[10].elements;

The following example creates a rectangle in the upper left corner of the Stage and a text string underneath the rectangle. Then it selects both objects using [document.setSelectionRect()](../Document_object/docu9689.md) and adds them to the document.selection array. Finally, it displays the contents of document.selection in the Output panel.
fl.getDocumentDOM().addNewRectangle({left:0, top:0, right:99, bottom:99}, 0); 
fl.getDocumentDOM().addNewText({left:-1, top:117.3, right:9.2, bottom:134.6}); fl.getDocumentDOM().setTextString('Hello World'); 
fl.getDocumentDOM().setSelectionRect({left:-28, top:-22, right:156.0, bottom:163});
var theSelectionArray = fl.getDocumentDOM().selection; 
for(var i=0;i<theSelectionArray.length;i++){
fl.trace("fl.getDocumentDOM().selection["+i+"] = " + theSelectionArray[i]);
}

The following example is an advanced example. It shows how to loop through the layer array and elements array to locate instances of a particular symbol and select them. You could extend this example to include loops for multiple frames or scenes. This example assigns all instances of the movie clip myMovieClip in the first frame to the current selection:

// Assigns the layers array to the variable "theLayers". 
var theLayers = fl.getDocumentDOM().getTimeline().layers;
// Creates an array to hold all the elements that are instances of "myMovieClip". 
var myArray = new Array();
// Counter variable 
var x = 0;
// Begin loop through all the layers.
for (var i = 0; i < theLayers.length; i++) {
// Gets the array of elements in Frame 1
// and assigns it to the array "theElems".
var theElems = theLayers[i].frames[0].elements;
// Begin loop through the elements on a layer. 
for (var c = 0; c < theElems.length; c++) {
// Checks to see if the element is of type "instance".
 if (theElems[c].elementType == "instance") {
// If the element is an instance, it checks
// if it is an instance of "myMovieClip".
if (theElems[c].libraryItem.name == "myMovieClip") {
// Assigns elements that are instances of "myMovieClip" to "myArray".
 myArray[x] = theElems[c];
// Increments counter variable.
 x++;
}
}
}
}
// Now that you have assigned all the instances of "myMovieClip" to "myArray", you then set the document.selection array equal to myArray. This selects the objects on the Stage.

 fl.getDocumentDOM().selection = myArray;

```