## textRun.textAttrs

#### Availability

Flash MX 2004.

#### Usage

textRun.textAttrs

#### Description

Property; the [TextAttrs object](../TextAttrs_object/textAttrs_summary.md) containing the attributes of the run of text.

#### Example

```javascript
The following example displays the properties of the first run of characters in the selected text field in the Output panel.
var curTextAttrs = fl.getDocumentDOM().selection\[0\].textRuns\[0\].textAttrs; for (var prop in curTextAttrs) {
fl.trace(prop + " = " + curTextAttrs\[prop\]);
}

```