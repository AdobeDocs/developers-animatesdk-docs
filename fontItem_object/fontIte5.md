## fontItem.font

#### Availability

Flash CS4 Professional.

#### Usage

fontItem.font

#### Description

Property; a string that specifies the name of the device font associated with the Font item. If you enter a string that does not correspond to an installed device font, an error message is displayed. To determine if a font exists on the system, use [fl.isFontInstalled()](#_bookmark498).
>
***Note:** When you set this value, the resulting property value might be different from the string you enter. See the following example.*

#### Example

```
Assuming that the first item in the Library is a Font item, the following code displays the name of the device font currently associated with the Font item, then changes it to Times:
fl.outputPanel.clear();
var theItem = fl.getDocumentDOM().library.items\[0\]; fl.trace(theItem.font);
theItem.font = "Times";
// depending on your system, the following may display something like "Times-Roman" fl.trace(theItem.font);

```