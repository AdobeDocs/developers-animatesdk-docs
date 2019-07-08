## timeline.libraryItem

#### Availability

Flash Professional CS5.

#### Usage

timeline.libraryItem

#### Description

Read-only property; If the timeline's libraryItem property is null, the timeline belongs to a scene. If it's not null, you can treat it like a LibraryItem object.

#### Example

```javascript
The following example outputs the name of the libraryItem if the value of libraryItem is not null, and the name of the scene if librayItem is null:
var item = fl.getDocumentDOM().getTimeline().libraryItem; if (item)
fl.trace("libraryItem name: " + item.name); else
fl.trace("scene name: " + fl.getDocumentDOM().getTimeline().name);

```