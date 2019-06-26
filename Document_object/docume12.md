## document.addNewText()

#### Availability

> Flash MX 2004; optional *text* parameter added in Flash CS3 Professional.

#### Usage

> document.addNewText(boundingRectangle \[, text \])

#### Parameters

> **boundingRectangle** Specifies the size and location of the text field. For information on the format of
>
> *boundingRectangle*, see [document.addNewRectangle()](#_bookmark128).
>
> **text** An optional string that specifies the text to place in the field. If you omit this parameter, the selection in the Tools panel switches to the Text tool. Therefore, if you don’t want the selected tool to change, pass a value for *text*.

#### Returns

> Nothing.

#### Description

> Method; inserts a new text field and optionally places text into the field. If you omit the *text* parameter, you can call
>
> [document.setTextString()](#_bookmark315) to populate the text field.

#### Example

> The following example creates a new text field in the upper left corner of the Stage and sets the text string to "Hello World":
>
> fl.getDocumentDOM().addNewText({left:0, top:0, right:100, bottom:100} , "Hello World!" ); fl.getDocumentDOM().setTextString('Hello World!');

#### See also

> [document.setTextString()](#_bookmark315)
