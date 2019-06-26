## deactivate()

#### Availability

> Flash MX 2004.

#### Usage

> function deactivate() {
>
> // statements
>
> }

#### Parameters

> None.

#### Returns

> Nothing.

#### Description

> Function; called when the extensible tool becomes inactive (that is, when the active tool changes from this tool to another one). Use this function to perform any cleanup the tool needs.

#### Example

> The following example displays a message in the Output panel when the tool becomes inactive:
>
> function deactivate() {
>
> fl.trace( "Tool is no longer active" );
>
> }
