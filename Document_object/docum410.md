## document.screenOutline - dropped

#### Availability

Flash MX 2004. *Dropped in Adobe Animate.*

#### Usage

document.screenOutline

#### Description

*Dropped in Adobe Animate.*

#### Example

```javascript
The following example displays the array of values in the screenOutline property:
var myArray = new Array();
for(var i in fl.getDocumentDOM().screenOutline) {
myArray.push(" "+i+" : "+fl.getDocumentDOM().screenOutline[i]) ;
}
fl.trace("Here is the property dump for screenOutline: "+myArray);

```
#### See also

[document.allowScreens() - dropped](../Document_object/docume14.md)
