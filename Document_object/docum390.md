## document.saveAsCopy()

#### Availability

Flash CS6.

#### Usage

document.saveAsCopy(URI \[, selectionOnly\])

#### Parameters

**URI** String: The URI to export the new FLA file to. This URI must reference a local file. Example: file:///c\|/tests/myTest.fla.
**selectionOnly** Optional. A boolean indicating whether only the current Stage selection should be saved to the new FLA file.

#### Returns

Boolean.

#### Description

Method; Saves a new FLA file based on the existing document object, with an option to save only the current selection on Stage.

#### Example

```
The following example exports the current selection to a new FLA file at the URI specified by the user:
var uri = fl.browseForFileURL("save"); var selectionOnly = true;
fl.getDocumentDOM().saveAsCopy(uri, selectionOnly);

```