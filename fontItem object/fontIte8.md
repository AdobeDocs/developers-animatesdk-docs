## fontItem.size

#### Availability

> Flash CS4 Professional.

#### Usage

> fontItem.size

#### Description

> Property; an integer that represents the size of the Font item, in points.

#### Example

> Assuming that the first item in the Library is a Font item, the following code displays the item’s point size in the Output panel and then sets it to 24.
>
> var theItem = fl.getDocumentDOM().library.items\[0\]; fl.outputPanel.clear();
>
> fl.trace("font size: "+ theItem.size); theItem.size=24;
>
> fl.trace("font size: "+ theItem.size);
