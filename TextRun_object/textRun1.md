## textRun.characters

#### Availability

Flash MX 2004.

**TextRun object**

#### Usage

*textRun.characters*

#### Description

Property; the text contained in the TextRun object.

#### Example

The following example displays the characters that make up the first run of characters in the selected text field in the Output panel:

```javascript
fl.trace(fl.getDocumentDOM().selection[0].textRuns[0].characters);

```