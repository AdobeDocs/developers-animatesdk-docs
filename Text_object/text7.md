## text.embedRanges

#### Availability

Flash MX 2004.

#### Usage

text.embedRanges

#### Description

Property; a string that consists of delimited integers that correspond to the items that can be selected in the Character Embedding dialog box. This property works only with dynamic or input text; it is ignored if used with static text.

This property corresponds to the XML file in the Configuration/Font Embedding folder.

***Note:** Beginning in Flash Professional CS5, font embedding is controlled at the document level instead of the text object level. Use the* *["fontItem.embedRanges" on page 311](../fontItem_object/fontIte3.md) property instead of the text.embedRanges property.*

#### Example

The following example assumes that the first or only item in the current selection is a classic text object and sets the
embedRanges property to "1|3|7":

```javascript
var doc = fl.getDocumentDOM(); doc.selection[0].embedRanges = "1|3|7";
```

The following example resets the property:
```javascript
var doc = fl.getDocumentDOM(); doc.selection[0].embedRanges = "";
```