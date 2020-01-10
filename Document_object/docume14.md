## document.allowScreens() - dropped

#### Availability

Flash MX 2004. *Dropped in Adobe Animate.*

#### Usage

document.allowScreens()

#### Parameters

None.

#### Returns

A Boolean value: true if document.screenOutline can be used safely; false otherwise.

#### Description

*Dropped in Adobe Animate.*

#### Example


The following example determines whether screens methods can be used in the current document:

```javascript
if(fl.getDocumentDOM().allowScreens()) { 
    fl.trace("screen outline is available.");
}
else {
    fl.trace("whoops, no screens.");
    }

```
#### See also

[document.screenOutline - dropped](../Document_object/docum410.md)
