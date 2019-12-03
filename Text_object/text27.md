## text.textRuns

#### Availability

Flash MX 2004.

#### Usage

text.textRuns

#### Description

Read-only property; an array of TextRun objects (see [TextRun object](../TextRun_object/textRun_summary.md)).

#### Example

The following example stores the value of the textRuns property in the myTextRuns variable:
```javascript
var myTextRuns = fl.getDocumentDOM().selection[0].textRuns;
```