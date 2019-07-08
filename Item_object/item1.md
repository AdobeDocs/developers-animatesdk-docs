## item.getData()

#### Availability

Flash MX 2004.

#### Usage

item.getData(name)

#### Parameters

**name** A string that specifies the name of the data to retrieve.

#### Returns

The data specified by the *name* parameter. The type of data returned depends on the type of stored data.

#### Description

Method; retrieves the value of the specified data.

#### Example

```javascript
The following example gets the value of the data named myData from the first item in the library and stores it in the variable libData:
var libData = fl.getDocumentDOM().library.items\[0\].getData("myData");

```