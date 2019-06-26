## document.path

#### Availability

> Flash MX 2004.

#### Usage

> document.path

#### Description

> Read-only property; a string that represents the path of the document in a platform-specific format. If the document has never been saved, this property is undefined.

#### Example

> The following example displays the path of the first document in the documents array in the Output panel. You must save the document before running this script. In the example, the file is named test.fla and is saved in the My Documents folder on a Windows computer.
>
> var filePath = flash.documents\[0\].path; fl.trace(filePath);
>
> // displays C:\\Documents and Settings\\\<user name\>\\My Documents\\test.fla

#### See also

> [document.pathURI](#document.pathURI)

<span id="document.pathURI" class="anchor"></span>
