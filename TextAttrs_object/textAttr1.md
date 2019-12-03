## textAttrs.alignment

#### Availability

Flash MX 2004.

#### Usage

*textAttrs.alignment*

#### Description

Property; a string that specifies paragraph justification. Acceptable values are *"left", "center", "right",* and
*"justify"*.

#### Example

The following example sets the paragraphs that contain characters between index 0 up to, but not including, index 3 to justify. This can affect characters outside the specified range if they are in the same paragraph.

```javascript
fl.getDocumentDOM().setTextSelection(0, 3); 
fl.getDocumentDOM().setElementTextAttr("alignment", "justify");

```