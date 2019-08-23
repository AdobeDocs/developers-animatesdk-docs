## document.library

#### Availability

Flash MX 2004.

#### Usage

document.library

#### Description

Read-only property; the [library object](#!AdobeDocs/developers-animatesdk-docs/master/library_object/library_summary.md) for a document.

#### Example

```javascript
The following example gets the library for the currently focused document:
var myCurrentLib = fl.getDocumentDOM().library;
Assuming the currently focused document is not fl.documents\[1\], the following example gets the library for a nonfocused library or for a library you opened using File \Open as external library:
var externalLib = fl.documents\[1\].library;

```