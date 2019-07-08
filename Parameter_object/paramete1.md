## parameter.insertItem()

#### Availability

Flash MX 2004.

#### Usage

parameter.insertItem(index, name, value, type)

#### Parameters

**index** A zero-based integer index that indicates where the item will be inserted in the object or array. If the index is 0, the item is inserted at the beginning. If the index is greater than the list size, the new item is inserted at the end.
**name** A string that specifies the name of the item to insert. This is a required parameter for object parameters.
**value** A string that specifies the value of the item to insert.
**type** A string that specifies the type of item to insert.

#### Returns

Nothing.

#### Description

Method; inserts an item in an object or array. If a parameter is an object or array, the *value* property is an array.

#### Example

```javascript
The following example inserts the value of New Value into the labelPlacement parameter:
// Select an instance of a Button component on the Stage. var parms = fl.getDocumentDOM().selection\[0\].parameters; parms\[3\].insertItem(0, "name", "New Value", "String"); var values = parms\[3\].value;
for(var prop in values){
fl.trace("labelPlacement parameter value = " + values\[prop\].value);
}

```