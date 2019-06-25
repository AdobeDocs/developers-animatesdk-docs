## document.setAlignToDocument()

#### Availability

> Flash MX 2004.

#### Usage

> document.setAlignToDocument(bToStage)

#### Parameters

> **bToStage** A Boolean value that, if set to true, aligns objects to the Stage. If set to false, it does not.

#### Returns

> Nothing.

#### Description

> Method; sets the preferences for [document.align()](#_bookmark132), [document.distribute()](#_bookmark173), [document.match()](#_bookmark237), and [document.space()](#_bookmark323) to act on the document. This method is equivalent to enabling the To Stage button in the Align panel.

#### Example

> The following example enables the To Stage button in the Align panel to align objects with the Stage:
>
> fl.getDocumentDOM().setAlignToDocument(true);

#### See also

> [document.getAlignToDocument()](#_bookmark198)
