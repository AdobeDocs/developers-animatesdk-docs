## item.name

#### Availability

Flash MX 2004.

#### Usage

item.name

#### Description

Method; a string that specifies the name of the library item, which includes the folder structure. For example, if Symbol\_1 is inside a folder called Folder\_1, the name property of Symbol\_1 is "Folder\_1/Symbol\_1".

#### Example

```
The following example shows the name of the specified library item in the Output panel:
fl.trace(fl.getDocumentDOM().library.items\[0\].name);

```