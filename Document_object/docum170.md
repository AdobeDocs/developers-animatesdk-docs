## document.name

#### Availability

> Flash MX 2004.

#### Usage

> document.name

#### Description

> Read-only property; a string that represents the name of a document (FLA file).

#### Example

> The following example sets the variable fileName to the filename of the first document in the documents array:
>
> var fileName = flash.documents\[0\].name;
>
> The following example displays the names of all the open documents in the Output panel:
>
> var openDocs = fl.documents;
>
> for(var i=0;i \< openDocs.length; i++){ fl.trace(i + " " + openDocs\[i\].name +"\\n");
>
> }
