## document.align()

#### Availability

> Flash MX 2004.

#### Usage

> document.align(alignmode \[, bUseDocumentBounds\])

#### Parameters

> **alignmode** A string that specifies how to align the selection. Acceptable values are "left", "right", "top", "bottom", "vertical center", and "horizontal center".
>
> **bUseDocumentBounds** A Boolean value that, if set to true, causes the method to align to the bounds of the document. Otherwise, the method uses the bounds of the selected objects. The default is false. This parameter is optional.

#### Returns

> Nothing.

#### Description

> Method; aligns the selection.

#### Example

> The following example aligns objects to the left and to the Stage. This is equivalent to turning on the To Stage setting in the Align panel and clicking the Align to Left button:
>
> fl.getDocumentDOM().align("left", true);

#### See also

> [document.distribute()](#_bookmark173), [document.getAlignToDocument()](#_bookmark198), [document.setAlignToDocument()](#_bookmark277)
