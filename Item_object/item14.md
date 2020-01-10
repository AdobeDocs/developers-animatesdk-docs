## item.removeData()

#### Availability

Flash MX 2004.

#### Usage

item.removeData(name)

#### Parameters

**name** Specifies the name of the data to remove from the library item.

#### Returns

Nothing.

#### Description

Property; removes persistent data from the library item.

#### Example

The following example removes the data named myData from the first item in the library:

```javascript
fl.getDocumentDOM().library.items[0].removeData("myData");
```