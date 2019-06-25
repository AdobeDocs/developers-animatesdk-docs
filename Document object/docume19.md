## document.as3StrictMode

#### Availability

> Flash CS3 Professional.

#### Usage

> document.as3StrictMode

#### Description

> Property; a Boolean value that specifies whether the ActionScript 3.0 compiler should compile with the Strict Mode option turned on (true) or off (false). Strict Mode causes warnings to be reported as errors, which means that compilation will not succeed if those errors exist. The default value is true.

#### Example

> The following example turns off the Strict Mode compiler option.
>
> var myDocument = fl.getDocumentDOM();
>
> fl.outputPanel.trace("Strict Mode value before modification is " + myDocument.as3StrictMode); myDocument.as3StrictMode = false;
>
> fl.outputPanel.trace("Strict Mode value after modification is " + myDocument.as3StrictMode);

#### See also

> [document.as3WarningsMode](#document.as3WarningsMode)

<span id="document.as3WarningsMode" class="anchor"></span>
