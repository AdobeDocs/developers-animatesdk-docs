## item.addData()

#### Availability

Flash MX 2004.

#### Usage

item.addData(name, type, data)

#### Parameters

**name** A string that specifies the name of the data.
**type** A string that specifies the type of data. Valid types are "integer", "integerArray", "double", "doubleArray", "string", and "byteArray".
**data** The data to add to the specified library item. The type of data depends on the value of the type parameter. For example, if type is "integer", the value of data must be an integer, and so on.

#### Returns

Nothing.

#### Description

Method; adds specified data to a library item.

#### Example

```javascript
The following example adds data named myData with an integer value of 12 to the first item in the library:
fl.getDocumentDOM().library.items\[0\].addData("myData", "integer", 12);

```