## document.addItem()

#### Availability

Flash MX 2004.

#### Usage

document.addItem(position, item)

#### Parameters

**position** A point that specifies the *x* and *y* coordinates of the location at which to add the item. It uses the center of a symbol or the upper left corner of a bitmap or video.
**item** An Item object that specifies the item to add and the library from which to add it (see [Item object](#_bookmark658)).

#### Returns

A Boolean value: true if successful; false otherwise.

#### Description

Method; adds an item from any open document or library to the specified Document object.

#### Example

```
The following example adds the first item from the library to the first document at the specified location for the selected symbol, bitmap, or video:
var item = fl.documents\[0\].library.items\[0\]; fl.documents\[0\].addItem({x:0,y:0}, item);
The following example adds the symbol myMovieClip from the current document’s library to the current document:
var itemIndex = fl.getDocumentDOM().library.findItemIndex("myMovieClip"); var theItem = fl.getDocumentDOM().library.items\[itemIndex\]; fl.getDocumentDOM().addItem({x:0,y:0}, theItem);
The following example adds the symbol myMovieClip from the second document in the documents array to the third document in the documents array:
var itemIndex = fl.documents\[1\].library.findItemIndex("myMovieClip"); var theItem = fl.documents\[1\].library.items\[itemIndex\]; fl.documents\[2\].addItem({x:0,y:0}, theItem);

```