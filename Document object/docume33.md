## document.close()

#### Availability

> Flash MX 2004.

#### Usage

> document.close(\[bPromptToSaveChanges\])

#### Parameters

> **bPromptToSaveChanges** A Boolean value that, when set to true, causes the method to prompt the user with a dialog box if there are unsaved changes in the document. If *bPromptToSaveChanges* is set to false, the user is not prompted to save any changed documents. The default value is true. This parameter is optional.

#### Returns

> Nothing.

#### Description

> Method; closes the specified document.

#### Example

> The following example closes the current document and prompts the user with a dialog box to save changes:
>
> fl.getDocumentDOM().close();
>
> The following example closes the current document without saving changes:
>
> fl.getDocumentDOM().close(false);
