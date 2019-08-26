## document.getTimeline()

#### Availability

Flash MX 2004.

#### Usage

document.getTimeline()

#### Parameters

None.

#### Returns

The current Timeline object.

#### Description

Method; retrieves the current [Timeline object](#!AdobeDocs/developers-animatesdk-docs/test/Timeline_object/timeline_summary.md) in the document. The current timeline can be the current scene, the current symbol being edited, or the current screen.

#### Example

```javascript
The following example gets the Timeline object and returns the number of frames in the longest layer:
var longestLayer = fl.getDocumentDOM().getTimeline().frameCount; fl.trace("The longest layer has" + longestLayer + "frames");
The following example enters edit-in-place mode for the selected symbol on the Stage and inserts a frame on the symbol’s timeline.
fl.getDocumentDOM().enterEditMode("inPlace"); fl.getDocumentDOM().getTimeline().insertFrames();
The following example gets the Timeline object and displays its name:
var timeline = fl.getDocumentDOM().getTimeline(); alert(timeline.name);

```
#### See also

[document.currentTimeline](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docume39.md), [document.timelines](#!AdobeDocs/developers-animatesdk-docs/test/Document_object/docu5995.md), [symbolItem.timeline](#!AdobeDocs/developers-animatesdk-docs/test/SymbolItem_object/symbolIt12.md)
