## instance.libraryItem

#### Availability

Flash MX 2004.

#### Usage

instance.libraryItem

#### Description

Property; a library item used to instantiate this instance. You can change this property only to another library item of the same type (that is, you cannot set a symbol instance to refer to a bitmap). See [library object](../library_object/library_summary.md).

#### Example

```javascript
The following example changes the selected symbol to refer to the first item in the library:
fl.getDocumentDOM().selection\[0\].libraryItem = fl.getDocumentDOM().library.items\[0\];

```