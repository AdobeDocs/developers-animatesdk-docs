## item.getPublishData()

#### Availability

Adobe Animate.

#### Usage

library.getPublishData(name, format)

#### Parameters

**name** A string that contains the name of the persistent data item, as specified in [“item.addData()” on page 345](#_bookmark660).
>
**format** A string that specifies the publishing format.
>
***Note:** \_EMBED\_SWF\_ is a special built-in publishing format for persistent data. If set, the persistent data is embedded in the SWF file every time a document is published. The persistent data can then be accessed via ActionScript with the*
>
*.metaData property. This feature applies to SWF version 19 (Flash Player 11.6) and above and only for symbol instances onstage. Other custom publishing formats may be specified for custom JSFL scripts if getPublishPersistentData() is called with the same format.*

#### Returns

A Boolean value that indicates whether publishing of the specified persistent data is enabled for the specified format on this library item.

#### Description

Method; Indicates whether publishing of the specified persistent data is enabled for the specified format on a specified library item.

#### Example

```
The following example illustrates use of this method:
var doc = fl.getDocumentDOM();
// example setting library data if (doc){
var libItem = doc.library.items\[0\]; if (libItem) {
libItem.addData("sampleData", "string", "Hello! I am persistent Data."); libItem.setPublishData("sampleData", "\_EXTERN\_JSON\_", true);
// enable JSON publishing for this document doc.setPublishDocumentData("\_EXTERN\_JSON\_", true);
}
}
// example getting instance data
if (doc && doc.getPublishDocumentData("\_EXTERN\_JSON\_")) { var libItem = doc.library.items\[0\];
if (libItem) {
if (libItem.hasData("sampleData") && libItem.getPublishData("sampleData", "\_EXTERN\_JSON\_")) {
alert("publish persistent data for libElem: sampleData = '" + libItem.getData("sampleData") + "'");
}
}
}

```
#### See also

[item.setPublishData()](#_bookmark677)
