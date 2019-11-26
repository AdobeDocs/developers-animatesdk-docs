## element.getPersistentData()

#### Availability

Flash MX 2004.

#### Usage

*element.getPersistentData(name)*

#### Parameters

**name** A string that identifies the data to be returned.

#### Returns

The data specified by the *name* parameter, or 0 if the data doesn’t exist.

#### Description

Method; retrieves the value of the data specified by the *name* parameter. The type of data depends on the type of the data that was stored (see [element.setPersistentData()](../Element_object/elemen17.md)). Only symbols and bitmaps support persistent data.

#### Example

```javascript
The following example sets and gets data for the specified element, shows its value in the Output panel, and then removes the data:
// At least one symbol or bitmap is selected in the first layer, first frame. 
var elt = fl.getDocumentDOM().getTimeline().layers[0].frames[0].elements[0]; 
elt.setPersistentData("myData","integer", 12);
if (elt.hasPersistentData("myData")){
fl.trace("myData = "+ elt.getPersistentData("myData")); elt.removePersistentData( "myData" );
fl.trace("myData = "+ elt.getPersistentData("myData"));
}

```