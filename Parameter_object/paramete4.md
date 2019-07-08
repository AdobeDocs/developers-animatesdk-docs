## parameter.removeItem()

#### Availability

Flash MX 2004.

#### Usage

parameter.removeItem(index)

#### Parameters

**index** The zero-based integer index of the item to be removed from the screen or component property.

#### Returns

Nothing.

#### Description

Method; removes an element of the object or array type of a screen or component parameter.

#### Example

```javascript
The following example removes the element at index 1 from the labelPlacement parameter of a component:
// Select an instance of a Button component on the Stage. var parms = fl.getDocumentDOM().selection\[0\].parameters; var values = parms\[2\].value;
fl.trace("--Original--"); for(var prop in values){
fl.trace("labelPlacement value = " + values\[prop\].value);
}
parms\[2\].removeItem(1);
var newValues = parms\[2\].value; fl.trace("--After Removing Item--"); for(var prop in newValues){
fl.trace("labelPlacement value = " + newValues\[prop\].value);
}
The following example removes the element at index 1 from the autoKeyNav parameter of a screen:
// Open a presentation document.
var parms = fl.getDocumentDOM().screenOutline.screens\[1\].parameters; var values = parms\[0\].value;
fl.trace("--Original--"); for(var prop in values){
fl.trace("autoKeyNav value = " + values\[prop\].value);
}
parms\[0\].removeItem(1);
var newValues = parms\[0\].value; fl.trace("--After Removing Item--"); for(var prop in newValues){
fl.trace("autoKeyNav value = " + newValues\[prop\].value);
}

```