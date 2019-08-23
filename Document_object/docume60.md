## document.enterEditMode()

#### Availability

Flash MX 2004.

#### Usage

document.enterEditMode(\[editMode\])

#### Parameters

**editMode** A string that specifies the editing mode. Acceptable values are "inPlace" or "newWindow". If no parameter is specified, the default is symbol-editing mode. This parameter is optional.

#### Returns

Nothing.

#### Description

Method; switches the authoring tool into the editing mode specified by the parameter. If no parameter is specified, the method defaults to symbol-editing mode, which has the same result as right-clicking the symbol to invoke the context menu and selecting Edit.

#### Example

```javascript
The following example puts Flash in edit-in-place mode for the currently selected symbol:
fl.getDocumentDOM().enterEditMode('inPlace');
The following example puts Flash in edit-in-new-window mode for the currently selected symbol:
fl.getDocumentDOM().enterEditMode('newWindow');

```
#### See also

[document.exitEditMode()](#!AdobeDocs/developers-animatesdk-docs/master/Document_object/docume61.md))

<span id="document.exitEditMode()" class="anchor"></span>
